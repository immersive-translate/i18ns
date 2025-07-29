---
sidebar_position: 6
---

# Registro de Cambios

Este registro de cambios se actualiza de acuerdo con el progreso del desarrollo. La fecha después de la versión es la fecha de fusión del código, no la fecha de lanzamiento en las tiendas de aplicaciones (el tiempo de revisión varía después de la presentación a cada tienda de aplicaciones, algunas pueden tardar hasta una semana en revisar). Actualmente, estamos avanzando con dos versiones.

La **versión Release** es la versión estable oficial, disponible en las principales tiendas de aplicaciones como
[Chrome](https://chromewebstore.google.com/detail/bpoadfkcbjbfhfodiogcnhhhpibjhbnh),
[Edge](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg),
[Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate/),
[Apple](https://apps.apple.com/app/id6447957425), etc.

La **versión Preview** se publica con más frecuencia e incluye algunas características experimentales. En comparación con la versión Release, puede contener más errores. Se publica principalmente en

- [userscript del sitio web oficial](https://download.immersivetranslate.com/immersive-translate.user.js)
- [versión beta en la tienda de Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate-beta/)
- [Github Release Assets](https://github.com/immersive-translate/immersive-translate/releases)

## 1.14.16 Release (2025-02-21)

- Añadido: Deepseek, Gemini, Claude soportan cambio de contexto.
- Corregido: Actualizar términos no envía nueva solicitud de traducción.
- Mejorado: El idioma de la interfaz añade húngaro.
- Mejorado: Calidad de traducción de Google.
- Mejorado: Formateo de imágenes gratuito.

## 1.14.12 Release (2025-02-19)

- Mejorado: Pausar la traducción limpia inmediatamente la cola de solicitudes.
- Mejorado: Filtra texto sucio en el servicio de traducción deepl.
- Corregido: Traducción de la barra lateral inválida en configuraciones avanzadas.
- Corregido: Problema de visualización de traducción personalizada deepseek.

## 1.14.11 Release (2025-02-18)

- Corregido: Error `401: Authentication Fails` de la clave API personalizada de DeepSeek.

## 1.14.10 Release (2025-02-17)

- Nuevo: Membresía Pro soporta el servicio de traducción DeepSeek (v3).
- Corregido: Resuelto el problema de que el archivo de configuración del usuario excedía el límite de tamaño.
- Mejorado: El elemento del menú del clic derecho se puede cerrar (operado en configuraciones avanzadas).
- Mejorado: Mejoradas las capacidades de reconocimiento de idioma para Greasemonkey y Safari en páginas con idiomas menores.
- Mejorado: Acceso a la interfaz de prueba de la página de configuraciones en línea.
- Mejorado: Mejorada la experiencia del usuario de la función de vista previa de comparación de contexto.
- Mejorado: Lógica de juicio de modo táctil y de ratón.

## 1.14.8 Release (2025-02-10)

- Corregido: Problema donde los archivos largos de PDF-Pro no se traducían automáticamente.
- Mejorado: Microsoft, Google y Tencent ahora soportan cantonés.
- Mejorado: BBC ahora soporta subtítulos.

## 1.14.6 Preview (2025-02-08)

- Corregido: Problema donde **Mouse Hover Translation** no podía traducir texto enriquecido.
- Mejorado: La versión de Tampermonkey ahora soporta la traducción de subtítulos de YouTube.

## 1.14.4 Release (2025-02-07)

- Corregido: Problema con la detección incorrecta de idioma en **Enhanced Input Box**.
- Corregido: Problema de coincidencia inteligente de expertos en IA en servicios de traducción personalizados.
- Corregido: Problema de fallo de sincronización de Google Drive en algunos navegadores.
- Corregido: Problema de traducción de comentarios en vivo de YouTube.
- Corregido: Problema de superposición de subtítulos en algunos videos de YouTube.
- Mejorado: Fallo en la traducción de manga en sitios como shonenjumpplus en el navegador Safari.

## 1.13.8 Release (2025-01-24)

- Nuevo: La traducción de imágenes gratuita ahora está disponible (actualmente solo soportada en versiones de PC de los navegadores Chrome y Edge), accesible a través del menú del clic derecho.
- Corregido: Abordado un problema donde se omitía contenido durante la traducción de múltiples segmentos en Gemini.
- Optimizado: Mejorada la carga de subtítulos de YouTube.
- Nuevo: El servicio de traducción de IA ahora soporta noruego.

## 1.13.6 Preview (2025-01-17)

- Mejorado: **AI Expert** se puede usar con **AI Context-Aware Translation**.
- Mejorado: **Image Translation** ahora es compatible con weibo.com (soportado solo en Chrome y Edge).
- Mejorado: Cuando el idioma de la interfaz está configurado en inglés, el idioma de destino predeterminado para **Enhanced Input Box** se cambia a chino.
- Mejorado: Añadida una entrada de revisión de tienda en las opciones **More** en el panel.

## 1.13.5 Release (2025-01-14)

- Mejorado: Compatible con el modelo de pensamiento Gemini 2.0.
- Mejorado: Soporta estilo en negrita en modo solo traducción.

## 1.13.4 Preview (2025-01-13)

- Añadido: Los miembros Pro ahora pueden usar directamente el modelo **zhipu 4.5**.
- Mejorado: Traducción de Gemini.

## 1.13.1 (2025-01-10)

- Añadido: Cuando el texto traducido y el texto original pertenecen al mismo sistema de escritura, se muestra la traducción usando un estilo especializado.
- Corregido: El problema donde **Mouse Hover Translation** no funciona en algunos sitios web.
- Mejorado: DeepLx ahora soporta árabe.
- Mejorado: Mejorado el reconocimiento del idioma original. Anteriormente, las páginas que contenían múltiples idiomas podrían no traducirse, pero ahora se traducen correctamente.
- Mejorado: Para Twitter, las traducciones de contenido de varias líneas están configuradas para no ajustarse por defecto. El ajuste ocurrirá solo cuando el contenido exceda las 10 líneas o 1000 caracteres. El ajuste se puede habilitar a través de configuraciones **Advanced Settings** -> **Enable automatic line wrapping for long paragraphs**.

## 1.12.8 (2025-01-03)

- Corregido: el problema donde la página de configuraciones de iOS 18.3 no se muestra correctamente.
- Corregido: la falta de líneas vacías al traducir tweets.
- Corregido: el problema de que los números decimales se rompen forzosamente al traducir textos largos.

## 1.12.7 Release (2024-12-30)

- Mejorado: Bing/Google ahora soportan portugués (Brasil).
- Mejorado: Mejoradas las descripciones para el idioma de la interfaz de usuario en chino tradicional.
- Mejorado: Ajuste de diseño para idiomas de derecha a izquierda en paneles y páginas de configuraciones.

## 1.12.6 (2024-12-26)

- Corregido: Problema donde la función de pasar el ratón carga el servicio de traducción incorrecto bajo ciertas condiciones.
- Corregido: Problema donde habilitar temporalmente subtítulos bilingües en YouTube no funciona.
- Corregido: Después de cambiar los servicios de traducción, el servicio de traducción en "**Enhanced Input Box**" no se actualiza.
- Corregido: El interruptor "**YouTube Enable Bilingual**" en la página de configuraciones no funciona.
- Mejorado: Eliminado el modelo gemini-1.0-pro obsoleto.

## 1.12.4 (2024-12-13)

- Añadido: **AI Context-Aware Translation** puede mejorar la precisión de la traducción de contenido profesional. (Disponible solo para miembros Pro, soportado exclusivamente por modelos de OpenAI) **Options** -> **Grneral** -> **Enable AI Context-Aware Translation**
- Corregido: Algunos errores en el efecto de traducción de múltiples líneas en Twitter.
- Corregido: Problemas con la traducción de ciertas fórmulas debido a texto enriquecido.
- Mejorado: Al traducir en **x.com**, los videos con subtítulos tendrán automáticamente subtítulos bilingües traducidos.
- Mejorado: Los videos sin subtítulos mostrarán un icono de traducción y proporcionarán una razón por la cual la traducción no es posible.

## 1.11.7 (2024-11-25)

- Añadido: Bing/Google ahora soportan jemer (camboyano).
- Añadido: Permitir que los archivos ePub incompletos continúen traduciendo desde donde se quedaron al volver a importarlos.
- Corregido: Problema con la traducción de imágenes de Twitter en el navegador Safari.
- Corregido: Las teclas de acceso rápido se vuelven ineficaces al activar o desactivar la función "**Hover Translation**".
- Mejorado: Mejorada la visualización de traducción bilingüe de múltiples líneas en Twitter y Youtube.
- Mejorado: La traducción de texto enriquecido está desactivada por defecto en modo bilingüe para mejorar la calidad de la traducción.
- ~~Mejorado: Añadida la opción de personalizar la "**Enable Sidebar & Navbar Translation**" en "**Advanced Settings**".~~
- Mejorado: Las imágenes ya no se traducen en el modo "**Hover - immediately translate this paragraph**".

## 1.11.4 (2024-11-16)

- Corregido: Problema con la traducción de fórmulas causado por la "Mejora de Traducción de Twitter" en la versión 1.11.2.

## 1.11.2 (2024-11-13)

- Corregido: Problema donde el contenido desaparece después de hacer clic en "ver más" en el modo solo traducción de Facebook.
- ~~Mejorado: Mejorada la visualización de traducciones bilingües de múltiples líneas en Twitter.~~
- Mejorado: Actualizada la interfaz de usuario de la lista desplegable de servicios de traducción en el panel.

## 1.11.1 (2024-11-05)

- Añadido: La **Subtitles Translation** en reuniones en tiempo real ahora soporta activación a través de "bola flotante", disponible en Zoom, Google Meet y Microsoft Teams.
- Corregido: Problemas de sincronización de subtítulos en YouTube después de ver anuncios.
- Corregido: Problemas de visualización con el menú de traducción del clic derecho en Safari en MacOS 15.
- Corregido: Problemas con la funcionalidad de deshacer Ctrl+Z en el **Enhanced input** en ciertos sitios web.

## 1.10.6 (2024-10-25)

- Corregido: Problema con las teclas de acceso rápido de **Enhanced input** que no se activan.
- Mejorado: Reducir el tamaño del paquete de instalación.
- Mejorado: Solución de visualización de subtítulos de Netflix.

## 1.10.5 (2024-10-23)

- Añadido: Mostrar una advertencia cuando el idioma de origen y el idioma de destino son el mismo.
- Corregido: Problema de traducción de caracteres de espacio en blanco en texto enriquecido [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175).
- Mejorado: Mejora de la funcionalidad de mejora de entrada y pasar el ratón dentro de iframes incrustados en páginas web.

## 1.10.2 (2024-10-11)

- Añadido: Traducción de imágenes (versión Beta).
- Añadido: Modo de Soporte de Ratón Forzado (Habilitar esta función solo si la función de pasar el ratón no está disponible en dispositivos tablet) **Settings** -> **Advanced Settings** -> **Forece Enable Mouse Support**.
- Añadido: Mostrar mensaje de error cuando la traducción de subtítulos de video falla.
- Corregido: Problema de traducción de texto enriquecido [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163).
- Mejorado: Abordados problemas donde el botón de traducción podría no funcionar durante la traducción de PDF.
- Mejorado: Mejorada la representación de fórmulas traducidas.
- Mejorado: Lista de selección de idioma.

## 1.9.8 (2024-09-28)

- Añadido: Servicio de traducción "Zhipu BigModel".
- Eliminado: Modelo "SiliconCloud" qwen1.5-7B-chat (debido a la discontinuación oficial).
- Corregido: Resuelto problema de compatibilidad de inicio de sesión con el complemento Safari en macOS 15.

## 1.9.7 (2024-09-20)

- Soporte mejorado para la entrada en Baidu, Gmail y otros campos de entrada
- Soporte para el encabezado de solicitud anthropic-dangerous-direct-browser-access para la API de Claude Anthropic
- Soporte para descargar subtítulos de videos de Hulu, Bloomberg y Domestika
- DeepX soporta traducción de texto enriquecido
- Se solucionó el problema de que los expertos en IA personalizados no se sincronizaban

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) soporta la copia de fórmulas (haga clic derecho en la fórmula para ver el menú de copia)
- Se solucionó el problema de la visualización de subtítulos bilingües para múltiples videos en la misma página de Twitter
- Se corrigieron algunos errores

## 1.9.3 (2024-09-05)

- La opción para la visualización de comparación bilingüe/solo traducción se ha movido a la configuración general.
- Por defecto, el sistema recordará el modo activado al hacer clic en el icono en el panel para la visualización de comparación bilingüe o solo traducción. Para cambiar temporalmente, haga clic en "Más" -> "Cambiar a visualización solo traducción" en el panel.
- Por defecto, traducir de chino simplificado a chino tradicional y viceversa usará el modo solo traducción, en lugar del modo de comparación bilingüe.
- Se corrigieron algunos errores.

## 1.9.1 (2024-09-03)

- Soporte para configurar excepciones para idiomas y sitios web en modo de contraste bilingüe o solo traducción (configurar en la página de Configuración -> Configuración Avanzada). Por ejemplo: Si su modo de traducción predeterminado es contraste bilingüe, pero no desea que el chino tradicional también use contraste bilingüe, entonces puede agregar el chino tradicional a los idiomas de excepción para el contraste bilingüe, de modo que el chino tradicional use el modo solo traducción para la traducción. De manera similar, si su modo de traducción predeterminado es solo traducción, pero desea que un cierto idioma o sitio web use el modo de contraste bilingüe, también puede agregar ese idioma o sitio web a los idiomas de excepción.
- Se solucionó un problema donde el cuadro de entrada en la interfaz de mensajes privados de Tiktok se traducía incorrectamente
- Se solucionó un problema donde los cómics en Read Comic Online no se podían traducir
- Se solucionó un problema donde la [Configuración Avanzada -> Número mínimo de caracteres requeridos para traducir un párrafo] no surtía efecto en algunos casos

## 1.8.4 (2024-08-30)

- El servicio de traducción DeepL ahora oficialmente soporta el chino tradicional como idioma de destino (anteriormente, traducir al chino tradicional con DeepL implicaba un proceso adicional de conversión de chino simplificado a chino tradicional de terceros).
- Se optimizó el rendimiento de la traducción de texto enriquecido.

## 1.8.3

- Google Meet ahora soporta subtítulos bilingües para reuniones en vivo: Ahora, puede disfrutar de la función de subtítulos bilingües en las reuniones de Google Meet. Simplemente abra el enlace de la reunión, active los subtítulos bilingües en el panel de traducción inmersiva y luego actualice la página para experimentarlo.
- Se agregó la opción de "Informar problemas de traducción de la página web actual" y la opción de "Encender/apagar rápidamente la bola flotante" en las más opciones del panel.
- Después de ajustar la posición de los subtítulos bilingües de YouTube, el sistema recordará automáticamente la nueva posición.
- Se optimizó la lógica de caché del complemento, ahora limpiando automáticamente los datos de caché que tienen más de 30 días.
- Se optimizaron los bloques de código dentro de los párrafos para una restauración más precisa del texto original.
- Se mejoró el manejo de "palabras no traducibles" en la configuración avanzada.

## 1.8.2

- Ahora puede traducir texto en cuadros de entrada con el clic derecho: Seleccione cualquier texto en un cuadro de entrada en una página web, haga clic derecho para elegir traducir, y la traducción inmersiva traducirá automáticamente el texto seleccionado al idioma de destino del cuadro de entrada, lo que facilita traducir rápidamente texto en idioma nativo en cuadros de entrada a otros idiomas.
- Ahora puede informar rápidamente problemas de traducción de páginas web en la bola flotante de traducción inmersiva. Después de traducir una página web, si hay algún problema, puede hacer clic en el botón [Feedback] en el lado derecho de la bola flotante, completar la descripción del problema y lo resolveremos lo antes posible.
- Los archivos Epub ahora soportan traducción de texto enriquecido (es decir, preservando el formato del texto original de cada párrafo, como enlaces, negritas, etc.)
- Soporte para subtítulos bilingües en tiempo real en reuniones de video de la versión web de Microsoft Teams (Abra el enlace de la reunión de Teams, active los subtítulos bilingües en el panel de traducción inmersiva y luego actualice)
- Se optimizaron los subtítulos bilingües para la versión en inglés de iQIYI (iq.com)
- Se proporcionaron más artículos de arXiv con un diseño de traducción bilingüe optimizado
- Debido a las restricciones del sitio web de Youtube, el script de Tampermonkey de Chrome ya no soporta subtítulos bilingües de Youtube. Por favor, use la [versión del complemento](https://immersivetranslate.com/).

## 1.8.1

- Se solucionaron problemas de traducción con el script de Tampermonkey SiliconCloud
- La traducción de Claude ahora soporta tibetano y permite la configuración del parámetro de Temperatura
- La página de detalles del experto en IA muestra los prompts utilizados por el experto
- La configuración de atajos ahora permite asignar teclas de atajo únicas para cualquier servicio de traducción
- Se optimizó la detección para traducciones de artículos de arXiv

## 1.7.9

- Se solucionaron problemas con la traducción de texto enriquecido para servicios de traducción como Google, DeepL (por ejemplo, páginas que muestran directamente `<button>` etc.)
- Se solucionó el problema donde el atajo bilingüe para videos de YouTube no se podía desactivar.

## 1.7.8

- DeepL, Microsoft Translate, Google Translate, OpenAI, Claude, Gemini y otros servicios de traducción soportan la traducción para retener el formato de texto original (por ejemplo, enlaces, negritas, etc.)
- Después de seleccionar el texto, el menú de clic derecho cambiará a [Traducir el texto], al hacer clic en el cual puede saltar automáticamente a la página de Traducción de Texto Inmersiva
- Nuevo servicio de traducción gratuito para grandes modelos: SiliconCloud, disponible para todos los usuarios.
- Se agregó la traducción de gran modelo Zero-One-Thing, que se puede usar llenando la API Key después de registrarse en la plataforma Zero-One-Thing.
- Nuevo botón de retroalimentación de usuario para la traducción de manga (después de traducir un manga, haga clic en el botón [Feedback] en el lado derecho de la bola flotante para dar retroalimentación sobre la calidad de la traducción).

## 1.7.7

- Adoptar algoritmo de división de oraciones inteligente de IA para subtítulos en inglés autogenerados en YouTube [Pro Disponible]
- Optimizar la traducción de clic derecho a "Traducir al idioma de destino xx"
- Soporte para la integración inmersiva [JS SDK](https://immersivetranslate.com/docs/js-sdk/) para sitios web de terceros
- Optimizar la visualización de subtítulos de Hulu
- Soporte para la traducción de subtítulos de reuniones de la versión web de ZOOM

## 1.7.6

- Soporte para personalizar expertos en IA, la entrada está en la parte inferior de la página de [Configuración]->[Experto en IA].
- Optimizar la carga de subtítulos en el sitio de TED
- Portugués (Brasil) es soportado como idioma del complemento.
- Sitios soportados para la traducción de cómics
  - [Antbyw](https://www.antbyw.com)
  - [Zerobywzz](https://www.zerobywzz.com)
  - [动漫之家](https://www.idmzj.com)
  - [Jmanga](https://jmanga.org)

## 1.7.5

- Habilitada la copia de subtítulos de YouTube
- Optimizada la visualización de subtítulos en algunos sitios de video
- Mejorada la velocidad de traducción de manga

## 1.7.2

- Se solucionó el fallo de traducción de cómics en el navegador Firefox.

## 1.7.1

- Mejorada la velocidad de traducción para traducciones de cómics
- Se agregó soporte para nuevos sitios en traducciones de cómics:
  - [ShonenJumpPlus](https://shonenjumpplus.com)
  - [Heros Web](https://viewer.heros-web.com/)
  - [Comic Days](https://comic-days.com/)
  - [ComicWalker](https://comic-walker.com/)
  - [Web Ace](https://web-ace.jp/)

## 1.6.6

- Se agregó soporte para nuevos sitios para la traducción de cómics:
  - [Mangabuddy](https://mangabuddy.com/)
  - [Hitomi](https://hitomi.la)
  - [Yamibo](https://www.yamibo.com)
  - [Copymanga](https://www.copymanga.site/)
- Los subtítulos bilingües de YouTube ahora soportan la división inteligente de oraciones (Beta) (Solo cuando se habilita manualmente la traducción inmersiva de subtítulos de YouTube en [Configuración] - [Subtítulos de Video], y los subtítulos originales del video son subtítulos en inglés autogenerados)
- Se agregó el servicio de traducción Tencent [【Hunyuan Large Model】](https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- Solucionar los problemas de diseño de texto de las traducciones de cómics para idiomas en el alfabeto latino.
- Nuevos sitios soportados para la traducción de cómics:
  - COMIC FUZCOMICFUZ(https://comic-fuz.com/)
  - MangaDexMangaDex(https://mangadex.org/)
  - KuaiKan ComicsKuaiKanComics(https://www.kuaikanmanhua.com/)
- Se solucionó un problema donde los servicios de IA personalizados no podían seleccionar expertos en IA.

## 1.6.4

- Cuando se utilizan expertos en IA para "Selección Inteligente", se pueden personalizar diferentes expertos en IA para diferentes sitios web. Esto se puede configurar en [Configuración] -> [Expertos en IA] -> [Ingresar cualquier experto].
- Se solucionó el problema donde los subtítulos no se mostraban en YouTube en modo "Solo Traducción".
- Se solucionó el problema de que los subtítulos bilingües no funcionaban en Mubi.
- Compatible con PDFs abiertos con el complemento Adobe Acrobat.
- Todos los usuarios pueden [contribuir en línea](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/) a la traducción multilingüe de la interfaz de traducción inmersiva.

## 1.6.3

- Nueva función: Traducción de manga (Beta), en sitios web de manga soportados, aparecerá un botón de traducción de manga debajo de la bola flotante de traducción rápida de la página web. Al hacer clic en él, se activará la traducción de manga. Esta función está disponible para miembros Pro (500 páginas por mes, se pueden comprar paquetes adicionales), actualmente soportando los siguientes sitios:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)

## 1.6.2

- Nueva función: Traducción de manga (Beta), en los sitios web de manga compatibles, aparecerá un botón de traducción de manga debajo de la bola flotante de traducción rápida de la página web. Al hacer clic en él, se activará la traducción de manga. Esta función está disponible para miembros Pro (500 páginas por mes, se pueden comprar paquetes adicionales), actualmente compatible con los siguientes sitios:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- Nueva función: La traducción AI admite el [modelo grande Doubao](https://www.volcengine.com/product/doubao)
- Nueva función: Soporte para el modo de comparación bilingüe con la traducción primero y el texto original después, que se puede habilitar en la página de configuración -> configuraciones avanzadas.
- La lista de modelos AI personalizados admite la sintaxis `-all`, que puede eliminar todos los modelos preestablecidos.
- En los subtítulos bilingües de video, cuando el idioma de destino es chino simplificado y el texto original es chino tradicional, el texto original se convertirá automáticamente a chino simplificado, y viceversa.
- Se solucionó el problema donde el atajo de la bola flotante no podía traducir en iOS 18.
- Se solucionó el problema donde los Prompts personalizados no eran efectivos cuando se usaban demasiados.

## 1.6.1

- Soporta la plataforma de modelos grandes Baidu Qianfan, la plataforma de modelos grandes Alibaba Bailian, la plataforma de modelos grandes DeepSeek.
- Se solucionó el problema donde al modificar el idioma de destino y otras configuraciones en el panel emergente se restablecían al hacer clic en la bola flotante de traducción.

## 1.5.8

- Los expertos AI admiten el modo "Selección Inteligente", donde el sistema seleccionará automáticamente el experto AI más adecuado según el sitio web actual (por ejemplo, se seleccionarán automáticamente expertos AI relacionados con tecnología para The Verge y Hacker News, mientras que se seleccionará automáticamente la mejora de traducción de Twitter para Twitter).

## 1.5.7

- Soporte para agregar servicios de traducción AI personalizados compatibles con OpenAI, accesibles en la parte inferior de la página [Configuración]->[Servicios de Traducción].
- Se solucionó un problema donde los subtítulos bilingües no funcionaban en la plataforma de video Domestika en Safari.

## 1.5.6

- Se optimizó significativamente el rendimiento de la traducción de grandes páginas web, la creación de ePub y los archivos de subtítulos.
- Se solucionó el error de sincronización en múltiples dispositivos en Pro.

## 1.5.4

- Los miembros Pro admiten servicios de traducción Claude y Gemini listos para usar (Beta)
- Los subtítulos bilingües de YouTube admiten configuraciones de fuente y peso de fuente
- Se solucionaron problemas de límites de palabras al ajustar párrafos largos [#86](https://github.com/immersive-translate/immersive-translate/issues/86)
- Se solucionó el reconocimiento de los idiomas japonés y coreano
- Se solucionó el problema donde las páginas de Reddit en dispositivos móviles no se traducían al desplazarse
- Se solucionó la falta de traducciones en algunas páginas con DeepL
- Se solucionó el tiempo de sincronización en múltiples dispositivos para usuarios Pro
- Se optimizó la cobertura de la configuración de sincronización en la nube
- Se optimizaron las palabras de prompt para los servicios de traducción AI

## 1.5.2

- Se solucionó el problema donde los cambios en el prompt general del experto sobrescribían el prompt del experto AI especificado [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- El nombre del modelo AI personalizado admite sintaxis avanzada, use + para agregar un modelo, use - para ocultar un modelo, y use model_name=display_name para personalizar el nombre de visualización del modelo, por ejemplo: +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- Se solucionó el error devuelto por Gemini
- Ocultar la bola flotante al imprimir la página
- Se solucionó el problema donde el tamaño de la fuente no se escalaba proporcionalmente cuando YouTube estaba en pantalla completa [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- Soporte para servicios de traducción AI para configurar [AI Expert] para especificar la estrategia de traducción, actualmente una función Beta, que se puede habilitar en [Configuración de Desarrollador](https://dash.immersivetranslate.com/#developer) después de habilitar Beta, y el menú [AI Expert] se puede ver después de actualizar.
- Los servicios de traducción AI ahora pueden personalizar la lista de modelos, como [OpenAI], el sistema solo tiene algunos de los modelos más utilizados integrados. Al hacer clic en la lista desplegable de modelos, el último elemento que ve es [Set More Models], después de configurar, se recordará automáticamente para la conveniencia de los usuarios que prueban diferentes modelos personalizados.
- Se optimizó la inconsistencia en el diseño de las traducciones en algunos casos.
- Se agregó un botón de restablecimiento para el estilo de subtítulos de YouTube, que puede restaurar rápidamente al estilo predeterminado.
- Se solucionó el problema donde los subtítulos en chino no se podían descargar en YouTube.
- Se optimizó la copia de la interfaz en chino tradicional.

## 1.4.12

- Se solucionó el problema del cuadro de diálogo de mensajes no traducidos al abrir la página de Reddit
- Se agregó una función temporal para habilitar la edición de traducción en la entrada "Más" del panel
- Se solucionó el problema donde YouTube Shorts sin subtítulos siempre muestra subtítulos del video anterior [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
- Se solucionó el problema donde los subtítulos bilingües de YouTube no se podían ajustar hacia arriba y hacia abajo en pantalla completa [#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)
- Soporte para subtítulos bilingües en [VK Video](https://vk.com/video)
- Soporte para configuraciones de activación independientes para subtítulos bilingües de video de YouTube (habilitado por defecto para nuevos usuarios)
- Se optimizaron los mensajes de error para la traducción de subtítulos bilingües locales

## 1.4.11

- Compatible con la traducción del cuadro de entrada de la página de Bing Copilot
- El control de estilo de subtítulos de YouTube admite el estilo de borde
- Soporte para seleccionar el servicio de traducción predeterminado en la página de Configuración -> Servicio de Traducción
- Se solucionó el reemplazo de marcadores de posición de OpenAI SystemPrompt
- Se solucionó el problema de fusión de reglas de usuario personalizadas
- Se solucionó la visualización anormal de subtítulos en algunos videos de Netflix [#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)
- Se solucionó el problema donde los cambios frecuentes en el color de traducción a través de la paleta de colores no eran efectivos [#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)

## 1.4.9

- Los servicios de traducción ahora están organizados de manera distinta bajo una pestaña separada, permitiendo una visión general completa de todos los servicios de traducción disponibles. Además, los usuarios tienen la flexibilidad de personalizar qué servicios de traducción se muestran. Por defecto, solo se muestra una selección limitada de servicios de traducción, pero los usuarios pueden adaptar sus preferencias de visualización en la sección [More Services](https://dash.immersivetranslate.com/#services).
- La página de configuración ahora acomoda ajustes para [estilos de subtítulos de YouTube](https://dash.immersivetranslate.com/#subtitle).
- Se han realizado mejoras para abordar el problema donde los subtítulos bilingües inmersivos no se mostraban cuando los usuarios configuraban el idioma de los subtítulos a chino en el sitio web de YouTube.
- Se ha introducido un nuevo atajo para la traducción temporal llamado Claude, que se puede configurar en la [página de Configuración de Atajos](https://dash.immersivetranslate.com/#shortcuts).

## 1.4.8

- Optimizar el rendimiento de traducción para archivos grandes en PDF-Pro
- Mejorar el rendimiento de traducción para páginas de contenido largo
- Implementar soporte de internacionalización (i18n) para la navegación de documentos de página
- YouTube introduce una función para habilitar temporalmente subtítulos bilingües
- YouTube admite la descarga de subtítulos bilingües (solo para miembros)
- Móvil agrega control por gestos, mejorando la entrada a través de [configuración de atajos](https://dash.immersivetranslate.com/#shortcuts)
- Soporte para traducción bilingüe en Google Docs

## 1.4.7

- Se solucionó el problema donde la traducción fallaba al cambiar las palabras de prompt personalizadas de OpenAI bajo el botón de prueba
- Se solucionó el problema del icono de atajo de subtítulos de YouTube que no se mostraba
- Se optimizó el reconocimiento de idioma de la extensión

## 1.4.6

- Se solucionó el problema donde las palabras de prompt definidas por el usuario no eran efectivas
- Se agregaron opciones de 50%, 150% para el tamaño de fuente de los subtítulos de YouTube

## 1.4.5

- Se solucionó el problema donde los cambios en los estilos de subtítulos de YouTube no se guardaban
- Se solucionó la desaparición de subtítulos en pantalla completa en iOS Safari
- Se optimizó aún más la velocidad de traducción de subtítulos de YouTube
- Las más opciones del panel ahora admiten [entrada de traducción de texto](https://app.immersivetranslate.com/text/)

## 1.4.2

- Soporte para el servicio de traducción Claude
- Se optimizaron las palabras de prompt múltiples de OpenAI, admitiendo formato YAML, lo que mejora la flexibilidad y facilidad de uso de la configuración
- Se optimizó significativamente la velocidad de traducción de subtítulos de YouTube, y se agregó soporte para cambiar entre el orden chino e inglés, personalizar el color y tamaño de la fuente, etc.
- La plataforma de subtítulos de video admite [University of Southampton](https://southampton.cloud.panopto.eu)
- Subtítulos bilingües de Udemy compatibles con la visualización móvil
- El servicio de traducción Gemini está oculto por defecto, se puede habilitar en la configuración de desarrollador para mostrar la beta de este servicio de traducción

## 1.3.4

- Soporte para el servicio de traducción gratuito de Yandex
- Se optimizaron las palabras de prompt de Gemini
- Los subtítulos de video admiten la configuración para la visualización bilingüe/original y de traducción
- Soporte para espacio entre chino e inglés en los resultados de traducción de OpenAI
- El interruptor del panel para mostrar solo el botón de traducción modificado para que solo tenga efecto en la página actual

## 1.3.3

- Se optimizó el problema de visualización de traducción de subtítulos de video CC de Twitter.
- El servicio DeepL ha agregado soporte para árabe.
- El servicio de traducción Colorful Clouds ahora admite coreano, español, francés y ruso.
- El servicio OpenAI ha agregado soporte para el dialecto del noreste de China.
- La detección automática del panel ahora muestra el idioma original.
- Se ajustó la descripción del atajo para el panel móvil.

## 1.3.2

- Se solucionó el problema donde el panel de control no se podía cerrar en dispositivos móviles

## 1.3.1

- La plataforma de subtítulos de video admite [DeepLearning.ai](https://learn.deeplearning.ai)
- Soporte para la traducción de páginas web y subtítulos de video en idiomas como árabe, hebreo, etc., abordando problemas de visualización RTL (de derecha a izquierda)
- Se solucionó la traducción de Gemini al hebreo
- Se solucionó un problema donde algunos subtítulos en chino tradicional en YouTube no se podían mostrar correctamente
- Se solucionó el problema de visualización de subtítulos de Twitter en Safari
- Se solucionó el atajo para la traducción inmediata al final de la página

## 1.2.4

- Se solucionó el problema donde los marcadores de posición en la creación de ePub no se reemplazaban correctamente
- Soporte para la traducción de subtítulos de video [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- Optimizado el control de frecuencia de las solicitudes de servicio de traducción
- Las solicitudes recientes al servicio de traducción de Microsoft desde China han sido inestables; cuando ocurren errores, el sistema detecta automáticamente el servicio de traducción disponible, permitiendo a los usuarios cambiar rápidamente.
- Optimizado el mensaje de error para errores de red
- Solucionado el problema donde la configuración del color del texto no soportaba la vista previa RGBA [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Solucionado el problema donde al actualizar la versión del plugin de Safari siempre se mostraba la página de éxito de instalación
- Microsoft añadió soporte para vietnamita
- Solucionado el problema donde los subtítulos traducidos en el sitio edx no se mostraban

## 1.2.2

- Soporte de traducción de subtítulos de video para [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). También soporta la traducción de algunos videos con subtítulos CC en Twitter.
- Optimización de ventanas emergentes de error, las ventanas emergentes de error de problemas de red detectan automáticamente servicios de traducción gratuitos válidos.
- Solucionado el soporte de la APP inmersiva de iOS para la reproducción en pantalla completa de YouTube.
- Solucionado el problema de traducción de párrafos con Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707).

## 1.2.1

- Soporte de traducción de subtítulos de video para [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/).
- Solucionado un problema donde algunos usuarios Pro no podían modificar configuraciones en el navegador Chrome.
- Soporte para la visualización de subtítulos bilingües en el modo de pantalla completa de YouTube en iOS.

## 1.2.0

- Soporte para la traducción de subtítulos de video en las plataformas [LinkedIn](https://www.linkedin.com/) y [Viu](https://www.viu.com/).
- Añadido más acceso rápido a subtítulos de video para plataformas adicionales.
- Soporte para configurar sitios web/idiomas específicos para mostrar solo el texto traducido.
- Solucionado un problema donde la página de configuraciones mostraba continuamente la carga en algunos casos en Safari.
- Soporte para traducir nodos de etiquetas de entrada.
- Optimización de la interfaz de usuario de la ventana emergente de error.

## 1.1.9

- Soporte de traducción de subtítulos para YouTube Live y la plataforma [Mubi](https://mubi.com/).
- Optimización: Página de configuraciones, interfaz de usuario de interacción de lista de URL (para evitar ambigüedades, las casillas de verificación no se muestran por defecto).
- Soporte para configurar la fuente de traducción en modo solo traducción.
- Añadido acceso rápido para habilitar subtítulos de video en Netflix, Ted, Bloomberg, Udemy, Coursera.
- Solucionado: Algunos estilos traducidos (como subrayados) no eran efectivos en Safari.
- Solucionado: Durante la traducción de la página, el problema donde al pasar el ratón no se activaba la retraducción.

## 1.1.8

- Añadida una opción para que el servicio de traducción secundario siga al servicio de traducción principal
- Soporte de subtítulos bilingües para [Amazon Prime Video](https://www.primevideo.com)
- Optimización adicional de la función de traducción de PDF incrustado en Sci-Hub
- Solucionado un problema con PDFs en línea que no se abrían correctamente
- Solucionado el problema con la reproducción continua de subtítulos bilingües en Netflix

## 1.1.7

- Ahora puedes especificar una fuente para la traducción en la página de configuraciones -> [Configuraciones Básicas] -> [Estilo de Traducción]
- Añadida una configuración de atajo para [Traducir Párrafo Especificado] en el panel de bola flotante en dispositivos móviles
- Optimizada la sensibilidad de detección del ratón sobre Ctrl para evitar confundir `Ctrl+C` como `Ctrl`
- Añadido soporte para una nueva configuración de atajo que permite alternar rápidamente si los subtítulos de video usan los subtítulos de traducción automática integrados
- En el sitio web de Sci-Hub, al hacer clic en la bola flotante se traducirán los PDFs incrustados en la página web

## 1.1.6

- **Soporte Móvil para Traducir Párrafos Específicos:** La versión móvil ahora soporta la traducción de párrafos especificados y ha añadido una variedad de operaciones de atajo, incluyendo deslizar a la izquierda, deslizar a la derecha, doble toque, triple toque y gestos de toque con varios dedos. Estos no están habilitados por defecto y requieren que el usuario seleccione activamente el gesto de activación en la página de configuraciones bajo [Pasar el Ratón].
- **Actualización de la Versión Predeterminada de Gemini:** La versión predeterminada ahora es `v1beta`.
- **Traducción de Chino Clásico Corregida:** Corregida la funcionalidad de traducción de Chino Clásico de Microsoft y OpenAI.
- **Optimización de Traducción Japonesa:** Optimizada aún más la traducción japonesa de OpenAI para mejorar la precisión y fluidez.
- **Experiencia de Traducción Inmersiva:** Para adaptarse mejor a los hábitos del usuario, hemos movido el atajo para subtítulos bilingües en modo de pantalla completa en la plataforma de YouTube al lado izquierdo.

## 1.1.5

- Solucionado el problema donde el menú desplegable en modo oscuro en Windows no tenía color.
- Solucionado el problema de alineación con la opción "Más" que no estaba alineada a la izquierda en Windows.

## 1.1.4

- **Actualización de la Interfaz de Usuario del Panel Emergente:** El nuevo diseño tiene como objetivo mejorar la usabilidad y comprensión. Esta actualización incluye:

  - **Nuevas características en el menú principal:**
    - **Interruptor de modo Bilingüe/Solo Traducción:** Ahora puedes cambiar entre "Modo de Traducción Bilingüe" y "Modo Solo Traducción" directamente en el menú principal, ubicado a la izquierda del botón de traducción.
    - **Entrada de traducción de documentos:** La entrada para traducir "archivos PDF/ePub/subtítulos" se ha movido al menú principal para un acceso rápido.
    - **Configuraciones de traducción de video:** La entrada para configuraciones de "Traducción de Video" también se ha colocado en el menú principal para ajustes rápidos.
    - **Nueva entrada para documentación de uso:** Proporciona guías de operación detalladas y documentos de ayuda.

- **Entrada de traducción de documentos integrada:** Ahora, puedes traducir archivos PDF, ePub y de subtítulos a través de una entrada de carga unificada. Simplemente haz clic en el botón [PDF/ePub] en el panel emergente, no es necesario seleccionar [Más] más.

- **Añadido soporte para 5 sitios web de video:**
  - Soporte para subtítulos de podcasts en Youtube Music.
  - Añadido soporte para el sitio web iview.abc.net.au.
  - Añadido soporte para el sitio web www.nma.art.
  - Añadido soporte para el sitio web creativecloud.adobe.com.
  - Añadido soporte para el sitio web www.masterclass.com.

## 1.1.3

- Solucionado el problema de anomalía de visualización del plugin móvil al abrir páginas PDF.
- Optimizado el efecto de traducción de conversaciones GPT.
- Soporte de traducción de dominios para Baidu Translate.
- Añadido un modo solo traducción en la página de configuraciones.
- Añadida una función de recordatorio al cambiar modos de traducción con atajos.
- Solucionado el problema donde al traducir campos de entrada que contenían URLs solo se traducían partes del contenido.

## 1.1.2

- Solución: El problema donde cambiar servicios de traducción no tenía efecto cuando la página aún no había sido traducida.
- Optimización: En el proceso de traducir Epub y PDF, si algún contenido falla en traducirse, ahora es posible cambiar a otro servicio de traducción en el panel sin reiniciar todo el proceso de traducción (la lógica anterior era usar inmediatamente un nuevo servicio de traducción para retraducir todo el libro). Esto significa que a mitad de la traducción, puedes cambiar a un servicio de traducción diferente y hacer clic en [Reintentar Todos los Párrafos Fallidos], después de lo cual el sistema continuará la traducción usando el nuevo servicio.
- Optimización: Ajustado el tamaño de fuente de los mensajes de error de traducción para mejorar la legibilidad.

## 1.1.1

- Solucionado el problema del atajo de subtítulos bilingües para YouTube que tenía texto en inglés excesivamente largo.

## 1.1.0

### Nuevas Características

- **Configuración de Teclas de Atajo**: Añadido un nuevo menú de nivel superior "Atajos" y las siguientes funciones de teclas de atajo personalizables:

  - Designar una combinación de teclas para traducir el contenido del cuadro de entrada actual, complementando el método anterior de presionar rápidamente la barra espaciadora tres veces.
  - Designar una combinación de teclas para habilitar temporalmente "traducción directa al pasar el ratón" en la página. Presionarlo nuevamente cancelará esta función.
  - Añadidas teclas de atajo dedicadas para 6 servicios de traducción (como DeepL, OpenAI, Google, Microsoft, Gemini, Tencent Interactive Translation) para facilitar el cambio temporal entre servicios de traducción.

- **Actualización de la Página de Configuración del Plugin**:

  - En "Configuraciones Avanzadas", se ha añadido una nueva opción para permitir a los usuarios especificar ciertas palabras (por ejemplo, "LLM") para ser excluidas de la traducción.
  - En "Configuraciones Avanzadas", se ha añadido una nueva opción para configurar el número mínimo de caracteres requeridos para traducir un párrafo. El valor predeterminado es 4 caracteres, pero se puede establecer más alto (por ejemplo, 20), de modo que solo se traduzcan párrafos más largos.
  - Añadido un tutorial para principiantes, que cubre configuraciones de bola flotante, configuraciones de subtítulos de video y configuraciones de pasar el ratón.

- **Subtítulos Bilingües de YouTube**: Añadido un acceso rápido en la ventana de reproducción de video de YouTube para habilitar o ocultar subtítulos bilingües (esta función se puede desactivar).

- **Soporte de Idioma de Deepl**: Añadido soporte para portugués (Brasil).

- **Guía para Nuevos Usuarios**: Cuando los nuevos usuarios abren por primera vez una página en un idioma no objetivo, se muestra una burbuja de guía de ayuda de bola flotante.

### Optimización y Correcciones

- **Optimización de la Interfaz de Usuario**: Rediseñada la interfaz de usuario para los mensajes de error de traducción de página para hacerlos más fáciles de entender. Cuando hay muchos errores, una ventana emergente activamente alertará al usuario.

- **Correcciones de Errores**:

  - Solucionado el problema donde la traducción al pasar el ratón fallaba cuando la página perdía el foco.
  - Solucionado el problema donde menos de 3 caracteres en la función de mejora del cuadro de entrada no se traducían.
  - Solucionado el problema donde algunos directorios no se traducían durante la producción de Epubs bilingües.

- **Eliminación de Características**: Eliminada la función de mejora de información bilingüe (mostrando resultados de búsqueda en inglés en páginas de búsqueda de Google simultáneamente).

### Otras Actualizaciones

- **Actualización de Configuración de openAI**: Ahora soporta configurar el número de configuraciones por segundo en decimales, como 0.5, lo que significa 1 solicitud cada 2 segundos.

## 0.12.14

- Solución: El problema de reconocimiento del idioma objetivo predeterminado en algunas máquinas después de la primera instalación.
- Optimización: El orden predeterminado de los títulos de las páginas web se cambia a [Chino - Inglés].

## 0.12.13

- Solucionado: Problema con la unión de traducciones de párrafos largos de OpenAI en algunos casos. [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- Optimizado: Al usar el ratón, el problema donde al perder el foco en la página y luego volver a activarlo se vuelve ineficaz.
- Solucionado: El problema donde la caché aún existía después de modificar el aviso/modelo en OpenAI.

## 0.12.12

- Actualizado: Optimizado el panel emergente, eliminando algunas opciones para el sitio web actual.
- Optimizado: Mejorado el proceso de fusión de subtítulos manuales.
- Optimizado: Configuración automática del idioma objetivo basado en el idioma del navegador.
- Añadido: Soporte de subtítulos bilingües para la plataforma de aprendizaje [ArtStation](https://www.artstation.com/learning) y [ZDF](https://www.zdf.de/).
- Corregido: Resuelto el problema donde los títulos en la página de lista de jstor no se traducían [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268).
- Corregido: Solucionado el problema donde solo parte del contenido desaparecía en Hacknews [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264).

## 0.12.11

- Añadido soporte de subtítulos bilingües para las plataformas [HBO Max](https://play.max.com/), [BBC](https://www.bbc.com/), [Disney+](https://www.disneyplus.com), [ARD Mediathek](https://www.ardmediathek.de/), [ITV](https://www.itv.com/), y [Domestika](https://www.domestika.org).

## 0.12.10

- Corregido el problema de autorización del dominio Gemini bajo el script de Tampermonkey.
- Soporte para traducción de subtítulos en tiempo real para Twitter Space.
- Para versiones anteriores del script de Tampermonkey, ahora se ha añadido un aviso de actualización en la página de configuración.

## 0.12.9

- Añadido soporte para traducción de Gemini.
- Corregido el problema donde las traducciones no respondían a tiempo cuando la página web se desplazaba a la posición media en algunos casos.
- Corregido el error donde el cambio de subtítulos en algunos sitios web de video causaba que la traducción se mostrara repetidamente.
- Corregido el problema donde el ratón se desplazaba para continuar traduciendo sin mantener presionada la tecla de acceso rápido en algunos casos.
- En macOS, optimizado el nombre de visualización del atajo del panel.

## 0.12.8

- Reparado que los subtítulos originales del video no se mostraban cuando "El sitio actual está configurado para nunca traducir".
- Reparado el conflicto con algunos complementos que causan un retorno infinito de la página.
- Reparado la no traducción de algunos párrafos después de activar los saltos de línea de párrafos largos.
- Corregido [Cuando se activa temporalmente la traducción de la página web durante un largo tiempo, al hacer clic en el panel [Siempre traducir este sitio web] no se cancela la traducción siempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- Subtítulos bilingües añadidos para soportar las plataformas [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) plataformas. https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/) plataformas.
- El hoverball ahora está oculto por defecto cuando el video está en pantalla completa.
- Corregido el problema de clics temblorosos del panel de acción hoverball de la página de Firefox.
- Soporte para colaboración bajo el sitio pubmed.ncbi.nlm.nih.gov y el complemento scholarscope.
- Corregido el problema de temblor de la página de traducción del cuadro de entrada de reddit.

## 0.12.6

- Corregido el problema de que la traducción de YouTube/Web of Science, etc. no es sensible al cambiar de pestañas.
- Hoverball en móvil ahora soporta operación de pulsación larga, pulsación corta para traducir, pulsación larga para abrir el panel.
- Traducir libros electrónicos bilingües ahora también traducirá el índice.
- La función de Mejora de Búsqueda (algunas páginas de Google Search muestran resultados de búsqueda bilingües) ahora no está habilitada por defecto y será eliminada en el próximo Release.

## 0.12.5

- Corregido el problema de que al crear eBooks desde el panel al hacer clic en traducciones no funcionaba.

## 0.12.4

- Cuando activas los subtítulos bilingües en el panel, primero se actualizará la página automáticamente (para mostrar subtítulos bilingües con más precisión), y algunos sitios aún requieren que los usuarios hagan clic manualmente en el botón "CC" en el sitio para activar los subtítulos.
- Optimizar Grease Monkey, detección de idioma de Safari.
- Proporciona acceso rápido a versiones bilingües de todos los artículos en el sitio de artículos de [Arxiv](https://arxiv.org/abs/1910.06709).
- [Soporte de hoverball configurado para estar fijado a la izquierda #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Corregir problema de visualización del Modo de Aprendizaje #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Activar temporalmente la traducción web durante un tiempo no cancela Siempre Traducir #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Optimizar problemas de inicialización de archivos PDF.

## 0.12.3

- Corrección para la función de [desactivar permanentemente subtítulos de video] que no funcionaba [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175).

## 0.12.2

- Se proporciona soporte de subtítulos bilingües para más plataformas de video, que ahora son compatibles: [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy](https://www.khanacademy.org/), [Coursera](https://www.coursera.org/), [Vimeo](https://vimeo.com/), [Nebula](https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), etc. (Tenga en cuenta que debido a las limitaciones técnicas, algunos sitios web necesitan actualizar la página después de activar los subtítulos bilingües por primera vez o esperar a que se complete la traducción para mostrar los subtítulos bilingües).
- Tamaño del plugin optimizado significativamente, reducido a la mitad en comparación con el original, descarga y actualización más rápida.
- Corregido problemas de descarga extendida de PDF.
- Añadido un portal de traducción rápida de PDF al lado derecho del sitio de artículos de [Arxiv](https://arxiv.org/abs/1910.06709), que lleva a una página HTML limpia (solo soportado por algunos artículos, ya que requiere que los autores originales envíen el código fuente, por lo que aproximadamente el 50% de los artículos mostrarán este portal).
- Las páginas PDF en línea sin extensión .pdf ahora pueden saltar directamente a la página de traducción de PDF al hacer clic en el hoverball en la página.
- Corregido algunos problemas de mejora del cuadro de entrada bajo Safari.
- Optimizar la detección de idioma en Grease Monkey y Safari.

## 0.11.6

- Añadido 11 nuevos idiomas de interfaz para el plugin y el sitio web oficial, ahora los idiomas de interfaz soportados alcanzan 14, incluyendo Chino Simplificado, Chino Tradicional, Inglés, Japonés, Coreano, Ruso, Español, Portugués, Hindi, Italiano, Alemán, Francés, Árabe y Persa.
- Modificar el compartir bilingüe (modo de actualización) añadido en la última versión a compartir instantáneas de página bilingüe, para que el contenido compartido sea más original, así como una mayor adaptabilidad.
- Corregido emoji al final del cuadro de entrada de Twitter que no se puede traducir.
- Corregido la situación donde el contenido de complementos de terceros se traduce en algunos escenarios.
- Reparado clic no responsivo del hoverball en línea de pdf.

## 0.11.5

- Ahora puedes generar un enlace público a la página bilingüe traducida para Immersive Translate.
  - [Haz clic](/docs/share/) en el Icono de Compartir de Immersive Translate para generarlo con un solo clic.
- Resuelto el problema de que algunas plataformas no podían reconocer si el ratón era compatible o no.
  - Hay algunos navegadores de escritorio que soportan tanto pantalla táctil como ratón, y Immersive Translates no puede detectar técnicamente si tales plataformas soportan ratón, por lo que hemos añadido la opción [Forzar Habilitar Soporte de Ratón] en la configuración de [Mouse Hover].

## 0.11.2-0.11.4

- Optimizar experiencia, corregir algunos errores.

## 0.11.1

- El modelo por defecto para traducciones de OpenAI es: GPT3.5-turbo-1106.
- Optimizado el Prompt en Chino para OpenAI, ahora menos propenso a alucinaciones.
- Reducida la longitud de los prompts de OpenAI de 90 a 40, ahorrando aún más tráfico.

## 0.11.0

- Corregido clics temblorosos del hoverball de la página.
- Corregido problemas de traducción de Azure.

## 0.10.9

- Corregido algunos problemas menores.

## 0.10.8

- Soporte para configurar botones de traducción rápida del hoverball (soporte tanto para PC/móvil).
- Optimización del juicio de idioma de Grease Monkey.
- Corregido traducción de archivos txt.

## 0.10.7

- Soporte de ratón hover presionar Ctrl de nuevo para mostrar texto original.
- Ignorar idioma de nunca traducir en Mouse Hover.
- Optimización de subtítulos bilingües de Youtube.

## 0.10.6

- Soporte de subtítulos de Youtube solo para traducciones.
- Añadir alerta de actualización de versión baja de Grease Monkey.
- Corregido el problema de que los archivos txt locales no se pueden traducir.

## 0.10.5

- Corregido que Youtube ocasionalmente regresa a la página de inicio.

## 0.10.4

- Corregido conflicto de subtítulos de Youtube con el plugin de subtítulos duales (la traducción de subtítulos de Youtube de Immersive Translate no está habilitada cuando se detecta el plugin dual de Youtube para evitar conflictos).
- Añadido [Función de Desactivar Permanentemente Subtítulos de Video], si hay otros problemas de conflicto y no deseas habilitar la función de subtítulos bilingües con Immersive Translate.
- Optimizar saltos de subtítulos.

## 0.10.3

- Corregido problema de traducción de clave de autenticación personalizada de DeppL.

## 0.10.3

- Soporte perfecto para videos de Youtube con subtítulos bilingües 🎉.
- Para páginas de artículos, el texto del cuerpo ahora se traducirá primero antes que el resto del contenido de la barra lateral.
- Optimizar la contextualización de la traducción de DeepL.
- Optimizar la traducción de archivos de subtítulos de OpenAI para la contextualización.

## 0.10.1

- Aumentar la prioridad de la traducción del cuerpo para optimizar la experiencia de traducción.
- Corregido problema de clic en más texto no traducido en ins.

## 0.9.8

- Optimizar experiencia, corregir algunos errores.

## 0.9.7

- Corregido auto-traducción cuando readwise está resaltado.

## 0.9.6

- Corregido limpiar la caché al cerrar sesión del usuario.

## 0.9.5

- Correcciones de errores de eBooks en línea.

## 0.9.4

- Optimizar la detección de mejora de entrada para reducir falsos toques.
- Traducción en línea de libros electrónicos y subtítulos.

## 0.9.3

- Traducción del cuadro de entrada: muestra un recordatorio emergente cuando se usa por primera vez, y el usuario puede elegir desactivarlo esta vez o permanentemente para evitar toques accidentales.
- Optimización de la velocidad de exportación de traducción solo en PDF, si eliges exportar solo la traducción, puedes llamar directamente a la vista previa del sistema PDF para exportar, más rápido.
- Deeplx admite múltiples URLs, solo sepáralas con .

## 0.9.2

- La herramienta de traducción de PDF se migra a la versión en línea: https://app.immersivetranslate.com/pdf/ , para que Grease Monkey y Safari puedan usar la traducción de PDF, y los problemas se puedan iterar mejor sin la necesidad de emitir una versión para resolver el problema.
- Optimización de la interfaz de usuario emergente, ¡el panel es más hermoso!

## 0.9.1

- Solucionar problemas de nombres de archivos con la creación de libros electrónicos Epub

## 0.8.8

- Soporte de pdf para ajustes de espaciado de líneas y palabras para volver a reconocer párrafos
- Solución de problemas de desplazamiento automático en la lectura en línea de epub en dispositivos móviles

## 0.8.7

- Soporte de pdf para descargas de traducción solamente
- Solucionar problema de inicio de sesión de Google en Safari

## 0.8.2 - 0.8.6

- Permite establecer el intervalo entre los disparadores de combinación de mejora de entrada
- Solucionar algunos errores

## 0.8.1

- Optimización de detección de idioma
- Funciones Beta: API personalizada (Beta habilitada en la configuración del desarrollador)
- Soporte para AliCloud Translation
- Solucionar algunos errores

## 0.8.0

- Sistemas de usuario compatibles
- Soporta [Habilitar Membresía Pro](/pricing), lo que permite a los usuarios disfrutar de traducciones de Deepl y OpenAI y configuraciones de sincronización en la nube.
- El servicio de traducción al pasar el ratón se puede configurar individualmente
- El servicio de traducción del cuadro de entrada se puede configurar por separado
- Optimización de traducción de PDF
- Solucionar algunos errores

## 0.7.16

- Traducción de PDF con nuevas opciones para un control rápido del estilo de traducción (los archivos PDF son muy extraños y activar estas opciones puede ser útil para algunos archivos PDF con formato desordenado)
- Las versiones de iOS y macOS están de vuelta en la Apple Store Country Store

## 0.7.15

- Hemos sido notificados por Apple de que las traducciones de OpenAI han sido eliminadas temporalmente de iOS y macOS, y estamos tratando de relanzarlas en China.

## 0.7.11- 0.7.14

- Solución: problema de Gmail Translate All Regions
- Desactivar temporalmente la función de exportación de PDF de Safari debido a la restricción de Safari en las descargas de complementos (error).
- Solucionar algunos otros problemas

## 0.7.10

- Actualización de la interfaz de usuario del panel de iconos del navegador emergente, un poco más de diseño ～
- Soluciona el problema de que algunos pasajes en japonés no se traducen.

## 0.7.9

- ¡Finalmente, el PDF admite la exportación de versiones bilingües! Puedes hacer clic en el botón [Guardar] para exportar el archivo PDF bilingüe traducido.
- Las reglas personalizadas ahora admiten la fusión con las reglas integradas predeterminadas, por ejemplo: `{"id": "youtube", "selectors.add":["#test"]}` significa agregar un `#test` a los selectores existentes, `selectors` significa anular el predeterminado, `selectors.remove` significa eliminar uno de los selectores predeterminados, y `selectors.remove` significa eliminar uno de los selectores predeterminados.
- Icono de Safari actualizado, un poco más grande.
- Otras correcciones de errores

## 0.7.8

- Correcciones de errores

## 0.7.7

- Adaptado al estilo del sistema de Safari, el icono de extensión de Safari cambió a contorno transparente.
- Agregar cambio de estado del icono del navegador, cuando una página web ha sido traducida, se agregará un ✅ en la esquina inferior derecha del icono del navegador automáticamente.
- Habilitar automáticamente la traducción de sitios web en inglés frecuentemente utilizados para nuevos usuarios
- Solucionar problemas de traducción con https://claude.ai/

## 0.7.6

- Soporte de traducción de resultados mejorados de entrada ctrl+z Deshacer
- Soporte de traducción en modo de lectura de documentos de Flying Book
- Adaptación https://pi.ai/talk

## 0.7.5

- Solucionar el problema de que el icono de Grease Monkey no se muestra
- Solucionar varios problemas

## 0.7.4

- Solucionar varios problemas
- La página de configuración admite la eliminación por lotes de URLs seleccionadas.
- Soporta habilitar/deshabilitar la traducción de subtítulos de Youtube para evitar conflictos con otros complementos relacionados.
- Arigato Translator admite la configuración de campos y terminología id

## 0.7.2

- Mejora del cuadro de entrada: permite omitir el prefijo // y activar la traducción de todo el cuadro de entrada con 3 espacios, o puedes desactivar esta opción en la página de configuración.

## 0.7.1

- Soporte de mejora de búsqueda, cuando está habilitado, cuando buscas en Google/Google News en chino, la columna derecha mostrará automáticamente los resultados de búsqueda de las palabras clave correspondientes en inglés, que está habilitado por defecto.
  - Razón: Descubrimos que en la búsqueda de Google, los resultados de búsqueda para palabras clave en chino y palabras clave en inglés pueden ser muy diferentes, con la mejora de búsqueda traducida inmersiva habilitada, buscamos automáticamente las mismas palabras clave en inglés para ti y las mostramos en el lado derecho. Puedes elegir desactivarlo si no necesitas la función.
  - Safari no es compatible debido a limitaciones de API.

## 0.6.20

- Modificar la configuración predeterminada: Debido a la gran cantidad de comentarios de los usuarios de que no usarán la herramienta de traducción después de la instalación, su expectativa de la herramienta de traducción es que traduzca automáticamente las páginas web en inglés después de la instalación, por lo que a partir de esta versión, para los usuarios chinos, la opción de traducir páginas en inglés por defecto se ha activado (si el usuario ha tenido una configuración previa del idioma que siempre se traducirá, entonces se respetará, y el cambio solo modifica la configuración inicial de la extensión), y si necesita cancelarse, se puede cancelar fácilmente en el [panel emergente o página de configuración](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91)

## 0.6.19

- Solucionar errores de PDF
- Solucionar error de web of science
- Adaptación feeder.com
- Solucionar que epub no traduzca algunos libros

## 0.6.18

- Solucionar problema de desbordamiento de ancho emergente de Safari.
- Optimización del proceso de construcción

## 0.6.17

- Optimizar alertas de error
- Optimizar la selección del idioma de destino, ahora solo mostrará los idiomas compatibles con el servicio de traducción correspondiente
- Optimización de traducción de PDF
- Adaptado para el sitio web de Good Reads, Amazon y South China Morning Post

## 0.6.16

- Agregar visualización de página sin permiso de PDF
- Reparar la visualización de párrafos de lista de texto de PDF
- Ampliar la escala de fuente pequeña de PDF en Chrome y Safari

## 0.6.15

- Reparar el problema de que al abrir archivos PDF, el panel de extensión indica que no hay permisos.
- Solucionar el problema de que la mejora del cuadro de entrada no está habilitada cuando el sitio está configurado para nunca traducir.

## 0.6.14

- Optimización de traducción de PDF, el área de traducción ahora se puede editar/arrastrar/eliminar
  - Arrastrar arriba a la izquierda, eliminar arriba a la derecha, cambiar tamaño abajo a la derecha
- Alineación a la izquierda del cuadro desplegable de Windows
- Soporte para chino tradicional y chino simplificado

## 0.6.13

- Solucionar el problema de traducción repetida al pasar el ratón
- Soporte de traducción de PDF para arrastrar para cambiar el tamaño y editar el contenido de la traducción

## 0.6.12

- Solucionar que las imágenes de traducción de Epub se hagan más pequeñas en algunos navegadores
- Optimización de traducción del cuadro de entrada, ¡ahora funciona sin problemas en Bard!

## 0.6.10

- El modelo predeterminado de OpenAI cambió a la versión 0613
- Solucionar algunos estilos de cuadros de entrada
- Más inteligente para determinar si es un área de navegación, y si es así, no se realiza la traducción
- Solucionar posibles ataques de inyección XSS

## 0.6.8

- El panel de extensión ahora puede indicar páginas no compatibles (por ejemplo, páginas sin permisos y páginas no HTML)
- Mejora del cuadro de entrada para mostrar el estado de carga en la traducción
- Actualizar colores de carga predeterminados en traducciones
- Cuando el cuadro de entrada está configurado sin prefijo, admite la traducción `ja Hello` al japonés y `English Hello` al inglés.

## 0.6.6

- Solución para: algunas áreas no se traducen (quora)

## 0.6.5

- Optimización de Google Bard
- La traducción del cuadro de entrada admite la traducción directa de todo el cuadro de texto sin prefijos.
- Optimizar el problema de las traducciones de OpenAI que agregan puntos sin sentido, (si no se detecta un punto en el texto original, si OpenAI devuelve un punto, entonces se elimina)
- Problemas con los archivos de subtítulos de Safari que no se reconocen

## 0.6.3

El idioma predeterminado para la traducción del cuadro de entrada ahora puede omitir el espacio, es decir, //Hello World también se puede traducir.

## 0.6.2

La mejora del cuadro de entrada más emocionante está aquí:

- Escribe: // Hello World en el cuadro de entrada en cualquier página web, luego haz triple clic en la barra espaciadora para traducir el párrafo al inglés
- También puedes especificar la traducción a un cierto idioma: /ja Hello World, luego haz triple clic en la barra espaciadora para traducir el párrafo al japonés

[Haz clic aquí para una introducción rápida de 30 segundos](/docs/input/)

## 0.6.0

- Primer lanzamiento en junio, migrado desde el subdominio personal anterior https://immersive-translate.owenyoung.com al nuevo dominio https://immersivetranslate.com/
- La funcionalidad es en gran medida la misma (¡nuevas características estarán disponibles en el próximo lanzamiento!)

## 0.5.17

- Solucionar el problema de que: los libros electrónicos bilingües no tienen imágenes después de exportar

## 0.5.16

- Solución: problema de traducción de OpenAI en chino tradicional

## 0.5.15

- Optimizar: El número mínimo de caracteres en un párrafo que activa la traducción se modificó a un mínimo de 4 caracteres para reducir la confusión, mientras se utilizan otras características para evitar traducir las áreas de navegación y finalización del sitio.
- Solución: detalles de Github no se traducen después de expandir.

## 0.5.14

- Solucionar el problema de que las imágenes en algunas páginas web de: se vuelven más grandes después de copiar
- Solución: sección de comentarios de medium no se traduce
- Solucionar el problema de que las imágenes en algunas páginas de: se copiaron incorrectamente

## 0.5.12

- Característica: El estilo de traducción de línea dividida agrega una línea dividida vertical para traducciones de una sola línea
- Solución: Casos muy raros de división de párrafos.
- Una gran página de orientación de configuración inicial para nuevos usuarios de iOS.

## 0.5.11

- Soporte de traducción de subtítulos para exportar solo traducciones
- Solución: Algunos elementos no son reconocidos al pasar el ratón
- Solución: los saltos de línea de tweet no se reconocen parcialmente
- Solución: el estilo de creación de libros electrónicos no funciona

## 0.5.10

- Solución: los saltos de línea de tweet no se reconocen
- Solución: la página de detalles de Reddit devuelve algunos párrafos que no se pueden traducir
- Solucionar un problema con: donde algunas de las etiquetas de código no se reconocieron correctamente.

## 0.5.9

- Corrige los saltos de párrafo en algunos casos en:
- Corrección: Tampermonkey Toggle solo muestra traducciones
- Corrección: Problema de estilo de lectura en línea de eBook no funciona

## 0.5.8

- Corrige el problema de que: la configuración temporal de la duración de la traducción del sitio web no surte efecto.

## 0.5.7

- ¡Super actualización!

- ¡La función Mostrar solo traducciones está aquí! Haz clic en [Más] -> [Cambiar para mostrar solo traducciones].

  - Soporte para atajos personalizados, configurados en configuración de interfaz -> Configuración de atajos

- Optimiza el problema de limitación de frecuencia de solicitudes de OpenAI

- ChatGPT por defecto usa el modelo móvil, ¡que es más rápido!

- Reestructuración del análisis del núcleo web, lo que significa:

  - Traducción de páginas web a gran escala en segundos
    - Por ejemplo: https://pve.proxmox.com/pve-docs/pve-admin-guide.html, que antes tomaba 30 segundos, ahora se traduce en segundos.
  - Uso de memoria ultra bajo para páginas web complejas
    - Por ejemplo: https://www\.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1
  - Adaptación a más sitios web

- Se admiten todas las traducciones del sitio web de ShadowRoot.

  - Por ejemplo: https://bugs.chromium.org/p/chromium/issues/detail?id=418987
  - Por ejemplo, la sección de comentarios de: https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html

- Corrige el problema de pantalla blanca después de la traducción de sitios web con hidratación como Next.js.

  - Por ejemplo: https://webpack.js.org/

- Se corrigió el problema de que modificar el atajo de desplazamiento del ratón requería actualizar la página para surtir efecto

- Se corrigió un problema con el reconocimiento de saltos de línea en archivos TXT.

- ¡Muchas actualizaciones!

- ¡La función 'Mostrar solo traducción' ha llegado! Haz clic en 'Más' -> 'Cambiar para mostrar solo traducciones'.

  - Soporta atajos personalizados, que se pueden configurar en 'Configuración de interfaz' -> 'Configuración de atajos'

- Optimizado para el problema de límite de tasa de solicitudes de OpenAI

- El análisis del núcleo web ha sido reconstruido, lo que significa.

  - Traducción instantánea para sitios web grandes
  - Uso mínimo de memoria para páginas web complejas
  - Mejor compatibilidad con más sitios web

- Ahora se admiten traducciones para todos los sitios web con ShadowRoot.

- Se corrigió el problema de pantalla blanca después de traducir sitios web con hidratación, como Next.js

- Se corrigió el problema donde cambiar el atajo de desplazamiento del ratón requería una actualización de la página para surtir efecto

- Se corrigió el problema con el reconocimiento de saltos de línea en archivos TXT.

## 0.5.6

- Corrección: problema de ventana emergente de nueva pestaña en macOS.
- Función: Nueva página de guía para nuevos usuarios.

## 0.5.5

- Corrección: problema de área de desplazamiento del ratón.

## 0.5.4

- Corrección: Página Spa duplicada

## 0.5.3

- Corrección: oyente de tecla de acceso rápido de desplazamiento del ratón.
- Corrección: traducción de documentos PDF
- Función: Añadir nueva página de guía para clientes

## 0.5.2

- Corrección: configuración de atajos de desplazamiento del ratón en userscript

## 0.5.1

- Corrección: OpenAI API no funciona.

## 0.5.0

- Función: Traducir el párrafo actual cuando se desplaza el ratón.
- Función: Reestructuración de la traducción de PDF, ahora puedes traducir la mayoría de los PDFs con Immersive Translate
- Corrección: Desactivar el menú contextual no funciona [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- Corrección: Evitar la política de seguridad de contenido para [Mastondon](https://mastodon.social/)

## 0.4.11

- Corrección: permiso de userscript (solo para userscript).

## 0.4.8

- Función: Bing Translate a Microsoft Translate para una calidad más estable.
- Corrección: Página web TXT pura como [esta](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- Rendimiento: Excluir algunas páginas de publicidad secundaria en el sitio web, y el rendimiento ha mejorado un poco

## 0.4.7

- Corrección: Falta de ventana emergente de Userscript en Firefox.

## 0.4.6

- Función: Permitir que terceros envíen eventos de documentos para llamar a `toggleTranslatePage`
- Función: La aplicación iOS añade botón de habilitar extensión y enlace a comunidades
- UI: El modelo de campo de configuración de OpenAI usa selección en lugar de cuadro de entrada de texto.

## 0.4.5

- Corrección: problema de extensión de safari en iOS 15.0.
- Corrección: atajos de extensión de safari en macOS
- Corrección: política de seguridad de contenido emergente para extensión, y parcialmente para userscript.

## 0.4.4

- Tarea: Eliminar console.log

## 0.4.3

- Corrección: detección de espacios en blanco en etiquetas sup, sub.
- Función: soporte para ChatGPT Plus Website como servicio de traducción, esta es una función beta, por lo que puedes acceder a ella habilitando la función beta en la configuración de desarrollador. Esto es muy lento, porque chatgpt solo puede enviar una solicitud a la vez. Asegúrate de tener una cuenta de ChatGPT Plus, porque hay más limitaciones en la cuenta gratuita, y no estoy seguro si esto representa un riesgo para tu cuenta, ten cuidado de usarlo.

## 0.4.1

- Corrección: el menú contextual de Firefox desaparece después de reiniciar.
- Soporte para Azure openai

## 0.4.0

- Función: Soporte para traducir archivo de subtítulos local (.srt,.ass,etc.)

## 0.3.17

- Función: Soporte para traducir archivo .txt local.
- Corrección: El menú contextual puede no estar disponible a veces. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Corrección: mantener &nbsp; como espacio en blanco.
- Eliminación: Retirar Papago, ya que [el servicio está caído](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI: permitir no tener clave API para openai
- UI: permitir restablecer Open AI a la configuración predeterminada

## 0.3.14

- Dependencia: Actualizar pdf.js a la última versión
- Corrección: color de fondo de selección de pdf
- Corrección: detección de espacios en blanco

## 0.3.13

- Corrección: problema de caracteres específicos del constructor de ebook, como algunas rutas de capítulos son `xxx' xxxx`.
- UI: plegar opciones personalizadas de openai por defecto.
- UI: Añadir estado de exportación para exportación de epub.
- Corrección: Gpt4 prompt predeterminado

## 0.3.12

- Función: Ahora podemos personalizar el color de fondo del tema de traducción de marcador.
- Corrección: postMessage cuando la página de inicio rompía algunos sitios, ahora solo lo haremos cuando realmente traduzcamos páginas
- Corrección: problema de progreso de ebook.
- Corrección: mejor para dividir párrafos largos, 1.5 mil millones, 25.5%, Sr. no se considerará como un límite

## 0.3.11

- Corrección: color de texto en modo oscuro del lector de ebook
- Corrección: prompt de openAI

## 0.3.10

- Mejor: detectar contenedor japonés/coreano.
- Corrección: Progreso del Constructor de Ebook detenido al 99%.

## 0.3.9

- Corrección: el estado de entrada de servicios de traducción de interruptor de UI de opciones no cambió.

## 0.3.8

- UI: color de carga más transparente
- Corrección: Detectar idioma de Ebook.
- Función: Añadir progreso de traducción para el constructor de ebook, y un hermoso confeti después del éxito.
- Función: Añadir reintento de todos los párrafos fallidos para el botón de reintento.
- Corrección: Manejo de errores de Deepl

## 0.3.7

- Corrección: el lector de ebook no puede cargar imágenes en Chrome.

## 0.3.6

- UI: mejor para hacer la UI de la página de ebook

## 0.3.5

- Corrección: exportación de ebook de userscript
- Función: añadir punto final de API personalizado para OpenAI
- Función: añadir opciones de tiempo de traducción temporal del sitio web en `Configuración avanzada`

## 0.3.4

- CI: Construcción fallida

## 0.3.3

- Corrección: creador de ebook para Kindle
- Cambio: color del icono de carga, de negro a azul, para adaptar la página web en modo oscuro.
- Función: Soporte para traducción de html local para extensión

## 0.3.2

- Corrección: movimiento del cursor de entrada del formulario de opciones.
- Función: OpenAI soporta apiUrl personalizado para configuración de desarrollador.

## 0.3.1

- Función: actualizar icono oscuro a transparencia.
- Corrección: Orden incorrecto para párrafo largo

## 0.3.0

- Versión: A partir de ahora, cambiaremos el número de versión menor una vez al mes, por ejemplo, ahora en marzo, la versión comenzará desde 0.3.0, en abril, el número de versión comenzará desde 0.3.0, en abril, el número de versión comenzará desde 0.4.0, el próximo abril, el número de versión será 1.4.0, y así sucesivamente. Esto se debe a que no tiene sentido que las extensiones sigan Esto se debe a que no tiene sentido que las extensiones sigan la semántica, pero estandarizar los números de versión según las leyes del tiempo es una motivación para el desarrollo para seguir actualizando, y para que los usuarios encuentren problemas más fácilmente.
- Función: Soporte para icono oscuro para firefox

## 0.2.86

- Añadir opción de longitud máxima de texto por solicitud con Open AI
- Corrección: identificador de ebook duplicado
- Función: Soporte para traducción de página web txt

## 0.2.85

- Corrección: algunos archivos epub no se pueden encontrar.

## 0.2.84

- Función: Soporte para Lector y Creador de Ebook

## 0.2.83

- Función: Permitir que el formulario de entrada de contraseña muestre la contraseña.

## 0.2.82

- Corrección: Algunos sitios usan `span` para estilos, por lo que usamos `font` en lugar de span para el contenedor de objetivo de traducción
- Corrección: límite máximo de tokens de OpenAI, cambiar caracteres máximos de 1500 a 1300.

## 0.2.81

- Corrección: m.youtube.com
- Corrección: formulario de opciones UI
- Corrección: prompt de Open AI
- Función: Soporte para múltiples claves de OpenAI, usa `,` para separarlas.

## 0.2.80

- Función: Añadir menú de habilitar/deshabilitar para ventana emergente -> más
- Corrección: conflicto de mensaje de DingTalk

## 0.2.79

- Corrección: Open AI para párrafo de espacio

## 0.2.78

- Función: soporte para OpenAI CHATGPT 3.5 (soporta interfaz OpenAI ChatGPT 3.5)
- Función: Añadir nuevo tema Borde Sólido (新增新主题，实线边框)

## 0.2.77

- Arreglo: error de múltiples etiquetas de código. [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Arreglo: error de múltiples etiquetas de código [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Función: Soporte para contar texto de traducción inmediata personalizada para diferentes servicios de traducción.

## 0.2.74

- Función: Soporte para Tencent (alpha)
- Arreglo: traducción de openai
- Arreglo: verificación de etiquetas desconocidas en línea

## 0.2.73

- Función: Soporte para Tema de Traducción Gris
- Arreglo: Página de Tendencias de Github

## 0.2.72

- Arreglo: problema de red de verificación del servicio de traducción en Firefox móvil.

## 0.2.71

- Arreglo: permiso de userscript de Open AI

## 0.2.70

- Arreglo: marcador de posición de Open AI

## 0.2.69

- Función: Soporte para Open AI como servicio de traducción.
- Función: Soporte para verificar el servicio de traducción en options.html
- Función: Soporte para marco principal personalizado ya que algunos sitios no usan body como marco principal

## 0.2.68

- Soporte para Caiyun (Alpha)
- Arreglo: etiquetas de bloque desconocidas

## 0.2.67

- Función: Añadir `<all>` para traducir siempre idiomas, ahora puedes usarlo para traducir todos los idiomas excepto el idioma objetivo, y nunca traducir idiomas
- Arreglo: Permitir configurar API de Google personalizada
- Mejor: Soporte gratuito de Deepl
- Arreglo: alto uso de memoria para userscripts y extensión (eliminando opencc zh-CN a zh-TW, en su lugar con Google translate)
- Arreglo: Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Arreglo: configuración de traducción de Azure pero aún muestra (necesita configuración)

## 0.2.66

- Arreglo: fallo en la traducción de archivos PDF, error desde 0.2.60 por soportar deepl de zh-CN a zh-TW

## 0.2.65

- Soporte para solicitud de limitación para múltiples marcos
- No traducir el título de la página cuando está en iframe

## 0.2.64

- Arreglo: elegir servicios de traducción de openl
- Función: Soporte para la opción de traducir título

## 0.2.63

- Función: Soporte para el Servicio de Traducción de Azure
- Función: Soporte para el Servicio de Traducción de Papago
- Arreglo: sincronización nativa de Google Drive en Firefox Android.
- Arreglo: cambiar la transparencia de 0.4 a 0.618 [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Arreglo: consejos de atajos emergentes
- Rendimiento: solicitudes de serie a concurrencia
- Mejor para detectar conteo japonés

## 0.2.62

- Función: Añadir regla de waitForSelectors, para arreglar algunos sitios como reddit

## 0.2.61

- Arreglo: userscript es demasiado grande para greasy fork
- Mejor: reducir el tamaño del archivo

## 0.2.60

- Función: Soporte para zh-CN a zh-TW para Deepl
- Función: Característica de Deepl de Immersive Translate
- Función: Soporte para zoom de tamaño de fuente personalizado
- Arreglo: estilo del foro de Steam
- Arreglo: estilo global no cambiado después de generar elementos dinámicos
- Arreglo: promover prioridad de exclusión
- UI: cambio de página sobre
- Arreglo: algunos elementos matemáticos permanecen originales

## 0.2.59

- Arreglo: Elemento de Bloque de Etiquetas Desconocidas
- Arreglo: elemento translate=no anula
- Arreglo: coincidencia de URL con múltiples \*

## 0.2.58

- Función: Soporte para color de texto de traducción personalizado, color de borde.

## 0.2.57

- Sin cambios, reconstruir

## 0.2.56

- Arreglo de traducción duplicada para elementos en línea con elemento de código.
- Arreglo de verificación de etiquetas desconocidas en línea/bloque
- Función: soporte para css inyectado en el tablero de desarrolladores
- Función: recortar authKey, appid appSecret
- Mejor: abrir página de configuración en nueva pestaña (pero no para Stay)

## 0.2.55

- Intentar arreglar el charset de la API de deepl

## 0.2.54

- Eliminar permiso de pestañas para rechazo de tienda de Chrome
- Arreglo de traducción de toda la página, el pie de página se ignora
- Añadir notas a la página sobre
- Soporte para URL personalizada desde Configuración incorporada

## 0.2.53

- Arreglo de error de sincronización de Google Drive en userscript.

## 0.2.52

### Código

- Usar la última versión de esbuild
- Usar la última versión de deno
- CI: enviar código fuente a Firefox

## 0.2.51

- Arreglo de necesidad de inicio de sesión de Google Auth en Chrome/Firefox
- Reemplazar enlaces de servicio de traducción
- Mejor para permiso.
- eliminar minify.

## 0.2.50

- Arreglo de problema de carga de Google Drive (realmente) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Eliminar atajos alt+d, alt+s porque pueden entrar en conflicto con atajos nativos.
- Arreglo de problema de carga de Google Drive [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Mejor para la velocidad, añadiendo minLength a 50 para detectar el idioma.
- Arreglo de validación de token de Google Drive.

## 0.2.47

- Arreglo de la API de deepl

## 0.2.46

- arreglar marca de bloque

## 0.2.45

- Arreglo de innerText de elemento indefinido
- Arreglo de idioma fuente indefinido en traducción de caiyun

## 0.2.44

- Arreglo de alternar máscara de userscript
- Arreglo de lógica de alternar máscara

## 0.2.43

- Arreglo de alternar máscara de userscript con evento táctil.
- Arreglo de velocidad (eliminando sleep(300))

## 0.2.42

- Arreglo de hover de máscara al alternar máscara de nuevo.
- Añadir atajos de máscara para móvil
- Arreglo de problema de sincronización en la nube de userscript
- Mover página de opción avanzada al menú de la izquierda.
- Añadir lógica de reintento al servicio de traducción

## 0.2.41

- Arreglo de traducción de niu en userscript
- Arreglo de traducción de xhtml

## 0.2.40

- Arreglo de mostrar característica beta
- Arreglo de página de configuración emergente en nueva pestaña
- Arreglo de reemplazo de marcador de posición de traducción

## 0.2.39

- Soporte para atajos para mostrar traducción de máscara
- Soporte para habilitar característica beta en el panel de desarrolladores
- Arreglo de atajos en extensión móvil

## 0.2.38

- Soporte para tema de carga
- Arreglo de getpocket.com
- Arreglo de pie de página para área de cuerpo
- Arreglo de icono de importación/exportación

## 0.2.37

- Arreglo de marca de exclusión de marco

## 0.2.36

- Soporte para sincronizar con Google Drive

## 0.2.35

- Arreglo de ignorar etiqueta rb, rt en japonés.
- Mejor para más UI emergente
- Mejor para consejos de userscript malos
- Añadir contribución a la página sobre
- Arreglo de volc translate para detección automática de idioma

## 0.2.34

- Arreglo de velocidad de múltiples idiomas

## 0.2.33

- Soporte para modo de escritura vertical, como el japonés.
- Añadir 3 temas
- Añadir servicio de traducción de Niu

## 0.2.32

- Arreglo de traducción básica de PDF
- Arreglo de selección emergente de un servicio no configurado, ir a la página de opciones.
- Arreglo de mantener abierta la configuración.
- Arreglo de velocidad de detección de múltiples idiomas

## 0.2.31

- Arreglo de inyección de css en iframe dinámico

## 0.2.30

- Soporte para traducción de iframe en línea de userscript.
- Soporte para traducción de shadowroot. Por ejemplo:
  https://www\.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Área de conversación.
- también verificar regla de sincronización en emergente

## 0.2.29

- Arreglo de traducción de Facebook
- Soporte para mostrar opción de menú contextual.

## 0.2.28

- Eliminar coincidencia no estándar para userscript

## 0.2.27

- Soporte para traducción de iframe en línea. (Solo para extensión, no disponible para
  userscript)
- Arreglo de traducción de múltiples idiomas

## 0.2.26

- Arreglo de addon de Firefox Android
- Añadir configuraciones avanzadas para nueva línea de traducción

## 0.2.25

- Soporte para traducir iframe, como correo de QQ, tweet incrustado.

## 0.2.24

- Añadir sitio de traducción temporal por un tiempo
- Arreglo de API de navegador de userscript de stay.app
- Arreglo de página de opciones de stay.app

## 0.2.23

- Arreglo de traducción de página de múltiples idiomas

## 0.2.22

- Arreglo de compilación de userscript

## 0.2.21

- Arreglo de traducción de PDF en línea de Firefox

## 0.2.20

- Arreglo de problema de solicitud de macaco
- Arreglo de altura de línea de resaltado de marca

## 0.2.19

- Arreglo de japonés inteligente de tencent
- Arreglo de navegador mundial de haikuo

## 0.2.18

- Arreglo de cambio de URL de cliente, auto mantener el estado de traducción.
- Eliminar contenedor lateral como contenedor de traducción.
- Refactorizar posición emergente.

## 0.2.17

- Cambiar resaltado a marca
- Añadir tema de traducción resaltado

## 0.2.16

- Compatibilidad con Macaque

## 0.2.15

- Arreglo de problema de rebote táctil

## 0.2.14

- Arreglo de que globalThis.GM no funciona en Safari

## 0.2.13

- Soporte para arrastrar emergente de Userscript
- Soporte para Tres Dedos en dispositivo táctil para activar alternar páginas de traducción
- Soporte para ocultar el icono emergente de userscript.

## 0.2.12

- Mejor para inoreader

## 0.2.11

- Arreglo
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  Annas archive El contenido principal de la página no se pudo traducir

## 0.2.10

- Arreglo de distancia de altura de línea de PDF

## 0.2.9

- Arreglo de marca de elementos excluidos
- Arreglo de verificación de tipo de deno
- eliminar importmap
- Arreglo de traducción de menús contextuales
- restaurar página cuando nunca traducir este sitio está habilitado
- Añadir descripción para añadir URL

## 0.2.8

- Detectar el idioma del agente de usuario para el idioma de la interfaz
- Arreglo de error de salto de línea.

## 0.2.7

- Arreglo de solicitud de grease monkey

## 0.2.6

- Arreglo
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  problema de coincidencia de URL de archivo

## 0.2.5

- aumentar versión para prueba de ci

## 0.2.4

- capturar error de conexión de mensaje para emergente.

## 0.2.3

- Arreglar
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  crear contexto múltiples veces

## 0.2.2

- Arreglar archivo de muestra PDF
- Arreglar archivo local PDF en Firefox
- Arreglar atajos de PDF

## 0.2.1

- Soporte para el administrador de atajos de Grease Monkey.
- Arreglar coincidencia de regex
- Arreglar comentarios de YouTube.
- Arreglar versión compacta móvil de Reddit
- Arreglar problema de traducción de texto completo

## 0.2.0

- Arreglar PDF de dos columnas.
- Arreglar error de versión de Chrome/Edge Store.
- Arreglar
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Publicar en el complemento de Firefox
- Publicar en Edge
- Arreglar margen de PDF.
- Cambiar archivo de muestra PDF

## 0.0.62

- Arreglar formato de PDF, sangría.
- Arreglar cambio de elemento preventivo en telegra.ph

## 0.0.61

- Arreglar cierre de elemento span.
- Arreglar permiso para navegador temprano

## 0.0.60

- Arreglar PDF de Chrome

## 0.0.59

- Soporte inicial para PDF

## 0.0.58

- Editar descripción del tema de traducción

## 0.0.57

- Cambiar interfaz de usuario emergente, para un uso más fácil

## 0.0.56

- Arreglar tiempo de espera de Chrome
- Arreglar error de división de oraciones.

## 0.0.55

- Arreglar visualización de elementos ocultos.
- Refactorizar marca de elemento

## 0.0.54

- Soporte para salto de línea para X caracteres.

## 0.0.53

- Usar sendMessage en lugar de connect, porque Chrome desconectará el puerto después de
  5 minutos
- Mejor para detectar contenedores de texto

## 0.0.52

- No traducir el párrafo que solo tiene elementos de marcador de posición, por
  [ejemplo](https://github.com/nank1ro/solidart), la primera línea.
- Mejor para detectar elementos secundarios.

## 0.0.51

- Arreglar problema de caché
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive-translate/next-immersive-translate/issues/7)
- Arreglar tamaño de fuente de la interfaz de usuario de opciones

## 0.0.50

- Arreglar traducción de imagen bloqueada.

## 0.0.49

- Arreglar extensión de Firefox

## 0.0.48

- Arreglar extensión de Chrome

## 0.0.47

- Reescribir mensaje con fondo, usar connect en lugar de sendMessage
- Agregar soporte móvil de Reddit
- Arreglar espacio en blanco previo para algunos artículos

## 0.0.46

- Formatear información meta de userscript

## 0.0.45

- Userscript usa un archivo.
- Agregar tiempo de espera para solicitud de caché

## 0.0.44

- Arreglar error de división de Tencent.
- Arreglar error de elemento sup en línea.
- Mejor para Twitter

## 0.0.43

- Arreglar tweet br
- Arreglar traducción global.

## 0.0.42

- Arreglar etiqueta BR
- Tratar etiquetas de bloque con reglas

## 0.0.41

- Arreglar verificación de elemento en línea
- Agregar opción de registro de depuración para desarrolladores

## 0.0.39

- Arreglar servicio de traducción que contiene mock2

## 0.0.38

- Soporte para resultado de caché para userscript
- Agregar interfaz de usuario de opciones
- Soporte para detectar más contenedores de contenido

## 0.0.37

- Arreglar cambio de servicio de traducción emergente que no funciona
- Arreglar traducción de contenido de publicación móvil de Reddit.

## 0.0.36

- Arreglar carácter especial de Wikipedia
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Arreglar tamaño de icono de userscript.
- Habilitar todos los sitios para detectar el idioma del párrafo.

## 0.0.35

- Arreglar YouTube para ir a la siguiente página
- Soporte para página de búsqueda de YouTube.
- Arreglar interruptor avanzado de opciones.
- Arreglar etiqueta img, etiqueta oculta
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Arreglar actualización forzada de búsqueda de Google
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Soporte para resultado de tabla de Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Arreglar espacio en blanco de Wikipedia
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Cambios Importantes

- La tecla de acceso rápido predeterminada para alternar la traducción se ha cambiado a `alt+A`, porque
  es la tecla más conveniente para escribir.

### Otros

- Soporte para establecer modo de traducción inmediata, para que puedas dejar que la página web se traduzca
  lo más rápido posible.
- Soporte para establecer el área de la página que necesita traducirse, para que puedas traducir más área.
- Soporte para establecer la primera cantidad de texto x para traducir inmediatamente.
- Arreglar traducción duplicada al cambiar la traducción
- Mejor interfaz de usuario emergente

## 0.0.33

- Soporte para más idiomas, zh-TW, en

## 0.0.32

- Arreglar traducción de archivo local después de guardado. Arreglado
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Agregar archivo js dist al repositorio público

## 0.0.31

- Soporte para traducir toda la página
- Soporte para traducir página inmediatamente
- Más interfaz de usuario de configuración
- Reflejar el tema
- Agregar nuevo icono
- Agregar nuevo tema de traducción dashedBorder

## 0.0.30

- Mejor para tema dashed

## 0.0.29

- Arreglar párrafo válido.
- Agregar tema dotted, thinDashed
- Mejor para tema dashed, highlight

## 0.0.28

- Arreglar subrayado
- Agregar tema dashed, paper
- Arreglar detección de encabezado

## 0.0.27

- Soporte para translationTheme

## 0.0.26

- Arreglar permiso de conexión de userscript volc alpha.
- Arreglar versión clicable.

## 0.0.25

- Soporte para selectorMatches, para que podamos coincidir con todo manstondon ahora.
- Arreglar error de userscript de Firefox.

## 0.0.23

- Mejor para detección de chino
- Arreglar problema de innerText de Reddit

## 0.0.22

- Soporte para deeplx
- Arreglar traducción múltiple al cambiar de servicio

## 0.0.21

- Arreglar algunos elementos span que son elementos de bloque

## 0.0.20

- Soporte para no traducir etiquetas hash como #hash, etiquetas at como @xxx, $tag, como $APPL
- Soporte para elemento de bloque

## 0.0.18

- Soporte para deepl, bing, baidu, youdao, volc, openl, caiyun.

## 0.0.13

- Soporte para userscript

## 0.0.4.8

- Arreglar orden de código.
- Soporte para interfaz de usuario emergente básica

## 0.0.4.6

- Soporte para verificar nueva versión

## 0.0.3

- Soporte para archivos locales

## 0.0.2

- Soporte para elementos dinámicos
- Soporte para traducción visible
