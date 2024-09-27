# Open AI (Azure OpenAI)

Acesso direto aos serviços de tradução da OpenAI abrindo uma [assinatura Immersive Translate Pro](https://immersivetranslate.com/en/pricing/) (recomendado)

[Clique aqui para apresentação](https://immersivetranslate.com/en/pricing/)

## Obtenha uma Chave de API da plataforma oficial de desenvolvedores da OpenAI.

- [endereço oficial da API openAI](https://openai.com/api/)
  - Nota: Atualmente, a OpenAI não está aberta para registro com números de celular chineses.
- Após registrar uma conta na OpenAI, abra [Chave Secreta da API](https://platform.openai.com/account/api-keys) para criar uma Chave Secreta da API
- Depois é só preencher a chave na configuração da OpenAI na extensão Immersive Translate.## Aviso

1. **Se você não tem um cartão de crédito vinculado, ou é um novo usuário do OpenAI 5-lâminas com até 3 solicitações por minuto**, basicamente torna-se inutilizável e é normal receber erros. [Você pode clicar aqui para ver os limites de frequência para sua API](https://platform.openai.com/account/rate-limits)
2. A API da OpenAI e o ChatGPT são dois serviços diferentes, a Extensão de Tradução Imersiva suporta a API da OpenAI, não a versão web do ChatGPT, então você precisa abrir o serviço da API da OpenAI em vez de abrir o ChatGPT Plus, e preencher a Chave da API na página de Configurações após abrir.
3. Erro 429 significa que o limite de frequência da openai foi excedido, é recomendado reduzir o número máximo de solicitações por segundo, especialmente ao traduzir e-books, mesmo que seja uma versão paga, você precisa reduzir o número máximo de solicitações por segundo e ajustá-lo para 5 solicitações por segundo para torná-lo mais estável.
4. O modelo OpenAI gpt-3.5-turbo tem o preço de: $0.002 / 1K tokens, e custa cerca de $1 para traduzir 660.000 caracteres em inglês e $0.25 para traduzir 170.000 caracteres em inglês.
5. A Extensão de Tradução Imersiva suporta múltiplas chaves de API para balanceamento de carga, por favor, use vírgula `,` para separar diferentes chaves quando preencher o formulário.

## Recomendação atual de número de solicitações

Recentemente, a OpenAI também se tornou muito restritiva para usuários pagos, a partir da versão 0.5.0 a contagem de solicitações padrão foi alterada para segundos, e o número máximo padrão de solicitações por segundo foi alterado para 10 solicitações por segundo.## Azure OpenAI

O serviço de tradução da OpenAI também é compatível com a interface do Azure OpenAI. Primeiro, crie o serviço OpenAI no console do Azure, depois vá para o Azure AI Studio: https://oai.azure.com, crie um deployment do gpt-35-turbo e lembre-se do nome do deployment.

Após fazer o deployment do modelo gpt-35-turbo, abra a página de configurações da OpenAI para o Immersive Translate:

1. Chave da API Por favor, preencha com a chave fornecida pelo console do Azure.
2. Clique para expandir mais configurações e defina o endereço personalizado para:

`https://{seu-nome-personalizado}.openai.azure.com/openai/deployments/{seu-nome-de-deployment}/chat/completions?api-version=2024-07-01-preview`

Altere `{seu-nome-personalizado}` para o seu próprio subdomínio e `{seu-nome-de-deployment}` para o nome do seu próprio deployment.

3. O nome do modelo precisa ser selecionado manualmente para o modelo personalizado ler: `gpt-35-turbo`,

> Se ainda houver dúvidas, você pode entrar no Azure AI Studio, abrir o PlayGround, [Ver Código], e lá embaixo terá o [EndPoint] e a [Chave] finais, conforme a seguir:

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/azure-openai-key.jpg)

## Personalizando o Endereço da API da OpenAI

- Isso pode ser configurado via `Mais Configurações` com o seguinte ponto de entrada

---

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

---
