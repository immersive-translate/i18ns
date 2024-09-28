---
sidebar_position: 9
---

# Preguntas Frecuentes

## Incapaz de descargar desde la Apple Store

- 2023.07.28: Apple Store degradada en China según la política
- 2023.08.05: ha sido relanzada en China

## Cómo desactivar la traducción automática

- Cancelar en el panel emergente o en la página de ajustes.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="desactivar la traducción automática" width="250" />

<!-- - O cambiar: a través de la página de ajustes

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## No tengo permiso para traducir la página actual

- Página predeterminada del navegador (sin dirección en la barra de direcciones)
- Página de plugin de terceros
- El plugin de Google deshabilita la página de Google Store

## ¿Cómo hago para no mostrar el texto original?

Toca el icono de Immersive Translate para abrir el panel de expansión, toca [Más], [Cambiar a Modo Solo Traducción]

## Aparece un signo de exclamación en la página

Un signo de exclamación en la página indica que el servicio de traducción ha encontrado un problema y ha devuelto un error, puedes mover tu ratón sobre el signo de exclamación para ver el error específico.

```

### Error 429

Este es uno de los errores más comunes, el 429 indica que la frecuencia de las solicitudes es demasiado rápida. La traducción de páginas web tiene un número muy grande de párrafos para ser traducidos, aunque hemos hecho una gran optimización, incluyendo la fusión de párrafos, control de frecuencia, etc., pero a veces todavía hay algunos servicios de traducción que se sobrecargan, devolviendo el error de límite de frecuencia 429. En este caso, usualmente puedes cambiar temporalmente a otros servicios de traducción, o esperar un rato y volver a intentarlo.

Si experimentas un 429 con un servicio de Google, generalmente es un caso de Google haciendo un límite de tráfico contra tu nodo, y se recomienda cambiar de nodo.

## Traducción de documentos locales

Si necesitas traducir archivos HTML locales, archivos txt o archivos PDF, puedes hacer clic en el icono de la extensión de Immersive Translate, luego hacer clic en [Más], hacer clic en [Traducir archivos PDF] o [Traducir archivos HTML/txt] para traducir archivos locales.

Si estás utilizando navegadores similares a Chrome, como (Chrome, Arc, navegador Edge), hay otra manera, es abrir la página de gestión de extensiones del navegador `chrome://extensions`, encontrar el complemento [Immersive Translate], [Permitir que la extensión acceda a archivos locales], y luego directamente en el navegador abrir el archivo HTML local o el archivo PDF local, puedes hacer clic derecho directamente en [traducción].

## ¿Cómo actualizo la extensión?

Hablando en general, las extensiones instaladas desde la tienda del navegador, el navegador se actualizará automáticamente, la situación general será actualizada automáticamente dentro de un día después de la actualización de la extensión, si quieres actualizar inmediatamente a la última versión, puedes en la página de [Gestión de Extensiones] del navegador, abrir el [Modo Desarrollador], y luego hacer clic en la parte superior en [Actualizaciones], puedes actualizar inmediatamente a la última versión de la tienda.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Configuración de subtítulos en Youtube

Puedes hacer clic en la configuración de subtítulos propia de Youtube, [Opciones], y luego podrás ajustar el tamaño, color, y así sucesivamente.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Navegadores compatibles con Immersive Translate Tampermonkey

Extensiones de Grease Monkey recomendadas para Chrome, Firefox en escritorio:

- [Tamper Monkey](https://www.tampermonkey.net/)

Extensión de Grease Monkey recomendada para Safari:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Si usas [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) en Safari, por favor busca el Script de Optimización de Immersive Translate para descargarlo directamente desde la tienda propia de Stay (optimizado específicamente para Stay) -->

Extensiones de Grease Monkey recomendadas para Android:

1. Puedes instalar la extensión [Tamper Monkey](https://www.tampermonkey.net/) usando [Firefox Última Versión](https://www.mozilla.org/firefox/browsers/mobile/android/).

<!-- 2. También puedes usar directamente [X Browser](https://www.xbext.com/?ref=immersive-translate), después de la instalación, abre directamente [Dirección de Tampermonkey de Immersive Translate](https://download.immersivetranslate.com/immersive-translate.user.js) para instalarlo! -->

<!-- Extensiones de Grease Monkey conocidas por no ser compatibles:

- Navegador Android Via
- Navegador iOS Alook -->

(ya que tales navegadores no implementan la API de Grease Monkey requerida)

## Problema de Acceso Bloqueado a la Interfaz de Google Translate

Por favor, añade el nombre de dominio `translate.googleapis.com` a la regla del proxy

## Cómo actualizar las últimas reglas

La extensión se sincronizará regularmente con las últimas reglas de adaptación del sitio web oficial cuando la uses. También puedes sincronizar manualmente con las últimas reglas haciendo clic en el icono de la Extensión de Immersive Translate del navegador para abrir una ventana emergente donde la extensión detectará automáticamente las últimas reglas de adaptación y se sincronizará con ellas, lo mismo aplica para Tampermonkeys.

## ¿Cómo guardo mis comentarios de la página web si tengo problemas con la traducción de la página?

Necesitas hacer clic derecho en "Guardar como" o usar el atajo ctrl+s en la página web, elegir la opción de guardar como archivo único, y finalmente el formato del archivo es .mht/.mhtml. Luego envía el archivo a support@immersivetranslate.com

<!-- ![guardar mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Error en la Traducción de Nube de Color

¿Mensaje de error "Tipo de traducción no soportado"? Puedes seleccionar que el idioma sea detectado automáticamente mediante el idioma especificado.

## La Lectura de WeChat No Puede Ser Traducida

No se puede traducir porque la Lectura de WeChat ha realizado un procesamiento especial en el contenido para prevenir el acceso al contenido mediante medios de terceros.

## La activación de la traducción no tiene efecto

Otros sitios se traducen, pero uno no.

- Si este sitio tiene menos visitantes
  - Se sugiere traducir párrafos pasando el mouse por encima
  - Si necesitas traducir todo el sitio puedes adaptarlo mediante [reglas de usuario](/docs/advanced/#user-rules)
- Si este sitio es utilizado por muchas personas
  - Puedes empezar pasando el mouse por encima para hacer uso de la traducción
  - Mencionalo en el grupo y será adaptado más adelante

## El refuerzo del cuadro de entrada no tiene efecto

- Búsqueda en Google de la Página de Inicio del Navegador

La caja de búsqueda de Google debe estar en la URL de la página web de [Google](https://www.google.com/) y no puede usarse en la página de inicio del navegador, los lugares en blanco de la barra de direcciones

## Registro de depuración de comentarios

- Activar el registro de depuración
  Abrir Panel -> Configuración -> Configuración del Desarrollador -> Habilitar "Imprimir registro de depuración en consola".
- Abrir la consola del sitio
  Hacer clic derecho para abrir la revisión -> Cambiar a la consola en la parte superior de la columna derecha -> Realizar la acción para ver los registros

## Cómo desactivar hoverball

- Ocultar en la página actual

Establecer en "Nunca traducir este sitio".

- Ocultar en todas las páginas

Abrir [Página de Configuración] - [Configuración de Interfaz] y desactivar [Mostrar Hoverball en la Página].

## Error al instalar el instalador de plugins en chrome

- valor inválido para web_accessible_resource[0]

  Se requiere una versión de Chromium mayor a 88 para soportar manifest_version 3.

## Cómo instalar el Navegador 360

Solo se soporta 360 Extreme Browser x, recuerda que es con x. Si tienes acceso a la tienda de Extensiones de Google, puedes ir directamente allí e instalarlo. Si no puedes acceder [instálalo manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## El navegador Opera no funciona

- No funciona en google.com y otras páginas de búsqueda, el plugin muestra `Por favor, actualiza la página actual antes de comenzar la traducción` y actualizar la página todavía muestra este mensaje.

Necesitas encontrar "Immersive Translate" en la configuración de plugins de Opera y activar la opción "Permitir acceso a los resultados de la página de búsqueda".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## Subtítulos bilingües en chino tradicional de YouTube no se muestran

YouTube viene con subtítulos traducidos por máquina, y el chino tradicional tendrá errores de formato, causando que todos los subtítulos aparezcan con una gran sección de subtítulos al principio, basado en este escenario se recomienda activar la opción [Usar Immersive Translate para Traducir Subtítulos] en [Configuración] [Subtítulos de Video].

## Más preguntas (ver mucho más)

<details>
<summary>¿Cómo limpio mi caché con Tampermonkeys?</summary>
<p>
Debido a la limitación de la API de Tampermonkeys, la caché de Immersive Translate Tampermonkeys se guardará en la caché del sitio web correspondiente, así que si quieres limpiarla, puedes abrir el panel de herramientas para desarrolladores del sitio web correspondiente en tu navegador y luego limpiar la caché de ese sitio web.
</p>
</details>

<details>
<summary>¿Falló la solicitud de dirección de interfaz personalizada de Tampermonkey?</summary>
<p>
Tampermonkeys requiere que todas las solicitudes desde el script necesiten declarar permisos al inicio del script, por ejemplo: `@connect api.google.com`, así que si necesitas agregar un nuevo nombre de dominio que no sea el predeterminado, por favor decláralo al inicio del Tampermonkey modelado después del otro nombre de dominio.
</p>
</details>
```
