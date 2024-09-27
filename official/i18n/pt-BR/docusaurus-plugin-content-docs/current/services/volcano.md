# Como implementar a Tradução Automática - Volcano Engine no Immersive Translate

### Informações Gerais

- **Website Oficial:** [Tradução Automática - Volcano Engine](https://www.volcengine.com/product/machine-translation)
- **Descrição Oficial de Tarifas:** [Faturamento de Produtos Tradução Automática - Volcano Engine](https://www.volcengine.com/docs/4640/68515)
- **Limite de Uso Gratuito:** 2 milhões de caracteres por mês.
- **Tarifa após o Limite:** US$ 49 por milhão de caracteres.

### Etapas de Configuração

1. **Acesso à API:**

   - Acesse o [Console Volcano Engine](https://console.volcengine.com/home).
   - Siga as instruções em [Visão Geral do Processo de Acesso à API Tradução Automática - Volcano Engine](https://www.volcengine.com/docs/4640/130872) para:
     - Registrar sua conta.
     - Realizar a autenticação de nome real.
     - Abrir os serviços de tradução.

2. **Obtenção da Chave de Acesso:**

   - **Opção 1: Conta Principal (Menos Segura):**
     - Selecione "Continuar a criar".
     - Anote o "ID da Chave de Acesso" e a "Chave de Acesso Secreta" exibidos na tabela.
   - **Opção 2: Subusuário (Recomendada):**
     - Crie um novo subusuário com a permissão `TranslateFullAccess`.
     - Anote o "ID da Chave de Acesso" e a "Chave de Acesso Secreta" do subusuário.

3. **Integração no Immersive Translate:**

   - Abra as "Configurações Básicas" do Immersive Translate.
   - Em "Serviços de Tradução", encontre a opção "Tradução Volcano".
   - Preencha os campos com o "ID da Chave de Acesso" e a "Chave de Acesso Secreta".

4. **Pronto!** Agora você pode utilizar a Tradução Automática da Volcano Engine no Immersive Translate.

**Dúvidas ou Problemas?** Envie seu feedback em [https://github.com/immersive-translate/immersive-translate/issues/137](https://github.com/immersive-translate/immersive-translate/issues/137).
