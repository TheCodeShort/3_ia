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
