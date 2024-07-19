# Como implementar o Tradutor de IA do Azure da Microsoft no Immersive Translate

## Informações Gerais

- **Explicação (Oficial):** [O que é a Tradução de Texto do Azure?](https://learn.microsoft.com/pt-br/azure/ai-services/translator/text-translation-overview)
- **Plano Gratuito:** Traduções gratuitas para até 2 milhões de palavras por mês.
- **Tarifa após o Limite:** US$10 por 1 milhão de palavras adicionais.
- **Detalhes dos Preços:** [Preços do IA do Azure Tradutor](https://azure.microsoft.com/pt-br/pricing/details/cognitive-services/translator/)

## Processo de Cadastro (Requer Paciência)

1. **Conta Azure:**
   - Acesse o site do [Microsoft Azure](https://azure.microsoft.com/pt-br/free/ai-services/) e crie uma conta.
   - **Importante:** É necessário um cartão de crédito internacional (Visa/Master) para o cadastro.

2. **Conta de Armazenamento Azure Blob:**
   - Acesse [https://portal.azure.com/#create/Microsoft.StorageAccount](https://portal.azure.com/#create/Microsoft.StorageAccount).
   - Crie um novo grupo de recursos e defina o nome da conta.
   - Escolha a região mais próxima (ex: "Ásia Oriental" para Hong Kong).
   - Siga as instruções e clique em "Criar" ao finalizar.

3. **Criação da Ferramenta de Tradução:**
   - Acesse [https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation).
   - Escolha a região mais próxima.
   - Selecione o plano `F0 Gratuito` (não suporta tradução de documentos) ou um plano pago.
   - Siga as instruções e clique em "Criar" ao finalizar.

## Obtenção da Chave de Acesso

1. **Painel do Azure:**
   - Acesse o [Painel do Azure](https://portal.azure.com/#home).
   - Vá para a página "Ferramentas de Tradução".
   - No menu à esquerda, em "Gerenciamento de Recursos", clique em "Chaves e Pontos de Extremidade".
   - Anote uma das duas chaves fornecidas e a região (ex: "eastasia").

2. **Configuração no Immersive Translate:**
   - Preencha o campo `APIKEY` com a chave obtida.
   - Preencha o campo `region` com a região correspondente.

## Suporte

Em caso de dúvidas: 
- Consulte a [Documentação de Introdução ao Microsoft Azure Translation]([https://learn.microsoft.com/en-us/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp)) 

- Ou nos envie seu feedback em [https://github.com/immersive-translate/immersive-translate/issues/137](https://github.com/immersive-translate/immersive-translate/issues/137).