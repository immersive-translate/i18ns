# Como implementar a Tradução da AliCloud no Immersive Translate

## Informações Gerais

- **Site Oficial:** [Machine Translation_Ali AI Translation_Document Image Translation - AliCloud](https://www.aliyun.com/product/ai/alimt)
- **Descrição Oficial de Tarifas:** [Payment Models and Specific Pricing for Machine Translation_Machine Translation-AliCloud Help Center](https://help.aliyun.com/document_detail/197134.html)
- **Limites de Uso Gratuito:**
    - Edição Geral: 1 milhão de caracteres por mês.
    - Edição Profissional: 1 milhão de caracteres por mês.
- **Tarifas após o Limite:**
    - Edição Geral: US$ 50 por milhão de caracteres.
    - Edição Profissional: US$ 60 por milhão de caracteres.

## Etapas de Configuração

1. **Login na Aliyun:** Acesse o [site oficial da Aliyun](https://www.aliyun.com/) e faça login na sua conta.

2. **Ativação do Serviço:**
    - Abra a página do serviço de Tradução Automática: [Machine Translation_Ali AI Translation_Document Image Translation-AliCloud](https://www.aliyun.com/product/ai/alimt).
    - Clique no botão "Abrir Agora".

3. **Seleção dos Tradutores:**
    - No console do serviço, selecione "Tradutor Universal" e "Tradutor Profissional".

4. **Criação da Chave de Acesso:**
    - Passe o mouse sobre seu avatar no canto superior direito da página e selecione [Gerenciamento de AccessKey](https://ram.console.aliyun.com/manage/ak).
    - **Recomendação de Segurança:** Crie uma subconta com o método de acesso "Método de chamada OpenAPI" para maior segurança.
    - Anote o "AccessKey ID" e o "AccessKey Secret" da subconta.

5. **Autorização da Subconta:**
    - Clique no nome de login da subconta.
    - Selecione "Gerenciamento de Permissões" > "Nova Autorização".
    - Em "Selecionar Permissão" > "Políticas do Sistema", procure por "Tradução Automática" e selecione "Gerenciar permissões para tradução automática (alimt)".

6. **Integração com o Immersive Translate:**
    - Insira o "AccessKey ID" e o "AccessKey Secret" nas configurações do Immersive Translate.

7. **Pronto!** Agora você pode utilizar a Tradução Automática da AliCloud no Immersive Translate.

**Dúvidas ou Problemas?** [Envie aqui](https://github.com/immersive-translate/immersive-translate/issues/137) o seu feedback.