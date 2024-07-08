# Microsoft Azure Translation

## Informações Gerais

1. Site oficial: [Traduzido por Microsoft Azure](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/text-translation-overview)
2. Descrição Oficial: As traduções são gratuitas até 2 milhões de palavras por mês. Se você exceder 2 milhões de palavras por mês, cobraremos uma taxa de US$ 10 / 1 milhão de palavras. Para mais detalhes, consulte a [Observação de Preços](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/).

## Processo de Cadastro

O processo de registro é mais complicado do que outros serviços de tradução e requer paciência.

Link de Referência: [Documentação de Introdução ao Microsoft Azure Translation] ([https://learn.microsoft.com/en-us/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp))

## Cadastro de Conta Azure

O primeiro passo é se inscrever em uma conta [Azure] ([https://azure.microsoft.com/en-us/free/cognitive-services/](https://azure.microsoft.com/en-us/free/cognitive-services/)), que requer um cartão de crédito internacional (Visa/Master) para ser vinculado. Caso contrário, não será possível se registrar.

## Cadastro de Conta de Armazenamento Azure Blob

Passo 2: Cadastre-se para uma conta de armazenamento [Azure Blob] ([https://portal.azure.com/#create/Microsoft.StorageAccount](https://portal.azure.com/#create/Microsoft.StorageAccount)).

1. Crie um novo grupo de recursos e preencha o nome da conta de armazenamento.
2. Escolha a região mais próxima de você, por exemplo, a região de Hong Kong seria `Ásia Oriental`.
3. O restante do processo é apenas seguir os próximos passos. Na última página, após a implantação ser concluída, clique no botão azul "Criar" no canto inferior esquerdo.

## Criação de Ferramentas de Tradução

Passo 3: Crie uma [ferramenta de tradução] ([https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation))

1. Escolha a região mais próxima de você, por exemplo, a região de Hong Kong seria `Ásia Oriental`.
2. Os planos de preços são selecionados conforme necessário, com o `F0 Gratuito` disponível para usuários gratuitos. O nível gratuito não suporta tradução de documentos. Um teste padrão S1 pode ser usado se necessário.
3. O restante do processo é apenas seguir os próximos passos. Na última página, após a implantação ser concluída, clique no botão azul "Criar" no canto inferior esquerdo.

## Chave de Acesso

Após a implantação bem-sucedida, vá para o [Painel do Azure] ([https://portal.azure.com/#home](https://portal.azure.com/#home)), acesse a página de **Ferramentas de Tradução** e encontre a chave no menu à esquerda - Gerenciamento de Recursos - `Chaves e Pontos de Extremidade`. A Microsoft fornecerá 2 chaves, escolha uma e preencha a chave no campo `APIKEY` da Extensão Immersive - Microsoft Translator.

Abaixo da chave, há também uma informação de `local/região`, por exemplo, `eastasia`, que também precisa ser preenchida no campo `region` da extensão Immersive - Microsoft Translate.

## Problemas Comuns

Em caso de dúvidas, envie seu feedback [aqui] ([https://github.com/immersive-translate/immersive-translate/issues/137](https://github.com/immersive-translate/immersive-translate/issues/137)).
