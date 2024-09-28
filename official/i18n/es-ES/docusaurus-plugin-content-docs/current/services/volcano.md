# Traducción de Volcán

## Declaración Breve

1. Sitio Web Oficial: [Traducción Automática - Motor de Volcán](https://www.volcengine.com/product/machine-translation)
2. Descripción oficial de tarifas: [Facturación de Producto Traducción Automática - Motor de Volcán](https://www.volcengine.com/docs/4640/68515)
3. El Traductor de Volcán es gratuito para los primeros 2 millones de caracteres por mes, y cobrará $49 por cada millón de caracteres que excedan, por favor consulte el documento oficial de tarifas para más detalles.

## Pasos para la Aplicación

1. [Visión General del Proceso de Acceso API Traducción Automática - Motor de Volcán](https://www.volcengine.com/docs/4640/130872), siga la guía oficial para completar los tres pasos de registrar una cuenta, autenticación con nombre real y apertura de servicios. Esto se debe hacer desde la consola, [Consola del Motor de Volcán](https://console.volcengine.com/home)
2. En el cuarto paso para obtener la clave, el Motor de Volcán proporciona dos opciones:
   1. Continuar para crear (usando la cuenta principal para crear la clave, más conveniente, esta clave puede llamar a los recursos de la cuenta principal, menos seguro), seleccione "Continuar para crear", la tabla aparecerá en un nuevo dato, que contiene el "ID de Clave de Acceso" y "Clave de Acceso Secreta" que queremos usar.
   2. Ir a crear un nuevo subusuario (se recomienda usar subusuario para crear la clave por más seguridad), obtener el "ID de Clave de Acceso" y "Clave de Acceso Secreta", esta subcuenta debe tener el permiso `TranslateFullAccess`.
3. Abrir Configuración Básica - Servicios de Traducción para Immersive Translate y encontrar la opción de Traducción de Volcán para rellenar.
4. Hecho 🎉, si tiene alguna duda, por favor deje su comentario [aquí](https://github.com/immersive-translate/immersive-translate/issues/137).
