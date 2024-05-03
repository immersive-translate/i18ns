---
sidebar_position: 4
---

# Ayuda con PDF

Immersive Translate PDF Bilingual Reader es una herramienta de traducción en tiempo real bilingüe y cruzada, adecuada para usar como ayuda de lectura.

Actualmente, caracteres especiales como fórmulas matemáticas, tablas, etc., no pueden manejarse correctamente debido a la técnica de reconocimiento de texto plano.

Si tu PDF contiene tablas y fórmulas matemáticas, con requisitos de traducción de mayor calidad para ellos puede experimentar nuestro [PDF PRO](https://app.immersivetranslate.com/pdf-pro/)

Consulta la [documentación aquí](/docs/usage/#pdf-file-translation) para preguntas básicas sobre el uso

Aquí hay algunos consejos avanzados para la traducción de PDF:

### Editar cuadro

La traducción predeterminada es editable. Incluso puedes hacer clic en "Mostrar texto original" en el panel, y el contenido del cuadro de texto se mostrará como el texto original reconocido inteligentemente, y puedes hacer correcciones al texto original en el cuadro de edición en este momento. Luego, vuelve a hacer clic en la traducción del panel

### Mover cuadros de texto

Cuando algunos párrafos se reconocen en una posición incorrecta, puedes optar por mover la posición del cuadro de edición del párrafo completo colocando el ratón en la esquina superior izquierda. (Si encuentras una situación en la que no puedes arrastrar, puedes ampliar y arrastrar hacia abajo la esquina inferior derecha, y la esquina superior izquierda se moverá normalmente)

### Eliminar cuadro de texto

Cuando algunos párrafos pueden tener problemas de reconocimiento, fusionar manualmente el párrafo anterior puede hacer que este párrafo sea redundante, en este momento puedes hacer clic en este botón ¡para eliminarlo!

### Ajuste del tamaño del cuadro de texto

Debido a que la altura y anchura de la traducción predeterminadas son las mismas que las del párrafo original por defecto, cuando el contenido de la traducción excede el texto original habrá un desbordamiento, en este caso, puedes verlo a través del desplazamiento interno. También puedes arrastrar y soltar en la esquina inferior derecha para agrandar este cuadro de texto adecuadamente para permitir que el contenido se muestre completamente.

<!-- 

## Botones de Estilo de Control

![](/assets/docs/doc-assets/pdf-control.png) -->

### Modo Caravana

Lo predeterminado es restaurar la imagen del texto original en el área traducida a la derecha. Es normal ver un marco de fondo blanco para el texto traducido, porque es necesario cubrir el texto original dibujado por el canvas para que el texto traducido pueda mostrarse correctamente.

Si encuentras que el modo de subcapa afecta tu lectura, simplemente desactívalo.

### Límite de Superposición

Debido a que usamos tanto como sea posible para restaurar el efecto tipográfico original, la posición de inicio del párrafo es la del párrafo original de la esquina superior izquierda de las coordenadas que prevalecen. Bajo circunstancias normales de traducción de inglés a chino, el contenido en chino generalmente será más pequeño que el inglés, esta vez la traducción puede ser completamente demostrada. Esto ocurre cuando el texto traducido es redundante con el texto original en algunos casos. Para evitar esto, hemos dado a la traducción una altura igual a la del párrafo original.

Esto se puede desactivar cuando sentimos que la distancia entre los párrafos superior e inferior es suficiente para la presentación de la parte traducida del excedente.

### Espaciado Ajustado

Este objetivo es en realidad similar al anterior, porque hay un cierto espaciado entre cada línea de texto para asegurar la legibilidad del texto traducido.

Si la pantalla es pequeña y el espaciado entre los párrafos superior e inferior puede no ser suficiente para mostrar el desbordamiento del texto traducido, puedes activar este ítem y eliminar el espaciado entre líneas de texto, de modo que el texto de los párrafos pueda mostrarse completamente.

### Indentación del encabezado de párrafo

Debido a la complejidad de los diversos diseños de PDF, no se puede identificar inteligentemente si un párrafo está en línea con las características de indentación, pero si no hay indentación, entonces puede que mirar el párrafo del artículo sea un poco complicado. Así que para este tipo de párrafo del artículo, el usuario puede activarlo y el primer renglón de cada párrafo se indentará para mostrarlo.

### Las líneas están ampliamente espaciadas y los párrafos no se reconocen

Algunos PDF pueden, para fines de visualización, tener un espaciado entre párrafos relativamente grande, lo que resulta en que, al momento de la identificación inteligente, se juzgue que esta oración sea un párrafo independiente. Por lo tanto, necesita ser ajustado apropiadamente por decir 10, de modo que 10px se use como el espaciado entre líneas para volver a reconocer los párrafos en la página.

### Ajustando la posición horizontal de las traducciones

Debido a que las coordenadas horizontales del texto traducido se leen de los datos originales del pdf, algunas de las coordenadas horizontales del pdf serán grandes. En este caso, puedes hacer que el contenido traducido se mueva hacia la izquierda arrastrando la barra de progreso.

### Ajustando el escalado de las traducciones

El tamaño del texto traducido es básicamente el mismo que el del texto original, cuando sientas que el tamaño del texto traducido no es apropiado, puedes arrastrar la barra de progreso para que el tamaño de la fuente se ajuste según la proporción.

## Ajuste manual de segmentos erróneos

Si el párrafo reconocido inteligentemente es incorrecto, se puede ajustar manualmente siguiendo los siguientes pasos:

- Haz clic en el panel de traducción para mostrar el texto original reconocido.
- Luego, ajusta manualmente el párrafo contra el texto original a la izquierda copiando y haciendo saltos de línea, etc.
- Cuando se confirme que el párrafo es correcto, haz clic en Traducir nuevamente.

<!--

## Descargar Impresión

Haz clic en el icono de descarga en la esquina superior derecha

![](/assets/docs/doc-assets/pdf-download.png) -->

Debido a que nuestra herramienta depende del navegador, la velocidad de descarga y los resultados dependen en gran medida del propio navegador. Por lo tanto, se recomienda no manejar más de 300 páginas de PDF.

### Descarga de Traducción (Impresión)

Esta función descarga solo las traducciones, no bilingües.
Cuando se muestra la traducción predeterminada, el modo de zoom se establece en el ancho de página para el efecto de lectura.

Sin embargo, cuando se necesita imprimir y ahorrar tiempo, se recomienda ajustar el modo de zoom, generalmente se recomienda ajustar al 100 por ciento o al tamaño real, el efecto de impresión será mejor.

### Conservación Bilingüe

Debido a limitaciones técnicas en los efectos de conservación bilingüe, las traducciones se conservan en forma de imágenes, permitiendo la conservación WYSIWYG de los efectos de traducción en línea. Toma alrededor de 5/6 minutos exportar 300 páginas de PDF.

## Otras situaciones

### Intraducible

- Verifica si el texto original a la izquierda se puede copiar, si no se puede copiar, se demuestra que es un PDF en forma de imagen, el soporte temporal actual para la traducción de PDF en forma de imagen.
- Verifica que la traducción sea reconocida pero no traducida, que 🔄❓ no aparezca al final del párrafo, y que el botón en el panel del complemento muestre "Traducir". En este punto, haz clic en el botón de traducir para activar la traducción.
- Si existe 🔄❓, haz clic debajo de ❓ para ver el mensaje de error.

### Documento de Retroalimentación por Correo

Puedes enviar una descripción de tu problema + una captura de pantalla con el PDF original a support@immersivetranslate.com. Revisaremos la situación del PDF y organizaremos para que el plan se introduzca en las reglas de reconocimiento inteligente.
