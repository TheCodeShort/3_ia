```toc
title: Redes neuronales
style: nestedOrderedList
minLevel: 1
maxLevel: 6
```

RAG son las siglas de **Retrieval-Augmented Generation** (Generación Aumentada por Recuperación). Es un **método o patrón de arquitectura de software** para desarrollo de IA.

# 🎯 ¿Cuál es su objetivo?

El objetivo de RAG es **darle conocimiento externo, privado y actualizado a un LLM** sin necesidad de volver a entrenar el modelo desde cero (lo cual costaría millones de dólares). Evita que la IA invente cosas (alucinaciones) obligándola a responder basándose únicamente en los documentos que tú le proporcionas.

# 🔄 Los 3 pasos del método RAG (Con el ejemplo de tu proyecto del SENA)

El proceso se divide exactamente en las piezas que ya conoces:

1. **Retrieval (Recuperación)**: Tú le haces una pregunta a tu Agente (Ej: _"¿Cómo hago el diagrama de clases de mi proyecto?"_). El sistema corre a tu base de datos en **Neon**, busca los **embeddings** de las guías del SENA más cercanos a tu duda y extrae esos fragmentos de texto exactos.
2. **Augmented (Aumentada)**: El sistema toma tu pregunta original y le **inyecta (aumenta)** los fragmentos de la guía que acaba de encontrar. El mensaje final que viaja de forma oculta a la IA se vuelve algo así: _"El estudiante pregunta esto. Basándote SOLO en este fragmento de la guía oficial del SENA que te adjunto aquí, responde su duda"_.
3. **Generation (Generación)**: El LLM lee la pregunta junto con el contexto real de tus guías y **genera** una respuesta perfecta, hiper-enfocada en tu plan de estudios y sin inventar metodologías raras.

En resumen: RAG es el método que une tus PDFs, los cortes (_chunks_), los _embeddings_, la base de datos vectorial y LangChain para crear tu Agente especializado.