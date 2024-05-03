# DeepL

## Acesso direto aos serviços de tradução do DeepL após abrir uma [Assinatura Pro do Immersive Translate](https://immersivetranslate.com/en/pricing/) (Recomendado)

[Clique aqui para apresentação](https://immersivetranslate.com/en/pricing/)

## Obtenha a API oficial do DeepL através do DeepL

1. Introdução Oficial: [API do DeepL](https://www.deepl.com/en/pro#developer)
   - Note que: [API do DeepL](https://www.deepl.com/en/pro#developer) e [DeepL Pro](https://www.deepl.com/pro) são dois tipos diferentes de contas, e a conta [API do DeepL](https://www.deepl.com/en/pro/select-country#developer).

2. [Por que](https://www.deepl.com/en/whydeepl) escolher o DeepL?

   - Inglês ⇄ Chinês 5x mais preciso
   - Inglês ⇄ Japonês 6x mais preciso
   - Motor de tradução baseado em tecnologia de inteligência artificial (redes neurais)

3. A API do Deepl é dividida em [API Gratuita e API Pro](https://www.deepl.com/en/pro#developer)

   - A API Gratuita fornece 500.000 caracteres gratuitos por mês.
   - A [taxa oficial](https://www.deepl.com/en/pro#developer) para a API Pro é: $25 por 1 milhão de caracteres.
   - Para um usuário de alta frequência, a quantidade de caracteres consumidos em um mês é de cerca de 10 milhões de caracteres, e o preço é de cerca de: 250 USD

4. Para registrar uma conta e abrir a [API do DeepL](https://www.deepl.com/en/pro#developer).

<!--## Construa sua própria API DeepL

Estamos experimentando o suporte para nosso próprio serviço DeeplX na funcionalidade Beta (mas não é bem adequado como um serviço de tradução web, conforme testado. Devido à enorme quantidade de solicitações de API para tradução de páginas web, se você construir este serviço, por favor, certifique-se de fazer um bom trabalho de balanceamento de carga), a seguir está como ativar os recursos experimentais das instruções:

1. Ativando Recursos de Teste Beta nas Configurações de Desenvolvedor
2. Encontre DeepLX (Beta) em Configurações Básicas e insira a URL da API DeepL construída por você, por exemplo, http\://seu-dominio/traduzir

> Q: Como posso construir o meu próprio?
>
> A: [OwO-Network/DeepLX](https://github.com/OwO-Network/DeepLX#setup-on-immersive-translate) ou [zu1k/deepl](https://github.com/KyleChoy/zotero-pdf-translate/blob/CustomDeepL/README.md) -->

## problemas comuns

### 1. A chave preenchida não está disponível.

DeepL API Pro e DeepL Pro são dois tipos de contas, a Auth Key que pode ser usada no Immersive Translate é a conta da DeepL API, por favor clique aqui para [DeepL API Pro](https://www.deepl.com/en/pro/select-country#) desenvolvedor)

### 2. Deepl Free API Indica 401 Sem Privilégio

As chaves da API Free da Deepl terminam todas em `:fx`, qualquer outra coisa não é uma chave de API Free.

### 3. 456, Cota para usuário foi atingida.

O uso excedeu o limite máximo oficial por usuário da DeepL, você pode ter violado a política de uso justo da DeepL e é aconselhado a evitar tal comportamento. Se você é um assinante pago, o uso será automaticamente reiniciado no próximo mês.