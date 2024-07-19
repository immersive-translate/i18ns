# Como implementar o ColourCloud Little Translator no Immersive Translate

## Informações Gerais

- **Site Oficial:** [ColorfulClouds Technology](https://docs.caiyunapp.com/en/) (Em inglês)
- **Introdução Oficial:** [Conheça a API do ColourCloud Little Translator em 5 minutos](https://docs.caiyunapp.com/lingocloud-api/)
- **Cota Gratuita:** 1 milhão de palavras por mês.
- **Tarifa após o Limite:** 39 yuan por 1 milhão de palavras (contados como caracteres no texto original, incluindo espaços e pontuação).

## Etapas de Configuração

1. **Certificação do Desenvolvedor:**
   - Faça login na [Plataforma Aberta da ColorCloud](https://dashboard.caiyunapp.com/).
   - Acesse "Minha Conta" > "Informações do Desenvolvedor" ([https://dashboard.caiyunapp.com/user/user/info/](https://dashboard.caiyunapp.com/user/user/info/)).
   - Preencha as informações:
     - Tipo de conta: "Indivíduos e Organizações sem Fins Lucrativos".
     - Nome pessoal, nome da organização, nome do contato e número de telefone.
   - Em "Categorias do Aplicativo", selecione "ColourCloud Little Translator API".
   - Preencha "immersive-translate" nos campos "Nome do Aplicativo" e "Link do Aplicativo".
   - Em "Desenvolvimento do Aplicativo", preencha "Extensões do Navegador".
   - Clique em "Enviar" e aguarde a aprovação (geralmente em até dois dias úteis).

2. **Obtenção do Token:**
   - Após a aprovação, acesse a lista "Meus Tokens - Token" ([https://dashboard.caiyunapp.com/v1/token/](https://dashboard.caiyunapp.com/v1/token/)).
   - Anote o seu "Token".

3. **Integração no Immersive Translate:**
   - Insira o "Token" nas configurações do Immersive Translate.

4. **Pronto!** Agora você pode utilizar o ColourCloud Little Translator no Immersive Translate.

**Dúvidas ou Problemas?** Envie seu feedback em [https://github.com/immersive-translate/immersive-translate/issues/137](https://github.com/immersive-translate/immersive-translate/issues/137).