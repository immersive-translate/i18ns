# Guia de Integração da OpenAI (Azure OpenAI) no Immersive Translate

## Opção Recomendada: Assinatura Pro do Immersive Translate

Para acesso direto e simplificado à OpenAI, adquira uma [Assinatura Pro do Immersive Translate](https://immersivetranslate.com/en/pricing/).

## Obtenção da Chave de API da OpenAI

1. **Plataforma OpenAI:**
   - Acesse o [site oficial da OpenAI](https://openai.com/api/).
   - **Obs.:** Atualmente, o registro na OpenAI não está disponível para números de celular chineses.
   - Após registrar uma conta, acesse a [página de Chaves da API](https://platform.openai.com/account/api-keys) nas configurações de sua conta OpenAI, e crie uma nova chave.

2. **Configuração no Immersive Translate:**
   - Insira a chave de API na seção de configuração da OpenAI no plugin.

## Advertências Importantes

1. **Limites de Uso:**
   - Novos usuários ou contas sem cartão de crédito vinculado podem ter um limite de até 3 solicitações por minuto, o que pode tornar o serviço inutilizável.
   - [Verifique aqui](https://platform.openai.com/account/rate-limits) seus limites de solicitações frequentes.

2. **API da OpenAI vs. ChatGPT:**
   - O Immersive Translate utiliza a API da OpenAI, não a versão web do ChatGPT. Certifique-se de ativar o serviço da API da OpenAI.

3. **Erro 429 (Limite Excedido):**
   - Reduza o número máximo de solicitações por segundo, especialmente ao traduzir e-books.
   - Recomenda-se um limite de 5 solicitações por segundo para maior estabilidade, mesmo em contas pagas.

4. **Custos:**
   - O modelo `gpt-3.5-turbo` custa US$ 0,002 por 1 mil tokens.
   - Traduzir 660.000 caracteres em inglês custa cerca de US$ 1.
   - Traduzir 170.000 caracteres em inglês custa cerca de US$ 0,25.

5. **Múltiplas Chaves de API:**
   - O Immersive Translate permite o uso de várias chaves para balanceamento de carga. Separe as chaves por vírgulas (`,`) na configuração.

## Recomendação de Número de Solicitações

- A partir da versão 0.5.0, a contagem de solicitações é feita por segundo, com um limite padrão de 10 solicitações por segundo.

## Azure OpenAI

1. **Criação do Serviço:**
   - Crie o serviço OpenAI no console do Azure.
   - Acesse o [Azure AI Studio](https://oai.azure.com) e crie uma implantação, e anote o nome da implantação. Ex: `gpt-35-turbo`.

2. **Configuração no Immersive Translate:**
   - Na página de configurações da OpenAI:
     - `Chave da API`: Insira a chave do console do Azure.
     - `Endereço personalizado`:
       - `https://{seu-nome-personalizado}.openai.azure.com/openai/deployments/{seu-nome-de-implantacao}/chat/completions?api-version=2024-07-01-preview`
       - Substitua `{seu-nome-personalizado}` e `{seu-nome-de-implantacao}` pelos seus dados.
     - `Nome do modelo`: Selecione manualmente. Ex: `gpt-35-turbo`.

Ainda tem dúvidas? Acesse o [Azure AI Studio](https://oai.azure.com), abra o PlayGround, [Exibir Código], e haverá o [EndPoint] e a [Chave] finais na parte inferior, como na imagem abaixo:

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/azure-openai-key.jpg)

### Personalização do Endereço da API da OpenAI

- Configure em `Mais Configurações` o seguinte ponto de entrada:

***

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

***