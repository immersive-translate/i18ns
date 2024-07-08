---
sidebar_position: 1
---

# Instalação
<iframe width="560" height="315" src="https://www.youtube.com/embed/SHznc5kQCM4?si=RyZYUcjW560Bc57-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Navegador Desktop

- Microsoft Edge: [Edge Store Immersive Translate](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg)
- Google Chrome: [Chrome Store Immersive Translate](https://chrome.google.com/webstore/detail/immersive-translate/bpoadfkcbjbfhfodiogcnhhhpibjhbnh)
- Firefox: [Firefox Addon Store Immersive Translate](https://addons.mozilla.org/firefox/addon/immersive-translate/)

> Se você não conseguir acessar a Google Store, você pode baixar diretamente o [instalador zip mais recente do Immersive Translate para Chrome](https://download.immersivetranslate.com/latest/chrome-immersive-translate.zip). Após o download, descompacte-o em uma pasta que você costuma usar, digite `chrome://extensions` na barra de endereço para abrir a janela de gerenciamento de extensões, ative o "Modo do Desenvolvedor", selecione "Carregar sem compactação" e escolha a pasta que você acabou de descompactar e carregar.

### Safari

- [Clique aqui para ir à Apple App Store para instalar](https://apps.apple.com/app/immersive-translate/id6447957425) \*\*GRÁTIS POR TEMPO LIMITADO!!!!\*\*

<div align="center">
<img src="/assets/immersive-app-store.png" width="150" alt="app store qrcode"/>
</div>

> Instruções: Após a primeira instalação, você precisa habilitar a extensão Immersive Translate em safari -> Gerenciar Extensões -> **Habilitar Extensão Immersive Translate** e conceder **Permitir acesso a todos os sites**. Se tiver alguma dúvida, você pode assistir ao vídeo tutorial abaixo:

### Safari para iOS

<video
controls style={{width:"100%", maxWidth:"350px"}}
controls
muted
height="800px"
poster="/assets/docs/ios_safari_turorial_en.jpeg" src="https://s.immersivetranslate.com/videos/ios_safari_turorial_en.mp4"></video>

### Safari para MacOS

<video
controls style={{width:"100%", maxWidth:"500px"}}
controls
muted
poster="/assets/docs/macOS_safari_en.jpeg" src="https://s.immersivetranslate.com/videos/macOS_safari_tutorial_en.mp4"></video>

## Android

Clique para baixar o [Navegador Immersive Translate Android](/android/). Após o download, você precisa habilitar o [Immersive Translate] manualmente em [Extensões]:

Você também pode tentar instalar o Immersive Translate com outros navegadores Android, como aqueles que suportam extensões do Firefox ou Chrome, como:

- [Firefox Beta ou Nightly](https://www.mozilla.org/firefox/channel/android/)
- [Lemur Browser](https://lemurbrowser.com/app/)
- [Kiwi Browser](https://kiwibrowser.com/)

Após a instalação, procure por [Immersive Translate](https://chrome.google.com/webstore/detail/immersive-translate/bpoadfkcbjbfhfodiogcnhhhpibjhbnh) diretamente na Chrome Store para instalá-lo.

## Instalação via Tampermonkey

Se você não conseguir instalar a extensão oficial do Immersive Translate com os passos acima, você pode instalar o Tampermonkey da seguinte maneira:

Endereço do script para o Tampermonkey: [https://download.immersivetranslate.com/immersive-translate.user.js](https://download.immersivetranslate.com/immersive-translate.user.js)

Abra [este endereço](https://download.immersivetranslate.com/immersive-translate.user.js) em um navegador que tenha a extensão Grease Monkey instalada para instalá-lo. Aqui estão alguns navegadores que suportam o Tampermonkey:

**Firefox para Android**

1. Baixe a [Versão Mais Recente do Firefox](https://www.mozilla.org/firefox/browsers/mobile/android/)
2. Encontre [Tamper Monkey](https://www.tampermonkey.net/) nos complementos recomendados do Firefox e instale-o.
3. Instale o [Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) para esta extensão (abra este link no seu navegador Firefox para ver a página de instalação)
4. Após a instalação, abra qualquer página da web e o ícone da janela flutuante da extensão Immersive Translate aparecerá no lado direito.

**Navegador Apple Safari [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)**

1. Instale o [plugin Userscripts para safari](https://itunes.apple.com/us/app/userscripts/id1463298887) e conceda a permissão "Sempre permitir acesso a qualquer site".
2. Instale o [Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) para esta extensão (abra este link no navegador Safari e clique no ícone da extensão Userscript para ver a página de instalação)
3. Após a instalação, abra qualquer página da web e atualize-a, uma janela flutuante desta extensão aparecerá no lado direito da página. (Se você estiver enfrentando problemas com janelas flutuantes não aparecendo, recomendamos atualizar a página com frequência ou reiniciar o Safari forçadamente para que o efeito ocorra)

<!-- Se você tiver dúvidas durante a instalação, pode consultar o [vídeo tutorial no YouTube](https://www.youtube.com/watch?v=IWOFFWDfZGY)

<iframe width="560" height="315" src="https://www.youtube.com/embed/IWOFFWDfZGY" title="YouTube video player" frameBorder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowFullScreen></iframe> -->

## Instalação manual (para acompanhar os recursos mais recentes de desenvolvimento)

A vantagem da instalação manual é que você não precisa esperar pela revisão da loja e pode experimentar os recursos da versão de desenvolvimento mais recente imediatamente:

1. Baixe o pacote zip na página [Releases](https://github.com/immersive-translate/immersive-translate/releases/) do repositório do Immersive Translation no GitHub.
2. Extraia o .zip para qualquer pasta, como por exemplo: `Documentos/chrome-immersive-translate`.
3. Para instalar em navegadores chromium, como por exemplo o Google Chrome, acesse `chrome://extensions` na barra de endereço para abrir a janela do Gerenciador de Extensões; Habilite o "Modo do Desenvolvedor", selecione "Carregar sem compactação" e escolha a pasta que você acabou de descompactar.
- Instalação no Navegador Firefox: (1) Digite: `about:debugging#/runtime/this-firefox` na barra de endereço para abrir a janela do Gerenciador de Extensões; (2) Carregue temporariamente o complemento e selecione `firefox/manifest.json`.

### Como faço para atualizar uma extensão instalada manualmente?

Baixe o instalador mais recente da página [Releases](https://github.com/immersive-translate/immersive-translate/releases/) do repositório do Immersive Translation no GitHub, delete o conteúdo da pasta antiga, depois copie e cole o conteúdo do arquivo zip mais recente nela e, finalmente, na página de Gerenciar extensões, clique em `Atualizar`.

> Se você está acostumado à linhas de comando (CLI), pode usar `git clone https://github.com/immersive-translate/immersive-translate.git`, depois instalar `dist/chrome` e poderá sincronizar com `git pull` a cada atualização.