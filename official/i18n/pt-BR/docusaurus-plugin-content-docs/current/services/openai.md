# Open AI (Azure OpenAI)

Obtenha acesso direto aos serviços de tradução da OpenAI adquirindo uma [assinatura Pro do Immersive Translate](https://immersivetranslate.com/en/pricing/) (recomendado).

[Clique aqui para apresentação](https://immersivetranslate.com/en/pricing/)

## Obtenha uma chave de API na plataforma oficial de desenvolvedores da OpenAI.

- [Endereço oficial da API OpenAI](https://openai.com/api/)
  - Observação: Atualmente, a OpenAI não está aberta para registro com números de celular chineses.
- Após registrar uma conta OpenAI, abra [Chave Secreta da API](https://platform.openai.com/account/api-keys) para criar uma chave secreta de API.
- Em seguida, preencha a chave na configuração da OpenAI na extensão Immersive Translate.

## Advertências

1. **Se você não tiver um cartão de crédito vinculado ou for um novo usuário da OpenAI com limite de até 3 solicitações por minuto**, o serviço será praticamente inutilizável e é normal ocorrerem erros. [Clique aqui para ver os limites de frequência da sua API](https://platform.openai.com/account/rate-limits).
2. A API da OpenAI e o ChatGPT são serviços diferentes. A extensão Immersive Translate suporta a API da OpenAI, não a versão web do ChatGPT. Portanto, você precisa ativar o serviço da API da OpenAI em vez de abrir o ChatGPT Plus e preencher a chave de API na página de configurações após a ativação.
3. O erro 429 significa que o limite de frequência da OpenAI foi excedido. Recomenda-se reduzir o número máximo de solicitações por segundo, especialmente ao traduzir e-books. Mesmo na versão paga, é necessário reduzir o número máximo de solicitações por segundo e ajustá-lo para 5 solicitações por segundo para maior estabilidade.
4. O modelo gpt-3.5-turbo da OpenAI custa US$ 0,002 por 1 mil tokens e custa cerca de US$ 1 para traduzir 660.000 caracteres em inglês e US$ 0,25 para traduzir 170.000 caracteres em inglês.
5. A extensão Immersive Translate suporta várias chaves de API para balanceamento de carga. Use vírgulas `,` para separar as diferentes chaves ao preencher o formulário.

## Recomendação atual de número de solicitações

Recentemente, a OpenAI também se tornou muito restritiva para usuários pagos. A partir da versão 0.5.0, a contagem de solicitações padrão foi alterada para segundos e o número máximo padrão de solicitações por segundo foi alterado para 10.

## Azure OpenAI

O serviço de tradução da OpenAI também é compatível com a interface do Azure OpenAI. Primeiro, crie o serviço OpenAI no console do Azure, depois vá para o Azure AI Studio: [https://oai.azure.com](https://oai.azure.com), crie uma implantação gpt-35-turbo e lembre-se do nome da implantação.

Após implantar o modelo gpt-35-turbo, abra a página de configurações da OpenAI para o Immersive Translate:

1. Chave da API: Preencha a chave fornecida pelo console do Azure.
2. Clique para expandir mais configurações e defina o endereço personalizado para:

`https://{seu-nome-personalizado}.openai.azure.com/openai/deployments/{seu-nome-de-implantacao}/chat/completions?api-version=2023-03-15-preview`

Altere `{your-custom-name}` para seu próprio subdomínio e `{you-deployment-name}` para seu próprio nome de implantação.

1. O nome do modelo precisa ser selecionado manualmente para que o modelo personalizado leia: `gpt-35-turbo`.

> Se ainda houver dúvidas, você pode acessar o Azure AI Studio, abrir o PlayGround, [Exibir Código], e haverá o [EndPoint] e a [Chave] finais na parte inferior, como a seguir:

![](/assets/docs/doc-assets/azure-openai-key.jpg)

## Personalizando o Endereço da API da OpenAI

- Isso pode ser configurado em `Mais Configurações` com o seguinte ponto de entrada:

***

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

***
