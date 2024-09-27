# Traducción de Microsoft Azure

## Declaración Breve

1. Sitio web oficial: [Traducido por Microsoft Azure](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/text-translation-overview)
2. Descripción oficial: Las traducciones son gratuitas hasta 2 millones de palabras por mes, si excedes los 2 millones de palabras por mes, te cobraremos a una tarifa de $10 / 1 millón de palabras. Para más detalles, por favor consulta la [Nota de Precios](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/)

## Proceso de Registro

El proceso de registro es más engorroso que otros servicios de traducción y requiere paciencia.

Enlace de referencia: [Documentación para Empezar con Microsoft Azure Translation](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp)

## Registrarse en una cuenta de Azure

El primer paso es registrarse para una cuenta de [Azure](https://azure.microsoft.com/en-us/free/cognitive-services/), lo cual requiere que se vincule una tarjeta de crédito internacional (Visa/Master). Si no, no será posible registrarse.

## Registrarse para una Cuenta de Almacenamiento Azure Blob

Paso 2: Registrarse para una cuenta de almacenamiento [Azure Blob](https://portal.azure.com/#create/Microsoft.StorageAccount).

1. Crear un nuevo grupo de recursos y llenar el nombre de la cuenta de almacenamiento
2. Elegir una región que esté lo más cerca posible de ti, por ejemplo, la región de Hong Kong sería `Asia Oriental`.
3. El resto del proceso es simplemente seguir los pasos. En la última página, después de que se complete el despliegue, haz clic en el botón azul "Crear" en la parte inferior izquierda.

## Creación de Herramientas de Traducción

Paso 3: Crear [herramienta de traducción](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation)

1. Elige una región que esté más cerca de ti, por ejemplo, la región de Hong Kong sería `Asia Oriental`.
2. Los niveles de precios se seleccionan según sea necesario, con `Free F0` disponible para usuarios gratuitos. La capa gratuita no admite la traducción de documentos. Se puede utilizar una prueba estándar S1 si es necesario.
3. El resto del proceso es simplemente un siguiente paso directo. En la última página, después de que se complete la implementación, haz clic en el botón azul "Crear" en la parte inferior izquierda.

## Clave de Acceso

Después de una implementación exitosa, ve a [Azure Dashboard](https://portal.azure.com/#home), ve a la página de **Herramientas de Traducción**, y encuentra la clave en el menú de la izquierda - Gestión de Recursos - `Claves y Puntos de Acceso`. Microsoft proporcionará 2 claves, elige una y rellena la clave en el `APIKEY` de la Extensión Inmersiva - Microsoft Translator.

Debajo de la clave también hay una información de `ubicación/región`, por ejemplo, `eastasia`, que también necesita ser poblada en la `región` de la extensión inmersiva - Microsoft Translate.

## Problemas Comunes

Si tienes dudas, por favor da tu opinión [aquí](https://github.com/immersive-translate/immersive-translate/issues/137).
