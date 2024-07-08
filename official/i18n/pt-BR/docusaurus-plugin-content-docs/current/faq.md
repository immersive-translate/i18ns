---
sidebar_position: 9
---

# Perguntas Frequentes

## O conteúdo principal de sites como Youtube e Facebook é traduzido, mas algumas barras laterais não são. Quero traduzir tudo.

Para facilitar a leitura da página, o Immersive Translation por padrão traduz apenas a área de conteúdo principal. Se você deseja traduzir tudo:

Abra o painel da botão flutuante (pressione longamente no celular) -> Clique em "Mais" no canto inferior direito -> Selecione "Todas as áreas".

## Botão Flutuante não Exibido em Aplicativos do Youtube (ou Outros) no Celular

Plugins de navegador funcionam apenas em navegadores e não podem ser usados em outros aplicativos.

- Clicar no YouTube em um navegador iOS abre diretamente o aplicativo.

  Pressione e segure o link do YouTube para abrir uma janela flutuante e escolha abrir em uma página da web.

## Como desativar a tradução automática?

- Cancele no painel pop-up ou na página de Configurações.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="como desativar a tradução automática" width="250" />

<!-- - Ou altere: através da página de configurações

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## Não há permissão para traduzir a página atual

- Página padrão do navegador (sem endereço na barra de endereço)
- Página de plugin de terceiros
- Página da Google Store com plugin do Google desativado

## Como não mostrar o texto original?

Toque no ícone do Immersive Translate para abrir o painel de expansão, toque em [Mais], [Mudar para o modo somente tradução].

## Um ponto de exclamação aparece na página

Um ponto de exclamação na página indica que o serviço de tradução encontrou um problema e retornou um erro. Você pode passar o mouse sobre o ponto de exclamação para ver o erro específico.

### Erro 429

Este é um dos erros mais comuns. 429 indica que a frequência de solicitações é muito rápida. A tradução de páginas da web tem um grande número de parágrafos a serem traduzidos. Embora tenhamos feito uma grande otimização, incluindo mesclagem de parágrafos, controle de frequência, etc., às vezes ainda há alguns serviços de tradução sobrecarregados, retornando o erro 429 de limite de frequência. Nesse caso, você pode geralmente mudar temporariamente para outros serviços de tradução ou esperar um pouco e tentar novamente.

Se você estiver usando o serviço do Google e encontrar o erro 429, geralmente é um caso de limite de tráfego do Google em seu nó, e é recomendado mudar de nó.

## Tradução de documentos locais

Se você precisar traduzir arquivos HTML, TXT ou PDF locais, clique no ícone da extensão Immersive Translate, depois clique em [Mais], clique em [Traduzir arquivos PDF] ou [Traduzir arquivos HTML/TXT] para traduzir arquivos locais.

Se você estiver usando navegadores do tipo Chrome, como (Chrome, Arc, Edge), há outra maneira: abra a página de gerenciamento de extensões do navegador `chrome://extensions`, encontre o plugin [Immersive Translate], [Permitir acesso a URLs de arquivo] e, em seguida, abra diretamente no navegador o arquivo HTML ou PDF local. Você poderá clicar com o botão direito e selecionar [traduzir].

## Como atualizar a extensão?

Geralmente, as extensões instaladas na loja do navegador são atualizadas automaticamente. A atualização geralmente ocorre em até um dia após a atualização da extensão. Se você quiser atualizar imediatamente para a versão mais recente, abra a página [Gerenciar Extensões] do navegador, ative o [Modo Desenvolvedor] e clique em [Atualizar] na parte superior para atualizar imediatamente para a versão mais recente da loja.

![](/assets/docs/doc-assets/update-extension.png)

## Estilo de configuração de legendas do YouTube

Você pode clicar nas configurações de legendas do próprio YouTube, em [Opções], e ajustar o tamanho, a cor e outros aspectos.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Navegadores compatíveis com o Immersive Translate Tampermonkey

Extensões Grease Monkey recomendadas para Chrome e Firefox em desktop:

- [Tampermonkey](https://www.tampermonkey.net/)

Extensão Grease Monkey recomendada para Safari:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Se você usa o [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) no Safari, busque pelo Script de Otimização Immersive Translate para baixar diretamente da loja do Stay (otimizado especificamente para o Stay) -->

Extensões Grease Monkey recomendadas para Android:

1. Você pode instalar a extensão [Tampermonkey](https://www.tampermonkey.net/) usando a [versão mais recente do Firefox](https://www.mozilla.org/firefox/browsers/mobile/android/).

<!-- 2. Você também pode usar diretamente o [X Browser](https://www.xbext.com/?ref=immersive-translate). Após a instalação, abra o [Endereço do Immersive Translate para o Tampermonkey ](https://download.immersivetranslate.com/immersive-translate.user.js) para instalá-lo! -->

<!-- Extensões Grease Monkey conhecidas por serem incompatíveis:

- Android Via Browser
- iOS Alook Browser -->

(since such browsers do not implement the required Grease Monkey API)

## Problema de bloqueio da interface do Google Tradutor

Adicione o nome de domínio `translate.googleapis.com` à regra de proxy.

## Como atualizar as regras mais recentes?

A própria extensão sincronizará regularmente as regras de adaptação mais recentes do site oficial quando você a usar. Você também pode sincronizar manualmente clicando no ícone da extensão Immersive Translate no navegador para abrir uma janela pop-up, onde a extensão detectará automaticamente as regras de adaptação mais recentes e as sincronizará. O mesmo vale para Tampermonkey.

## Como salvar o feedback da página da web se eu tiver problemas com a tradução da página?

Clique com o botão direito e selecione "Salvar como" ou use o atalho Ctrl+S na página da web, escolha a opção de salvar como arquivo único e, por fim, o formato do arquivo será .mht/.mhtml. Em seguida, envie o arquivo para support@immersivetranslate.com.

<!-- ![save mht](/assets/save_mht.png) -->

## Erro de tradução na Color Cloud

Toque para remover a mensagem de erro "Unsupported trans_type". Você pode selecionar o idioma para ser detectado automaticamente por meio do idioma especificado.

## A leitura do WeChat não pode ser traduzida

Não é possível traduzir porque o WeChat Reading fez um processamento especial no conteúdo para impedir o acesso ao conteúdo por meios de terceiros.

## A tradução acionada não funciona

Outros sites são traduzidos, mas um site não.

- Se este site tiver poucos visitantes:
  - Sugira parágrafos para serem traduzidos passando o mouse sobre eles.
  - Se você precisar traduzir o site inteiro, pode adaptá-lo através de [regras do usuário](/docs/advanced/#user-rules).
- Se este site for usado por muitas pessoas:
  - Você pode começar passando o mouse para traduzir o uso.
  - Relate no grupo para que seja adaptado posteriormente.

## O aprimoramento da caixa de entrada não funciona

- Pesquisa do Google na página inicial do navegador

A caixa de pesquisa do Google deve estar na página da web com a URL [Google](https://www.google.com/) e não pode ser usada na página inicial do navegador ou em espaços em branco na barra de endereço.

## Log de depuração de feedback

- Ative o registro de depuração:
  Abra o Painel -> Configurações -> Configurações do desenvolvedor -> Ative "Imprimir log de depuração no console".
- Abra o console do site:
  Clique com o botão direito para abrir a revisão -> Mude para o console na parte superior da coluna direita -> Execute a ação para ver os logs.

## Como desativar o Botão Flutuante

- Ocultar na página atual

- Defina como "Nunca traduzir este site".

- Ocultar em todas as páginas

Abra [Página de Configurações] - [Configurações da Interface] e desative [Mostrar Botão Flutuante na Página].

## Erro ao instalar o instalador do plugin no Chrome

- Valor inválido para web_accessible_resource[0]

  É necessária a versão Chromium 88 ou superior para suportar manifest_version 3.

## Como instalar no navegador 360?

Somente o 360 Extreme Browser x é compatível (lembre-se, é com x). Se você tiver acesso à loja de extensões do Google, poderá ir diretamente lá e instalá-lo. Se você não conseguir acessá-lo, [instale-o manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features).

## O navegador Opera não funciona

- Não funciona em google.com e outras páginas de pesquisa. O plugin exibe `Atualize a página atual antes de iniciar a tradução` e atualizar a página ainda exibe esta mensagem.

Você precisa encontrar "Immersive Translate" nas configurações de plugins do Opera e ativar a opção "Permitir acesso aos resultados da página de pesquisa".

<!-- ![](/assets/opera-allow-search.png) -->

## As legendas bilíngues do YouTube em chinês tradicional não são exibidas

O YouTube vem com legendas traduzidas automaticamente, e o chinês tradicional terá erros de formatação, fazendo com que todas as legendas apareçam com uma grande seção de legendas no início. Com base nesse cenário, é recomendável ativar a opção [Usar Immersive Translate para traduzir legendas] em [Configurações] [Legendas de vídeo].

## Mais perguntas (ver muito)

<details>
<summary>Como limpar o cache com Tampermonkey?</summary>
<p>
Devido à limitação da API do Tampermonkey, o cache do Immersive Translate Tampermonkey será salvo no cache do site correspondente. Para limpá-lo, abra as ferramentas do desenvolvedor do site correspondente no seu navegador e limpe o cache do site.
</p>
</details>

<details>
<summary>A solicitação de endereço da interface personalizada do Tampermonkey falhou? </summary>
<p>
O Tampermonkey exige que todas as solicitações do script precisem declarar permissões no início do script, por exemplo: `@connect api.google.com`. Portanto, se você precisar adicionar um novo nome de domínio que não seja o padrão, declare-o no início do Tampermonkey, seguindo o modelo de outros nomes de domínio.
</p>
</details>
