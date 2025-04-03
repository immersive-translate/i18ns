---
sidebar_position: 9
---

# FAQ

### 1. Android App, floating ball disappeared

Las versiones antiguas de complementos están deshabilitadas, desinstala e instala la última versión desde el [sitio web oficial](https://immersivetranslate.com/).

## El contenido principal en sitios web como Youtube, Facebook está traducido, pero algunas barras laterales no, quiero traducir todo

Por el bien de la legibilidad de la página, la traducción inmersiva por defecto solo traduce el área de contenido principal. Si deseas traducir todo.

Abre el panel de la bola flotante (mantén presionado en el móvil) -> Haz clic en más en la esquina inferior derecha -> Selecciona todas las áreas

## La burbuja flotante no se muestra en Youtube (u otras) aplicaciones en móviles

Los complementos del navegador solo pueden ejecutarse en navegadores y no pueden usarse en otras aplicaciones.

- Al hacer clic en YouTube en un navegador iOS se abre directamente la aplicación.

  Mantén presionado el enlace de YouTube para que aparezca una ventana flotante y elige abrir en una página web.

## Cómo desactivar la traducción automática

- Cancela en el panel emergente o en la página de Configuración.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="turn off automatic translation" width="250" />

<!-- - O cambia: a través de la página de configuración

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## Sin permiso para traducir la página actual

- Página predeterminada del navegador (sin dirección en la barra de direcciones)
- Página de complemento de terceros
- El complemento de Google desactiva la página de la tienda de Google

## ¿Cómo no mostrar el texto original?

Toca el icono de Immersive Translate para abrir el panel de expansión, toca [Más], [Cambiar a Modo Solo Traducción]

## Aparece un signo de exclamación en la página

Un signo de exclamación en la página indica que el servicio de traducción ha encontrado un problema y ha devuelto un error, puedes mover el ratón sobre el signo de exclamación para ver el error específico.

### Error 429

Este es uno de los errores más comunes, 429 indica que la frecuencia de las solicitudes es demasiado rápida. La traducción de páginas web tiene un gran número de párrafos para traducir, aunque hemos hecho una gran optimización, incluyendo la fusión de párrafos, control de frecuencia, etc., pero a veces todavía hay algunos servicios de traducción sobrecargados, devolviendo el error de límite de frecuencia 429, en este momento generalmente puedes cambiar temporalmente a otros servicios de traducción, o esperar un tiempo e intentarlo de nuevo.

Si experimentas un 429 en un servicio de Google, generalmente es un caso de Google imponiendo un límite de tráfico contra tu nodo, y se recomienda cambiar de nodo.

## Traducción de documentos locales

Si necesitas traducir archivos HTML locales, archivos txt o archivos PDF, puedes hacer clic en el icono de extensión de Immersive Translate, luego hacer clic en [Más], hacer clic en [Traducir archivos PDF] o [Traducir archivos HTML/txt] para traducir archivos locales.

Si estás usando navegadores similares a Chrome, como (Chrome, Arc, Edge), hay otra manera, que es abrir la página de gestión de extensiones del navegador `chrome://extensions`, encontrar el complemento [Immersive Translate], [Permitir que la extensión acceda a archivos locales], y luego directamente en el navegador abrir el archivo HTML local o el archivo PDF local, puedes hacer clic derecho directamente [traducción].

**Nota**: El navegador Safari tiene restricciones estrictas sobre el acceso de extensiones a archivos locales. Los usuarios de Safari deben usar directamente el Método 1: hacer clic en el icono de extensión de Immersive Translate, luego hacer clic en [Más], hacer clic en [Traducir archivos PDF] o [Traducir archivos HTML/txt] para traducir archivos locales.

## ¿Cómo actualizo la extensión?

En general, las extensiones instaladas en la tienda del navegador se actualizarán automáticamente, la situación general se actualizará automáticamente dentro de un día después de la actualización de la extensión, si deseas actualizar inmediatamente a la última versión, puedes en la página de [Gestión de Extensiones] del navegador, abrir el [Modo Desarrollador], y luego hacer clic en la parte superior de [Actualizaciones], puedes actualizar inmediatamente a la última versión de la tienda.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Configuración de subtítulos de Youtube

Puedes hacer clic en la configuración de subtítulos propia de Youtube, [Opciones], y luego puedes ajustar el tamaño, color, etc.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Navegadores compatibles con Immersive Translate Tampermonkey

Extensiones Grease Monkey recomendadas para Chrome, Firefox en escritorio:

- [Tamper Monkey](https://www.tampermonkey.net/)

Extensión Grease Monkey recomendada para Safari:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Si usas [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) en Safari, busca el Script de Optimización de Immersive Translate para descargar directamente desde la tienda de Stay (optimizado específicamente para Stay) -->

Extensiones Grease Monkey recomendadas para Android:

1. Puedes instalar la extensión [Tamper Monkey](https://www.tampermonkey.net/) usando [Firefox Última Versión](https://www.mozilla.org/firefox/browsers/mobile/android/).

<!-- 2. También puedes usar directamente [X Browser](https://www.xbext.com/?ref=immersive-translate), después de la instalación, abre directamente [Dirección de Tampermonkey de Immersive Translate](https://download.immersivetranslate.com/immersive-translate.user.js) para instalarlo! -->

<!-- Extensiones Grease Monkey no compatibles conocidas:

- Android Via Browser
- iOS Alook Browser -->

(debido a que tales navegadores no implementan la API requerida de Grease Monkey)

## Problema de interfaz de Google Translate bloqueada

Por favor, añade el nombre de dominio `translate.googleapis.com` a la regla de proxy

## Cómo actualizar las últimas reglas

La extensión en sí misma sincronizará regularmente con las últimas reglas de adaptación del sitio web oficial cuando la uses, también puedes sincronizar manualmente con las últimas reglas haciendo clic en el icono de Extensión de Immersive Translate en el navegador para abrir una ventana emergente donde la extensión detectará automáticamente las últimas reglas de adaptación y se sincronizará con ellas, lo mismo ocurre con Tampermonkeys.

## ¿Cómo guardo mi retroalimentación de página web si tengo problemas con la traducción de la página web?

Necesitas hacer clic derecho "Guardar como" o el atajo ctrl+s en la página web, elegir archivo único para la opción de guardar, y finalmente el formato del archivo es .mht/.mhtml. Luego envía el archivo a support@immersivetranslate.com

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Error de traducción de Color Cloud

¿Tocar lejos? El mensaje de error para el número "Unsupported trans_type" se muestra. Puedes seleccionar el idioma para ser detectado automáticamente mediante el idioma especificado.

## WeChat Reading no se puede traducir

No se puede traducir porque WeChat Reading ha hecho un procesamiento especial para el contenido para evitar el acceso al contenido a través de medios de terceros.

## La traducción activada no surte efecto

Otros sitios se traducen, pero un sitio no.

- Si este sitio tiene menos visitantes
  - Se sugiere párrafos para ser traducidos al pasar el ratón
  - Si necesitas traducir todo el sitio puedes adaptarlo a través de [reglas de usuario](/docs/advanced/#user-rules)
- Si este sitio es utilizado por muchas personas
  - Puedes comenzar pasando el ratón para traducir el uso de
  - Llamarlo en el grupo y se adaptará más tarde

## La mejora del cuadro de entrada no surte efecto

- Página de inicio del navegador Búsqueda de Google

El cuadro de búsqueda de Google debe estar en la URL de la página web de [Google](https://www.google.com/), y no puede usarse en la página de inicio del navegador, el lugar en blanco de la barra de direcciones

## Retroalimentación del registro de depuración

- Habilitar el registro de depuración
  Abrir Panel -> Configuración -> Configuración de Desarrollador -> Habilitar "Imprimir registro de depuración en consola".
- Abrir la consola del sitio
  Haz clic derecho para abrir la revisión -> Cambia a la consola en la parte superior de la columna derecha -> Realiza la acción para ver los registros

## Cómo desactivar la bola flotante

- Ocultar en la página actual

Configúralo en "Nunca traducir este sitio".

- Ocultar en todas las páginas

Abre [Página de Configuración] - [Configuración de Interfaz] y desactiva [Mostrar Bola Flotante en la Página].

## Error al instalar el instalador del complemento en chrome

- valor no válido para web_accessible_resource[0]

  Se requiere una versión de Chromium mayor a 88 para soportar manifest_version 3.

## Cómo instalar el Navegador 360

Solo se admite el Navegador 360 Extreme x, recuerda que es con x. Si tienes acceso a la tienda de Extensiones de Google, puedes ir directamente allí e instalarlo. Si no puedes acceder [instálalo manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## El navegador Opera no funciona

- No funciona en google.com y otras páginas de búsqueda, el complemento muestra `Por favor, actualiza la página actual antes de comenzar la traducción` y al actualizar la página sigue mostrando este mensaje.

Necesitas encontrar "Immersive Translate" en la configuración del complemento de Opera y activar la opción "Permitir acceso a los resultados de la página de búsqueda".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## Subtítulos bilingües de YouTube en chino tradicional no se muestran

YouTube viene con subtítulos traducidos automáticamente, y el chino tradicional tendrá errores de formato, causando que todos los subtítulos aparezcan con una gran sección de subtítulos al principio, basado en este escenario se recomienda activar la opción [Usar Immersive Translate para Traducir Subtítulos] en [Configuración] [Subtítulos de Video].

## Más preguntas (ver mucho)

<details>
<summary>¿Cómo borro mi caché con Tampermonkeys?</summary>
<p>
Debido a la limitación de la API de Tampermonkeys, la caché de Immersive Translate Tampermonkeys se guardará en la caché del sitio web correspondiente, por lo que si deseas borrarla, puedes abrir el panel de herramientas de desarrollador del sitio web correspondiente en tu navegador y luego borrar la caché de ese sitio web.
</p>
</details>

<details>
<summary>¿Falló la solicitud de dirección de interfaz personalizada de Tampermonkey?</summary>
<p>
Tampermonkeys requieren que todas las solicitudes del script necesiten declarar permisos al principio del script, por ejemplo: `@connect api.google.com`, así que si necesitas agregar un nuevo nombre de dominio que no sea el predeterminado, por favor decláralo al principio del Tampermonkey siguiendo el modelo de los otros nombres de dominio.
</p>
</details>