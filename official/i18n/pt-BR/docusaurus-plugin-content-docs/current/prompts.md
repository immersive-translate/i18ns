---
sidebar_position: 5
---
# Guia de Configuração de Prompt de IA

## Visão Geral

O Immersive Translate suporta configuração personalizada de Prompt para tradução por IA, permitindo que usuários avançados ajustem o comportamento da tradução de acordo com suas necessidades. Este documento fornece instruções detalhadas sobre métodos de configuração, variáveis suportadas e uso avançado.

## Variáveis Suportadas

### Variáveis Básicas

- `{{text}}` - O conteúdo do texto a ser traduzido
- `{{from}}` - Idioma de origem
- `{{to}}` - Idioma de destino
- `{{content_type}}` - Tipo de texto original (`html` ou `text`)

### Variáveis de Contexto
- `{{title_prompt}}` - Título da página web (quando disponível)
- `{{summary_prompt}}` - Resumo do contexto da página web (quando disponível)
- `{{terms_prompt}}` - Terminologia profissional relacionada (quando disponível)

## Métodos de Configuração

### 1. System Prompt(`systemPrompt`)
Solicitação de tradução enviada à IA como identidade do sistema. Usado para definir o papel da IA e as regras básicas.

### 2. Prompt(`prompt`)
Conversa enviada à IA como identidade do usuário, contendo o conteúdo real que precisa ser traduzido.

### 3. System Multiple Prompt(`systemMultiplePrompt`)
Solicitação de tradução enviada à IA como identidade do sistema quando o número de parágrafos é maior que 1. Usado para lidar com cenários de tradução de múltiplos parágrafos.

### 4. Multiple Prompt(`multiplePrompt`)
Solicitação enviada como identidade do usuário para tradução de múltiplos parágrafos. Suporta o uso de separadores ou formato YAML.

### 5. Subtitle Prompt(`subtitlePrompt`)

Quando a tradução de legendas é necessária, conversa enviada à IA como identidade do usuário, contendo o conteúdo real que precisa ser traduzido.

## Exemplos de Configuração Padrão

Se apenas um parágrafo for coletado, usará o Prompt de parágrafo único por padrão. Se múltiplos parágrafos forem coletados, usará o Prompt de múltiplos parágrafos por padrão. A maioria dos casos será de múltiplos parágrafos. O separador padrão para múltiplos parágrafos é `%%`. Usamos deliberadamente este separador incomum para reduzir alucinações de modelos grandes. Você pode usar este Prompt como base para modificá-lo conforme suas necessidades. Aqui estão as configurações de Prompt padrão:

### Tradução de Parágrafo Único

```yaml
systemPrompt: |
    Você é um tradutor nativo profissional de {{to}} que precisa traduzir texto fluentemente para {{to}}.

    ## Regras de Tradução
    1. Gere apenas o conteúdo traduzido, sem explicações ou conteúdo adicional (como "Aqui está a tradução:" ou "Tradução como segue:")
    2. A tradução retornada deve manter exatamente o mesmo número de parágrafos e formato do texto original
    3. Se o texto contiver tags HTML, considere onde as tags devem ser colocadas na tradução mantendo a fluência
    4. Para conteúdo que não deve ser traduzido (como nomes próprios, código, etc.), mantenha o texto original
    5. Gere a tradução diretamente (sem separadores, sem texto adicional){{title_prompt}}{{summary_prompt}}{{terms_prompt}}
prompt: |
  Traduza para {{to}} (gere apenas a tradução):

  {{text}}
```

### Tradução de Múltiplos Parágrafos

```yaml
multipleSystemPrompt: |
    Você é um tradutor nativo profissional de {{to}} que precisa traduzir texto fluentemente para {{to}}.

    ## Regras de Tradução
    1. Gere apenas o conteúdo traduzido, sem explicações ou conteúdo adicional (como "Aqui está a tradução:" ou "Tradução como segue:")
    2. A tradução retornada deve manter exatamente o mesmo número de parágrafos e formato do texto original
    3. Se o texto contiver tags HTML, considere onde as tags devem ser colocadas na tradução mantendo a fluência
    4. Para conteúdo que não deve ser traduzido (como nomes próprios, código, etc.), mantenha o texto original{{title_prompt}}{{summary_prompt}}{{terms_prompt}}

    ## Exemplos de Formato de Entrada-Saída

    ### Exemplo de Entrada:
    Paragraph A

    %%

    Paragraph B

    %%

    Paragraph C

    %%

    Paragraph D

    ### Exemplo de Saída:
    Translation A

    %%

    Translation B

    %%

    Translation C

    %%

    Translation D

multiplePrompt: |
  Traduza para {{to}}:

  {{text}}
subtitlePrompt: |
  Traduza para {{to}}:

  {{text}}
```

## Uso Avançado (Formato YAML)

Para cenários que requerem controle mais preciso (por exemplo, saídas de múltiplas etapas), o formato YAML pode ser usado para configuração:

### Variáveis Avançadas

- `{{yaml}}` - Dados de entrada em formato YAML

A variável 'yaml' padrão se parece com isso:

```
- id: 1
  text: Hello world
- id: 2
  text: How are you?
```

Esperamos por padrão que a saída do modelo grande seja assim:

```
- id: 1
  text: 你好世界
- id: 2
  text: 你好吗？
```

Se você usar o `{{yaml}}` padrão, precisa expressar claramente essa expectativa no prompt. Se desejar modificar o formato `yaml` padrão e de resposta, isso não pode ser resolvido através da UI da página de configurações do Immersive Translate. Você deve editar diretamente a configuração do usuário em formato JSON do Immersive Translate.

Caminho de edição da configuração do usuário: `Página de Configurações`->`Configurações do Desenvolvedor`->`Edit Full User Config` (Por favor, faça backup da sua configuração do usuário antes de editar)

Você pode encontrar a configuração do serviço de tradução no JSON da configuração do usuário (se não existir, simplesmente adicione de acordo com esta estrutura):

```
{
  ...
  "translationServices": {
    "openai": {
       ...
      }
  },
  ...

```

A variável `yaml` é composta por `env.imt_yaml_item`, então você pode modificar o formato de `imt_yaml_item` assim:

```json
  "translationServices": {
    "openai": {
       "env": {
          "imt_yaml_item": "- id: {{id}}\n  source: {{text}}"
        }
    }
   }
```

Outra variável especial é `imt_subtitle_yaml_item`, similar a `imt_yaml_item`, usada para itens YAML de tradução de legendas.

Para outras variáveis `env`, você pode adicionar qualquer variável `env` e usá-la diretamente no prompt no formato `{{nome_variável}}`, como as seguintes variáveis `env` padrão:

- `{{imt_source_field}}` - Nome do campo de texto fonte (padrão: text)
- `{{imt_trans_field}}` - Nome do campo de texto traduzido (padrão: text)
- `{{imt_sub_source_field}}` - Nome do campo de texto fonte de legendas
- `{{imt_sub_trans_field}}` - Nome do campo de texto traduzido de legendas

Incluindo `title_prompt`, `summary_prompt`, `terms_prompt` também são configurados através de `env`, padrão como segue:

```
        "title_prompt": "\n\n## Consciência Contextual\nMetadados do Documento:\nTítulo: 《{{imt_title}}》",
        "summary_prompt": "\n\n## Consciência Contextual\nMetadados do Documento:\nResumo: {{imt_theme}}...",
        "terms_prompt": "\n\nTerminologia Obrigatória: Você DEVE usar os seguintes termos durante a tradução. Se 'source':'target' e source == target, mantenha o termo fonte inalterado.\n\n Termos -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## Consciência Contextual\nMetadados do Documento:\nTipo: Legenda\nResumo: {{imt_theme}}...",
        "sub_terms_prompt": "\n\nTerminologia Obrigatória: Você DEVE usar os seguintes termos durante a tradução. Se 'source':'target' e source == target, mantenha o termo fonte inalterado.\n\n Termos -> \n\n {{imt_terms}}"

```

Onde `imt_title`, `imt_theme`, `imt_terms` são variáveis especiais injetadas pelo sistema. `imt_title` é o título, `imt_theme` é o resumo de toda a página web, `imt_terms` são os termos-chave extraídos pelo modelo.

> Nota: `imt_theme`, `imt_terms` são extraídos por um serviço proprietário e estão atualmente disponíveis apenas para [membros Pro](https://immersivetranslate.com/pricing/).

### Exemplo de YAML Prompt

```yaml
systemPrompt: |
  Você é um motor de tradução automática profissional e autêntico.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
    Você receberá uma entrada em formato YAML contendo entradas com campos "id" e "{{imt_source_field}}". Aqui está a entrada:

    <yaml>
    {{yaml}}
    </yaml>

    Para cada entrada no YAML, traduza o conteúdo do campo "{{imt_source_field}}" para {{to}},{{html_only}} escreva a tradução de volta no campo "{{imt_source_field}}" dessa entrada.

    Aqui está um exemplo do formato esperado:

    {{normal_result_yaml_example}}

    Por favor, retorne o YAML traduzido diretamente sem tag <yaml> ou informações adicionais.
subtitlePrompt: |
    Você receberá uma entrada de legendas em formato YAML contendo entradas com campos "id" e "{{imt_sub_source_field}}". Aqui está a entrada:

    <yaml>
    {{yaml}}
    </yaml>

    Para cada entrada no YAML, traduza o conteúdo do campo "{{imt_sub_source_field}}" para {{to}},{{html_only}} escreva a tradução de volta no campo "{{imt_sub_source_field}}" dessa entrada.

    Aqui está um exemplo do formato esperado:

    {{subtitle_result_yaml_example}}

    Por favor, retorne o YAML traduzido diretamente sem tag <yaml> ou informações adicionais.

```

`html_only` é uma variável especial que existe apenas quando o texto original a ser traduzido está em formato HTML. O valor é: `\n\nNota: Se o texto contiver tags HTML, por favor considere após a tradução onde as tags devem estar no resultado da tradução, mantendo ao mesmo tempo a fluência do resultado.`, esta variável existe apenas quando o usuário ativa ativamente "Tradução de Texto Rico" nos serviços de tradução por IA. Caso contrário, está vazia.

`normal_result_yaml_example` é definido em `env`, o padrão é:

```
<example>
Input:
  - id: 1
    {{imt_source_field}}: Source
Output:
  - id: 1
    {{imt_trans_field}}: Translation
</example>
```

`subtitle_result_yaml_example` é definido em `env`, o valor padrão é:

```
<example>
Input:
  - id: 1
    {{imt_sub_source_field}}: ...
  - id: 2
    {{imt_sub_source_field}}: ...
  - id: 3
    {{imt_sub_source_field}}: ...
Output:
  - id: 1
    {{imt_sub_source_field}}: ...
  - id: 2
    {{imt_sub_source_field}}: ...
  - id: 3
    {{imt_sub_source_field}}: ...
</example>

```

Você pode substituí-lo em `env`.

## Exemplo Avançado: Tradução Reflexiva

Este exemplo mostra como usar o formato YAML para implementar um fluxo de tradução mais complexo, incluindo duas etapas: tradução inicial e tradução otimizada:

```yaml
env:
  imt_source_field: source
  imt_trans_field: step2  # A tradução final usa o campo step2
  imt_sub_source_field: source
  imt_sub_trans_field: step2
  imt_yaml_item: |-
    - id: {{id}}
      {{imt_source_field}}: {{text}}
  imt_subtitle_yaml_item: |-
    - id: {{id}}
      {{imt_sub_source_field}}: {{text}}

systemPrompt: |
  Você é um motor de tradução automática profissional e autêntico.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
  Aqui está a entrada YAML:
  <yaml>
  {{yaml}}
  </yaml>
  
  Por favor, siga estes passos:
  1. Extraia o conteúdo do campo "source" do objeto YAML fornecido.
  2. Traduza o conteúdo extraído para {{to}}. Coloque esta tradução inicial no campo step1.
  3. Otimize a tradução inicial de step1 para torná-la mais natural e compreensível em {{to}}. 
     Coloque esta tradução otimizada no campo step2.
  4. Formate o resultado como uma matriz YAML com campos id, step1 e step2, como mostrado neste exemplo:
  
  - id: 1 
    step1: Tradução inicial
    step2: Tradução otimizada
  
  Por favor, retorne o YAML traduzido diretamente sem tags <example_output> ou informações adicionais.
```

### Descrição do Fluxo de Trabalho

1. **Formato de Entrada**：
   ```yaml
   - id: 1
     source: "Hello world"
   - id: 2
     source: "How are you?"
   ```

2. **Etapas de Processamento de IA**：
   - Etapa 1: Execute a tradução inicial
   - Etapa 2: Otimize a tradução para torná-la mais natural e fluente

3. **Formato de Saída**：
   ```yaml
   - id: 1
     step1: "你好世界"
     step2: "你好，世界"
   - id: 2
     step1: "你怎么样？"
     step2: "你好吗？"
   ```
