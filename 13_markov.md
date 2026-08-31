```toc
title: Redes neuronales
style: nestedOrderedList
minLevel: 1
maxLevel: 6
```

1. Modelos Ocultos de Markov (HMM) [[1](https://bibdigital.epn.edu.ec/handle/15000/23291)]

Son un caso específico y simplificado de las Redes Bayesianas Dinámicas.

- **Estructura**: El sistema es una cadena de estados ocultos (no medibles directamente) que cambian con el tiempo, donde cada estado genera una observación visible.
- **Propiedad clave**: Siguen la propiedad de Markov (el futuro solo depende del estado presente, no del pasado).
- **Uso en IA**: Reconocimiento de voz, procesamiento de lenguaje natural (etiquetado de palabras) y bioinformática.

2. Filtros de Kalman y Filtros de Partículas

Son modelos secuenciales diseñados para estimar el estado de un sistema dinámico a partir de mediciones ruidosas.

- **Estructura**: Se pueden ver como una Red Bayesiana Dinámica continua. El Filtro de Kalman asume variables continuas y distribuciones lineales-gaussianas. El Filtro de Partículas maneja sistemas no lineales y no gaussianos mediante simulación de Monte Carlo.
- **Uso en IA**: Navegación de vehículos autónomos, seguimiento de objetos en video (robótica) y trayectorias en Google Maps.

3. Campos Aleatorios de Markov Dinámicos (Dynamic MRFs)

A diferencia de las Redes Bayesianas (que usan flechas dirigidas), estos modelos utilizan **grafos no dirigidos** que evolucionan en el tiempo.

- **Estructura**: Las relaciones son simétricas (influencia mutua) en lugar de causa-efecto. Su versión dinámica permite que los pesos y la estructura de las conexiones cambien con cada paso de tiempo.
- **Uso en IA**: Visión por computadora (segmentación de video en movimiento) y física estadística.

4. Campos Aleatorios Condicionales (CRF)

Son modelos gráficos no dirigidos "discriminativos" que calculan la probabilidad condicional de una secuencia de etiquetas dado un conjunto de observaciones. [[1](https://medium.com/soldai/ner-m%C3%A9todos-supervisados-ii-m%C3%A1quina-de-soporte-vectorial-y-campos-aleatorios-condicionales-1ccf56625ec6)]

- **Estructura**: Modelan directamente la relación de dependencia entre las etiquetas consecutivas para datos secuenciales.
- **Uso en IA**: Extracción de entidades en texto y reconocimiento de estructuras en documentos.

---

Comparación de Modelos Probabilísticos

| Modelo                                | Tipo de Grafo       | Manejo del Tiempo | Tipo de Variables         |
| ------------------------------------- | ------------------- | ----------------- | ------------------------- |
| **Red Bayesiana Estándar**            | Dirigido (DAG)      | No (Fijo)         | Discretas o Continuas     |
| **Red Bayesiana Dinámica (DBN)**      | Dirigido (DAG)      | Sí (Evolutivo)    | Discretas o Continuas     |
| **Modelos Ocultos de Markov (HMM)**   | Dirigido (Cadena)   | Sí (Secuencial)   | Estados discretos ocultos |
| **Filtros de Kalman**                 | Dirigido (Continuo) | Sí (Tiempo Real)  | Continuas (Gaussianas)    |
| **Campos Aleatorios de Markov (MRF)** | No Dirigido         | No (Fijo)         | Discretas o Continuas     |

---