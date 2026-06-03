🐍 Semana 1: Consolidación de Python (Fundamento Vital)

Todo lo que verás en agentes e ingeniería de IA corre bajo Python. Si no dominas las bases de código, te costará seguir los ejercicios.

- **Qué estudiar:**
    - Variables, tipos de datos (strings, enteros) y estructuras de control (`if`, `for`, `while`).
    - Colecciones de datos esenciales: **Listas** y **Diccionarios** (estos últimos se usan todo el tiempo para manipular datos de IA).
    - Definición y uso de **Funciones** (`def`) y manejo de archivos locales.
- **Recurso recomendado:** Busca cursos gratuitos de "Python desde cero" en YouTube o la misma plataforma de Alura si tienes acceso previo.

🌐 Semana 2: APIs, Formato JSON y Entornos Virtuales

Los agentes de IA y la automatización consisten en conectar aplicaciones entre sí. Para ello, necesitas entender cómo viaja la información en la web.

- **Qué estudiar:**
    - **¿Qué es una API?** Entiende los conceptos de peticiones HTTP (`GET`, `POST`) y códigos de respuesta (200, 404, 500).
    - **Formato JSON:** Aprende a leer y estructurar un archivo JSON, ya que es el lenguaje universal con el que responden los modelos de OpenAI, Oracle y Gemini.
    - **Entornos virtuales en Python:** Aprende a usar `venv` o `conda` y cómo instalar librerías usando `pip install`.

🤖 Semana 3: Introducción a la Ingeniería de Prompts y n8n

Antes de programar IA con código complejo, debes entender la lógica de las instrucciones y el flujo visual de los datos.

- **Qué estudiar:**
    - **Prompt Engineering:** Investiga técnicas avanzadas como _Few-Shot Prompting_ (darle ejemplos a la IA) y _Chain-of-Thought_ (pedirle que piense paso a paso).
    - **Conceptos de n8n:** Crea una cuenta gratuita en la nube de **n8n** o mira tutoriales básicos. Entiende qué es un _Trigger_ (disparador), un _Node_ (nodo) y un _Workflow_ (flujo de trabajo).

🗄️ Semana 4: Conceptos de Datos e IA Moderna (Sin Código)

La última parte del módulo habla de "Embeddings" y "RAG". No necesitas programarlos aún, solo entender conceptualmente qué son.

- **Qué estudiar:**
    - **Bases de Datos Vectoriales:** Entiende la diferencia entre una base de datos tradicional (tablas) y una vectorial (coordenadas matemáticas).
    - **Concepto de RAG:** Busca qué significa _Retrieval-Augmented Generation_. En términos sencillos, es ponerle un "libro de respuestas en la mano" a ChatGPT para que no invente cosas.

---

🛠️ Herramientas que debes instalar ya mismo

Para ganar tiempo, deja tu computadora lista con el software que usarás en el día a día:

1. **Visual Studio Code (VS Code):** El editor de código estándar.
2. **Python (Versión 3.10 o superior):** Asegúrate de marcar la casilla "Add Python to PATH" durante la instalación.
3. **Git:** Configúralo en tu terminal para que puedas conectar tu entorno local con GitHub.

--- 

# FALTA APRENDER 
1. Memoria del Agente (Conversational Memory)

Los LLMs no recuerdan nada de la pregunta anterior. Si le dices _"No entendí el punto 2"_, la IA no sabrá de qué hablas a menos que le pases el historial.

- **Lo que faltó**: Decidir cómo guardar el historial de chat. ¿Lo guardamos en la memoria RAM del servidor (se borra si se reinicia) o usamos una tabla en **Neon/PostgreSQL** para que el Agente recuerde tus charlas de hace una semana? Con LangChain debes configurar un componente llamado `ChatMessageHistory`.

2. Evaluación del RAG (RAG Triad & Métricas)

¿Cómo sabes si los fragmentos de texto (_chunks_) que recupera tu base de datos son los correctos o si la IA está respondiendo con coherencia?

- **Lo que faltó**: Frameworks de evaluación como **Ragas** o **TruLens**. Te permiten medir con números tres cosas: si la base de datos encontró la guía correcta (**Context Relevance**), si la IA usó solo esa guía para responder (**Groundedness**), y si la respuesta de la IA de verdad contesta tu duda (**Answer Relevance**).

3. Guardrails (Sistemas de Seguridad)

¿Qué pasa si en lugar de estudiar, le pides a tu Agente del SENA que te escriba un poema de amor o te dé una receta de cocina? Estarías gastando dinero de tu API en cosas que no son de tu carrera.

- **Lo que faltó**: Implementar herramientas como **NVIDIA NeMo Guardrails** o filtros por código. Son reglas estrictas que bloquean la pregunta del usuario antes de que llegue a la API de OpenAI si detectan que te saliste del tema de Análisis de Software.

4. Estrategias de Orquestación Avanzada (Routing y Re-ranking)

- **Routing (Enrutamiento)**: Si le preguntas _"¿Cuándo es la entrega del taller?"_, el Agente no debe ir a buscar en los libros de programación. Debe ser capaz de decidir: _"Esta pregunta es de calendario, voy a mirar el Webhook"_ o _"Esta pregunta es teórica, voy a buscar los embeddings"_.
- **Re-ranking**: Cuando buscas en Neon, la base de datos te puede devolver 10 fragmentos de texto. Un modelo de _Re-ranking_ (como Cohere Rerank) los vuelve a ordenar para asegurarse de que los 2 fragmentos más ultra-precisos queden arriba del todo antes de enviárselos a la IA.

5. Monitoreo en Producción (LLMOps)

Una vez que subas tu código a internet (Render/Railway), necesitas ver qué está pasando "por dentro" cuando el agente falla o se pone lento.

- **Lo que faltó**: Integrar herramientas gratuitas de monitoreo como **LangSmith** (de los mismos creadores de LangChain) o **Phoenix**. Te muestran visualmente cuánto tardó cada embedding, cuánto costó cada pregunta y en qué paso exacto de la cadena hubo un error.

---