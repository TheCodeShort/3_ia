```toc
title: Redes neuronales
style: nestedOrderedList
minLevel: 1
maxLevel: 6
```
# 🧩 1. ¿Qué es un Framework (Marco de Trabajo)?

En programación, un _framework_ es una **caja de herramientas con plantillas y código ya prefabricado**.

- **Metáfora**: En lugar de talar árboles y fundir metal para construir una casa, compras piezas prefabricadas (paredes, tuberías).
- **En IA**: Te evita tener que escribir desde cero el código para conectar tu base de datos con la Inteligencia Artificial.

# 🎼 2. ¿Qué es Orquestar?

Orquestar significa **organizar, coordinar y encadenar varias tareas o modelos de IA** para que trabajen juntos en un orden específico.

- **Metáfora**: Un LLM (como ChatGPT) es un músico brillante, pero solo sabe tocar su instrumento. El "orquestador" es el director de la orquesta que le dice cuándo tocar, qué partitura seguir y cómo coordinarse con los demás músicos.
- **Ejemplo real**: Si creas una IA para atención al cliente, la orquestación hace esto de forma automática:
    1. _Paso 1_: Recibe el correo del cliente.
    2. _Paso 2_: Un LLM analiza si el cliente está enojado.
    3. _Paso 3_: Si está enojado, busca en la base de datos el historial de compras.
    4. _Paso 4_: Otro LLM redacta una disculpa personalizada usando esos datos.


# 🔗 3. ¿Qué es LangChain?

LangChain es, específicamente, el **framework (la herramienta) más famoso del mercado para orquestar LLMs**. Está escrito principalmente en Python y JavaScript.

- Te permite crear **"Cadenas" (Chains)**: Enlazar el texto que introduce el usuario con un LLM, y el resultado de ese LLM mandarlo a otra herramienta.
- Te permite crear **"Agentes"**: IAs autónomas que pueden decidir por sí mismas si necesitan usar Google, una calculadora o una base de datos para responderte.

## ¿Qué es el LCEL?

El **LangChain Expression Language (LCEL)** es un lenguaje que ayuda en la creación de flujos optimizados (_chains_) para procesar datos e interactuar con modelos de lenguaje (LLMs). Con el LCEL, puedes conectar diferentes etapas de un flujo de manera simple y eficiente, reduciendo el esfuerzo de codificación, optimizando el rendimiento y manteniendo el código más limpio.

## ¿Por qué usar el LCEL?

1 - **Flujos Simplificados**:

- Crea secuencias de pasos para procesar entradas y generar salidas de manera organizada.
- _Ejemplo_: Transformar un texto, analizarlo con un modelo y devolver el resultado formateado.

2 - **Ejecución Optimizada**:

- Permite procesar múltiples etapas simultáneamente, reduciendo el tiempo total de ejecución.
- _Ejemplo_: Consultar dos modelos (como **Gemini** y **Maritaca**) al mismo tiempo para validar respuestas cruzadas.

3 - **Facilidad de Integración**:

- La sintaxis intuitiva del LCEL permite conectar etapas usando operadores simples, como `|`, haciendo el flujo más legible.

## ¿Cómo funciona este lenguaje?

En el LCEL, puedes encadenar diferentes componentes (prompts, modelos, parsers) para crear un flujo de trabajo. Por ejemplo, el operador `|` (barra vertical) indica que la salida de una etapa es la entrada de la siguiente, permitiendo construir pipelines complejos de forma simple.

## ¿Cómo utilizar el LCEL?

A continuación, tenemos un ejemplo simplificado que demuestra el uso de LangChain y LCEL para:

- Recibir una imagen (codificada en base64).
- Analizarla a través de un modelo LLM (Google Generative AI).
- Extraer una descripción y etiquetas.
- Luego, generar un resumen final en español, validado y estructurado en formato JSON.

Observa cómo el uso de `|` facilita la conexión entre las etapas del flujo (prompt, modelo y parser):

```python
from langchain_google_genai import ChatGoogleGenerativeAI
from langchain_core.output_parsers import StrOutputParser, JsonOutputParser
from langchain.prompts import ChatPromptTemplate, PromptTemplate
from langchain.globals import set_debug
from my_keys import GEMINI_API_KEY
from my_models import GEMINI_FLASH
from my_helper import encode_image
from detalles_imagen_modelo import detallesimagenModelo

# Desactiva logs de depuración
set_debug(False)

# Instancia el modelo LLM con las credenciales y configuración adecuadas
llm = ChatGoogleGenerativeAI(
    api_key=GEMINI_API_KEY,
    model=GEMINI_FLASH
)

# Codifica la imagen en base64
imagen = encode_image("datos/ejemplo_grafico.jpg")

# Template para análisis de la imagen
template_analisador = ChatPromptTemplate.from_messages(
    [
        (
            "system",
            """
            Asume que eres un analizador de imágenes. Tu tarea es analizar la imagen
            y extraer información de forma objetiva.

            # FORMATO DE SALIDA
            Descripción de la Imagen: 'Inserta aquí tu descripción'
            Etiquetas: 'Inserta tres términos clave separados por comas'
            """
        ),
        (
            "user",
            [
                {"type": "text", "text": "Describe la imagen:"},
                {"type": "image_url", "image_url": {"url": "data:image/jpeg;base64,{imagen_informada}"}}
            ]
        )
    ]
)

# Cadena de análisis de la imagen: Template -> Modelo -> Salida en texto
cadena_analise_imagen = template_analisador | llm | StrOutputParser()

# Parser para transformar la salida final en un formato JSON validado por el modelo detallesimagenModelo
parser_json_imagen = JsonOutputParser(pydantic_object=detallesimagenModelo)

# Template para generar un resumen final, estructurando el resultado en JSON
template_respuesta = PromptTemplate(
    template=""" 
    Genera un resumen en lenguaje claro y objetivo, enfocado en el público latinoamericano.
    La comunicación debe ser simple, pensando en consultas futuras.

    # Resultado de la imagen
    {respuesta_cadena_analise_imagen}

    # FORMATO DE SALIDA
    {formato_salida}
    """,
    input_variables=["respuesta_cadena_analise_imagen"],
    partial_variables={
        "formato_salida": parser_json_imagen.get_format_instructions()
    }
)

# Cadena para resumir el resultado anterior en JSON
cadena_resumo = template_respuesta | llm | parser_json_imagen

# Combina las dos cadenas: primero análisis de la imagen, luego resumen formateado
cadena_completa = cadena_analise_imagen | cadena_resumo

# Ejecuta la cadena completa con la imagen proporcionada
respuesta = cadena_completa.invoke({"imagen_informada": imagen})

# Imprime la respuesta final estructurada en JSON
print(respuesta)
```

## Conclusión

El LCEL, junto con LangChain, permite orquestar cadenas de ejecución de forma simple y eficiente. El ejemplo anterior demuestra cómo partir de una imagen, extraer información relevante usando un LLM, y luego presentar los resultados en un formato estructurado, listo para su uso. Este enfoque agiliza el desarrollo, minimiza errores y facilita la integración en aplicaciones más complejas.

Para saber más sobre el LCEL y LangChain, explora la [documentación oficial](https://python.langchain.com/docs/concepts/lcel/) y profundiza en el universo de los LLMs, flujos optimizados y validaciones automatizadas.
