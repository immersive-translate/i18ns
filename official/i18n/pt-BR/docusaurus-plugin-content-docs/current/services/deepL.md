# Como implementar a DeepL API Pro no Immersive Translate

## Opção Recomendada: Assinatura Pro do Immersive Translate

Para acesso imediato e simplificado à DeepL, adquira uma [Assinatura Pro do Immersive Translate](https://immersivetranslate.com/en/pricing/).

## Obtenção da DeepL API Pro

1. **DeepL API Pro:**
   - Acesse o [site oficial da DeepL](https://www.deepl.com/en/pro#developer):
   - **Importante:** Certifique-se de selecionar o plano **DeepL API Pro**, e não o DeepL Pro.

2. **Por que escolher a DeepL?**
   - Traduções Inglês ⇄ Chinês 5x mais precisas.
   - Traduções Inglês ⇄ Japonês 6x mais precisas.
   - Tecnologia de ponta com inteligência artificial (redes neurais).

3. **Planos da DeepL API:**
   - **DeepL API Free:** 500.000 caracteres gratuitos por mês.
   - **DeepL API Pro:**
     - Tarifa: US$25 por 1 milhão de caracteres.
     - Estimativa para uso intenso (10 milhões de caracteres/mês): US$250.

4. **Registro e Ativação:**
   - Acesse [https://www.deepl.com/en/pro#developer](https://www.deepl.com/en/pro#developer) para registrar uma conta e ativar a DeepL API Pro.

<!-- ## Construa sua própria API DeepL

Estamos implementando o suporte experimental para o DeepL X (Beta). (De acordo com nossos testes, ele ainda não é ideal para a tradução de páginas da web, devido à alta demanda de solicitações de API. Se você optar por usar este serviço, recomendamos que implemente um sistema robusto de balanceamento de carga.) Veja abaixo como ativar os recursos experimentais:

1. Ative os Recursos de Teste Beta nas Configurações do Desenvolvedor
2. Encontre DeepLX (Beta) nas Configurações Básicas e insira a URL da API DeepL auto-implementada, por exemplo, http\://seu-dominio/translate

> P: Como posso implementar eu mesmo?
>
> R: [OwO-Network/DeepLX](https://github.com/OwO-Network/DeepLX#setup-on-immersive-translate) ou [zu1k/deepl](https://github.com/KyleChoy/zotero-pdf-translate/blob/CustomDeepL/README.md) -->

## Solução de Problemas

1. **"A chave fornecida não está disponível":**
   - Verifique se você está utilizando a chave da **DeepL API Pro** e não da DeepL Pro.

2. **"DeepL API Free Retorna 401 Sem Privilégio":**
   - Confirme se sua chave termina em `:fx`, indicando que é uma chave da API Free.

3. **"456, Cota do usuário atingida":**
   - Você excedeu o limite de uso da DeepL.
   - Evite o uso excessivo para não violar a política de uso justo.
   - Se for um assinante pago, o uso será redefinido no próximo mês.
