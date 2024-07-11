# DeepL

## Acesso direto aos serviços de tradução da DeepL após adquirir uma [Assinatura Pro do Immersive Translate](https://immersivetranslate.com/en/pricing/) (Recomendado)

[Clique aqui para apresentação](https://immersivetranslate.com/en/pricing/)

## Obtenha a DeepL API oficial através da DeepL

1. Introdução Oficial: [DeepL API](https://www.deepl.com/en/pro#developer)
   - Observação: [DeepL API](https://www.deepl.com/en/pro#developer) e [DeepL Pro](https://www.deepl.com/pro) são dois tipos de contas diferentes. A conta a ser utilizada é a [DeepL API](https://www.deepl.com/en/pro/select-country#developer).

2. [Por que](https://www.deepl.com/en/whydeepl) escolher a DeepL?

   - Traduções Inglês ⇄ Chinês 5x mais precisas
   - Traduções Inglês ⇄ Japonês 6x mais precisas
   - Mecanismo de tradução baseado em tecnologia de inteligência artificial (redes neurais)

3. A DeepL API é dividida em [API Gratuita e API Pro](https://www.deepl.com/en/pro#developer)

   - A API Gratuita oferece 500.000 caracteres gratuitos por mês.
   - A [tarifa oficial](https://www.deepl.com/en/pro#developer) da API Pro é: US$25 por 1 milhão de caracteres.
   - Para usuários de alta frequência, o consumo mensal é de cerca de 10 milhões de caracteres, resultando em um custo aproximado de: US$250

4. Para registrar uma conta e ativar a [DeepL API](https://www.deepl.com/en/pro#developer).

<!-- ## Construa sua própria API DeepL

Estamos experimentando suporte para nosso próprio serviço DeeplX na função Beta (mas não é bem adequado como um serviço de tradução de páginas web, conforme testado. Devido à grande quantidade de solicitações de API para tradução de páginas web, se você construir esse serviço, certifique-se de fazer um bom trabalho de balanceamento de carga), a seguir está como ativar os recursos experimentais das instruções:

1. Ativando Recursos de Teste Beta nas Configurações do Desenvolvedor
2. Encontre DeepLX (Beta) nas Configurações Básicas e insira a URL da API DeepL autoconstruída, por exemplo, http\://seu-dominio/translate

> P: Como posso construir o meu próprio?
>
> R: [OwO-Network/DeepLX](https://github.com/OwO-Network/DeepLX#setup-on-immersive-translate) ou [zu1k/deepl](https://github.com/KyleChoy/zotero-pdf-translate/blob/CustomDeepL/README.md) -->

## Problemas comuns

### 1. A chave inserida não está disponível.

DeepL API Pro e DeepL Pro são dois tipos de contas diferentes. A Chave de Autenticação que pode ser utilizada no Immersive Translate é a da conta DeepL API. Clique aqui para acessar o [desenvolvedor DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer).

### 2. DeepL Free API Retorna 401 Sem Privilégio

Todas as chaves da DeepL Free API terminam em `:fx`. Qualquer outra chave não é uma chave da Free API.

### 3. 456, Cota do usuário atingida.

O uso excedeu o limite rígido oficial da DeepL por usuário. Você pode ter violado a política de uso justo da DeepL e é aconselhável evitar tal comportamento. Se você for um assinante pago, o uso será automaticamente redefinido no próximo mês.
