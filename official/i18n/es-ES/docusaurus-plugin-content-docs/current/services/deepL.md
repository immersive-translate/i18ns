# DeepL

## Acceso directo a los servicios de traducción de DeepL después de abrir una [Membresía Pro de Immersive Translate](https://immersivetranslate.com/en/pricing/) (Recomendado)

[Aprender más](https://immersivetranslate.com/en/pricing/)

## Obtener la API oficial de DeepL a través de DeepL

1. Introducción oficial: [DeepL API](https://www.deepl.com/en/pro#developer)

   - Nota: [DeepL API](https://www.deepl.com/en/pro#developer) y [DeepL Pro](https://www.deepl.com/pro) son dos tipos de cuentas diferentes, y la cuenta de [DeepL API](https://www.deepl.com/en/pro/select-country#developer).

2. [Por qué](https://www.deepl.com/en/whydeepl) elegir DeepL?

   - Inglés ⇄ Chino 5x más preciso
   - Inglés ⇄ Japonés 6x más preciso
   - Motor de traducción basado en tecnología de inteligencia artificial (redes neuronales)

3. La API de DeepL se divide en [Free API y Pro API](https://www.deepl.com/en/pro#developer)

   - La Free API proporciona 500,000 caracteres gratuitos por mes.
   - La [tarifa oficial](https://www.deepl.com/en/pro#developer) para la Pro API es: $25 por 1 millón de caracteres.
   - Para un usuario de alta frecuencia, la cantidad de caracteres consumidos en un mes es de aproximadamente 10 millones de caracteres, y el precio es de aproximadamente: 250 USD

4. Para registrar una cuenta y abrir la [DeepL API](https://www.deepl.com/en/pro#developer).

## problemas comunes

### 1. La clave ingresada no está disponible.

DeepL API Pro y DeepL Pro son dos tipos de cuentas, la Auth Key que se puede usar en Immersive Translate es la cuenta de DeepL API, por favor haga clic aquí para [DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer)

### 2. Solución de problemas de errores de autenticación 401, 403

Estos errores suelen ocurrir cuando estás usando el tipo incorrecto de clave de autenticación. Por favor, ten en cuenta:

1. DeepL ofrece dos productos diferentes: DeepL Pro (servicio de traducción) y DeepL API (interfaz para desarrolladores)
2. Las claves encontradas en la configuración de tu cuenta de DeepL Pro **no son compatibles** con llamadas a la API
3. Necesitas registrarte específicamente para una cuenta de DeepL API para obtener una clave de API
4. Las claves de DeepL Free API se identifican por terminar con `:fx`
5. Las claves de DeepL Pro API no tienen el sufijo `:fx` y aparecen como una cadena regular de caracteres

Por favor, asegúrate de haberte registrado correctamente para el servicio de DeepL API, no solo para el servicio de traducción de DeepL Pro.

### 3. 456, Se ha alcanzado la cuota para el usuario.

El uso ha excedido el límite oficial máximo por usuario de DeepL, es posible que hayas violado la política de uso justo de DeepL y se te aconseja evitar tal comportamiento. Si eres un suscriptor de pago, el uso se restablecerá automáticamente el próximo mes.
