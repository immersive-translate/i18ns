---
sidebar_position: 9
---

# FAQ

## Relacionado con la Seguridad

### 1. Android App, el balón flotante desapareció

Los complementos de versiones antiguas están deshabilitados, desinstala e instala la última versión desde el [sitio web oficial](https://immersivetranslate.com/).

## Relacionado con la Instalación

### 1. Cómo actualizar la extensión

En general, las extensiones instaladas en la tienda del navegador se actualizarán automáticamente, generalmente dentro de un día después de que la extensión se actualice. Si deseas actualizar inmediatamente a la última versión, puedes ir a la [página de Gestión de Extensiones] del navegador, habilitar el [Modo Desarrollador] y luego hacer clic en [Actualizar] en la parte superior para actualizar inmediatamente a la última versión en la tienda.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

### 2. Navegadores compatibles con Immersive Translate Tampermonkey

iOS:

- [Tamper Monkey Browser](https://www.tampermonkey.net/)
- Navegador Safari con la extensión Tampermonkey instalada, extensiones compatibles:
  - [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)
  - [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171): Se recomienda buscar directamente el Script de Optimización de Immersive Translate desde la propia tienda de Stay (especialmente optimizado para Stay).

Android:

- [Firefox Latest Version](https://www.firefox.com.cn/download/#product-android-release): Después de la instalación, instala la extensión [Tamper Monkey](https://www.tampermonkey.net/).
- [X Browser](https://www.xbext.com/?ref=immersive-translate): Después de la instalación, abre directamente la [dirección del script de Immersive Translate Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) para instalar.

Navegadores conocidos que no soportan extensiones Tampermonkey (estos navegadores no han implementado la API requerida de Tampermonkey):

- Android Via Browser
- iOS Alook Browser

### 3. Error al instalar el instalador del plugin en Chrome

Error `invalid value for web_accessible_resource[0]`: Se requiere una versión de Chromium mayor a 88 para soportar manifest_version 3.

### 4. Cómo instalar 360 Browser

Solo se soporta 360 Extreme Browser X, recuerda que es con X. Si puedes acceder a la tienda de Extensiones de Google, puedes ir directamente allí para instalarlo. Si no puedes acceder, [instálalo manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features).

### 5. El navegador Opera no funciona

No funciona en google.com y otras páginas de búsqueda, el plugin muestra `Por favor, actualiza la página actual antes de comenzar la traducción` y al actualizar la página sigue mostrando este mensaje: Necesitas encontrar "Immersive Translate" en la configuración del plugin de Opera y habilitar la opción "Permitir acceso a los resultados de la página de búsqueda".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

### 6. No se pueden habilitar extensiones en dispositivos iOS

Si no puedes habilitar extensiones en tu dispositivo iOS, sigue estos pasos:

1. Abre la aplicación [Configuración]
2. Desplázate hacia abajo y toca [Tiempo de Uso]
3. Selecciona [Restricciones de Contenido y Privacidad]
4. Toca [Restricciones de Contenido]
5. Selecciona [Contenido Web] y configúralo en [Sin Restricciones]

Si no necesitas las otras funciones de Restricciones de Contenido y Privacidad, también puedes optar por simplemente desactivar las Restricciones de Contenido y Privacidad:

1. Abre la aplicación [Configuración]
2. Selecciona [Tiempo de Uso]
3. Desactiva [Restricciones de Contenido y Privacidad]

### 7. La página de configuración de Safari sigue cargando

Configuración del Sistema -> Navegador Safari -> Avanzado -> Datos del Sitio Web -> Editar, encuentra immersivetranslate.com y elimínalo.

### 8. Después de instalar iOS18, redirigido a una página en blanco al iniciar sesión desde la página de configuración

Mantén presionado el balón flotante y haz clic en el avatar para iniciar sesión.

### 9. "El archivo no existe" al arrastrar el archivo crx a las extensiones del navegador

Necesitas primero extraer el archivo zip, luego arrastrar solo el archivo CRX.

### 10. ¿Por qué la descarga de crx instala la versión 1.13.5 en lugar de la última?

Porque se detecta que tu motor de Chrome está por debajo de la versión 115, lo que no soporta algunas características avanzadas del plugin, por lo que automáticamente se degrada a la versión 1.13.5.

## Relacionado con la Traducción Básica

### 1. El contenido principal en sitios web como Youtube, Facebook está traducido, pero algunas barras laterales no, quiero traducir todo

Por el bien de la legibilidad de la página, la traducción inmersiva por defecto solo traduce el área de contenido principal. Si deseas traducir todas las áreas:

Abre el panel del balón flotante (mantén presionado en móvil) -> Haz clic en más en la esquina inferior derecha -> Selecciona todas las áreas.

### 2. Burbuja Flotante No Mostrada en Aplicaciones en Móvil

- El plugin Immersive Translate es un plugin de navegador que **solo puede ejecutarse en navegadores**, no puede usarse en otras aplicaciones, y no soporta traducción dentro de otras aplicaciones.

- El plugin solo funciona en el navegador donde está instalado y **no puede funcionar entre navegadores** (por ejemplo, instalarlo en Safari no te permite usarlo en Chrome)

### 3. Al hacer clic en YouTube en el navegador iOS se abre directamente la App

Mantén presionado el enlace de YouTube para que aparezca una ventana flotante y elige abrir en una página web.

### 4. Cómo desactivar la traducción automática

- Cancela en el panel emergente o en la página de Configuración.
- O cambia a través de la página de configuración

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="desactivar traducción automática" width="250" />

### 5. Sin permiso para traducir la página actual

- Página predeterminada del navegador (sin dirección en la barra de direcciones)
- Página de plugin de terceros
- Google plugin desactiva la página de la tienda de Google

### 6. ¿Cómo no mostrar el texto original?

Toca el icono de Immersive Translate para abrir el panel de expansión, toca [Más], [Cambiar a Modo Solo Traducción].

### 7. Aparece un signo de exclamación en la página

Un signo de exclamación en la página indica que el servicio de traducción ha encontrado un problema y ha devuelto un error. Puedes mover el ratón sobre el signo de exclamación para ver el error específico.

#### Ejemplo: Error 429

Este es uno de los errores más comunes, 429 indica que la frecuencia de las solicitudes es demasiado rápida. La traducción de páginas web tiene un gran número de párrafos para traducir, aunque hemos hecho una gran optimización, incluyendo la fusión de párrafos, control de frecuencia, etc., pero a veces todavía hay algunos servicios de traducción que están sobrecargados, devolviendo un error de límite de frecuencia 429. En este caso, generalmente puedes cambiar temporalmente a otros servicios de traducción, o esperar un tiempo e intentarlo de nuevo.

Si estás usando el servicio de Google y experimentas un error 429, generalmente es un caso de que Google está haciendo un límite de tráfico contra tu nodo, y se recomienda cambiar de nodo.

### 8. Cómo cambiar el idioma de origen y destino de la traducción

En móvil, mantén presionado el balón flotante; en escritorio, mueve el ratón al balón flotante para abrir la configuración, selecciona otro servicio de traducción/otro idioma de destino.

### 9. Problema de Interfaz de Google Translate Bloqueada

Por favor, añade el dominio `translate.googleapis.com` a la regla del proxy.

### 10. ¿Afecta la prohibición de OpenAI sobre las API Keys en China a los servicios de AI para miembros?

No hay impacto, el producto utiliza Azure Enterprise OpenAI, que no está sujeto a restricciones regionales de API.

### 11. Error de Traducción de Color Cloud

Al hacer clic en el mensaje de error `?` muestra "trans_type no soportado". Puedes seleccionar manualmente para configurar el idioma detectado automáticamente a un idioma específico.

### 12. WeChat Reading No Puede Ser Traducido

No puede ser traducido porque WeChat Reading ha hecho un procesamiento especial para el contenido para evitar el acceso al contenido a través de medios de terceros.

### 13. Parte del contenido en las páginas web no está traducido

Generalmente, es porque el administrador del sitio web ha definido áreas para no ser traducidas usando `translate="no"` o `notranslate class`, pero puedes resolver esto:

1. Habilitando la función de pasar el ratón
2. Usando el ratón para forzar la traducción del contenido del párrafo en esa área

### 14. La traducción activada no surte efecto

Cuando otros sitios pueden ser traducidos pero un sitio en particular no:

- Si este sitio tiene menos visitantes
  - Se sugiere traducir párrafos pasando el ratón
  - Si necesitas traducir todo el sitio, puedes adaptarlo a través de [reglas de usuario](/docs/advanced/#user-rules)
- Si este sitio es utilizado por muchas personas
  - Puedes comenzar usando el ratón para traducir
  - Informarlo en el grupo, y se adaptará más tarde

### 15. ¿Cómo guardo mi retroalimentación de la página web si tengo problemas con la traducción de la página web?

Necesitas hacer clic derecho en "Guardar como" o usar el atajo Ctrl+S en la página web, elegir archivo único para la opción de guardar, y guardar con el formato de archivo .mht/.mhtml. Luego envía el archivo a support@immersivetranslate.com.

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

### 16. Retroalimentación del registro de depuración

1. Habilitar el registro de depuración: Abrir Panel -> Configuración -> Configuración de Desarrollador -> Habilitar "Imprimir registro de depuración en consola".
2. Abrir la consola del sitio: Hacer clic derecho para abrir la inspección -> Cambiar a la consola en la parte superior de la columna derecha -> Realizar la acción para ver los registros.

### 17. Cómo desactivar el hoverball

- Ocultar en la página actual: Configúralo en "Nunca traducir este sitio"
- Ocultar en todas las páginas: Abre [Página de Configuración] - [Configuración de Interfaz] y desactiva [Mostrar Hoverball en la Página]

### 18. La función de traducción de pasar el ratón + tecla de acceso rápido no funciona

Para habilitar la función de traducción de pasar el ratón más tecla de acceso rápido, la página debe tener primero el foco. Si encuentras que la función no se activa, prueba estos pasos:

1. Haz clic en cualquier parte de la página una vez para asegurarte de que la página tenga el foco.
2. Intenta usar el ratón y la tecla de acceso rápido para la traducción de nuevo.
3. Si la función de traducción aún no responde, verifica si tus configuraciones de teclas de acceso rápido son correctas.

### 19. Cómo actualizar las últimas reglas

La extensión en sí misma sincronizará regularmente con las últimas reglas de adaptación del sitio web oficial cuando la uses. También puedes sincronizar manualmente con las últimas reglas haciendo clic en el icono de la Extensión Immersive Translate en el navegador para abrir una ventana emergente donde la extensión detectará automáticamente las últimas reglas de adaptación y se sincronizará con ellas. Lo mismo se aplica a los scripts de Tampermonkey.

### 20. La traducción falla / La traducción sigue girando

1. Verifique la razón del fallo:
   - Si se alcanza el límite de cuota, significa que la cuota mensual del miembro para esa fuente de traducción está agotada.
   - Si la traducción muestra un error de red, primero verifique el estado de su nodo/red.

2. Cambie la fuente de traducción: mantenga presionada la bola flotante para seleccionar otra fuente de traducción.

### 21. Cómo verificar la cuota y el uso de traducción de miembros Pro

- Los miembros Pro disfrutan de una cuota de traducción base de 20 millones de Tokens por mes, que se puede usar para todos los servicios de traducción. Ya sea usándola toda para DeepL (equivalente a 20 millones de caracteres), toda para OpenAI (20 millones de Tokens), o una mezcla de múltiples servicios, puede asignar libremente la cuota según sus necesidades reales.

  > Los precios de OpenAI se basan en tokens. Para texto en inglés, 1 token es aproximadamente 4 caracteres o 0.75 palabras. Normalmente, 1000 Tokens equivalen a unas 750 palabras en inglés o 400-500 caracteres chinos.

- Dirección de consulta de uso: [https://immersivetranslate.com/accounts/usage](https://immersivetranslate.com/accounts/usage)

### 22. Por qué la calidad de traducción de Google del plugin no es tan buena como la traducción de la página web de Google

Porque el plugin llama a la API gratuita de Google, que es una API antigua que Google no mantiene continuamente, mientras que la traducción oficial de la página web de Google se mantiene continuamente. Teóricamente, la calidad no es tan buena como la traducción oficial de Google, y recientemente la calidad de traducción de la API gratuita de Google ha disminuido significativamente. Recomendamos cambiar a otros servicios de traducción, y estamos buscando activamente soluciones alternativas. Discusión relacionada: [#2574](https://github.com/immersive-translate/immersive-translate/issues/2547)

### 23. Mostrar modo táctil cuando está en modo de ratón

En [Configuración Avanzada](https://dash.immersivetranslate.com/#advanced), habilite el modo solo ratón. La versión 1.14.9 optimizará esta detección de modo.

## Relacionado con la Traducción de Video

### 1. Configuración de subtítulos de Youtube

Puede hacer clic en la configuración de subtítulos propia de Youtube, [Opciones], y luego puede ajustar el tamaño, color, etc.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

### 2. Subtítulos bilingües de YouTube en chino tradicional no se muestran

YouTube viene con subtítulos traducidos automáticamente, y el chino tradicional tendrá errores de formato, causando que todos los subtítulos aparezcan con una gran sección de subtítulos al principio. Basado en este escenario, se recomienda activar la opción [Usar Immersive Translate para traducir subtítulos] en [Configuración] [Subtítulos de Video].

### 3. Cómo habilitar la traducción de subtítulos para Bilibili

Al traducir subtítulos de video de Bilibili, siga estos pasos:

1. Primero, habilite los subtítulos integrados de Bilibili haciendo clic en el botón "Subtítulo" en la esquina inferior derecha del reproductor. Si el video no tiene botón de subtítulo o contenido de subtítulo, no se admiten subtítulos bilingües.
2. Haga clic en el icono "Immersive Translate" en el reproductor para habilitar la función de subtítulos bilingües.

Nota al usar:

1. Asegúrese de que los subtítulos integrados de Bilibili estén habilitados.
2. Asegúrese de que el idioma objetivo de Immersive Translate sea diferente del idioma de los subtítulos integrados de Bilibili para activar la función de traducción.

### 4. Traducción de subtítulos de Netflix usando el estilo de subtítulos original

- El enfoque actual de Netflix utiliza traducción progresiva, con estilo de subtítulos autoalojado, y no admite subtítulos manuales.
- El enfoque antiguo requiere esperar a que todos los subtítulos se traduzcan antes de mostrarlos, pero admite subtítulos manuales.

Para volver al enfoque antiguo, vaya a [[Configuración de Desarrollador](https://dash.immersivetranslate.com/#developer)], busque [Editar Reglas de Usuario] y agregue la siguiente regla:

```json
[
  {
    "id": "netflix",
    "subtitleRule.add": {
      "attachRule": {
        "appendSelector": ""
      }
    }
  }
]
```

## Relacionado con la Traducción de Archivos

### 1. Traducción de documentos locales

- Método 1: Vaya al [sitio web de Traducción de Archivos de Immersive Translate](https://app.immersivetranslate.com/), o haga clic en el icono de la extensión Immersive Translate y haga clic en [Traducción de Archivos] para ingresar.

- Método 2: Si está utilizando navegadores similares a Chrome, como (Chrome, Arc, navegador Edge), hay otra manera: abra la página de gestión de extensiones del navegador `chrome://extensions`, encuentre el plugin [Immersive Translate], [Permitir que la extensión acceda a archivos locales], y luego directamente en el navegador abra el archivo HTML local o PDF local, puede hacer clic derecho directamente [Traducción].

**Nota**: El navegador Safari tiene restricciones estrictas sobre el acceso de extensiones a archivos locales. Los usuarios de Safari deben usar directamente el Método 1: ir al [sitio web de Traducción de Archivos de Immersive Translate](https://app.immersivetranslate.com/) para traducir archivos locales.

### 2. La traducción de PDF es lenta cuando hay muchas páginas

Se recomienda dividir el documento en varias partes de menos de 100 páginas cada una, traducirlas por separado y luego unirlas después de la traducción.

### 3. Traducciones duplicadas o superpuestas en PDF

Esto se debe a problemas de reconocimiento del archivo fuente. Actualmente, se recomienda hacer clic manualmente en esa sección y eliminar los cuadros de texto adicionales. Continuaremos optimizando esta situación en futuras actualizaciones.

### 4. ¿Hay un glosario / traducción especial o no traducción para ciertos términos?

La versión 1.16.1+ admite la función de [Biblioteca de Terminología AI](https://dash.immersivetranslate.com/#terms).

La biblioteca de terminología AI no admite la terminología de traducción automática de Google/Microsoft por defecto.

Método para habilitar forzosamente:
(ps: la traducción automática utiliza reemplazo de marcadores de posición, la terminología puede reducir la calidad de la traducción)

Vaya a [[Configuración de Desarrollador](https://dash.immersivetranslate.com/#developer)] -> [Editar Configuración Completa de Usuario]

```
{
  ....
  "enableMachineTranslateTerms":true,
  ...
}
```

### 5. No se pueden exportar archivos de Word traducidos en formato Word

Actualmente, hay algunos problemas técnicos con la exportación de archivos de Word. Se recomienda mantener el formato existente. Estamos trabajando continuamente en la optimización.

### 6. Cómo ajustar el tamaño mínimo de fuente en PDFs

Esto se debe a la restricción del tamaño mínimo de fuente del navegador. Ajuste la fuente del navegador a la configuración más baja. Para Chrome, por ejemplo: haga clic en [Configuración de tamaño de fuente de Chrome](chrome://settings/fonts?search=%E5%AD%97%E5%8F%B7)

## Relacionado con la Traducción de Cuadro de Entrada

### 1. La mejora del cuadro de entrada no surte efecto

- Navegadores que se sabe que no son compatibles: Consulte la sección de compatibilidad de [Traducción de Cuadro de Entrada](https://immersivetranslate.com/docs/input/)
- No se puede traducir en la barra de URL o la página inicial del navegador, solo admite barras de búsqueda. Puede probar en https://www.bing.com/
- Intente presionar la tecla de espacio más rápido

## Relacionado con el Pago

### 1. ¿Puedo usar WeChat Pay?

Los pagos de WeChat requieren enviar un mensaje privado a los miembros del personal en el grupo y anotar "pago WeChat". Después de que el personal proporcione el código QR de pago, realice el pago y proporcione los detalles del pago. El personal proporcionará el código de canje de membresía anual/mensual requerido, que se puede canjear en la [Página de Canje de Miembros](https://immersivetranslate.com/exchange/)

### 2. ¿Puedo obtener una factura?

Actualmente, solo las membresías anuales pueden recibir facturas. Los usuarios que ya han pagado y necesitan una factura deben enviar un mensaje privado a los miembros del personal en el grupo y anotar "emisión de factura". Los usuarios no pagados pueden consultar: [Información de Factura de Membresía Anual](https://immersivetranslate.com/bill/)

## Más preguntas (poco comunes)

<details>
<summary>¿Cómo borro mi caché con Tampermonkeys?</summary>
<p>
Debido a la limitación de la API de Tampermonkeys, la caché de Immersive Translate Tampermonkeys se guardará en la caché del sitio web correspondiente, por lo que si desea borrarla, puede abrir el panel de herramientas de desarrollador del sitio web correspondiente en su navegador y luego borrar la caché de ese sitio web.
</p>
</details>

<details>
<summary>¿Falló la solicitud de dirección de interfaz personalizada de Tampermonkey?</summary>
<p>
Tampermonkeys requiere que todas las solicitudes del script necesiten declarar permisos al principio del script, por ejemplo: `@connect api.google.com`, por lo que si necesita agregar un nuevo nombre de dominio que no sea el predeterminado, declárelo al principio del Tampermonkey modelado según el otro nombre de dominio.
</p>
</details>

<details>
<summary>El plugin del navegador Edge se abre en blanco y el navegador informa un error MANIFEST-000001</summary>
<p>
Abra la aplicación [Quick File Finder (Everything)](https://www.voidtools.com/en-us/downloads/), busque `amkbmndfnliijdhojkpoglbnaaahippg` (el ID de extensión de Immersive) en la carpeta de almacenamiento del navegador, elimínela, luego desinstale y reinstale el plugin.
</p>
</details>

<details>
<summary>¿Cómo descargar subtítulos bilingües / Se pueden descargar subtítulos bilingües de otros sitios web?</summary>
<p>
- Actualmente, la descarga de subtítulos solo se admite en el escritorio.
- Incluyendo YouTube, cuando hay un botón de descarga de subtítulos, el sitio web actual admite la descarga de subtítulos bilingües.
</p>
</details>