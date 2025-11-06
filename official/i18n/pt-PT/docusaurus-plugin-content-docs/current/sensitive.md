---
sidebar_position: 7
---

# Mascaramento de informações sensíveis

> Esta funcionalidade é suportada na versão 1.23.1+ do plugin.

Após ativar o [OneAIFW](https://github.com/funstory-ai/aifw) integrado ou personalizado, o plugin identificará e mascarará automaticamente informações sensíveis (como endereços de correio eletrónico, números de telefone, números de identificação, etc.) durante a tradução para proteger a sua privacidade e segurança. Este guia mostrará como ver quais informações sensíveis foram identificadas e mascaradas durante a tradução.

## Visualizar registos de mascaramento

### Passo 1: Ativar registo

1. Abra a [**página de definições do programador**](https://dash.immersivetranslate.com/#advanced) do plugin
2. Ative a opção **"Ativar registo da consola"**

### Passo 2: Abrir a consola do programador

1. Pressione `F12` na página web (ou clique com o botão direito na página e selecione "Inspecionar" / "Inspecionar elemento")
2. Mude para o separador "Console" (Consola)

### Passo 3: Filtrar registos de mascaramento

Digite `sensitive-` na caixa de filtro da consola para filtrar todos os registos relacionados com o mascaramento de informações sensíveis.

## Explicação do formato de registo

Na consola, verá registos no seguinte formato:

```
[sensitive-encode] "Correio: tester.cn+alias@example.com" -> "Correio: __PII_EMAIL_ADDRESS_1__"

[sensitive-decode] "Correio: __PII_EMAIL_ADDRESS_1__" -> "Correio: tester.cn+alias@example.com"
```

### Significados dos registos

- **`[sensitive-encode]`**: Indica o processo de identificação e mascaramento de informações sensíveis
  - O lado esquerdo é o texto original (contendo informações sensíveis)
  - O lado direito é o texto mascarado (`__PII_*` é o marcador de posição de mascaramento)

- **`[sensitive-decode]`**: Indica o processo de restauração do texto mascarado
  - O lado esquerdo é o texto mascarado (contendo marcadores de posição)
  - O lado direito é o texto original restaurado

### Explicação dos marcadores de posição

Marcadores de posição no formato `__PII_*` representam o tipo de informações sensíveis que foram mascaradas, por exemplo:
- `__PII_EMAIL_ADDRESS_1__`: Endereço de correio eletrónico
- `__PII_PHONE_NUMBER_1__`: Número de telefone
- `__PII_ID_CARD_1__`: Número de identificação
- etc.

## Princípios de mascaramento

Para os princípios específicos e detalhes de implementação do mascaramento de informações sensíveis, pode consultar a documentação e o código do [projeto OneAIFW](https://github.com/funstory-ai/aifw).

## Notas

- Esta funcionalidade está atualmente em **fase de teste beta**, e pode haver casos de identificação imprecisa ou falhas de mascaramento
- Se encontrar falhas de mascaramento ou erros de identificação, envie feedback através de [GitHub Issues](https://github.com/funstory-ai/aifw/issues), e continuaremos a iterar e otimizar

