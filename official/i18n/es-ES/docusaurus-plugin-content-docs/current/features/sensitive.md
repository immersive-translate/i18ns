---
sidebar_position: 7
---

# Modo de privacidad (Beta)

## Guía de enmascaramiento de información sensible

> Esta función es compatible con la versión 1.23.1+ del plugin.

Después de habilitar [OneAIFW](https://github.com/funstory-ai/aifw) integrado o personalizado, el plugin identificará y enmascarará automáticamente la información sensible (como direcciones de correo electrónico, números de teléfono, números de identificación, etc.) durante la traducción para proteger su privacidad y seguridad. Esta guía le mostrará cómo ver qué información sensible ha sido identificada y enmascarada durante la traducción.

### Ver registros de enmascaramiento

#### Paso 1: Habilitar el registro

1. Abra la [**página de configuración del desarrollador**](https://dash.immersivetranslate.com/#advanced) del plugin
2. Habilite la opción **"Habilitar registro de consola"**

#### Paso 2: Abrir la consola del desarrollador

1. Presione `F12` en la página web (o haga clic derecho en la página y seleccione "Inspeccionar" / "Inspeccionar elemento")
2. Cambie a la pestaña "Console" (Consola)

#### Paso 3: Filtrar registros de enmascaramiento

Ingrese `sensitive-` en el cuadro de filtro de la consola para filtrar todos los registros relacionados con el enmascaramiento de información sensible.

### Explicación del formato de registro

En la consola, verá registros en el siguiente formato:

```
[sensitive-encode] "Correo: tester.cn+alias@example.com" -> "Correo: __PII_EMAIL_ADDRESS_1__"

[sensitive-decode] "Correo: __PII_EMAIL_ADDRESS_1__" -> "Correo: tester.cn+alias@example.com"
```

#### Significado de los registros

- **`[sensitive-encode]`**: Indica el proceso de identificación y enmascaramiento de información sensible
  - El lado izquierdo es el texto original (que contiene información sensible)
  - El lado derecho es el texto enmascarado (`__PII_*` es el marcador de posición de enmascaramiento)

- **`[sensitive-decode]`**: Indica el proceso de restauración del texto enmascarado
  - El lado izquierdo es el texto enmascarado (que contiene marcadores de posición)
  - El lado derecho es el texto original restaurado

#### Explicación de los marcadores de posición

Los marcadores de posición en formato `__PII_*` representan el tipo de información sensible que ha sido enmascarada, por ejemplo:
- `__PII_EMAIL_ADDRESS_1__`: Dirección de correo electrónico
- `__PII_PHONE_NUMBER_1__`: Número de teléfono
- `__PII_ID_CARD_1__`: Número de identificación
- etc.

### Principios de enmascaramiento

Para los principios específicos y los detalles de implementación del enmascaramiento de información sensible, puede consultar la documentación y el código del [proyecto OneAIFW](https://github.com/funstory-ai/aifw).

### Notas

- Esta función se encuentra actualmente en **fase de prueba beta**, y puede haber casos de identificación inexacta o fallos de enmascaramiento
- Si encuentra fallos de enmascaramiento o errores de identificación, envíe comentarios a través de [GitHub Issues](https://github.com/funstory-ai/aifw/issues), y continuaremos iterando y optimizando

