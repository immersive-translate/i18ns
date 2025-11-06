---
sidebar_position: 7
---

# Mascaramento de informações sensíveis

> Este recurso é suportado na versão 1.23.1+ do plugin.

Após habilitar o [OneAIFW](https://github.com/funstory-ai/aifw) integrado ou personalizado, o plugin identificará e mascarará automaticamente informações sensíveis (como endereços de e-mail, números de telefone, números de identidade, etc.) durante a tradução para proteger sua privacidade e segurança. Este guia mostrará como ver quais informações sensíveis foram identificadas e mascaradas durante a tradução.

## Visualizando logs de mascaramento

### Etapa 1: Habilitar registro

1. Abra a [**página de configurações do desenvolvedor**](https://dash.immersivetranslate.com/#advanced) do plugin
2. Habilite a opção **"Habilitar registro do console"**

### Etapa 2: Abrir o console do desenvolvedor

1. Pressione `F12` na página da web (ou clique com o botão direito na página e selecione "Inspecionar" / "Inspecionar elemento")
2. Mude para a aba "Console"

### Etapa 3: Filtrar logs de mascaramento

Digite `sensitive-` na caixa de filtro do console para filtrar todos os logs relacionados ao mascaramento de informações sensíveis.

## Explicação do formato de log

No console, você verá logs no seguinte formato:

```
[sensitive-encode] "E-mail: tester.cn+alias@example.com" -> "E-mail: __PII_EMAIL_ADDRESS_1__"

[sensitive-decode] "E-mail: __PII_EMAIL_ADDRESS_1__" -> "E-mail: tester.cn+alias@example.com"
```

### Significados dos logs

- **`[sensitive-encode]`**: Indica o processo de identificação e mascaramento de informações sensíveis
  - O lado esquerdo é o texto original (contendo informações sensíveis)
  - O lado direito é o texto mascarado (`__PII_*` é o marcador de posição de mascaramento)

- **`[sensitive-decode]`**: Indica o processo de restauração do texto mascarado
  - O lado esquerdo é o texto mascarado (contendo marcadores de posição)
  - O lado direito é o texto original restaurado

### Explicação dos marcadores de posição

Marcadores de posição no formato `__PII_*` representam o tipo de informações sensíveis que foram mascaradas, por exemplo:
- `__PII_EMAIL_ADDRESS_1__`: Endereço de e-mail
- `__PII_PHONE_NUMBER_1__`: Número de telefone
- `__PII_ID_CARD_1__`: Número de identidade
- etc.

## Princípios de mascaramento

Para os princípios específicos e detalhes de implementação do mascaramento de informações sensíveis, você pode consultar a documentação e o código do [projeto OneAIFW](https://github.com/funstory-ai/aifw).

## Notas

- Este recurso está atualmente em **fase de teste beta**, e pode haver casos de identificação imprecisa ou falhas de mascaramento
- Se você encontrar falhas de mascaramento ou erros de identificação, envie feedback através de [GitHub Issues](https://github.com/funstory-ai/aifw/issues), e continuaremos a iterar e otimizar

