---
sidebar_position: 1
---

# Instalação

<iframe width="560" height="315" src="https://www.youtube.com/embed/SHznc5kQCM4?si=RyZYUcjW560Bc57-" title="Reprodutor de vídeo do YouTube" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Navegador de Desktop

- Navegador Microsoft Edge: [Edge Store Immersive Translate](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg)
- Google Chrome: [Chrome Store Immersive Translate](https://chrome.google.com/webstore/detail/immersive-translate/bpoadfkcbjbfhfodiogcnhhhpibjhbnh)
- Firefox: [Loja de Addons do Firefox Immersive Translate](https://addons.mozilla.org/firefox/addon/immersive-translate/)

> Se você não consegue acessar a loja oficial do Google, você pode baixar diretamente o [Instalador zip do Immersive Translate Chrome mais recente](https://download.immersivetranslate.com/latest/chrome-immersive-translate.zip), após o download, por favor, primeiro Descompacte-o em uma pasta que você costuma usar, então digite: `chrome://extensions` na barra de endereços para abrir a janela de gerenciamento de extensões, em seguida, habilite o "Modo Desenvolvedor", selecione "Carregar Extensões Descompactadas", e escolha a pasta que você acabou de descompactar e carregar. Selecione a pasta que você acabou de extrair e carregue-a.

## Safari

- [Clique aqui para instalar da App Store](https://apps.apple.com/app/immersive-translate/id6447957425) **É GRÁTIS!!!!**

<div align="center">
<img src="https://s.immersivetranslate.com/static/official-static/assets/immersive-app-store.png" width="150" alt="qrcode da app store"/>
</div>

> Instruções: Após a primeira instalação, você precisa habilitar a extensão Immersive Translate\*\* no safari -> Gerenciar Extensões -> **Habilitar Extensão Immersive Translate** e conceder a ela **Sempre Permitir Acesso a Todos os Sites**, se você tiver alguma dúvida, pode assistir ao seguinte vídeo tutorial:

### iOS Safari

<video
controls style={{width:"100%", maxWidth:"350px"}}
controls
muted
height="800px"
poster="https://s.immersivetranslate.com/static/official-static/assets/docs/ios_safari_turorial_en.jpeg" src="https://s.immersivetranslate.com/videos/ios_safari_turorial_en.mp4"></video>

### MacOS Safari

<video
controls style={{width:"100%", maxWidth:"500px"}}
controls
muted
poster="https://s.immersivetranslate.com/static/official-static/assets/docs/macOS_safari_en.jpeg" src="https://s.immersivetranslate.com/videos/macOS_safari_tutorial_en.mp4"></video>

Please note, the URLs and the paths to images or videos haven't been translated as they are specific resources and should remain unchanged.

## Android

Clique para baixar o [Navegador Android do Immersive Translate](/android/), você precisa ativar o [Immersive Translate] manualmente em [Extensões] após o download:

Você pode tentar instalar o Immersive Translate com outros navegadores Android, como aqueles que suportam extensões do Firefox ou extensões do Chrome, como

- [Firefox Beta ou Nightly](https://www.mozilla.org/firefox/channel/android/)
- [Lemur Browser](https://lemurbrowser.com/app/)
- [Kiwi Browser](https://kiwibrowser.com/)

Uma vez instalado, procure por [Immersive Translate](https://chrome.google.com/webstore/detail/immersive-translate/bpoadfkcbjbfhfodiogcnhhhpibjhbnh) diretamente na loja do Chrome para instalá-lo.

## Instalação via Tampermonkey

Se você não conseguir instalar a extensão oficial do Immersive Translates da maneira descrita acima, você pode instalar o Tampermonkey por:

Endereço do Tampermonkey: https://download.immersivetranslate.com/immersive-translate.user.js

Abra [este endereço](https://download.immersivetranslate.com/immersive-translate.user.js) em um navegador que tenha a extensão Grease Monkey instalada para instalá-lo. Aqui estão alguns navegadores que suportam o Tampermonkey:

**Firefox para Android**

1. Baixe a [Versão Mais Recente do Firefox](https://www.mozilla.org/firefox/browsers/mobile/android/)
2. Encontre o [Tamper Monkey](https://www.tampermonkey.net/) nos complementos recomendados do Firefox e instale-o.
3. Instale o [Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) para esta extensão (abra este link no seu navegador Firefox para ver a página de instalação)
4. Após a instalação, abra qualquer página da web e o ícone da janela flutuante da extensão Immersive Translate aparecerá no lado direito.

**Navegador Safari da Apple [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)**

1. Instale o [plugin safari Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887) e conceda a ele a permissão "Sempre permitir acesso a qualquer site".
2. Instale o [Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) para esta extensão (abra este link no navegador Safari e clique no ícone da extensão Userscript para ver a página de instalação)
3. Após a instalação, abra qualquer página da web e atualize-a, uma janela flutuante desta extensão aparecerá no lado direito da página. (Se você estiver enfrentando problemas com janelas flutuantes não aparecendo, recomendamos atualizar a página com mais frequência ou forçar o reinício do Safari para que ele tenha efeito)

## Instalação manual (para acompanhar as últimas funcionalidades em desenvolvimento)

A vantagem da instalação manual é que você não precisa esperar pela revisão da loja e pode experimentar imediatamente as funcionalidades da versão de desenvolvimento mais recente:

1. Baixe o pacote zip na [página de lançamentos](https://github.com/immersive-translate/immersive-translate/releases/)
2. Extraia o zip para uma pasta comum, como `Documentos/chrome-immersive-translate`.
3. Instalação

- Instalar: (1) Digite: `chrome://extensions` na barra de endereços para abrir a janela do Gerenciador de Extensões; (2) Ative o "Modo Desenvolvedor", selecione "Carregar Extensões Descompactadas" e escolha a pasta que você acabou de descompactar para carregar. a pasta que você acabou de descompactar e carregue.
- Instalação no Navegador Firefox: (1) Digite: `about:debugging#/runtime/this-firefox` na barra de endereços para abrir a janela do Gerenciador de Extensões; (2) Carregue temporariamente o complemento e selecione `firefox/manifest.json`.

### Como atualizo uma extensão instalada manualmente?

Baixe o instalador mais recente da [página de lançamentos](https://github.com/immersive-translate/immersive-translate/releases/), delete o conteúdo da pasta original, depois copie o conteúdo do arquivo zip mais recente para a pasta original, e finalmente na página de gerenciamento da extensão clique em `Recarregar`.

> Se você está acostumado com a linha de comando, pode usar `git clone https://github.com/immersive-translate/immersive-translate.git`, depois instalar `dist/chrome` e você será capaz de sincronizar com `git pull` a cada vez.
