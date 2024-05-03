# Tradução Microsoft Azure

## Declaração Breve

1. Site oficial: [Traduzido pelo Microsoft Azure](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/text-translation-overview)
2. Descrição Oficial: As traduções são gratuitas até 2 milhões de palavras por mês, se você exceder 2 milhões de palavras por mês, será cobrado à taxa de $10 / 1 milhão de palavras. Para mais detalhes, consulte [Nota de Preços](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/)

## Processo de Registro

O processo de registro é mais complicado do que outros serviços de tradução e requer paciência.

Link de Referência: [Documentação de Introdução à Tradução do Microsoft Azure](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp)

## Inscreva-se para uma conta Azure

O primeiro passo é se inscrever para uma conta [Azure](https://azure.microsoft.com/en-us/free/cognitive-services/), o que requer um cartão de crédito internacional (Visa/Master) para ser vinculado. Caso contrário, não será possível registrar.

## Registrando-se para uma Conta de Armazenamento Azure Blob

Passo 2: Registrar-se para uma conta de armazenamento [Azure Blob](https://portal.azure.com/#create/Microsoft.StorageAccount).

1. Crie um novo grupo de recursos e preencha o nome da conta de armazenamento
2. Escolha uma região que esteja mais próxima de você, por exemplo, a região de Hong Kong seria `Ásia Oriental`.
3. O resto do processo é apenas um passo simples. Na última página, após a conclusão da implantação, clique no botão azul "Criar" no canto inferior esquerdo.## Criando Ferramentas de Tradução

Etapa 3: Crie uma [ferramenta de tradução](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation)

1. Escolha uma região que esteja mais próxima de você, por exemplo, a região de Hong Kong seria `Leste Asiático`.
2. Os níveis de preço são selecionados conforme necessário, com `Grátis F0` disponível para usuários gratuitos. O nível gratuito não suporta tradução de documentos. Um teste padrão S1 pode ser usado, se necessário.
3. O restante do processo é apenas um próximo passo simples. Na última página, após a conclusão da implantação, clique no botão azul "Criar" no canto inferior esquerdo.

## Chave de Acesso

Após a implantação bem-sucedida, vá para o [Painel do Azure](https://portal.azure.com/#home), acesse a página de **Ferramentas de Tradução** e encontre a chave no menu à esquerda - Gerenciamento de Recursos - `Chaves e Endpoints`. A Microsoft fornecerá 2 chaves, escolha uma e preencha a chave no `APIKEY` da Extensão Imersiva - Tradutor da Microsoft.

Abaixo da chave, também há uma informação de `localização/região`, por exemplo, `lesteasiático`, que também precisa ser preenchida na `região` da extensão imersiva - Tradutor da Microsoft.

## Problemas Comuns

Em caso de dúvidas, por favor, dê seu feedback [aqui](https://github.com/immersive-translate/immersive-translate/issues/137).