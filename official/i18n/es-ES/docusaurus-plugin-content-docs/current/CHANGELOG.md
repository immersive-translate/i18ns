---
sidebar_position: 6
---

# Registro de cambios

## 1.12.3 (2024-12-13)

- Añadido: La **Traducción Consciente del Contexto con IA** puede mejorar la precisión de la traducción de contenido profesional. (Disponible solo para miembros Pro) **Opciones** -> **General** -> **Habilitar Traducción Consciente del Contexto con IA**
- Corrección: Algunos errores en el efecto de traducción multilínea en Twitter.
- Corrección: Problemas con la traducción de ciertas fórmulas debido al texto enriquecido
- Mejora: Al traducir en **x.com**, los videos con subtítulos tendrán automáticamente subtítulos bilingües traducidos.
- Mejora: Los videos sin subtítulos mostrarán un icono de traducción y proporcionarán una razón por la que no es posible la traducción.

## 1.11.7 (2024-11-25)

- Añadido: Bing/Google ahora soporta Khmer (Camboyano).
- Añadido: Permitir que los archivos ePub incompletos continúen la traducción desde donde se quedaron al reimportarlos.
- Corrección: Problema con la traducción de imágenes de Twitter en el navegador Safari.
- Corrección: Las teclas de acceso rápido se vuelven inefectivas al activar o desactivar la función de **Traducción al Pasar el Ratón**.
- Mejora: Mejorada la visualización de traducción bilingüe multilínea en Twitter y Youtube.
- Mejora: La traducción de texto enriquecido está desactivada por defecto en modo bilingüe para mejorar la calidad de la traducción.
- ~~Mejora: Añadida la opción para personalizar la "**Traducción de Barra Lateral y Barra de Navegación**" en "**Configuración Avanzada**".~~
- Mejora: Las imágenes ya no se traducen en el modo "**Pasar el Ratón - traducir inmediatamente este párrafo**".

## 1.11.4 (2024-11-16)

- Corrección: Problema con la traducción de fórmulas causado por la "Mejora de traducción de Twitter" en la versión 1.11.2.

## 1.11.2 (2024-11-13)

- Corrección: Problema donde el contenido desaparece después de hacer clic en "ver más" en el modo de solo traducción de Facebook.
- ~~Mejora: Mejorada la visualización de traducciones bilingües multilínea en Twitter.~~
- Mejora: Actualizada la interfaz de usuario de la lista desplegable de servicios de traducción en el panel.

## 1.11.1 (2024-11-05)

- Añadido: La **Traducción de Subtítulos** para reuniones en tiempo real ahora soporta activación vía "bola flotante", disponible en Zoom, Google Meet y Microsoft Teams.
- Corrección: Problemas de sincronización de subtítulos en YouTube después de ver anuncios.
- Corrección: Problemas de visualización del menú de traducción con clic derecho en Safari en MacOS 15.
- Corrección: Problemas con la funcionalidad Ctrl+Z para deshacer en la **Mejora de entrada** en ciertos sitios web.

## 1.10.6 (2024-10-25)

- Corrección: Problema con las teclas de acceso rápido de **Mejora de entrada** que no se activaban
- Mejora: Reducción del tamaño del paquete de instalación
- Mejora: Solución de visualización de subtítulos de Netflix

## 1.10.5 (2024-10-23)

- Añadido: Mostrar advertencia cuando el idioma de origen y destino son el mismo
- Corrección: Problema de traducción de caracteres en blanco en texto enriquecido [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175)
- Mejora: Mejora de entrada y funcionalidad de pasar el ratón dentro de iframes incrustados en páginas web

## 1.10.2 (2024-10-11)

- Añadido: Traducción de imágenes (versión Beta)
- Añadido: Modo Solo Ratón (habilitar esta función solo si la función de pasar el ratón no está disponible en dispositivos tablet) **Configuración** -> **Configuración Avanzada** -> **Habilitar Modo Solo Ratón**
- Añadido: Mostrar mensaje de error cuando falla la traducción de subtítulos de video
- Corrección: Problema de traducción de texto enriquecido [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163)
- Mejora: Abordados problemas donde el botón de traducción podría no funcionar durante la traducción de PDF
- Mejora: Mejorado el renderizado de fórmulas traducidas
- Mejora: Lista de selección de idiomas

## 1.9.8 (2024-09-28)

- Añadido: Servicio de traducción "Zhipu BigModel"
- Eliminado: Modelo "SiliconCloud" qwen1.5-7B-chat (debido a la discontinuación oficial)
- Corrección: Resuelto problema de compatibilidad de inicio de sesión con el plugin de Safari en macOS 15

## 1.9.7 (2024-09-20)

- Soporte de entrada mejorada para campos de entrada de Baidu, Gmail y otros
- Soporte para el encabezado de solicitud anthropic-dangerous-direct-browser-access para Claude Anthropic API
- Soporte para descargar subtítulos de videos de Hulu, Bloomberg y Domestika
- DeepX soporta traducción de texto enriquecido
- Corregido el problema de no sincronización de expertos AI personalizados

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) soporta copia de fórmulas (haz clic derecho en la fórmula para ver el menú de copia)
- Corregido el problema de visualización de subtítulos bilingües para múltiples videos en la misma página de Twitter
- Corregidos algunos errores

## 1.9.3 (2024-09-05)

- La opción para comparación bilingüe/mostrar solo traducción se ha movido a configuración general
- Por defecto, el sistema recordará el modo alternado haciendo clic en el icono en el panel para comparación bilingüe o mostrar solo traducción. Para cambiar temporalmente, haz clic en "Más" -> "Cambiar a mostrar solo traducción" en el panel
- Por defecto, la traducción de Chino Simplificado a Tradicional y viceversa usará el modo de solo traducción, en lugar del modo de comparación bilingüe
- Corregidos algunos errores

## 1.9.1 (2024-09-03)

- Soporte para configurar excepciones de idiomas y sitios web en modo de comparación bilingüe o solo traducción (configurar en página de Configuración -> Configuración Avanzada). Por ejemplo: Si tu modo de traducción predeterminado es comparación bilingüe, pero no deseas usar comparación bilingüe para Chino Tradicional, entonces puedes agregar Chino Tradicional a los idiomas de excepción para comparación bilingüe, así el Chino Tradicional usará el modo de solo traducción. De manera similar, si tu modo de traducción predeterminado es solo traducción, pero deseas que cierto idioma o sitio web use el modo de comparación bilingüe, también puedes agregar ese idioma o sitio web a los idiomas de excepción
- Corregido problema de traducción incorrecta del cuadro de entrada en la interfaz de mensajes privados de Tiktok
- Corregido problema donde los cómics en Read Comic Online no se podían traducir
- Corregido problema donde la [Configuración Avanzada -> Número mínimo de caracteres requeridos para traducir un párrafo] no tenía efecto en algunos casos

## 1.8.4 (2024-08-30)

- El servicio de traducción DeepL ahora soporta oficialmente Chino Tradicional como idioma de destino (anteriormente, traducir a Chino Tradicional con DeepL involucraba un proceso adicional de conversión de terceros de Simplificado a Tradicional)
- Optimizado el rendimiento de traducción de texto enriquecido

## 1.8.3

- Google Meet ahora soporta subtítulos bilingües para reuniones en vivo: Simplemente abre el enlace de la reunión, activa los subtítulos bilingües en el panel de traducción inmersiva, y luego actualiza la página para experimentarlo
- Añadidas las opciones para "Reportar problemas de traducción de la página web actual" y "Activar/desactivar rápidamente la bola flotante" en las opciones adicionales del panel
- Después de ajustar la posición de los subtítulos bilingües de YouTube, el sistema recordará automáticamente la nueva posición
- Optimizada la lógica de caché del plugin, ahora limpia automáticamente los datos de caché que tienen más de 30 días
- Optimizados los bloques de código dentro de párrafos para una restauración más precisa del texto original
- Mejorado el manejo de "palabras no traducibles" en configuración avanzada

## 1.8.2

- Ahora puedes traducir texto en cuadros de entrada con clic derecho: Selecciona cualquier texto en un cuadro de entrada en una página web, haz clic derecho para elegir traducir, y la traducción inmersiva traducirá automáticamente el texto seleccionado al idioma objetivo del cuadro de entrada, haciendo conveniente traducir rápidamente texto en idioma nativo a otros idiomas en cuadros de entrada
- Ahora puedes reportar rápidamente problemas de traducción de páginas web en la bola flotante de traducción inmersiva. Después de traducir una página web, si hay algún problema, puedes hacer clic en el botón [Retroalimentación] en el lado derecho de la bola flotante, llenar la descripción del problema, y lo trataremos lo antes posible
- Los archivos Epub ahora soportan traducción de texto enriquecido (es decir, preservar el formato del texto original de cada párrafo, como enlaces, negrita, etc.)
- Soporte para subtítulos bilingües en tiempo real en reuniones de video de la versión web de Microsoft Teams (Abre el enlace de la reunión Teams, activa los subtítulos bilingües en el panel de traducción inmersiva, y luego actualiza)
- Optimizados los subtítulos bilingües para la versión en inglés de iQIYI (iq.com)
- Proporcionados más artículos de arXiv con diseño de traducción bilingüe optimizado
- Debido a restricciones del sitio web de Youtube, el script de Chrome Tampermonkey ya no soporta subtítulos bilingües. Por favor usa la [versión del plugin](https://immersivetranslate.com/)

## 1.8.1

- Corregidos problemas de traducción con el script Tampermonkey SiliconCloud
- La traducción Claude ahora soporta Tibetano y permite configuración del parámetro Temperature
- La página de detalles de expertos AI muestra los prompts utilizados por el experto
- La configuración de accesos directos ahora permite asignar teclas de acceso rápido únicas para cualquier servicio de traducción
- Optimizada la detección para traducciones de artículos arXiv

## 1.7.9

- Corregidos problemas con la traducción de texto enriquecido para servicios de traducción como Google, DeepL (por ejemplo, páginas que muestran directamente `<button>` etc.)
- Corregido el problema donde el acceso directo bilingüe para videos de YouTube no se podía desactivar

## 1.7.8

- DeepL, Microsoft Translate, Google Translate, OpenAI, Claude, Gemini y otros servicios de traducción soportan traducción manteniendo el formato del texto original (por ejemplo, enlaces, negrita, etc.)
- Después de seleccionar el texto, el menú de clic derecho cambiará a [Traducir el texto], al hacer clic en él puedes saltar automáticamente a la página de Traducción de Texto de Immersive Translation

## 1.7.7

- Optimizado el control de frecuencia de solicitudes del servicio de traducción
- Recientemente, las solicitudes domésticas del servicio de traducción de Microsoft han sido inestables, cuando ocurre un error, detectará automáticamente los servicios de traducción actualmente disponibles y permitirá a los usuarios cambiar rápidamente
- Optimizados los mensajes de error de red
- Corregida la configuración de color de texto que no soportaba vista previa RGBA [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Corregido el problema donde la página de instalación exitosa siempre se mostraba al actualizar la versión del plugin de Safari
- Microsoft agregó soporte para vietnamita
- Corregido el problema donde los subtítulos traducidos no se mostraban en el sitio edx

## 1.7.6

- La traducción de subtítulos de video ahora soporta [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). También soporta la traducción de algunos videos con subtítulos CC en Twitter
- Optimización de ventanas emergentes de error, las ventanas emergentes de error de problemas de red detectarán automáticamente servicios de traducción gratuitos válidos
- Corregida la reproducción en pantalla completa de YouTube en el soporte inmersivo de la APP iOS
- Corregido el problema de traducción de párrafos en Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707)

## 1.7.5

- La traducción de subtítulos de video ahora soporta [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/)
- Corregido el problema donde algunos usuarios Pro no podían cambiar la configuración en el navegador Chrome
- Soporte para mostrar subtítulos bilingües de YouTube en modo pantalla completa en iOS

## 1.7.4

- La traducción de subtítulos de video ahora soporta las plataformas [LinkedIn](https://www.linkedin.com/) y [Viu](https://www.viu.com/)
- Añadidos más accesos directos de subtítulos de video para más plataformas
- Soporte para mostrar solo traducción para configuraciones específicas de sitio web/idioma

## 1.7.3

- Optimizado el problema de visualización de traducción de subtítulos CC de videos de Twitter
- El servicio DeepL ahora soporta árabe
- El servicio Caiyun ahora soporta coreano, español, francés y ruso
- El servicio OpenAI ahora soporta dongbeihua
- El panel de detección automática ahora muestra el idioma del texto original
- Ajustada la descripción de accesos directos del panel en dispositivos móviles

## 1.7.2

- Corregido el problema donde no se podía cerrar el panel de control en dispositivos móviles

## 1.7.1

- Soporte de plataforma de subtítulos de video para [DeepLearning.ai](https://learn.deeplearning.ai)
- Soporte para problemas de visualización RTL en árabe, hebreo, etc. en traducción de páginas web y subtítulos de video
- Corregida la traducción al hebreo de Gemini
- Corregido el problema donde algunos subtítulos en chino tradicional de YouTube no se mostraban correctamente
- Corregido el problema de visualización de subtítulos de Twitter en Safari
- Corregida la tecla de acceso rápido para traducir inmediatamente al final de la página

## 1.6.4

- Corregido el problema donde los marcadores de posición no se reemplazaban correctamente en la creación de ePub
- Soporte de traducción de subtítulos de video para [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.6.3

- Optimizado el control de frecuencia de solicitudes del servicio de traducción
- Recientemente, las solicitudes domésticas del servicio de traducción de Microsoft han sido inestables, cuando ocurre un error, detectará automáticamente los servicios de traducción actualmente disponibles y permitirá a los usuarios cambiar rápidamente
- Optimizados los mensajes de error de red
- Corregida la configuración de color de texto que no soportaba vista previa RGBA [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Corregido el problema donde la página de instalación exitosa siempre se mostraba al actualizar la versión del plugin de Safari
- Microsoft agregó soporte para vietnamita
- Corregido el problema donde los subtítulos traducidos no se mostraban en el sitio edx

## 1.6.2

- La traducción de subtítulos de video ahora soporta [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). También soporta la traducción de algunos videos con subtítulos CC en Twitter
- Optimización de ventanas emergentes de error, las ventanas emergentes de error de problemas de red detectarán automáticamente servicios de traducción gratuitos válidos
- Corregida la reproducción en pantalla completa de YouTube en el soporte inmersivo de la APP iOS
- Corregido el problema de traducción de párrafos en Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707)

## 1.6.1

- La traducción de subtítulos de video ahora soporta [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/)
- Corregido el problema donde algunos usuarios Pro no podían cambiar la configuración en el navegador Chrome
- Soporte para mostrar subtítulos bilingües de YouTube en modo pantalla completa en iOS

## 1.6.0

- La traducción de subtítulos de video ahora soporta las plataformas [LinkedIn](https://www.linkedin.com/) y [Viu](https://www.viu.com/)
- Añadidos más accesos directos de subtítulos de video para más plataformas
- Soporte para mostrar solo traducción para configuraciones específicas de sitio web/idioma

## 1.5.3

- Optimizado el problema de visualización de traducción de subtítulos CC de videos de Twitter
- El servicio DeepL ahora soporta árabe
- El servicio Caiyun ahora soporta coreano, español, francés y ruso
- El servicio OpenAI ahora soporta dongbeihua
- El panel de detección automática ahora muestra el idioma del texto original
- Ajustada la descripción de accesos directos del panel en dispositivos móviles

## 1.5.2

- Corregido el problema donde no se podía cerrar el panel de control en dispositivos móviles

## 1.5.1

- Soporte de plataforma de subtítulos de video para [DeepLearning.ai](https://learn.deeplearning.ai)
- Soporte para problemas de visualización RTL en árabe, hebreo, etc. en traducción de páginas web y subtítulos de video
- Corregida la traducción al hebreo de Gemini
- Corregido el problema donde algunos subtítulos en chino tradicional de YouTube no se mostraban correctamente
- Corregido el problema de visualización de subtítulos de Twitter en Safari
- Corregida la tecla de acceso rápido para traducir inmediatamente al final de la página

## 1.4.7

- Corregido el problema donde los marcadores de posición no se reemplazaban correctamente en la creación de ePub
- Soporte de traducción de subtítulos de video para [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 0.12.7

- Se añadieron subtítulos bilingües para apoyar las plataformas [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/)
- El hoverball ahora se oculta por defecto cuando el video está en pantalla completa.
- Corrección del problema de clic tembloroso del panel de acción hoverball de la página de firefox.
- Soporte para colaboración bajo el sitio pubmed.ncbi.nlm.nih.gov y el complemento scholarscope
- Corrección del problema de temblor de la página de traducción del cuadro de entrada de reddit

## 0.12.6

- Corrección del problema de que la traducción de YouTube/Web of Science, etc., no es sensible al cambiar de pestañas.
- El hoverball en móviles ahora soporta la operación de presión larga, presión corta para traducir, presión larga para abrir el panel.
- Traducir ebooks bilingües ahora también traducirá la tabla de contenidos.
- La función de Mejora de Búsqueda (algunas páginas de Búsqueda de Google muestran resultados de búsqueda bilingües) ahora no está habilitada por defecto y será eliminada en la próxima versión.

## 0.12.5

- Corrección en la creación de eBooks en formato Epub desde el panel al hacer clic en traducciones que no funcionaba

## 0.12.4

- Al activar los subtítulos bilingües en el panel, primero se refrescará la página automáticamente (para mostrar los subtítulos bilingües con mayor precisión), y algunos sitios aún requieren que los usuarios hagan clic manualmente en el botón "CC" en el sitio para activar los subtítulos.
- Optimización de la detección de idiomas en Grease Monkey y Safari
- Proporciona acceso rápido a versiones bilingües de todos los artículos en el sitio de documentos [Arxiv](https://arxiv.org/abs/1910.06709).
- [Soporte de Hoverball configurado para fijarse a la izquierda #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Corrección del problema de visualización del Modo de Aprendizaje #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Activar temporalmente la traducción web por un período de tiempo no cancela Traducir Siempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Optimización de problemas de inicialización de archivos PDF

## 0.12.3

- Corrección para la función de [deshabilitar permanentemente los subtítulos de video] que no funcionaba [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175)

## 0.12.2

- Se proporciona soporte para subtítulos bilingües en más plataformas de video, ahora son compatibles: [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy](https://www.khanacademy.org/), [Coursera](https://www.coursera.org/), [Vimeo](https://vimeo.com/), [Nebula](https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), etc. (Nota: debido a limitaciones técnicas, algunos sitios web necesitan refrescar la página después de activar por primera vez los subtítulos bilingües o esperar a que la traducción se complete para mostrar los subtítulos bilingües).
- Optimización significativa del tamaño del archivo zip del complemento, reducido a la mitad en comparación con el original, descarga y actualización más rápidas.
- Corrección de problemas en la descarga de PDF extendidos.
- Añadido un portal de traducción rápida de PDF en el lado derecho del sitio de artículos de [Arxiv](https://arxiv.org/abs/1910.06709), que lleva a una página HTML limpia (solo soportado por algunos artículos, ya que requiere que los autores originales envíen el código fuente, así que aproximadamente el 50% de los artículos mostrarán este portal).
- Las páginas de PDF en línea sin extensión .pdf ahora pueden saltar directamente a la página de traducción de PDF haciendo clic en el hoverball de la página.
- Corrección de algunos problemas de mejora de cajas de entrada bajo Safari.
- Optimización de la detección de idiomas en Grease Monkey y Safari.

## 0.11.6

- Se han añadido 11 nuevos idiomas de interfaz para el plugin y el sitio web oficial, ahora los idiomas de interfaz soportados alcanzan los 14, incluyendo Chino Simplificado, Chino Tradicional, Inglés, Japonés, Coreano, Ruso, Español, Portugués, Hindi, Italiano, Alemán, Francés, Árabe y Persa.
- Modificar la compartición bilingüe (modo de actualización) añadida en la última versión a compartición de captura de página bilingüe, para que el contenido compartido sea más original, así como de mayor adaptabilidad.
- Corregir el emoji al final del cuadro de entrada de Twitter que no se puede traducir
- Corregir la situación en la que el contenido de plugins de terceros se traduce en algunos escenarios
- Reparar el clic no responsivo del hoverball de pdf en línea

## 0.11.5

- Ahora puedes generar un enlace público a la página bilingüe traducida para Immersive Translate.
  - ¡[Haz clic](/docs/share/) en el Icono de Compartir de Immersive Translate para generarlo en un solo clic!
- Resuelto el problema de que algunas plataformas no podían reconocer si se soportaba el ratón o no
  - Hay algunos navegadores de escritorio que soportan tanto la pantalla táctil como el ratón, y Immersive Translate técnicamente no puede detectar si dichas plataformas soportan ratón, por lo que hemos añadido la opción [Forzar Habilitación del Soporte de Ratón] en la configuración de [Hover del Ratón]

## 0.11.2-0.11.4

- Optimizar experiencia, corregir algunos errores

## 0.11.1

- El modelo predeterminado para las traducciones de OpenAI es: GPT3.5-turbo-1106.
- Optimizada la Sugerencia en Chino para OpenAI, ¡ahora menos propensa a alucinaciones!
- Reducida la longitud de las sugerencias de OpenAI de 90 a 40, ahorrando aún más tráfico.

## 0.11.0

- Corregir clics temblorosos del hoverball de la página
- Corregir problemas de traducción de Azure

## 0.10.9

- Corregir algunos problemas menores

## 0.10.8

- Soporte para configurar botones de traducción rápida hoverball (soporte tanto para PC/móvil)
- Optimización del juicio de idioma de Grease Monkey
- Corrección de la traducción de archivos txt

## 0.10.7

- Soporte de mouse hover presiona Ctrl nuevamente para mostrar el texto original
- Mouse Hover Ignora Nunca Traducir Idioma
- Optimización de Subtítulos Bilingües de Youtube

## 0.10.6

- Soporte de subtítulos de Youtube solo para traducciones
- Añadir alerta de actualización de baja versión de Grease Monkey
- Corregir el problema de que los archivos txt locales no se pueden traducir

## 0.10.5

- Corregir Youtube ocasionalmente regresando a la página de inicio

## 0.10.4

- Corregir conflicto de subtítulos de Youtube con el plugin de Subtítulos Duales (La traducción de subtítulos de Youtube de Immersive Translate no se activa cuando se detecta el plugin Dual de Youtube para evitar conflictos)
- Añadido [Desactivar Permanentemente la Función de Subtítulos de Video], si hay otros problemas de conflicto y no quieres activar la función de subtítulos bilingües con Immersive Translate.
- Optimizar cortes de subtítulos

## 0.10.3

- Corregir problema de traducción con la clave de autorización personalizada de DeepL

## 0.10.3

- Soporte perfecto para videos de Youtube con subtítulos bilingües 🎉.
- Para las páginas de artículos, el texto del cuerpo ahora se traducirá primero antes del resto del contenido de la barra lateral
- Optimizar la contextualización de la traducción de DeepL
- Optimizar la traducción de OpenAI de archivos de subtítulos para la contextualización

## 0.10.1

- Aumentar la prioridad de la traducción del cuerpo para optimizar la experiencia de traducción
- Corregir el problema de no traducción del texto al hacer clic en más en Instagram

## 0.9.8

- Optimizar experiencia, corregir algunos errores

## 0.9.7

- Corregir la auto-traducción cuando se resalta readwise

## 0.9.6

- Corregido el borrado de la caché al cerrar sesión del login del usuario.

## 0.9.5

- Correcciones de errores en eBooks en línea

## 0.9.4

- Optimización de la detección de mejora de entrada para reducir toques falsos
- Traducción en línea de libros electrónicos y subtítulos

## 0.9.3

- Traducción de Caja de Entrada: muestra un recordatorio emergente cuando se usa por primera vez, y el usuario puede elegir desactivarlo esta vez o permanentemente para evitar toques accidentales.
- Optimización de la velocidad de exportación de traducción solo de PDF, si eliges exportar solo la traducción, puedes llamar directamente a la vista previa de PDF del sistema para exportar, más rápido.
- Deeplx soporta múltiples URLs, solo sepáralas con un punto.

## 0.9.2

- La herramienta de traducción de PDF se ha migrado a la versión en línea: https://app.immersivetranslate.com/pdf/ , para que Grease Monkey y Safari puedan usar la traducción de PDF, y los problemas pueden iterarse mejor sin la necesidad de emitir una versión para resolver el problema.
- Optimización de la UI POPUP, ¡el panel es más hermoso!

## 0.9.1

- Corrección de problemas de nombre de archivo con la creación de libros electrónicos Epub

## 0.8.8

- soporte de pdf para ajustes de espaciado de líneas y palabras para volver a reconocer párrafos
- solución de problemas de desplazamiento automático móvil de lectura en línea epub

## 0.8.7

- soporte de pdf para descargas de traducción solamente
- Corrección del problema de inicio de sesión de Google en Safari

## 0.8.2 - 0.8.6

- Te permite establecer el intervalo entre disparadores de combo de mejora de entrada
- Corrección de algunos errores

## 0.8.1

- Optimización de Detección de Idioma
- Características Beta: API Personalizada (Beta habilitada en configuraciones de desarrollador)
- Soporte para Traducción de AliCloud
- Corregidos algunos errores

## 0.8.0

- Sistemas de Usuario Soportados
- Soporta [Habilitar Membresía Pro](/pricing), lo cual permite a los usuarios disfrutar de traducciones de Deepl y OpenAI y configuraciones de sincronización en la nube.
- El servicio de traducción al pasar el mouse se puede configurar individualmente
- El servicio de traducción en cajas de entrada se puede configurar por separado
- Optimización de Traducción de PDF
- Corrección de algunos errores

## 0.7.16

- Traducción de PDF con nuevas opciones para un control rápido del estilo de traducción (los archivos PDF son muy extraños y activar estas opciones puede ser útil para algunos archivos PDF con formato desordenado)
- Las versiones de iOS y macOS están de vuelta en la Tienda de Países de Apple Store

## 0.7.15

- Apple nos ha notificado que las Traducciones de OpenAI han sido temporalmente retiradas de iOS y macOS, y estamos intentando relanzarlas en China.

## 0.7.11- 0.7.14

- Corrección: Problema de Traducción de Gmail en Todas las Regiones
- Desactivación temporal de la función de exportación de PDF de Safari debido a la restricción de Safari sobre la descarga de complementos (bug).
- Corrección de algunos otros problemas

## 0.7.10

- Mejora de la UI del Panel del Icono del Navegador Emergente, un poco más de diseño ～
- Corrige el problema de que algunos pasajes en japonés no se traducen.

## 0.7.9

- ¡PDF finalmente soporta la exportación de versiones bilingües! Puedes hacer clic en el botón [Guardar] para exportar el archivo PDF traducido bilingüe.
- Las reglas personalizadas ahora soportan la fusión con las reglas incorporadas por defecto, por ejemplo: `{"id": "youtube", "selectors.add":["#test"]}` significa añadir un `#test` a los selectores existentes, `selectors` significa sobrescribir el predeterminado, `selectors.remove` significa eliminar uno de los selectores predeterminados, y `selectors.remove` significa eliminar uno de los selectores predeterminados, y `selectors.remove` significa eliminar uno de los selectores predeterminados. elimina uno de los selectores predeterminados.
- Icono de Safari actualizado, un poco más grande.
- Otras Correcciones de Errores

## 0.7.8

- Correcciones de errores

## 0.7.7

- Adaptado al estilo del sistema de Safari, el icono de la extensión de Safari cambió a un contorno transparente.
- Añadir cambio de estado del icono del navegador, cuando una página web ha sido traducida, un ✅ se añadirá automáticamente en la esquina inferior derecha del icono del navegador.
- Habilitar automáticamente la traducción de sitios web en inglés frecuentemente utilizados para nuevos usuarios.
- Solucionar problemas de traducción con https://claude.ai/

## 0.7.6

- Soporte Mejorado de Entrada Traducción de Resultados ctrl+z Deshacer
- Soporte de traducción en modo de lectura de documento de Flying Book
- Adaptación https://pi.ai/talk

## 0.7.5

- Solucionar que el icono de Grease Monkey no se muestra
- Solucionar una serie de problemas

## 0.7.4

- Solucionar una serie de problemas
- La página de configuración soporta la eliminación por lotes de urls seleccionadas.
- Soporta habilitar/deshabilitar la traducción de subtítulos de Youtube para prevenir conflictos con otros complementos relacionados.
- Arigato Translator soporta la configuración de campos y el id de terminología

## 0.7.2

- Mejora del Cuadro de Entrada: permite omitir el prefijo // y activar la traducción de todo el cuadro de entrada con 3 espacios, o puedes desactivar esta opción en la página de configuración.

## 0.7.1

- Soporte de Mejora de Búsqueda, cuando está habilitado, cuando buscas en Google/Google News en chino, la columna derecha mostrará automáticamente los resultados de búsqueda de las correspondientes palabras clave en inglés, lo cual está habilitado por defecto.
  - Razón: Encontramos que en la búsqueda de Google, los resultados de búsqueda para palabras clave en chino y en inglés pueden ser muy diferentes, con la Mejora de Búsqueda Traducida Inmersiva habilitada, buscamos automáticamente las mismas palabras clave en inglés para ti y las mostramos en el lado derecho. Puedes elegir desactivarlo si no necesitas la función.
  - Safari no es compatible debido a limitaciones de la API.

## 0.6.20

- Modificar la configuración predeterminada: Debido a la gran cantidad de comentarios de usuarios que indican que no utilizarán la herramienta de traducción después de la instalación, su expectativa respecto a la herramienta de traducción es que traduzca automáticamente las páginas web en inglés después de la instalación. Por lo tanto, a partir de esta versión, para los usuarios chinos, se ha activado por defecto la opción de traducir páginas en inglés (si el usuario tenía una configuración previa del idioma que siempre se traducirá, entonces se respetará, y el cambio solo modifica los ajustes iniciales de la extensión), y si se necesita cancelar, se puede hacer fácilmente en [Panel emergente o página de configuración](/docs/faq/#%C3%B3mo-desactivar-la-traducci%C3%B3n-autom%C3%A1tica)

## 0.6.19

- Corregir errores de PDF
- Corregir error de Web of Science
- Adaptación para feeder.com
- Corregir que no se traducen algunos libros en epub

## 0.6.18

- Corregir el problema de desbordamiento de ancho del popup en Safari.
- Optimización del proceso de construcción

## 0.6.17

- Optimizar alertas de error
- Optimizar la selección del idioma objetivo, ahora solo mostrará los idiomas que el servicio de traducción correspondiente soporta
- Optimización de la traducción de PDF
- Adaptado para el sitio web de Good Reads, Amazon y el sitio web de South China Morning Post

## 0.6.16

- Añadir visualización de página sin permiso en PDF
- Reparar la visualización de párrafos de lista de texto en PDF
- Aumentar la escala de fuente pequeña en PDF en Chrome y Safari

## 0.6.15

- Reparar el problema de que al abrir archivos PDF, el panel de extensión indica que no hay permisos.
- Corregir el problema de que el refuerzo del cuadro de entrada no está habilitado cuando el sitio está configurado para nunca traducir.

## 0.6.14

- Optimización de la traducción de PDF, ahora el área de traducción puede ser editada/arrastrada/eliminada
  - Arrastrar arriba a la izquierda, eliminar arriba a la derecha, cambiar tamaño abajo a la derecha
- Alineación a la izquierda del cuadro desplegable de Windows
- Soporte para chino tradicional y chino simplificado

## 0.6.13

- Solucionar el problema de traducción repetida al pasar el ratón por encima
- Soporte de traducción de PDF con arrastre para cambiar el tamaño y editar el contenido de la traducción

## 0.6.12

- Soluciona que las imágenes de traducción de Epub se reduzcan en algunos navegadores
- Optimización de la traducción de cajas de entrada, ahora funciona sin problemas en Bard!

## 0.6.10

- El modelo predeterminado de OpenAI cambió a la versión 0613
- Corregir algunos estilos de cajas de entrada
- Más inteligente para determinar si es un área de navegación, y si es así, no se realiza la traducción
- Corregir posibles ataques de inyección XSS

## 0.6.8

- El panel de extensión ahora puede indicar páginas no soportadas (por ejemplo, páginas sin permisos y páginas no HTML)
- Mejora de la caja de entrada para mostrar el estado de carga en la traducción
- Actualizar los colores de carga predeterminados en las traducciones
- Cuando la caja de entrada está configurada sin prefijo, soporta la traducción `ja Hola` al japonés y `Inglés Hola` al inglés.

## 0.6.6

- Corrección para: algunas áreas no se traducen (quora)

## 0.6.5

- Optimización de Google Bard
- La traducción de cajas de entrada soporta la traducción directa de todo el cuadro de texto sin prefijos.
- Optimizar el problema de las traducciones de OpenAI añadiendo puntos sin pensar, (si no se detecta un punto en el texto original, si openai devuelve un punto, entonces quitarlo)
- Problemas con archivos de subtítulos de safari no reconocidos

## 0.6.3

El idioma predeterminado para la traducción de cajas de entrada ahora puede omitir el espacio, es decir, //Hola Mundo también puede ser traducido.

## 0.6.2

La mejora más emocionante en el cuadro de entrada está aquí:

- Escribe: // Hola Mundo en el cuadro de entrada en cualquier página web, luego haz triple clic en la barra espaciadora para traducir el párrafo al inglés.
- También puedes especificar la traducción a un idioma determinado: /ja Hola Mundo, luego haz triple clic en la barra espaciadora para traducir el párrafo al japonés.

[Haz clic aquí para una rápida introducción de 30 segundos](/docs/input/)

## 0.6.0

- Primera versión en junio, migrada desde el subdominio personal anterior https://immersive-translate.owenyoung.com al nuevo dominio https://immersivetranslate.com/
- La funcionalidad es en gran medida inalterada (¡las nuevas características estarán disponibles en la próxima versión!)

## 0.5.17

- Soluciona el problema de que: los eBooks bilingües no tienen imágenes después de exportar.

## 0.5.16

- Solución: problema de traducción de openai en Chino Tradicional.

## 0.5.15

- Optimización: El número mínimo de caracteres en un párrafo que activa la traducción se modificó a un mínimo de 4 caracteres para reducir la confusión, mientras se utilizan otras características para evitar traducir las áreas de navegación y final del sitio.
- Solución: Detalles de Github no se traducen después de expandirse.

## 0.5.14

- Soluciona el problema de que las imágenes en algunas páginas web: se hacen más grandes después de copiar.
- Solución: sección de comentarios de medium no se traduce.
- Solucionado el problema de que las imágenes en algunas páginas: se copiaban incorrectamente.

## 0.5.12

- Característica: El Estilo de Traducción de Línea Dividida añade una línea vertical dividida para traducciones de una sola línea.
- Solución: Casos muy raros de división de párrafos.
- Una excelente página de orientación de configuración inicial para nuevos usuarios de iOS.

## 0.5.11

- Soporte de traducción de subtítulos solo para exportar traducciones
- Corrección: Algunos elementos no son reconocidos al pasar el ratón por encima
- Corrección: No se reconocen los saltos de línea parciales en tweets
- Corrección: Estilo de autoría de eBook no funciona

## 0.5.10

- Corrección: No se reconocen los saltos de línea en tweets
- Corrección: La página de detalles de Reddit devuelve algunos párrafos que no se pueden traducir
- Se corrigió un problema con: donde algunas de las etiquetas de Código no se reconocían correctamente.

## 0.5.9

- Corrige saltos de párrafo en algunos casos en:
- Corrección: El interruptor de Tampermonkey solo muestra traducciones
- Corrección: Problema con el estilo de lectura en línea de eBook no funciona

## 0.5.8

- Corregir el problema de que: la configuración temporal de la duración de la traducción del sitio web no surte efecto.

## 0.5.7

- ¡Super actualización!

- ¡La función Mostrar Solo Traducciones está aquí! Haz clic en [Más] -> [Cambiar a mostrar solo traducciones].

  - Soporte para atajos personalizados, configurar en ajustes de interfaz -> Configuración de Atajos

- Optimización de la limitación de frecuencia de solicitudes a OpenAI

- ChatGPT por defecto al modelo móvil, ¡que es más rápido!

- Refactorización del análisis del núcleo web, lo que significa:

  - Traducción de páginas web a gran escala en segundos
    - Por ejemplo: https://pve.proxmox.com/pve-docs/pve-admin-guide.html, lo que antes tomaba 30 segundos, ahora se hace en segundos.
  - Uso ultra bajo de memoria para páginas web complejas
    - Por ejemplo: https://www.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1
  - Adaptación a más sitios web

- Todas las traducciones de sitios web con ShadowRoot son compatibles.

  - Por ejemplo: https://bugs.chromium.org/p/chromium/issues/detail?id=418987
  - Por ejemplo, la sección de comentarios de: https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html

- Solucionado el problema de pantalla blanca después de la traducción de sitios web con hidratación como Next.js.

  - Por ejemplo: https://webpack.js.org/

- Solucionado el problema que requería refrescar la página para que la modificación del atajo de mouse al pasar por encima tomara efecto

- Solucionado un problema con el reconocimiento de saltos de línea en archivos TXT.

- ¡Muchas actualizaciones!

- ¡La función 'Mostrar Solo Traducciones' ha llegado! Haz clic en 'Más' -> 'Cambiar a Mostrar Solo Traducciones'.

  - Soporta atajos personalizados, que se pueden configurar en 'Ajustes de Interfaz' -> 'Configuración de Atajos'

- Optimización para el problema de límite de tasa de solicitudes de OpenAI

- El análisis del núcleo web ha sido reconstruido, lo que significa.

  - Traducción instantánea para sitios web grandes
  - Uso mínimo de memoria para páginas web complejas
  - Mejor compatibilidad con más sitios web

- Ahora soporta traducciones para todos los sitios web con ShadowRoot.

- Solucionado el problema de pantalla blanca después de traducir sitios web con hidratación, como Next.js

- Solucionado el problema donde cambiar el atajo de mouse al pasar por encima requería un refresco de página para tomar efecto

- Solucionado el problema con el reconocimiento de saltos de línea en archivos TXT.

## 0.5.6

- Corrección: problema de la ventana emergente de nueva pestaña en macOS.
- Característica: Nueva página de guía para el usuario nuevo.

## 0.5.5

- Corrección: Problema del área al pasar el mouse.

## 0.5.4

- Corrección: Duplicado de la página Spa

## 0.5.3

- Corrección: Escuchador de teclas rápidas al pasar el mouse.
- Corrección: Traducción de documentos PDF.
- Característica: Añadir nueva página de guía para el cliente.

## 0.5.2

- Corrección: configuraciones de atajos de mouse hover en userscript.

## 0.5.1

- Corrección: La API de OpenAI no funciona.

## 0.5.0

- Característica: Traducir el párrafo actual al pasar el mouse.
- Característica: Refactorización de la traducción de PDF, ahora puedes traducir la mayoría de los PDFs con Immersive Translate.
- Corrección: Deshabilitar el menú contextual no funciona [#428](https://github.com/immersive-translate/immersive-translate/issues/428).
- Corrección: Evitar la Política de Seguridad de Contenido para [Mastodon](https://mastodon.social/).

## 0.4.11

- Corrección: permiso de userscript (solo para userscript).

## 0.4.8

- Característica: Bing Translate a Microsoft Translate para una calidad más estable.
- Corrección: Página web de TXT puro como [esta](https://edoras.sdsu.edu/~vinge/misc/singularity.html).
- Rendimiento: Excluir algunas páginas de publicidad infantil en el sitio web, y el rendimiento ha mejorado un poco.

## 0.4.7

- Corrección: Falta el popup de Userscript en Firefox.

## 0.4.6

- Característica: Permitir que terceros envíen eventos de documento para llamar a `toggleTranslatePage`.
- Característica: La aplicación iOS añade botón de habilitación de extensión y enlace a comunidades.
- UI: El campo de configuración de OpenAI usa selección en lugar de caja de texto de entrada.

## 0.4.5

- Corrección: problema con la extensión de safari en iOS 15.0.
- Corrección: atajos de la extensión de safari en macOS.
- Corrección: ventana emergente de política de seguridad de contenido para la extensión, y parcialmente para el script de usuario.

## 0.4.4

- Tarea: Eliminar console.log

## 0.4.3

- Corrección: detección de espacios en blanco en etiquetas sup, sub.
- Característica: soporte del sitio web de ChatGPT Plus como Servicio de Traducción. Esta es una característica beta, por lo que puedes acceder a ella habilitando Característica Beta en la configuración de desarrollador. Esto es muy lento, porque chatgpt solo puede enviar una solicitud a la vez. Asegúrate de tener una Cuenta ChatGPT Plus, porque hay más límites en la Cuenta Gratuita, y no estoy seguro si esto podría representar un riesgo para tu cuenta, ten cuidado al usarlo.

## 0.4.1

- Corrección: el menú contextual de firefox desaparecía después de reiniciar.
- Soporte para Azure openai

## 0.4.0

- Característica: Soporte para traducir archivos de subtítulos locales (.srt, .ass, etc.)

## 0.3.17

- Característica: Soporte para traducir archivos locales .txt.
- Corrección: El Menú Contextual puede no estar disponible a veces. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Corrección: mantener &nbsp; como espacio en blanco.
- Eliminación: Retirar Papago, ya que [el servicio está caído](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI: permitir sin clave API para openai
- UI: permitir el restablecimiento de Open AI a la configuración predeterminada

## 0.3.14

- Dependencia: Actualizar pdf.js a la última versión
- Corrección: color de fondo de selección de pdf
- Corrección: detección de espacios en blanco

## 0.3.13

- Corrección: problema con caracteres específicos en constructor de ebooks, como algunas rutas de capítulos son `xxx' xxxx`.
- UI: plegar por defecto las opciones personalizadas de openai.
- UI: Añadir estado de exportación para la exportación de epub.
- Corrección: prompt predeterminado de Gpt4

## 0.3.12

- Característica: Ahora podemos personalizar el color de fondo del tema de traducción de Marker.
- Corrección: postMessage cuando la página inicial se rompía en algunos sitios, ahora haremos esto solo cuando realmente traduzcamos páginas
- Corrección: problema de progreso de ebook.
- Corrección: mejor para dividir párrafos largos, 1.5 mil millones, 25.5%, Mr. no se considerará como un límite

## 0.3.11

- Corrección: color de texto en modo oscuro del lector de ebooks
- Corrección: prompt de openAI

## 0.3.10

- Mejora: detectar contenedor japonés/coreano.
- Corrección: Progreso del Constructor de Ebook se detuvo al 99%.

## 0.3.9

- Corrección: Estado de entrada de cambio de servicios de traducción de la UI de Opciones no cambiado.

## 0.3.8

- UI: color de carga más transparente
- Corrección: Detectar idioma del Ebook.
- Característica: Añadir progreso de traducción para el constructor de ebooks, y un hermoso confeti después del éxito.
- Característica: Añadir reintentar todos los párrafos fallidos para el botón de reintentar.
- Corrección: Manejo de error de Deepl

## 0.3.7

- Corrección: el lector de ebooks no puede cargar imágenes en Chrome.

## 0.3.6

- UI: mejor para hacer la página UI del ebook

## 0.3.5

- Corrección: exportación de ebook de userscript
- Característica: añadir punto final de API personalizado para OpenAI
- Característica: añadir opciones de tiempo de traducción de sitio web temporal en `Configuración Avanzada`

## 0.3.4

- CI: La construcción falló

## 0.3.3

- Corrección: creador de ebooks para Kindle
- Cambio: Color del icono de carga, de negro a azul, para adaptarse a la página web en modo oscuro.
- Característica: Soporte para traducción local de html para la extensión

## 0.3.2

- Corrección: Movimiento del cursor en el formulario de opciones.
- Característica: Soporte de OpenAI para apiUrl personalizada para configuraciones de desarrollo.

## 0.3.1

- Característica: actualizar icono oscuro a transparencia.
- Corrección: Orden incorrecto para párrafos largos

## 0.3.0

- Versión: A partir de ahora, cambiaremos el número de versión menor una vez al mes, por ejemplo, ahora en marzo, la versión comenzará desde 0.3.0, en abril, el número de versión comenzará desde 0.3.0, en abril, el número de versión comenzará desde 0.4.0, el próximo abril, el número de versión será 1.4.0, y así sucesivamente. Esto es porque no tiene sentido que las extensiones sigan Esto es porque no tiene sentido que las extensiones sigan la semántica, pero estandarizar los números de versión según las leyes del tiempo es una motivación para que el desarrollo continúe actualizándose, y para que los usuarios encuentren problemas más fácilmente.
- Característica: Soporte de icono oscuro para Firefox

## 0.2.86

- Añadir opción de longitud máxima de texto por solicitud con Open AI
- Corrección: identificador de ebook duplicado
- Característica: Soporte para traducción de páginas web txt

## 0.2.85

- Corrección: algunos archivos epub no se pueden encontrar.

## 0.2.84

- Característica: Soporte para Lector y Creador de Ebook

## 0.2.83

- Característica: Permitir que el formulario de entrada de contraseña muestre la contraseña.

## 0.2.82

- Corrección: Algunos sitios usan `span` para estilos, así que usamos `font` en lugar de span para el contenedor del objetivo de traducción.
- Corrección: Límite máximo de tokens de OpenAI, cambio de máximo de caracteres de 1500 a 1300.

## 0.2.81

- Corrección: m.youtube.com
- Corrección: interfaz de formulario de opciones
- Corrección: prompt de Open AI
- Característica: Soporte para múltiples claves de OpenAI, usar `,` para separarlas.

## 0.2.80

- Característica: Añadir menú de Habilitar/Deshabilitar para más opciones en el popup
- Corrección: Conflicto de mensajes de DingTalk

## 0.2.79

- Corrección: Open AI para párrafos con espacios

## 0.2.78

- Característica: soporte para OpenAI CHATGPT 3.5 (soporta la interfaz de OpenAI ChatGPT 3.5)
- Característica: Añadir nuevo tema Borde Sólido

## 0.2.77

- Corrección: error de múltiples etiquetas de código. [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Corrección: error de múltiples etiquetas de código [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Característica: Soporte para conteo de texto de traducción inmediata personalizado para diferentes servicios de traducción.

## 0.2.74

- Característica: Soporte para Tencent (alfa)
- Corrección: traducción de openai
- Corrección: verificación de etiquetas desconocidas en línea

## 0.2.73

- Característica: Soporte para Tema de Traducción Gris
- Corrección: Página de Tendencias de Github

## 0.2.72

- Corrección: problema de red del servicio de traducción de verificación móvil de firefox.

## 0.2.71

- Corrección: permiso de userscript de Open AI

## 0.2.70

- Corrección: Marcador de posición de Open AI

## 0.2.69

- Característica: Soporte para Open AI como servicio de traducción.
- Característica: Soporte para verificar el servicio de traducción en options.html
- Característica: Soporte para marco principal personalizado porque algunos sitios no utilizan body como el marco principal

## 0.2.68

- Soporte para Caiyun (Alfa)
- Corrección de etiquetas de bloque desconocidas

## 0.2.67

- Característica: Añadir `<all>` para siempre traducir idiomas, así que ahora puedes usarlo para traducir todos los idiomas excepto el idioma objetivo, y nunca traducir idiomas
- Corrección: Permitir configuración personalizada de la API de Google
- Mejora: Soporte gratuito de Deepl
- Corrección: Uso alto de memoria para userscripts y extensiones (eliminando opencc de zh-CN a zh-TW, en su lugar con Google translate)
- Corrección: Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Corrección: Configuración de Azure translate pero aún muestra (necesita configuración)

## 0.2.66

- Corrección: Falla en la traducción de archivos PDF, Bug desde 0.2.60 por soportar deepl de zh-CN a zh-TW

## 0.2.65

- Soporte para solicitudes de aceleración para múltiples marcos
- No traducir el título de la página cuando está en iframe

## 0.2.64

- Corrección: openl elige servicios de traducción
- Característica: Soporte es traducir opción de título

## 0.2.63

- Característica: Soporte para el Servicio de Traducción de Azure
- Característica: Soporte para el Servicio de Traducción de Papago
- Corrección: sincronización de google drive en firefox android nativo.
- Corrección: cambio de transparencia de 0.4 a 0.618 [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Corrección: consejos de atajos de popup
- Rendimiento: solicitudes seriales a concurrencia
- Mejora para detectar el conteo japonés

## 0.2.62

- Característica: Añadir regla waitForSelectors, para arreglar algunos sitios como reddit

## 0.2.61

- Corrección: el userscript es demasiado grande para greasy fork
- Mejora: reducir tamaño del archivo

## 0.2.60

- Característica: Soporte de zh-CN a zh-TW para Deepl
- Característica: Función de Immersive Translate de Deepl
- Característica: Soporte para zoom de tamaño de fuente personalizado
- Corrección: estilo del foro de Steam
- Corrección: el estilo global no cambia después de que se generan elementos dinámicos
- Corrección: promover la exclusión de prioridad
- UI: cambio en la página de acerca de
- Corrección: algunos elementos matemáticos permanecen originales

## 0.2.59

- Corrección: Bloqueo de Elementos de Etiquetas Desconocidas
- Corrección: elemento translate=no sobrescribe
- Corrección: coincidencia de URL con múltiples \*

## 0.2.58

- Característica: Soporte para color de texto de traducción personalizado, color del borde.

## 0.2.57

- Sin cambios, reconstrucción

## 0.2.56

- Corrección de traducción duplicada para elementos en línea con elemento de código.
- Corrección de verificación de etiquetas desconocidas en línea/bloque
- Característica: soporte de css inyectado en el tablero de desarrolladores
- Característica: recortar authKey, appid appSecret
- Mejora: abrir página de configuraciones en una nueva pestaña (pero no para Stay)

## 0.2.55

- Intento de corrección del conjunto de caracteres de la API de deepl

## 0.2.54

- Eliminar permiso de pestañas para rechazo de la tienda de Chrome
- Corrección de traducir toda la página, el pie de página es ignorado
- Añadir notas a la página de acerca de
- Soporte de URL personalizada desde Configuración incorporada

## 0.2.53

- Corrección de error de sincronización de google drive de userscript.

## 0.2.52

### Código

- Usar el esbuild más reciente
- Usar la versión más reciente de deno
- CI: enviar código fuente a firefox

## 0.2.51

- Corrección de la necesidad de iniciar sesión en Google Auth en Chrome/Firefox
- Reemplazo de enlaces de servicio de traducción
- Mejor para permisos.
- eliminar minificar.

## 0.2.50

- Corrección del problema de subida a Google Drive (realmente) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Eliminar atajos alt+d, alt+s porque pueden entrar en conflicto con atajos nativos.
- Corrección del problema de subida a Google Drive [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Mejor para velocidad, al añadir minLength a 50 para la detección de idioma.
- Corrección de la validación del token de Google Drive.

## 0.2.47

- Corrección de la API de deepl

## 0.2.46

- corrección de marca de bloqueo

## 0.2.45

- Corrección de innerText de elemento es indefinido
- Corrección de traducción de caiyun con idioma de origen indefinido

## 0.2.44

- Corrección del interruptor de máscara de userscript
- Corrección de la lógica de interruptor de máscara

## 0.2.43

- Corrección del interruptor de máscara de userscript con evento táctil.
- Corrección de velocidad (eliminando sleep(300))

## 0.2.42

- Corrección del hover de máscara al activar la máscara de nuevo.
- Añadir atajos de máscara para móvil
- Corrección del problema de sincronización en la nube de userscript
- Mover la página de opción avanzada al menú izquierdo.
- Añadir lógica de reintento al servicio de traducción

## 0.2.41

- Corrección de la traducción de userscript niu
- Corrección de la traducción de xhtml

## 0.2.40

- Corrección de la visualización de la función beta
- Corrección de la página de configuración emergente en la nueva página de pestaña
- Corrección del reemplazo del marcador de posición de traducción

## 0.2.39

- Soporte de atajos para mostrar la traducción de máscara
- Soporte para habilitar la función beta en el panel de desarrollador
- Corrección de atajos en la extensión móvil

## 0.2.38

- Soporte para cargar tema
- Corrección de getpocket.com
- Corrección del pie de página para el área del cuerpo
- Corrección del icono de importar/exportar

## 0.2.37

- Corrección de marco para excluir marca

## 0.2.36

- Soporte para sincronización con Google Drive

## 0.2.35

- Corrección de ignorar etiquetas japonesas rb, rt.
- Mejoras para la interfaz de usuario emergente
- Mejoras para consejos de malos scripts de usuario
- Añadir contribución a la página de acerca de
- Corrección de traducción de Volc para detección automática de idioma

## 0.2.34

- Corrección de velocidad de traducción de múltiples idiomas

## 0.2.33

- Soporte para modo de escritura vertical, como el japonés.
- Añadir 3 temas
- Añadir servicio de traducción de Niu

## 0.2.32

- Corrección de traducción básica de PDF
- Corrección de selección emergente de un servicio no configurado, ir a la página de opciones.
- Corrección de mantener abiertas las configuraciones.
- Corrección de velocidad de detección de múltiples idiomas

## 0.2.31

- Corrección de inyección dinámica de CSS en iframe

## 0.2.30

- Soporte para traducción de iframe en línea en userscript.
- Soporte para traducción de shadowroot. Por ejemplo:
  https://www.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Área de conversación.
- también verificar regla de sincronización en emergente

## 0.2.29

- Corrección de traducción de Facebook
- Soporte para mostrar opción de menú contextual.

## 0.2.28

- Eliminar coincidencia no estándar para userscript

## 0.2.27

- Soporte para traducción de iframe en línea. (Solo para extensión, no disponible para
  userscript)
- Corrección de traducción de múltiples idiomas

## 0.2.26

- Corrección de addon de Firefox para Android
- Añadir configuraciones avanzadas para la traducción de saltos de línea

## 0.2.25

- Soporte para traducción de iframe, como correo de QQ, tweet incrustado.

## 0.2.24

- Añadir sitio temporal de traducción por un tiempo.
- Corregir la API del navegador de usuarios de stay.app.
- Corregir la página de opciones de stay.app.

## 0.2.23

- Corregir la traducción de páginas en múltiples idiomas.

## 0.2.22

- Corregir la construcción de userscript.

## 0.2.21

- Corregir la traducción de PDF en línea en Firefox.

## 0.2.20

- Corregir el problema de solicitud de macaco.
- Corregir la altura de línea de resaltado.

## 0.2.19

- Corregir el japonés inteligente de Tencent.
- Corregir el navegador del mundo de haikuo.

## 0.2.18

- Corregir el cambio de URL del cliente, mantener automáticamente el estado de traducción.
- Eliminar el contenedor lateral como el contenedor de traducción.
- Refactorizar la posición del popup.

## 0.2.17

- Cambiar resaltado por marca.
- Añadir tema de traducción de resaltado.

## 0.2.16

- Compatibilidad con macaco.

## 0.2.15

- Corregir el problema de rebote al tocar.

## 0.2.14

- Corregir que globalThis.GM no funciona en Safari.

## 0.2.13

- Soportar arrastre del Popup de Userscript.
- Soportar tres dedos en dispositivo táctil para activar la traducción de páginas.
- Soportar ocultar el icono del popup de userscript.

## 0.2.12

- Mejor para inoreader.

## 0.2.11

- Corregir
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  El archivo de Annas. El contenido principal de la página no se pudo traducir.

## 0.2.10

- Corregir la distancia de altura de línea en PDF.

## 0.2.9

- Corregir marcas de elementos excluidos.
- Corregir la verificación de tipo de deno.
- Eliminar importmap.
- Corregir la traducción de menús contextuales.
- Restaurar página cuando está habilitado nunca traducir este sitio.
- Añadir descripción para añadir URL.

## 0.2.8

- Detectar el idioma del agente de usuario para el idioma de la interfaz
- Corregir el error de salto de línea.

## 0.2.7

- Corregir solicitud de Grease Monkey

## 0.2.6

- Corregir
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  problema de coincidencia de URL de archivo

## 0.2.5

- Incrementar versión para prueba de CI

## 0.2.4

- Capturar error de conexión de mensaje para el popup.

## 0.2.3

- Corregir
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  crear contexto múltiples veces

## 0.2.2

- Corregir archivo de muestra PDF
- Corregir archivo local PDF en Firefox
- Corregir atajos de PDF

## 0.2.1

- Soporte para el gestor de atajos de Grease Monkey.
- Corregir expresión regular de coincidencia
- Corregir comentarios de YouTube.
- Corregir versión móvil compacta de Reddit
- Corregir problema de traducción de texto completo

## 0.2.0

- Corregir PDF de dos columnas.
- Corregir error de versión de Chrome/Edge Store.
- Corregir
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Publicar en complemento de Firefox
- Publicar en Edge
- corregir margen de pdf.
- Cambiar archivo pdf de muestra

## 0.0.62

- Corregir formato de pdf, indentación.
- Corregir telegra.ph prevenir cambio de elemento

## 0.0.61

- Corregir cierre de elemento span.
- Corregir permiso para navegador antiguo

## 0.0.60

- Corregir PDF de Chrome

## 0.0.59

- Soporte inicial para PDF

## 0.0.58

- Editar descripción del tema de traducción

## 0.0.57

- Cambiar UI de popup, para un uso más fácil

## 0.0.56

- Corregir tiempo de espera en Chrome.
- Corregir error de división de oraciones.

## 0.0.55

- Corregir que se muestren elementos con display none.
- Refactorizar marca de elemento.

## 0.0.54

- Soportar salto de línea cada X caracteres.

## 0.0.53

- Usar sendMessage en lugar de connect, ya que Chrome desconectará el puerto después de 5 minutos.
- Mejor detección de contenedores de texto.

## 0.0.52

- No traducir el párrafo que solo tiene elementos de marcadores de posición, por [ejemplo](https://github.com/nank1ro/solidart), la primera línea.
- Mejor detección de elementos hijos.

## 0.0.51

- Corregir problema de caché [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12), [#7](https://github.com/immersive-translate/next-immersive-translate/issues/7).
- Corregir tamaño de fuente en UI de opciones.

## 0.0.50

- Corregir que se traduzcan imágenes bloqueadas.

## 0.0.49

- Corregir extensión de Firefox.

## 0.0.48

- Corregir extensión de Chrome.

## 0.0.47

- Reescribir mensaje con fondo, usar connect en lugar de sendMessage.
- Añadir soporte para Reddit móvil.
- Corregir espacio en blanco previo para algunos artículos.

## 0.0.46

- Formatear información meta de userscript.

## 0.0.45

- Userscript usa un archivo.
- Añadir tiempo de espera para solicitud de caché.

## 0.0.44

- Corregir error de división en Tencent.
- Corregir error en elemento sup en línea.
- Mejor para Twitter.

## 0.0.43

- Corregir tweet br.
- Corregir traducción global.

## 0.0.42

- Corregir etiqueta BR.
- Tratar etiquetas de bloque como reglas.

## 0.0.41

- Corrección de la verificación de elementos en línea
- Añadir opción de registro de depuración para desarrolladores

## 0.0.39

- Corrección del servicio de traducción contiene mock2

## 0.0.38

- Soporte para cachear resultados para userscript
- Añadir UI de Opciones
- Soporte para detectar más contenedores de contenido

## 0.0.37

- Corrección de cambio en el servicio de traducción de popup no funciona
- Corrección de traducción de contenido de publicaciones móviles de Reddit.

## 0.0.36

- Corrección de caracteres especiales en Wikipedia
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Corrección del tamaño del icono de userscript.
- Habilitar la detección del idioma del párrafo en todos los sitios.

## 0.0.35

- Corrección de ir a la siguiente página en YouTube
- Soporte para la página de búsqueda de YouTube.
- Corrección del interruptor avanzado de opciones.
- Corrección de etiqueta img, etiqueta oculta
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Corrección de la actualización forzada de Búsqueda de Google
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Soporte para el resultado de Tabla de Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Corrección de página en blanco en Wikipedia
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Cambios Importantes

- La tecla de acceso rápido predeterminada para activar la traducción ha sido cambiada a `alt+A`, porque
  es la tecla más conveniente para escribir.

### Otros

- Soporte para establecer modo de traducción inmediata, para que puedas hacer que la página web se traduzca
  lo más rápido posible.
- Soporte para establecer el área de la página que necesita traducción, para que puedas traducir más área.
- Soporte para establecer el primer conteo de texto x para traducir inmediatamente.
- Corrección de traducción duplicada al cambiar de traducción
- Mejora de la UI del popup

## 0.0.33

- Soporte para más idiomas, zh-TW, en

## 0.0.32

- Corregir la traducción de archivos locales después de guardar. Corregido
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Añadir archivo js de distribución al repositorio público

## 0.0.31

- Soporte para Traducir la Página Completa
- Soporte para Traducir la página inmediatamente
- Más Configuración de UI
- Reflejar el tema
- Añadir nuevo icono
- Añadir nuevo tema de traducción dashedBorder

## 0.0.30

- Mejor para el tema con guiones

## 0.0.29

- Corregir párrafo válido.
- Añadir temas punteado, thinDashed
- Mejor para los temas con guiones, resaltado

## 0.0.28

- Corregir subrayado
- Añadir temas con guiones, papel
- Corregir detección de encabezados

## 0.0.27

- Soporte para translationTheme

## 0.0.26

- Corregir permiso de conexión de script de usuario de volc alpha.
- Corregir versión clickeable.

## 0.0.25

- Soporte para selectorMatches, así podemos coincidir con todo manstondon ahora.
- Corregir error de script de usuario en Firefox.

## 0.0.23

- Mejor para la detección de chino
- Corregir problema de innerText en reddit

## 0.0.22

- Soporte para deeplx
- Corregir múltiples traducciones al cambiar de servicio

## 0.0.21

- Corregir algunos tags span que son elementos de bloque

## 0.0.20

- Soporte para no traducir etiquetas hash como #hash, etiquetas at como @xxx, $tag, como $APPL
- Soporte para elemento de bloque

## 0.0.18

- Soporte para deepl, bing, baidu, youdao, volc, openl, caiyun.

## 0.0.13

- Soporte para userscript

## 0.0.4.8

- Corregir el orden del código.
- Soporte para interfaz de usuario emergente básica

## 0.0.4.6

- Soporte para verificar nueva versión

## 0.0.3

- Soporte para archivos locales

## 0.0.2

- Soporte para Elementos Dinámicos
- Soporte para traducción visible
