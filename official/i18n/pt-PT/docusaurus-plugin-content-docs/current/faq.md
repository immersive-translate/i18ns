---
sidebar_position: 9
---

# FAQ

### 1. Android App, floating ball disappeared

As extensões de versões antigas estão desativadas, desinstale e instale a versão mais recente a partir do [site oficial](https://immersivetranslate.com/).

## O conteúdo principal em sites como Youtube, Facebook é traduzido, mas algumas barras laterais não são, quero traduzir tudo

Para a legibilidade da página, a tradução imersiva por padrão só traduz a área de conteúdo principal. Se quiser traduzir tudo.

Abra o painel da bola flutuante (pressione longamente no celular) -> Clique em mais no canto inferior direito -> Selecione todas as áreas

## Bolha Flutuante Não Exibida em Apps do Youtube (ou Outros) no Celular

Os plugins do navegador só podem ser executados em navegadores e não podem ser usados em outros aplicativos.

- Clicar no YouTube em um navegador iOS abre diretamente o App.

  Pressione e segure o link do YouTube para abrir uma janela flutuante e escolha abrir em uma página da web.

## Como desativar a tradução automática

- Cancele no painel Popup ou na página de Configurações.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="desativar tradução automática" width="250" />

<!-- - Ou altere: via a página de configurações

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## Sem permissão para traduzir a página atual

- Página padrão do navegador (sem endereço na barra de endereços)
- Página de plugin de terceiros
- Plugin do Google desativa a página da Google Store

## Como não mostrar o texto original?

Toque no ícone do Immersive Translate para abrir o painel de expansão, toque em [Mais], [Mudar para Modo Somente Tradução]

## Exclamação aparece na página

Um ponto de exclamação na página indica que o serviço de tradução encontrou um problema e retornou um erro, você pode mover o mouse sobre o ponto de exclamação para ver o erro específico.

### Erro 429

Este é um dos erros mais comuns, 429 indica que a frequência de solicitações é muito rápida. A tradução de páginas da web tem um número muito grande de parágrafos a serem traduzidos, embora tenhamos feito uma grande otimização, incluindo a fusão de parágrafos, controle de frequência, etc., mas às vezes ainda há alguns serviços de tradução sobrecarregados, retornando o erro de limite de frequência 429, neste momento você pode geralmente mudar temporariamente para outros serviços de tradução, ou esperar um pouco e tentar novamente.

Se você estiver usando um serviço do Google e encontrar o erro 429, geralmente é um caso de o Google aplicar um limite de tráfego contra o seu nó, e é recomendado mudar de nó.

## Tradução de documentos locais

Se precisar traduzir arquivos HTML locais, arquivos txt ou arquivos PDF, você pode clicar no ícone da extensão Immersive Translate, depois clicar em [Mais], clicar em [Traduzir arquivos PDF] ou [Traduzir arquivos HTML/txt] para traduzir arquivos locais.

Se você estiver usando navegadores semelhantes ao Chrome, como (Chrome, Arc, navegador Edge), há outra maneira, que é abrir a página de gerenciamento de extensões do navegador `chrome://extensions`, encontrar o plugin [Immersive Translate], [Permitir que a extensão acesse arquivos locais], e então abrir diretamente no navegador o arquivo HTML local ou arquivo PDF local, você pode clicar com o botão direito diretamente em [tradução].

**Nota**: O navegador Safari tem restrições rigorosas sobre o acesso de extensões a arquivos locais. Os usuários do Safari devem usar diretamente o Método 1 - clicar no ícone da extensão Immersive Translate, depois clicar em [Mais], clicar em [Traduzir arquivos PDF] ou [Traduzir arquivos HTML/txt] para traduzir arquivos locais.

## Como atualizar a extensão?

De modo geral, as extensões instaladas na loja do navegador serão atualizadas automaticamente, a situação geral será atualizada automaticamente dentro de um dia após a atualização da extensão, se você quiser atualizar imediatamente para a versão mais recente, você pode na página [Gerenciamento de Extensões] do navegador, abrir o [Modo Desenvolvedor], e então clicar no topo em [Atualizações], você pode atualizar imediatamente para a versão mais recente da loja.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Configuração de estilo de legendas do Youtube

Você pode clicar nas configurações de legendas do próprio Youtube, [Opções], e então ajustar o tamanho, cor, e assim por diante.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Navegadores Suportados pelo Immersive Translate Tampermonkey

Extensões Grease Monkey recomendadas para Chrome, Firefox no desktop:

- [Tamper Monkey](https://www.tampermonkey.net/)

Extensão Grease Monkey recomendada para Safari:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Se estiver usando [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) no Safari, por favor, procure o Script de Otimização do Immersive Translate para baixar diretamente da própria loja do Stay (otimizado especificamente para Stay) -->

Extensões Grease Monkey recomendadas para Android:

1. Você pode instalar a extensão [Tamper Monkey](https://www.tampermonkey.net/) usando [Firefox Última Versão](https://www.mozilla.org/firefox/browsers/mobile/android/).

<!-- 2. Você também pode usar diretamente o [X Browser](https://www.xbext.com/?ref=immersive-translate), após a instalação, abra diretamente o [Endereço do Immersive Translate Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) para instalá-lo! -->

<!-- Extensões Grease Monkey conhecidas por não serem suportadas:

- Android Via Browser
- iOS Alook Browser -->

(como esses navegadores não implementam a API Grease Monkey necessária)

## Problema de Bloqueio da Interface do Google Translate

Por favor, adicione o domínio `translate.googleapis.com` à regra de proxy

## Como atualizar as regras mais recentes

A própria extensão irá sincronizar regularmente com as regras de adaptação do site oficial mais recentes quando você a usar, você também pode sincronizar manualmente com as regras mais recentes clicando no ícone da Extensão Immersive Translate no navegador para abrir uma janela pop-up onde a extensão detectará automaticamente as regras de adaptação mais recentes e sincronizará com elas, o mesmo vale para Tampermonkeys.

## Como salvar meu feedback da página da web se eu tiver problemas com a tradução da página da web?

Você precisa clicar com o botão direito em "Salvar como" ou usar o atalho ctrl+s na página da web, escolher arquivo único para a opção de salvar, e finalmente o formato do arquivo é .mht/.mhtml. Em seguida, envie o arquivo para support@immersivetranslate.com

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Erro de Tradução da Nuvem de Cores

Desapareceu? A mensagem de erro para o número "Unsupported trans_type" é exibida. Você pode selecionar o idioma a ser detectado automaticamente por meio do idioma especificado.

## Leitura do WeChat Não Pode Ser Traduzida

Não pode ser traduzido porque a Leitura do WeChat fez um processamento especial para o conteúdo para impedir o acesso ao conteúdo por meio de meios de terceiros.

## Acionamento de tradução não surte efeito

Outros sites traduzem, mas um site não.

- Se este site tem menos visitantes
  - Sugestão de parágrafos a serem traduzidos passando o mouse
  - Se precisar traduzir todo o site, você pode adaptá-lo via [regras do usuário](/docs/advanced/#user-rules)
- Se este site é usado por muitas pessoas
  - Você pode começar passando o mouse para traduzir o uso
  - Chame no grupo e ele será adaptado mais tarde

## Aprimoramento da caixa de entrada não surte efeito

- Pesquisa do Google na Página Inicial do Navegador

A caixa de pesquisa do Google deve estar no URL da página da web do [Google](https://www.google.com/), e não pode ser usada na página inicial do navegador, nos espaços em branco da barra de endereços

## Feedback do log de depuração

- Ativar registro de depuração
  Abrir Painel -> Configurações -> Configurações do Desenvolvedor -> Ativar "Imprimir log de depuração no console".
- Abrir o console do site
  Clique com o botão direito para abrir a revisão -> Mude para o console no topo da coluna direita -> Execute a ação para ver os logs

## Como desativar a bola flutuante

- Ocultar na página atual

Defina como "Nunca traduzir este site".

- Ocultar em todas as páginas

Abra [Página de Configurações] - [Configurações de Interface] e desative [Mostrar Bola Flutuante na Página].

## Erro ao instalar o instalador do plugin no chrome

- valor inválido para web_accessible_resource[0]

  É necessário que a versão do Chromium seja maior que 88 para suportar manifest_version 3.

## Como instalar o Navegador 360

Apenas o 360 Extreme Browser x é suportado, lembre-se que é com x. Se você tiver acesso à loja de Extensões do Google, pode ir diretamente lá e instalá-lo. Se não puder acessar, [instale manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## Navegador Opera não funciona

- Não funciona no google.com e em outras páginas de pesquisa, o plugin exibe `Por favor, atualize a página atual antes de iniciar a tradução` e atualizar a página ainda exibe esta mensagem.

Você precisa encontrar "Immersive Translate" nas configurações do plugin do Opera e ativar a opção "Permitir acesso aos resultados da página de pesquisa".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## Legendas bilíngues do YouTube em chinês tradicional não exibidas

O YouTube vem com legendas traduzidas por máquina, e o Chinês Tradicional terá erros de formatação, fazendo com que todas as legendas apareçam com uma grande seção de legendas no início, com base neste cenário é recomendado ativar a opção [Usar Immersive Translate para Traduzir Legendas] em [Configurações] [Legendas de Vídeo].

## Mais perguntas (ver muito)

<details>
<summary>Como limpar meu cache com Tampermonkeys?</summary>
<p>
Devido à limitação da API dos Tampermonkeys, o cache dos Tampermonkeys do Immersive Translate será salvo no cache do site correspondente, então se você quiser limpá-lo, pode abrir o painel de ferramentas de desenvolvedor do site correspondente no seu navegador e então limpar o cache desse site.
</p>
</details>

<details>
<summary>Falha no pedido de endereço de interface personalizada do Tampermonkey?</summary>
<p>
O Tampermonkey requer que todos os pedidos do script declarem permissões no início do script, por exemplo: `@connect api.google.com`, portanto, se precisar adicionar um novo nome de domínio que não seja o padrão, por favor, declare-o no início do Tampermonkey seguindo o modelo dos outros nomes de domínio.
</p>
</details>