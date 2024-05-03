---
sidebar_position: 1
---

# Instalación
<iframe width="560" height="315" src="https://www.youtube.com/embed/SHznc5kQCM4?si=RyZYUcjW560Bc57-" title="Reproductor de vídeos de YouTube" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Navegador de Escritorio

- Navegador Microsoft Edge: [Edge Store Immersive Translate](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg)
- Google Chrome: [Chrome Store Immersive Translate](https://chrome.google.com/webstore/detail/immersive-translate/bpoadfkcbjbfhfodiogcnhhhpibjhbnh)
- Firefox: [Tienda de Complementos de Firefox Immersive Translate](https://addons.mozilla.org/firefox/addon/immersive-translate/)

> Si no puedes acceder a la tienda oficial de Google, puedes descargar directamente el [último instalador zip de Immersive Translate para Chrome](https://download.immersivetranslate.com/latest/chrome-immersive-translate.zip), después de descargarlo, por favor, primero descomprímelo en una carpeta que suelas usar, luego escribe: `chrome://extensions` en la barra de direcciones para abrir la ventana de gestión de extensiones, luego habilita el "Modo Desarrollador", selecciona "Cargar Extensiones Descomprimidas", y elige la carpeta que acabas de descomprimir y cargar. Selecciona la carpeta que acabas de extraer y cárgala.

## Safari

- [Haz clic aquí para instalar desde la App Store](https://apps.apple.com/app/immersive-translate/id6447957425) **¡Es GRATIS!**

<div align="center">
<img src="/assets/immersive-app-store.png" width="150" alt="código QR de la app store"/>
</div>

> Instrucciones: Después de la primera instalación, necesitas habilitar la extensión Immersive Translate\*\* en Safari -> Administrar Extensiones -> **Habilitar la Extensión de Immersive Translate** y otorgarle **Permitir Siempre el Acceso a Todos los Sitios Web**, si tienes alguna pregunta, puedes ver el siguiente video tutorial:

### iOS Safari

<video
controls style={{width:"100%", maxWidth:"350px"}}
controls
muted
height="800px"
poster="/assets/docs/ios_safari_turorial_en.jpeg" src="https://s.immersivetranslate.com/videos/ios_safari_turorial_en.mp4"></video>

### MacOS Safari

<video
controls style={{width:"100%", maxWidth:"500px"}}
controls
muted
poster="/assets/docs/macOS_safari_en.jpeg" src="https://s.immersivetranslate.com/videos/macOS_safari_tutorial_en.mp4"></video>

Note: The URLs and some technical terms have been left unchanged as they are universal or do not have a direct translation that would be understood in the context of software or web applications.

## Android

Haz clic para descargar el [Navegador Android de Immersive Translate](/es/android/), necesitas activar [Immersive Translate] manualmente en [Extensiones] después de descargarlo:

Puedes intentar instalar Immersive Translate con otros navegadores de Android, como aquellos que soportan extensiones de Firefox o extensiones de Chrome, tales como

- [Firefox Beta o Nightly](https://www.mozilla.org/firefox/channel/android/)
- [Lemur Browser](https://lemurbrowser.com/app/)
- [Kiwi Browser](https://kiwibrowser.com/)

Una vez instalado, busca [Immersive Translate](https://chrome.google.com/webstore/detail/immersive-translate/bpoadfkcbjbfhfodiogcnhhhpibjhbnh) directamente en la tienda de Chrome para instalarlo.

## Instalación vía Tampermonkey

Si no puedes instalar la extensión oficial de Immersive Translates de la manera descrita anteriormente, puedes instalar Tampermonkey mediante:

Dirección de Tampermonkey: https://download.immersivetranslate.com/immersive-translate.user.js

Abre [esta dirección](https://download.immersivetranslate.com/immersive-translate.user.js) en un navegador que tenga instalada la extensión Grease Monkey para instalarlo. Aquí hay algunos navegadores que soportan Tampermonkey:

**Firefox para Android**

1. Descarga [Firefox Última Versión](https://www.mozilla.org/firefox/browsers/mobile/android/) 
2. Busca [Tamper Monkey](https://www.tampermonkey.net/) en los complementos recomendados de Firefox e instálalo.
3. Instala [Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) para esta extensión (abre este enlace en tu navegador Firefox para ver la página de instalación)
4. Después de la instalación, abre cualquier página web y el icono de la ventana flotante de la extensión Immersive Translate aparecerá en el lado derecho.

**Navegador Apple Safari [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)**

1. Instala el [plugin de safari Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887) y otórgale el permiso "Siempre permitir acceso a cualquier sitio web".
2. Instala [Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) para esta extensión (abre este enlace en el navegador Safari y haz clic en el icono de la extensión Userscript para ver la página de instalación)
3. Después de la instalación, abre cualquier página web y refrescala, una ventana flotante de esta extensión aparecerá en el lado derecho de la página. (Si experimentas problemas con que las ventanas flotantes no aparezcan, recomendamos refrescar la página más a menudo o forzar el reinicio de Safari para que tenga efecto)

<!-- Si tienes preguntas al instalar, puedes referirte a [tutorial de video en YouTube](https://www.youtube.com/watch?v=IWOFFWDfZGY)

<iframe width="560" height="315" src="https://www.youtube.com/embed/IWOFFWDfZGY" title="Reproductor de video de YouTube" frameBorder="0" allow="acelerómetro; autoplay; escritura en el portapapeles; medios cifrados; giroscopio; imagen en imagen; compartir en la web" allowFullScreen></iframe> -->

## Instalación manual (para seguir las últimas características de desarrollo)

La ventaja de la instalación manual es que no tienes que esperar a que la tienda la revise y puedes experimentar las características de la última versión de desarrollo inmediatamente:

1. Descarga el paquete zip en la [página de lanzamientos](https://github.com/immersive-translate/immersive-translate/releases/).
2. Extrae el zip en una carpeta común, como `Documents/chrome-immersive-translate`.
3. Instalación

- Instalar: (1) Escribe: `chrome://extensions` en la barra de direcciones para abrir la ventana del Administrador de Extensiones; (2) Activa el "Modo de desarrollador", selecciona "Cargar extensiones descomprimidas" y elige la carpeta que acabas de descomprimir para cargarla.
- Instalación en el Navegador Firefox: (1) Escribe: `about:debugging#/runtime/this-firefox` en la barra de direcciones para abrir la ventana del Administrador de Extensiones; (2) Carga temporalmente el complemento y selecciona `firefox/manifest.json`.

### ¿Cómo actualizo una extensión instalada manualmente?

Descarga el último instalador desde la [página de lanzamientos](https://github.com/immersive-translate/immersive-translate/releases/), elimina el contenido de la carpeta original, luego copia el contenido del último archivo zip en la carpeta original, y finalmente en la página de gestión de la extensión haz clic en `Recargar`.

> Si estás acostumbrado a la línea de comandos, puedes usar `git clone https://github.com/immersive-translate/immersive-translate.git`, luego instalar `dist/chrome` y podrás sincronizar con `git pull` cada vez.