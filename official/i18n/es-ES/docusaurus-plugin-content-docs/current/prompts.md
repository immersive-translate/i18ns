---
sidebar_position: 5
---
# Guía de Configuración de AI Prompt

## Resumen

Immersive Translate admite la configuración personalizada de Prompt para traducción con IA, permitiendo a los usuarios avanzados ajustar el comportamiento de la traducción según sus necesidades. Este documento proporciona instrucciones detalladas sobre los métodos de configuración, las variables admitidas y el uso avanzado.

## Variables Admitidas

### Variables Básicas

- `{{text}}` - El contenido de texto a traducir
- `{{from}}` - Idioma de origen
- `{{to}}` - Idioma de destino
- `{{content_type}}` - Tipo de texto original (`html` o `text`)

### Variables de Contexto
- `{{title_prompt}}` - Título de la página web (cuando esté disponible)
- `{{summary_prompt}}` - Resumen del contexto de la página web (cuando esté disponible)
- `{{terms_prompt}}` - Terminología profesional relacionada (cuando esté disponible)

## Métodos de Configuración

### 1. System Prompt(`systemPrompt`)
Solicitud de traducción enviada a la IA como identidad del sistema. Se utiliza para establecer el rol de la IA y las reglas básicas.

### 2. Prompt(`prompt`)
Conversación enviada a la IA como identidad del usuario, que contiene el contenido real que necesita ser traducido.

### 3. System Multiple Prompt(`systemMultiplePrompt`)
Solicitud de traducción enviada a la IA como identidad del sistema cuando el número de párrafos es mayor que 1. Se utiliza para manejar escenarios de traducción de múltiples párrafos.

### 4. Multiple Prompt(`multiplePrompt`)
Solicitud enviada como identidad del usuario para traducción de múltiples párrafos. Admite el uso de separadores o formato YAML.

### 5. Subtitle Prompt(`subtitlePrompt`)

Cuando se necesita traducción de subtítulos, conversación enviada a la IA como identidad del usuario, que contiene el contenido real que necesita ser traducido.

## Ejemplos de Configuración por Defecto

Si solo se recopila un párrafo, utilizará el Prompt de párrafo único por defecto. Si se recopilan múltiples párrafos, utilizará el Prompt de múltiples párrafos por defecto. La mayoría de los casos serán de múltiples párrafos. El separador predeterminado para múltiples párrafos es `%%`. Usamos deliberadamente este separador poco común para reducir las alucinaciones de los modelos grandes. Puede usar este Prompt como base para modificarlo según sus necesidades. Aquí están las configuraciones de Prompt predeterminadas:

### Traducción de Párrafo Único

```yaml
systemPrompt: |
    Eres un traductor nativo profesional de {{to}} que necesita traducir texto con fluidez a {{to}}.

    ## Reglas de Traducción
    1. Solo genera el contenido traducido, sin explicaciones ni contenido adicional (como "Aquí está la traducción:" o "Traducción como sigue:")
    2. La traducción devuelta debe mantener exactamente el mismo número de párrafos y formato que el texto original
    3. Si el texto contiene etiquetas HTML, considera dónde deben colocarse las etiquetas en la traducción mientras mantienes la fluidez
    4. Para el contenido que no debe traducirse (como nombres propios, código, etc.), mantén el texto original
    5. Genera la traducción directamente (sin separadores, sin texto adicional){{title_prompt}}{{summary_prompt}}{{terms_prompt}}
prompt: |
  Traduce a {{to}} (solo genera la traducción):

  {{text}}
```

### Traducción de Múltiples Párrafos

```yaml
multipleSystemPrompt: |
    Eres un traductor nativo profesional de {{to}} que necesita traducir texto con fluidez a {{to}}.

    ## Reglas de Traducción
    1. Solo genera el contenido traducido, sin explicaciones ni contenido adicional (como "Aquí está la traducción:" o "Traducción como sigue:")
    2. La traducción devuelta debe mantener exactamente el mismo número de párrafos y formato que el texto original
    3. Si el texto contiene etiquetas HTML, considera dónde deben colocarse las etiquetas en la traducción mientras mantienes la fluidez
    4. Para el contenido que no debe traducirse (como nombres propios, código, etc.), mantén el texto original{{title_prompt}}{{summary_prompt}}{{terms_prompt}}

    ## Ejemplos de Formato de Entrada-Salida

    ### Ejemplo de Entrada:
    Paragraph A

    %%

    Paragraph B

    %%

    Paragraph C

    %%

    Paragraph D

    ### Ejemplo de Salida:
    Translation A

    %%

    Translation B

    %%

    Translation C

    %%

    Translation D

multiplePrompt: |
  Traduce a {{to}}:

  {{text}}
subtitlePrompt: |
  Traduce a {{to}}:

  {{text}}
```

## Uso Avanzado (Formato YAML)

Para escenarios que requieren un control más preciso (por ejemplo, salidas de múltiples pasos), se puede usar el formato YAML para la configuración:

### Variables Avanzadas

- `{{yaml}}` - Datos de entrada en formato YAML

La variable 'yaml' predeterminada se ve así:

```
- id: 1
  text: Hello world
- id: 2
  text: How are you?
```

Esperamos por defecto que la salida del modelo grande sea así:

```
- id: 1
  text: 你好世界
- id: 2
  text: 你好吗？
```

Si usas el `{{yaml}}` predeterminado, necesitas expresar claramente esta expectativa en el prompt. Si deseas modificar el formato `yaml` predeterminado y de respuesta, esto no se puede resolver a través de la UI de la página de configuración de Immersive Translate. Debes editar directamente la configuración de usuario en formato JSON de Immersive Translate.

Ruta de edición de configuración de usuario: `Página de Configuración`->`Configuración de Desarrollador`->`Edit Full User Config` (Por favor, haz una copia de seguridad de tu configuración de usuario antes de editar)

Puedes encontrar la configuración del servicio de traducción en el JSON de la configuración de usuario (si no existe, simplemente agrégalo según esta estructura):

```
{
  ...
  "translationServices": {
    "openai": {
       ...
      }
  },
  ...

```

La variable `yaml` está compuesta por `env.imt_yaml_item`, por lo que puedes modificar el formato de `imt_yaml_item` así:

```json
  "translationServices": {
    "openai": {
       "env": {
          "imt_yaml_item": "- id: {{id}}\n  source: {{text}}"
        }
    }
   }
```

Otra variable especial es `imt_subtitle_yaml_item`, similar a `imt_yaml_item`, utilizada para elementos YAML de traducción de subtítulos.

Para otras variables `env`, puedes agregar cualquier variable `env` y usarla directamente en el prompt en el formato `{{nombre_variable}}`, como las siguientes variables `env` predeterminadas:

- `{{imt_source_field}}` - Nombre del campo de texto fuente (predeterminado: text)
- `{{imt_trans_field}}` - Nombre del campo de texto traducido (predeterminado: text)
- `{{imt_sub_source_field}}` - Nombre del campo de texto fuente de subtítulos
- `{{imt_sub_trans_field}}` - Nombre del campo de texto traducido de subtítulos

Incluyendo `title_prompt`, `summary_prompt`, `terms_prompt` también se configuran a través de `env`, predeterminado como sigue:

```
        "title_prompt": "\n\n## Conciencia del Contexto\nMetadatos del Documento:\nTítulo: 《{{imt_title}}》",
        "summary_prompt": "\n\n## Conciencia del Contexto\nMetadatos del Documento:\nResumen: {{imt_theme}}...",
        "terms_prompt": "\n\nTerminología Requerida: DEBES usar los siguientes términos durante la traducción. Si 'source':'target' y source == target, mantén el término fuente sin cambios.\n\n Términos -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## Conciencia del Contexto\nMetadatos del Documento:\nTipo: Subtítulo\nResumen: {{imt_theme}}...",
        "sub_terms_prompt": "\n\nTerminología Requerida: DEBES usar los siguientes términos durante la traducción. Si 'source':'target' y source == target, mantén el término fuente sin cambios.\n\n Términos -> \n\n {{imt_terms}}"

```

Donde `imt_title`, `imt_theme`, `imt_terms` son variables especiales inyectadas por el sistema. `imt_title` es el título, `imt_theme` es el resumen de toda la página web, `imt_terms` son los términos clave extraídos por el modelo.

> Nota: `imt_theme`, `imt_terms` son extraídos por un servicio propietario y actualmente solo están disponibles para [miembros Pro](https://immersivetranslate.com/pricing/).

### Ejemplo de YAML Prompt

```yaml
systemPrompt: |
  Eres un motor de traducción automática profesional y auténtico.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
    Recibirás una entrada en formato YAML que contiene entradas con campos "id" y "{{imt_source_field}}". Aquí está la entrada:

    <yaml>
    {{yaml}}
    </yaml>

    Para cada entrada en el YAML, traduce el contenido del campo "{{imt_source_field}}" a {{to}},{{html_only}} escribe la traducción de vuelta en el campo "{{imt_source_field}}" de esa entrada.

    Aquí hay un ejemplo del formato esperado:

    {{normal_result_yaml_example}}

    Por favor, devuelve el YAML traducido directamente sin etiqueta <yaml> o información adicional.
subtitlePrompt: |
    Recibirás una entrada de subtítulos en formato YAML que contiene entradas con campos "id" y "{{imt_sub_source_field}}". Aquí está la entrada:

    <yaml>
    {{yaml}}
    </yaml>

    Para cada entrada en el YAML, traduce el contenido del campo "{{imt_sub_source_field}}" a {{to}},{{html_only}} escribe la traducción de vuelta en el campo "{{imt_sub_source_field}}" de esa entrada.

    Aquí hay un ejemplo del formato esperado:

    {{subtitle_result_yaml_example}}

    Por favor, devuelve el YAML traducido directamente sin etiqueta <yaml> o información adicional.

```

`html_only` es una variable especial que solo existe cuando el texto original a traducir está en formato HTML. El valor es: `\n\nNota: Si el texto contiene etiquetas HTML, por favor considera después de traducir dónde deben estar las etiquetas en el resultado de la traducción, manteniendo al mismo tiempo la fluidez del resultado.`, esta variable solo existe cuando el usuario activa activamente "Traducción de Texto Enriquecido" en los servicios de traducción con IA. De lo contrario, está vacía.

`normal_result_yaml_example` se establece en `env`, el predeterminado es:

```
<example>
Input:
  - id: 1
    {{imt_source_field}}: Source
Output:
  - id: 1
    {{imt_trans_field}}: Translation
</example>
```

`subtitle_result_yaml_example` se establece en `env`, el valor predeterminado es:

```
<example>
Input:
  - id: 1
    {{imt_sub_source_field}}: ...
  - id: 2
    {{imt_sub_source_field}}: ...
  - id: 3
    {{imt_sub_source_field}}: ...
Output:
  - id: 1
    {{imt_sub_source_field}}: ...
  - id: 2
    {{imt_sub_source_field}}: ...
  - id: 3
    {{imt_sub_source_field}}: ...
</example>

```

Puedes sobrescribirlo en `env`.

## Ejemplo Avanzado: Traducción Reflexiva

Este ejemplo muestra cómo usar el formato YAML para implementar un flujo de traducción más complejo, que incluye dos pasos: traducción inicial y traducción optimizada:

```yaml
env:
  imt_source_field: source
  imt_trans_field: step2  # La traducción final usa el campo step2
  imt_sub_source_field: source
  imt_sub_trans_field: step2
  imt_yaml_item: |-
    - id: {{id}}
      {{imt_source_field}}: {{text}}
  imt_subtitle_yaml_item: |-
    - id: {{id}}
      {{imt_sub_source_field}}: {{text}}

systemPrompt: |
  Eres un motor de traducción automática profesional y auténtico.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
  Aquí está la entrada YAML:
  <yaml>
  {{yaml}}
  </yaml>
  
  Por favor, sigue estos pasos:
  1. Extrae el contenido del campo "source" del objeto YAML proporcionado.
  2. Traduce el contenido extraído a {{to}}. Coloca esta traducción inicial en el campo step1.
  3. Optimiza la traducción inicial de step1 para que sea más natural y comprensible en {{to}}. 
     Coloca esta traducción optimizada en el campo step2.
  4. Formatea el resultado como una matriz YAML con campos id, step1 y step2, como se muestra en este ejemplo:
  
  - id: 1 
    step1: Traducción inicial
    step2: Traducción optimizada
  
  Por favor, devuelve el YAML traducido directamente sin etiquetas <example_output> o información adicional.
```

### Descripción del Flujo de Trabajo

1. **Formato de Entrada**：
   ```yaml
   - id: 1
     source: "Hello world"
   - id: 2
     source: "How are you?"
   ```

2. **Pasos de Procesamiento de IA**：
   - Paso 1: Realiza la traducción inicial
   - Paso 2: Optimiza la traducción para que sea más natural y fluida

3. **Formato de Salida**：
   ```yaml
   - id: 1
     step1: "你好世界"
     step2: "你好，世界"
   - id: 2
     step1: "你怎么样？"
     step2: "你好吗？"
   ```
