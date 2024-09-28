# Open AI (Azure OpenAI)

Acceso directo a los servicios de traducción de OpenAI abriendo una membresía de [Immersive Translate Pro](https://immersivetranslate.com/es/pricing/) (recomendado)

[Haz clic aquí para la presentación](https://immersivetranslate.com/es/pricing/)

## Obtén una clave API de la plataforma oficial de desarrolladores de OpenAI.

- [Dirección oficial de la API de openAI](https://openai.com/api/)
  - Nota: Actualmente, OpenAI no está abierto para el registro con números de teléfono chinos.
- Después de registrarte para una cuenta de OpenAI, abre [Clave Secreta de la API](https://platform.openai.com/account/api-keys) para crear una Clave Secreta de la API
- Luego solo tienes que llenar la clave en la configuración de OpenAI en la extensión de Immersive Translate.

## Advertencia

1. **Si no tienes una tarjeta de crédito vinculada, o eres un nuevo usuario de OpenAI 5-blade con hasta 3 solicitudes por minuto**, básicamente es inutilizable y es normal recibir errores. [Puedes hacer clic aquí para ver los límites de frecuencia para tu API](https://platform.openai.com/account/rate-limits)
2. La API de OpenAI y ChatGPT son dos servicios diferentes, la Extensión de Immersive Translate soporta la API de OpenAI, no la versión web de ChatGPT, por lo que necesitas abrir el servicio de API de OpenAI en lugar de abrir ChatGPT plus, y llenar la clave API en la página de Configuración después de abrir.
3. Error 429, significa que se ha superado el límite de frecuencia de openai, se recomienda reducir el número máximo de solicitudes por segundo, especialmente al traducir libros electrónicos, incluso si es una versión de pago, necesitas reducir el número máximo de solicitudes por segundo, y ajustarlo a 5 solicitudes por segundo para hacerlo más estable.
4. El modelo OpenAI gpt-3.5-turbo tiene un precio de: $0.002 / 1K tokens, y cuesta aproximadamente $1 traducir 660,000 caracteres en inglés y $0.25 para traducir 170,000 caracteres en inglés.
5. La Extensión de Immersive Translate soporta múltiples claves API para el equilibrio de carga, por favor usa una coma `,` para separar diferentes claves cuando llenes el formulario.

## Recomendación actual del número de solicitudes

Recientemente, OpenAI también se ha vuelto muy restrictivo para los usuarios pagos, a partir de la versión 0.5.0 el conteo de solicitudes predeterminado ha cambiado a segundos, y el número máximo predeterminado de solicitudes por segundo ha cambiado a 10 solicitudes por segundo.

## Azure OpenAI

El servicio de traducción de OpenAI también es compatible con la interfaz de Azure OpenAI. Primero, crea el servicio OpenAI en la consola de Azure, luego ve a Azure AI Studio: https://oai.azure.com, crea una implementación de gpt-35-turbo y recuerda el nombre de la implementación.

Después de desplegar el modelo gpt-35-turbo, abre la página de configuración de OpenAI para Immersive Translate:

1. Api Key Por favor, rellena la clave proporcionada por la consola de Azure.
2. Haz clic para expandir más configuraciones y establece la dirección personalizada a:

`https://{tu-nombre-personalizado}.openai.azure.com/openai/deployments/{tu-nombre-de-implementación}/chat/completions?api-version=2024-07-01-preview`

Cambia `{tu-nombre-personalizado}` por tu propio subdominio y `{tu-nombre-de-implementación}` por tu propio nombre de implementación.

3. El nombre del modelo necesita ser seleccionado manualmente para que el modelo personalizado pueda leer: `gpt-35-turbo`,

> Si aún tienes preguntas, puedes entrar en Azure AI Studio, abrir PlayGround, [Ver Código], y allí estarán el [EndPoint] y [Key] finales, como sigue:

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/azure-openai-key.jpg)

## Personalizando la Dirección de la API de OpenAI

- Esto se puede configurar a través de `Más Configuraciones` con el siguiente punto de entrada

---

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

---
