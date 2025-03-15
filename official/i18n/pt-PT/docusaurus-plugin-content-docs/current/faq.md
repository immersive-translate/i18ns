---
sidebar_position: 9
---

# FAQ

### 1. Android App, floating ball disappeared

As extensões de versões antigas estão desativadas, desinstale e instale a versão mais recente a partir do [site oficial](https://immersivetranslate.com/).

## O conteúdo principal em sites como Youtube, Facebook é traduzido, mas algumas barras laterais não são, quero traduzir tudo

Para a legibilidade da página, a tradução imersiva por padrão só traduz a área de conteúdo principal. Se quiser traduzir tudo.

Abra o painel da bola flutuante (pressione longamente no telemóvel) -> Clique em mais no canto inferior direito -> Selecione todas as áreas

## Bolha Flutuante Não Exibida em Apps do Youtube (ou Outros) no Telemóvel

Os plugins do navegador só podem ser executados em navegadores e não podem ser usados em outros apps.

- Clicar no YouTube num navegador iOS abre diretamente o App.

  Pressione e segure o link do YouTube para abrir uma janela flutuante e escolha abrir numa página web.

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

Toque no ícone do Immersive Translate para abrir o painel de expansão, toque em [Mais], [Mudar para Modo Apenas Tradução]

## Aparece um ponto de exclamação na página

Um ponto de exclamação na página indica que o serviço de tradução encontrou um problema e retornou um erro, pode mover o mouse sobre o ponto de exclamação para ver o erro específico.

### Erro 429

Este é um dos erros mais comuns, 429 indica que a frequência de pedidos é muito rápida. A tradução de páginas web tem um número muito grande de parágrafos a serem traduzidos, embora tenhamos feito uma grande otimização, incluindo a fusão de parágrafos, controle de frequência, etc., mas às vezes ainda há alguns serviços de tradução sobrecarregados, retornando o erro de limite de frequência 429, neste momento pode geralmente mudar temporariamente para outros serviços de tradução, ou esperar um pouco e tentar novamente.

Se estiver a usar um serviço do Google e experimentar o erro 429, geralmente é um caso de o Google fazer um limite de tráfego contra o seu nó, e é recomendado mudar de nó.

## Tradução de documentos locais

Se precisar de traduzir ficheiros HTML locais, ficheiros txt ou ficheiros PDF, pode clicar no ícone da extensão Immersive Translate, depois clicar em [Mais], clicar em [Traduzir ficheiros PDF] ou [Traduzir ficheiros HTML/txt] para traduzir ficheiros locais.

Se estiver a usar navegadores semelhantes ao Chrome, como (Chrome, Arc, Edge browser), há outra maneira, que é abrir a página de gestão de extensões do navegador `chrome://extensions`, encontrar o plugin [Immersive Translate], [Permitir que a extensão aceda a ficheiros locais], e depois diretamente no navegador abrir o ficheiro HTML local ou ficheiro PDF local, pode diretamente clicar com o botão direito [tradução].

## Como atualizar a extensão?

De um modo geral, as extensões instaladas na loja do navegador serão atualizadas automaticamente, a situação geral será atualizada automaticamente dentro de um dia após a atualização da extensão, se quiser atualizar imediatamente para a versão mais recente, pode na página de [Gestão de Extensões] do navegador, abrir o [Modo de Desenvolvedor], e depois clicar no topo em [Atualizações], pode imediatamente atualizar para a versão mais recente da loja.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Configuração de estilo de legendas do Youtube

Pode clicar nas configurações de legendas próprias do Youtube, [Opções], e depois pode ajustar o tamanho, cor, e assim por diante.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Navegadores suportados pelo Immersive Translate Tampermonkey

Extensões Grease Monkey recomendadas para Chrome, Firefox no desktop:

- [Tamper Monkey](https://www.tampermonkey.net/)

Extensão Grease Monkey recomendada para Safari:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Se estiver a usar [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) no Safari, por favor procure o Script de Otimização do Immersive Translate para descarregar diretamente da loja do Stay (otimizado especificamente para Stay) -->

Extensões Grease Monkey recomendadas para Android:

1. Pode instalar a extensão [Tamper Monkey](https://www.tampermonkey.net/) usando [Firefox Última Versão](https://www.mozilla.org/firefox/browsers/mobile/android/).

<!-- 2. Pode também usar diretamente [X Browser](https://www.xbext.com/?ref=immersive-translate), após a instalação, abrir diretamente o [Endereço do Tampermonkey do Immersive Translate](https://download.immersivetranslate.com/immersive-translate.user.js) para instalá-lo! -->

<!-- Extensões Grease Monkey conhecidas como não suportadas:

- Android Via Browser
- iOS Alook Browser -->

(como tais navegadores não implementam a API Grease Monkey necessária)

## Problema de Interface do Google Translate Bloqueada

Por favor, adicione o domínio `translate.googleapis.com` à regra de proxy

## Como atualizar as regras mais recentes

A extensão em si irá sincronizar regularmente com as regras de adaptação do site oficial mais recentes quando a usar, pode também sincronizar manualmente com as regras mais recentes clicando no ícone da Extensão Immersive Translate no navegador para abrir uma janela pop-up onde a extensão irá automaticamente detectar as regras de adaptação mais recentes e sincronizar com elas, o mesmo se aplica aos Tampermonkeys.

## Como guardar o meu feedback da página web se tiver problemas com a tradução da página web?

Precisa clicar com o botão direito "Guardar como" ou atalho ctrl+s na página web, escolher ficheiro único para opção de guardar, e finalmente o formato do ficheiro é .mht/.mhtml. Depois envie o ficheiro para support@immersivetranslate.com

<!-- ![guardar mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Erro de Tradução de Nuvem de Cor

Desviar? A mensagem de erro para o número "Unsupported trans_type" é exibida. Pode selecionar o idioma a ser automaticamente detetado por meio do idioma especificado.

## Leitura do WeChat Não Pode Ser Traduzida

Não pode ser traduzida porque a Leitura do WeChat fez um processamento especial para o conteúdo para evitar o acesso ao conteúdo através de meios de terceiros.

## Acionamento de tradução não tem efeito

Outros sites traduzem, mas um site não.

- Se este site tem menos visitantes
  - Sugestão de parágrafos a serem traduzidos ao passar o mouse
  - Se precisar traduzir todo o site pode adaptá-lo via [regras de usuário](/docs/advanced/#user-rules)
- Se este site é usado por muitas pessoas
  - Pode começar por passar o mouse para traduzir o uso de
  - Chame-o no grupo e será adaptado mais tarde

## Melhoria da caixa de entrada não tem efeito

- Página Inicial do Navegador Pesquisa Google

A caixa de pesquisa do Google deve estar no URL da página web do [Google](https://www.google.com/), e não pode ser usada na página inicial do navegador, nos lugares em branco da barra de endereços

## Feedback do log de depuração

- Ativar o registo de depuração
  Abrir Painel -> Configurações -> Configurações de Desenvolvedor -> Ativar "Imprimir log de depuração no console".
- Abrir o console do site
  Clique com o botão direito para abrir a revisão -> Mudar para o console no topo da coluna direita -> Executar a ação para ver os logs

## Como desativar a bola flutuante

- Ocultar na página atual

Defina para "Nunca traduzir este site".

- Ocultar em todas as páginas

Abra [Página de Configurações] - [Configurações de Interface] e desative [Mostrar Bola Flutuante na Página].

## Erro ao instalar o instalador do plugin no chrome

- valor inválido para web_accessible_resource[0]

  É necessário que a versão do Chromium seja maior que 88 para suportar manifest_version 3.

## Como instalar o Navegador 360

Apenas o Navegador 360 Extreme x é suportado, lembre-se que é com x. Se tiver acesso à loja de Extensões do Google, pode ir diretamente lá e instalá-lo. Se não puder aceder [instale manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## Navegador Opera não funciona

- Não funciona em google.com e outras páginas de pesquisa, o plugin exibe `Por favor, atualize a página atual antes de iniciar a tradução` e atualizar a página ainda exibe esta mensagem.

Precisa encontrar "Immersive Translate" nas configurações do plugin do Opera e ativar a opção "Permitir acesso aos resultados da página de pesquisa".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## Legendas bilíngues do YouTube em chinês tradicional não exibidas

O YouTube vem com legendas traduzidas por máquina, e o Chinês Tradicional terá erros de formatação, causando que todas as legendas apareçam com uma grande seção de legendas no início, com base neste cenário é recomendado ativar a opção [Usar Immersive Translate para Traduzir Legendas] em [Configurações] [Legendas de Vídeo].

## Mais perguntas (ver muito)

<details>
<summary>Como limpar o meu cache com Tampermonkeys?</summary>
<p>
Devido à limitação da API dos Tampermonkeys, o cache dos Tampermonkeys do Immersive Translate será guardado no cache do site correspondente, por isso se quiser limpá-lo, pode abrir o painel de ferramentas de desenvolvedor do site correspondente no seu navegador e depois limpar o cache desse site.
</p>
</details>

<details>
<summary>Pedido de endereço de interface personalizada do Tampermonkey falhou?</summary>
<p>
Os Tampermonkeys exigem que todos os pedidos do script precisem declarar permissões no início do script, por exemplo: `@connect api.google.com`, por isso se precisar adicionar um novo domínio que não seja o padrão, por favor declare-o no início do Tampermonkey modelado após o outro domínio.
</p>
</details>