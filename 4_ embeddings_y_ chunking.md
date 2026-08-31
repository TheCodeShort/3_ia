```toc
title: Redes neuronales
style: nestedOrderedList
minLevel: 1
maxLevel: 6
```
# 🧩 ¿Qué son los Embeddings?

Un _embedding_ es la **traducción de una palabra, frase, imagen o video a una lista de números** (un vector) 

Las computadoras no entienden el significado de "perro" o "gato", solo entienden números. Un _embedding_ toma un concepto del mundo real y lo convierte en coordenadas numéricas dentro de un mapa gigante 

## 🎯 ¿Para qué sirven? (El "Mapa Matemático")

Sirven para que la IA entienda el **significado y el contexto** de las cosas midiendo la distancia entre esos números 

Si pones las palabras en un mapa gráfico basado en sus números:

- Las palabras **"perro"** y **"cachorro"** quedarán casi en el mismo punto del mapa porque son muy similares [1].
- La palabra **"manzana"** quedará muy lejos de "perro", pero muy cerca de "plátano" [1].
- **El truco mágico**: La IA puede hacer matemáticas con significados. Por ejemplo:
    - _Vector("Rey") - Vector("Hombre") + Vector("Mujer") = **Vector("Reina")**_. [[1]

## 🛠️ ¿Para qué los usas al crear una IA?

Cuando programas aplicaciones con frameworks como LangChain, usas _embeddings_ para:

- **Sistemas de recomendación**: Si a un usuario le gusta un libro, buscas qué otros libros tienen _embeddings_ (números) numéricamente más cercanos.

- **Búsqueda Semántica (Búsqueda por significado)**: Si el usuario busca "vehículo familiar", la IA sabe que debe mostrarle resultados de "camionetas" o "SUVs", aunque la palabra "vehículo" no aparezca en el texto.

- **Bases de datos vectoriales**: Es donde guardas estos números para que tu IA recuerde información de forma ultra rápida.

	-  **Las Vectoriales Puras**: Bases de datos como **Chroma**, **Pinecone** o **Milvus** se crearon desde cero _solo_ para guardar vectores (números) y hacer búsquedas matemáticas ultra rápidas.
	
	- **El caso de PostgreSQL y Neon**: PostgreSQL tiene una extensión oficial y muy poderosa llamada **`pgvector`**. Al activar esta extensión, transformas a PostgreSQL (y por ende a Neon, que está basado en Postgres) en una base de datos vectorial capaz de almacenar e indexar _embeddings_.

# ✂️ ¿Qué es el Chunking?

_Chunking_ significa **fragmentar o cortar un texto largo en pedazos más pequeños** (llamados _chunks_ o fragmentos).

Si tienes un libro de 300 páginas o un PDF de 50 hojas, no puedes meter todo ese texto junto a la IA para crear un solo _embedding_. Tienes que cortarlo en bloques (por ejemplo, párrafos de 500 palabras).

## 🤝 ¿Por qué se necesita para los Embeddings?

Hay dos razones técnicas fundamentales por las que están conectados:

- **Límite de Tokens (Capacidad)**: Los modelos que crean _embeddings_ (como los de OpenAI o Cohere) tienen un límite máximo de texto que pueden procesar de un solo golpe. Si te pasas, el sistema arroja un error.

- **Pérdida de Significado (Precisión)**: Recuerda que un _embedding_ convierte el significado de un texto en coordenadas numéricas. Si intentas convertir un libro entero en un solo vector, el número resultante será un promedio genérico de todo el libro y perderá los detalles. Al cortarlo en pedazos, cada fragmento tiene su propio vector preciso.

## 💡 Ejemplo Práctico

Imagina que estás creando una IA para consultar leyes:

1. **Chunking**: Cortas la constitución artículo por artículo (cada artículo es un _chunk_).
2. **Embedding**: Conviertes cada artículo por separado en su lista de números.
3. **Almacenamiento**: Guardas esos números en tu base de datos (como Neon con `pgvector`).

Cuando el usuario pregunte por el "Artículo de la libertad de expresión", la IA buscará el vector exacto de ese fragmento específico, no de toda la constitución.

