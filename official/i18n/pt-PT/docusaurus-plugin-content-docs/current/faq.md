---
sidebar_position: 9
---

# FAQ

## Impossível baixar da Apple Store

- 2023.07.28: Apple Store rebaixada na China de acordo com a política
- 2023.08.05: foi relançada na China

## Como desativar a tradução automática

- Cancelar no painel Popup ou na página de Configurações.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="desativar tradução automática" width="250" />


## Sem permissão para traduzir a página atual

- Página padrão do navegador (sem endereço na barra de endereços)
- Página de plugin de terceiros
- Plugin do Google desabilita página da Google Store

## Como não mostrar o texto original?

Toque no ícone do Immersive Translate para abrir o painel de expansão, toque em [Mais], [Mudar para o Modo Apenas Tradução]

## Ponto de exclamação aparece na página

Um ponto de exclamação na página indica que o serviço de tradução encontrou um problema e retornou um erro, você pode mover o mouse sobre o ponto de exclamação para visualizar o erro específico.


### Erro 429

Este é um dos erros mais comuns, o 429 indica que a frequência de solicitações é muito rápida. A tradução de páginas da web possui um número muito grande de parágrafos a serem traduzidos, embora tenhamos feito uma grande otimização, incluindo a fusão de parágrafos, controle de frequência, etc., mas às vezes ainda há alguns serviços de tradução sobrecarregados, retornando o erro de limite de frequência 429. Neste caso, você pode geralmente alternar temporariamente para outros serviços de tradução, ou esperar um pouco e tentar novamente.

Se você está enfrentando o erro 429 em um serviço do Google, geralmente é um caso de o Google estar fazendo um limite de tráfego contra seu nó, e é recomendado trocar de nó.

## Tradução de documentos locais

Se você precisa traduzir arquivos HTML locais, arquivos txt ou arquivos PDF, você pode clicar no ícone da extensão Immersive Translate, depois clicar em [Mais], clicar em [Traduzir arquivos PDF] ou [Traduzir arquivos HTML/txt] para traduzir arquivos locais.

Se você está usando navegadores semelhantes ao Chrome, como (Chrome, Arc, navegador Edge), há outra maneira, que é abrir a página de gerenciamento de extensões do navegador `chrome://extensions`, encontrar o plug-in [Immersive Translate], [Permitir que a extensão acesse arquivos locais], e então diretamente no navegador abrir o arquivo HTML local ou arquivo PDF local, você pode clicar com o botão direito em [tradução].

## Como faço para atualizar a extensão?

De modo geral, extensões instaladas na loja do navegador serão atualizadas automaticamente, a situação geral será atualizada automaticamente dentro de um dia após a atualização da extensão, se você quiser atualizar imediatamente para a versão mais recente, você pode, na página [Gerenciamento de Extensões] do navegador, abrir o [Modo Desenvolvedor], e então clicar em [Atualizações] no topo, você pode imediatamente atualizar para a versão mais recente da loja.

![](/assets/docs/doc-assets/update-extension.png)

## Configuração de legendas no Youtube

Você pode clicar nas próprias configurações de legendas do Youtube, [Opções], e então ajustar o tamanho, cor, e assim por diante.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Navegadores Suportados pelo Immersive Translate Tampermonkey

Extensões Grease Monkey recomendadas para Chrome, Firefox no desktop:

- [Tamper Monkey](https://www.tampermonkey.net/)

Extensão Grease Monkey recomendada para Safari:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Se usando [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) no Safari, por favor, procure pelo Script de Otimização do Immersive Translate para baixar diretamente da loja própria do Stay (otimizado especificamente para Stay) -->

Extensões Grease Monkey Recomendadas para Android:

1. Você pode instalar a extensão [Tamper Monkey](https://www.tampermonkey.net/) usando a [Última Versão do Firefox](https://www.mozilla.org/firefox/browsers/mobile/android/).

<!-- 2. Você também pode usar diretamente o [X Browser](https://www.xbext.com/?ref=immersive-translate), após a instalação, abra diretamente o [Endereço Tampermonkey do Immersive Translate](https://download.immersivetranslate.com/immersive-translate.user.js) para instalá-lo! -->

<!-- Extensões Grease Monkey conhecidas por não serem suportadas:

- Navegador Via no Android
- Navegador Alook no iOS -->

(já que tais navegadores não implementam a API Grease Monkey necessária)

## Problema de Acesso Bloqueado da Interface do Google Tradutor

Por favor, adicione o nome de domínio `translate.googleapis.com` à regra de proxy

## Como atualizar as regras mais recentes

A própria extensão irá sincronizar regularmente com as regras de adaptação mais recentes do site oficial quando você a utilizar. Você também pode sincronizar manualmente com as regras mais recentes clicando no ícone da Extensão de Tradução Imersiva do navegador para abrir uma janela pop-up onde a extensão detectará automaticamente as regras de adaptação mais recentes e sincronizará com elas. O mesmo se aplica ao Tampermonkeys.

## Como salvo o feedback da minha página web se tiver problemas com a tradução da página?

Você precisa clicar com o botão direito em "Salvar como" ou usar o atalho ctrl+s na página web, escolher a opção de salvar arquivo único, e finalmente o formato do arquivo é .mht/.mhtml. Em seguida, envie o arquivo para support@immersivetranslate.com

<!-- ![salvar mht](/assets/save_mht.png) -->

## Erro de Tradução da Nuvem de Cores

Toque para longe? A mensagem de erro para o número "Tipo de translação não suportado" é exibida. Você pode selecionar o idioma para ser detectado automaticamente por meio do idioma especificado.

## Leitura do WeChat Não Pode Ser Traduzida

Não pode ser traduzida porque a Leitura do WeChat fez um processamento especial no conteúdo para impedir o acesso ao conteúdo por meios de terceiros.

## A tradução acionada não tem efeito

Outros sites traduzem, mas um site não.

- Se este site tem menos visitantes
  - Sugere-se parágrafos a serem traduzidos passando o mouse
  - Se você precisa traduzir o site inteiro, você pode adaptá-lo via [regras do usuário](/docs/advanced/#user-rules)
- Se este site é usado por muitas pessoas
  - Você pode começar passando o mouse para traduzir o uso de
  - Chame-o no grupo e ele será adaptado mais tarde

## O aprimoramento da caixa de entrada não tem efeito

- Página inicial do navegador Pesquisa Google

A caixa de pesquisa do Google deve estar na URL da página web do [Google](https://www.google.com/) e não pode ser usada na página inicial do navegador, nos lugares em branco da barra de endereços

## Registro de depuração de feedback

- Ativar o registro de depuração
  Abrir Painel -> Configurações -> Configurações do Desenvolvedor -> Ativar "Imprimir registro de depuração no console".
- Abrir o console do site
  Clique com o botão direito para abrir a revisão -> Mudar para o console no topo da coluna direita -> Realizar a ação para ver os registros

## Como desativar o hoverball

- Ocultar na página atual

Defina como "Nunca traduzir este site".

- Ocultar em todas as páginas

Abra [Página de Configurações] - [Configurações de Interface] e desative [Mostrar Hoverball na Página].

## Erro ao instalar o instalador de plugin no chrome

- valor inválido para web_accessible_resource[0]

  É necessário ter a versão do Chromium maior que 88 para suportar manifest_version 3.

## Como instalar o Navegador 360

Apenas o Navegador 360 Extreme x é suportado, lembre-se de que é com x. Se você tem acesso à loja de Extensões do Google, pode ir diretamente lá e instalá-lo. Se não conseguir acessar [instale manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## Navegador Opera não funciona

- Não funciona no google.com e outras páginas de pesquisa, o plugin exibe `Por favor, atualize a página atual antes de iniciar a tradução` e atualizar a página ainda assim exibe esta mensagem.

Você precisa encontrar "Immersive Translate" nas configurações de plugin do Opera e ativar a opção "Permitir acesso aos resultados da página de pesquisa".

<!-- ![](/assets/opera-allow-search.png) -->

## Legendas bilíngues do YouTube em chinês tradicional não exibidas

O YouTube vem com legendas traduzidas por máquina, e o Chinês Tradicional terá erros de formatação, fazendo com que todas as legendas apareçam com uma grande seção de legendas no início, com base neste cenário, é recomendado ativar a opção [Usar Immersive Translate para Traduzir Legendas] em [Configurações] [Legendas de Vídeo].

## Mais perguntas (ver muito mais)

<details>
<summary>Como limpo meu cache com Tampermonkey?</summary>
<p>
Devido à limitação da API do Tampermonkey, o cache do Immersive Translate Tampermonkey será salvo no cache do site correspondente, então, se você quiser limpá-lo, você pode abrir o painel de ferramentas do desenvolvedor do site correspondente no seu navegador e, em seguida, limpar o cache desse site.
</p>
</details>

<details>
<summary>Falha na solicitação de endereço de interface personalizada do Tampermonkey?</summary>
<p>
O Tampermonkey exige que todas as solicitações do script precisem declarar permissões no início do script, por exemplo: `@connect api.google.com`, então, se você precisar adicionar um novo nome de domínio que não seja o padrão, por favor, declare-o no início do Tampermonkey modelado após o outro nome de domínio.
</p>
</details>