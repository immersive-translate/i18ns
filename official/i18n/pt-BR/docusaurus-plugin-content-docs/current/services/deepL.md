# DeepL

## Acesso direto aos serviços de tradução do DeepL após abrir uma [Assinatura Pro do Immersive Translate](https://immersivetranslate.com/en/pricing/) (Recomendado)

[Saiba Mais](https://immersivetranslate.com/en/pricing/)

## Obtenha a API oficial do DeepL via DeepL

1. Introdução Oficial: [DeepL API](https://www.deepl.com/en/pro#developer)

   - Note que: [DeepL API](https://www.deepl.com/en/pro#developer) e [DeepL Pro](https://www.deepl.com/pro) são dois tipos de contas diferentes, e a conta [DeepL API](https://www.deepl.com/en/pro/select-country#developer).

2. [Por que](https://www.deepl.com/en/whydeepl) escolher o DeepL?

   - Inglês ⇄ Chinês 5x mais preciso
   - Inglês ⇄ Japonês 6x mais preciso
   - Motor de tradução baseado em tecnologia de inteligência artificial (redes neurais)

3. A API do DeepL é dividida em [Free API e Pro API](https://www.deepl.com/en/pro#developer)

   - A Free API fornece 500.000 caracteres gratuitos por mês.
   - A [taxa oficial](https://www.deepl.com/en/pro#developer) para a Pro API é: $25 por 1 milhão de caracteres.
   - Para um usuário de alta frequência, a quantidade de caracteres consumidos em um mês é de cerca de 10 milhões de caracteres, e o preço é de cerca de: 250 USD

4. Para registrar uma conta e abrir a [DeepL API](https://www.deepl.com/en/pro#developer).

## problemas comuns

### 1. A chave preenchida não está disponível.

DeepL API Pro e DeepL Pro são dois tipos de contas, a Chave de Autenticação que pode ser usada no Immersive Translate é a conta DeepL API, por favor clique aqui para [DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer)

### 2. Solução de problemas de erros de autenticação 401, 403

Esses erros geralmente ocorrem quando você está usando o tipo errado de chave de autenticação. Por favor, note:

1. DeepL oferece dois produtos diferentes: DeepL Pro (serviço de tradução) e DeepL API (interface de desenvolvedor)
2. As chaves encontradas nas configurações da sua conta DeepL Pro **não são compatíveis** com chamadas de API
3. Você precisa se registrar especificamente para uma conta DeepL API para obter uma chave de API
4. As chaves da DeepL Free API são identificadas por terminarem com `:fx`
5. As chaves da DeepL Pro API não têm o sufixo `:fx` e aparecem como uma sequência regular de caracteres

Por favor, certifique-se de que você se registrou corretamente para o serviço DeepL API, e não apenas para o serviço de tradução DeepL Pro.

### 3. 456, Limite de cota para o usuário foi atingido.

O uso excedeu o limite oficial imposto por usuário do DeepL, você pode ter violado a política de uso justo do DeepL e é aconselhado a evitar tal comportamento. Se você for um assinante pago, o uso será automaticamente redefinido no próximo mês.
