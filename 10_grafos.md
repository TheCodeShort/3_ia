```toc
title: Redes neuronales
style: nestedOrderedList
minLevel: 1
maxLevel: 6
```

[[14_machine_learning]]

![[1_grafo.png]]

![[2_ramas_ia.png]]

En la Inteligencia Artificial, los **grafos** son ==estructuras matemáticas y computacionales que se utilizan para **representar y analizar información compleja basándose en las relaciones entre los datos**, en lugar de tratarlos como variables aisladas==. [[1](https://www.caixabanktech.com/es/blogs/grafos-y-redes-neuronales-como-la-ia-transforma-las-conexiones-en-valor/), [2](https://www.youtube.com/watch?v=1aqVM8R-Qv0&t=624)]


# Anatomía básica de un grafo

Cualquier sistema basado en grafos se compone de dos elementos fundamentales: [[1](https://www.instagram.com/p/DQG5lzOCD0F/)]

##  **Nodos (o Vértices)**
Representan las entidades individuales u objetos (por ejemplo: un usuario, un concepto, un medicamento, una ciudad). 

[[1](https://translate.google.com/translate?u=https://www.linkedin.com/pulse/graph-theory-artificial-intelligence-applications-impact-abirami-ckfgc&hl=es&sl=en&tl=es&client=sge), [2](https://unade.edu.mx/que-son-los-grafos/)]

## **Aristas (o Enlaces)**

Representan la conexión, acción o relación con significado semántico que une a dos nodos (por ejemplo: "es amigo de", "es un síntoma de", "está conectado por carretera con").

Las ==**aristas son las conexiones, relaciones o enlaces que unen a los nodos entre sí**==.

Si los nodos son los "objetos" (personas, lugares, canciones), las aristas son el **"pegamento" o el puente que explica cómo se relacionan esos objetos**. Sin las aristas, los datos estarían completamente aislados y la Inteligencia Artificial no podría entender el contexto.

Para entenderlo a fondo de forma práctica, las aristas tienen tres características clave que los programadores de IA configuran en el código:


### Representan un significado (Semántica)

Una arista no es solo una línea vacía; siempre describe **qué tipo de relación** existe entre dos nodos. Por ejemplo:

- Nodo A (**Juan**) => es amigo de => Nodo B (**Pedro**)
- Nodo A (**Usuario_123**)  => compró => Nodo B (**Laptop Asus**)
- Nodo A (**París**) => es la capital de => Nodo B (**Francia**)

### Pueden tener dirección (Direccionalidad)

Las aristas pueden ser de dos tipos según cómo fluya la relación:

- **Dirigidas (Un solo sentido):** Como en Twitter o Instagram. Tú puedes seguir a un famoso (arista que va de ti hacia el famoso), pero el famoso no necesariamente te sigue a ti.
- **No dirigidas (Bidireccional):** Como en Facebook o LinkedIn. Ser amigos o conectar requiere que ambos lados estén de acuerdo; la relación va en ambos sentidos al mismo tiempo.

## Pueden tener importancia o costo (Pesos)

En la IA, las aristas suelen llevar un número asignado llamado **"peso"**. Esto le dice al algoritmo qué tan fuerte, costosa o cercana es una relación:

- **En Google Maps:** El nodo es una intersección y el otro nodo es otra esquina. La arista es la calle, y su "peso" es el tiempo de tráfico (por ejemplo, 5 minutos). La IA busca el camino sumando los pesos más bajos.

- **En Spotify:** Si escuchas una canción una sola vez, la IA crea una arista débil (peso: 1). Si la escuchas en bucle 50 veces, la arista se vuelve gruesa y fuerte (peso: 50). Así la IA sabe que esa relación es prioritaria para recomendarte música similar.

- [[1](https://www.youtube.com/watch?v=QyAz3wr9i-M), [2](https://translate.google.com/translate?u=https://www.linkedin.com/pulse/graph-theory-artificial-intelligence-applications-impact-abirami-ckfgc&hl=es&sl=en&tl=es&client=sge


---

## ¿Por qué son cruciales para la Inteligencia Artificial?

A diferencia de las bases de datos tradicionales en tablas (filas y columnas), los modelos de IA modernos aprovechan los grafos debido a que el mundo real no funciona de forma aislada. El uso de grafos aporta ventajas determinantes: [[1](https://www.caixabanktech.com/es/blogs/grafos-y-redes-neuronales-como-la-ia-transforma-las-conexiones-en-valor/)]

- **Comprensión del Contexto**: Permiten a los algoritmos de IA "entender" no solo el dato en sí, sino todo su entorno relacional y jerárquico. [[1](https://www.caixabanktech.com/es/blogs/grafos-y-redes-neuronales-como-la-ia-transforma-las-conexiones-en-valor/), [2](https://translate.google.com/translate?u=https://www.linkedin.com/pulse/graph-theory-artificial-intelligence-applications-impact-abirami-ckfgc&hl=es&sl=en&tl=es&client=sge)]

- **Eficiencia en Datos Complejos**: Estudiar estructuras de alta complejidad (como redes sociales o cadenas moleculares) es mucho más rápido y preciso. [[1](https://www.grapheverywhere.com/inteligencia-artificial-y-ml-uso-de-grafos-en-proyectos-de-ia-y-ml/), [2](https://cidai.eu/es/masterclass/la-inteligencia-artificial-aplicada-a-grafos-graph-neural-networks/), [3](https://siigroup-spain.com/base-de-datos-orientadas-a-grafos/)]

- **Razonamiento Lógico**: Proporcionan un marco estructurado que ayuda a la IA a deducir conclusiones lógicas y evitar errores o "alucinaciones" de texto plano. [[1](https://gnoss.com/grafo-de-conocimiento), [2](https://razonpublica.com/saber-vs-saber/)]

---



# Tipos de grafos
## Grafos de Conocimiento (Knowledge Graphs)

Son redes masivas de datos interconectados que le dan un significado semántico a la información. En lugar de buscar palabras clave sueltas, la IA mapea conceptos interconectados. [[1](https://www.youtube.com/watch?v=QyAz3wr9i-M), [2](https://www.proof-reading-service.com/es/blogs/ai-in-scholarly-publishing/how-ai-knowledge-graphs-improve-research-efficiency-and-connectivity), [3](https://gnoss.com/grafo-de-conocimiento), [4](https://www.couchbase.com/es/resources/concepts/knowledge-graphs/)]

- **Ejemplo práctico**: El buscador que impulsa la tecnología de Google Knowledge Graph para entender conexiones exactas entre celebridades, lugares o fechas, u optimizar sistemas avanzados de IA mediante arquitecturas empresariales descritas por firmas como [![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABEAAAARCAYAAAA7bUf6AAACM0lEQVR4AaxSTWsTURS9701oI7VdSFu0EBCL6Eb6B6ToWhERzc6ViHTqQpJYMlWIEZKGNMli0EnESkHc6NatG6k/wIUbF4JuhCBYGhnSGOZd75nOyJTZ9jFn7jsf987kTTQdwUoNcV13ZqPtfdvoeH6j3VvCM1DBocOHlkRqiD/O9InUzdGUNcdkPpMsVHAS/cCnQys1RBENWKssDcxxSQ4FuIbgoU78B0ISqSFncrMLKjDvJzX3LW1dRBgVHPpibu4UtCRSQ/L5fOCU7FmnaCvD5pacw1dUcOjwkwOwTw2BCEjzTyIekqFV1AMOJ41DQ+qt7u1K5d2ENLxUip6VC/ZT56H9ARW80e724COXHPV/SKPVXVOKXxP50JaZ6Vxt8/mTGOBMfBk+csjHg9BAjZZXM4ptEXcF0cXzWutcDPlJ85FBitQe8uiDphsdr8ZE19aL9mkxw6EwyOhNp7hyJwZ4qEc35KXval1eQJqUI6d+AZ68rkIFlOaFpvtiMQY4dCDOSd+SnNW6ZuaR676ZqWxvZyUwTfSdsJjUq2AcfIkBDj3yp5HvbG2dEG1fB2zO++PBbvb3cKDYWq5Wq/vyJEOGr8h/41gMcOjwkUN+tPf3F/r149L9HxLMlAsrk+XSvU8ymdiauMSa3jabvbPgqODQwZFDHn3olzOBTKyU4nAnt0cP7vYzim4EVrBTb3s+qnyS69DFDq8oH/bEQ0IjeVsr2B+d4upJ+QpTYS3YO0k/uf8HAAD//32kFwcAAAAGSURBVAMASDcjMr+YzkgAAAAASUVORK5CYII=)⁠IBM](https://www.ibm.com/es-es/think/topics/knowledge-graph). [[1](https://translate.google.com/translate?u=https://www.linkedin.com/pulse/graph-theory-artificial-intelligence-applications-impact-abirami-ckfgc&hl=es&sl=en&tl=es&client=sge), [2](https://www.ibm.com/es-es/think/topics/knowledge-graph)]

## Redes Neuronales de Grafos (GNNs)

Son arquitecturas especializadas de Aprendizaje Profundo (_Deep Learning_) diseñadas para procesar datos directamente en forma de red. [[1](https://www.caixabanktech.com/es/blogs/grafos-y-redes-neuronales-como-la-ia-transforma-las-conexiones-en-valor/)]

- **Ejemplo práctico**: Se utilizan para predecir si una molécula servirá como medicamento efectivo analizando los enlaces de sus átomos, o para descubrir patrones de lavado de dinero en transacciones bancarias interconectadas, según analizan expertos en innovación de CaixaBank Tech. [[1](https://www.caixabanktech.com/es/blogs/grafos-y-redes-neuronales-como-la-ia-transforma-las-conexiones-en-valor/)]

## Sistemas de Recomendación y Logística

Plataformas de streaming o comercio electrónico analizan el grafo de usuarios y productos para predecir qué te gustará basándose en comportamientos de perfiles similares. Asimismo, optimizan rutas físicas calculando trayectorias óptimas en mapas de transporte reales. [[1](https://www.youtube.com/watch?v=1aqVM8R-Qv0&t=624), [2](https://www.youtube.com/watch?v=QyAz3wr9i-M), [3](https://www.youtube.com/watch?v=pKVGl7Y6DRU&t=3), [4](https://www.campusbigdata.com/blog/como-aplicar-la-teoria-de-grafos-en-big-data/), [5](https://www.couchbase.com/es/resources/concepts/knowledge-graphs/)]

---

# Heuristica
una ==**heurística es un "atajo mental" o una regla práctica que sirve para resolver un problema de forma rápida**==, especialmente cuando el problema es tan complejo que buscar la solución perfecta tardaría años.

En lugar de revisar absolutamente todas las opciones posibles (lo cual consumiría demasiada memoria y tiempo), la Inteligencia Artificial usa una heurística para **adivinar de forma inteligente** cuál es el mejor camino a seguir.

Para entenderlo a fondo, mira este ejemplo de la vida real y luego cómo se aplica en la IA:

---

El ejemplo de la vida real (Cómo lo usas tú)

Imagina que entras a un supermercado gigante que no conoces y buscas **leche**.

- **Solución Perfecta (Algoritmo estricto):** Recorrer cada pasillo, estante por estante, desde la entrada hasta la salida. Encontrarás la leche seguro, pero tardarás una hora.
- **Solución Heurística (Atajo inteligente):** Usas la regla práctica _"los lácteos y la comida fría suelen estar al fondo del supermercado"_. Caminas directo al fondo. No tienes la certeza matemática de que esté ahí, pero tu experiencia te dice que es el lugar más probable. Ahorraste 50 minutos.

---

¿Cómo se aplica en la Inteligencia Artificial?

En la IA, las heurísticas se programan como funciones matemáticas que le asignan una "puntuación" o una estimación a cada opción disponible.

1. **En los videojuegos (Ajedrez o Juegos de Estrategia)**  
    En el ajedrez hay trillones de jugadas posibles. Una IA no puede calcular todas las combinaciones hasta el final de la partida porque la computadora se colgaría. En su lugar, usa una **función heurística**: le da puntos a las piezas (Peón = 1 punto, Reina = 9 puntos). La IA elige el movimiento que maximice sus puntos en los próximos 3 o 4 turnos, asumiendo que esa es una buena posición.
2. __En Google Maps (Algoritmo A_)_*  
    Para calcular la ruta de un país a otro, el algoritmo usa una heurística muy famosa: **la distancia en línea recta (como vuela un pájaro)**. Aunque las calles tienen curvas y semáforos, medir la distancia en línea recta hacia tu destino le ayuda a la IA a descartar instantáneamente carreteras que te desvían en la dirección opuesta, encontrando la ruta en milisegundos.
3. **En los Antivirus**  
    Los antivirus tradicionales buscan firmas (el "ADN" exacto de un virus conocido). Los antivirus modernos usan **análisis heurístico**: observan el comportamiento de un archivo. Si el archivo intenta modificarse a sí mismo, ocultarse y duplicarse, la heurística de la IA dice: _"No sé exactamente qué virus es, pero se comporta como uno"_, y lo bloquea.

---

En resumen

|Tipo de Búsqueda|Enfoque|Ventaja|Desventaja|
|---|---|---|---|
|**Algoritmo Exacto**|Revisa el 100% de los datos.|Garantiza la solución perfecta.|Es extremadamente lento y costoso.|
|**Heurística (IA)**|Usa un atajo inteligente.|Es ultra rápido y eficiente.|La solución es buena, pero puede no ser la óptima.|

La heurística es, literalmente, enseñarle a la IA a tener **"sentido común" matemático** para tomar decisiones rápidas.



# Pasos para construir un grafo

Para construir un grafo en código desde cero, de forma limpia y profesional, ==debes seguir una metodología estricta de **5 pasos lógicos**==. Esto aplica tanto si programas en Python, Java o cualquier otro lenguaje.

Aquí tienes la guía definitiva paso a paso, enfocada en la arquitectura del software:


## 🌟 Paso 1: Definir el Objetivo del Mapa (La Planificación)

Antes de tocar una sola línea de código, debes responder en papel a tres preguntas críticas. El objetivo del sistema dictará cómo diseñarás tus estructuras en los siguientes pasos:

- **¿Qué serán los Nodos?** (¿Productos de PC? ¿Pasillos de almacén? ¿Variables de probabilidad?).
- **¿Qué significan las Aristas?** (¿Compatibilidad? ¿Distancia en metros? ¿Causa y efecto?).
- **¿Qué medirá el Peso?** (¿Probabilidad de compra? ¿Tiempo de tráfico? ¿Costo de envío?).

## 📦 Paso 2: Crear el Molde de los Nodos (La Clase Individual)

Siguiendo la filosofía de la Programación Orientada a Objetos (POO), necesitas diseñar la unidad básica del grafo.

- Creas una **Clase** (por ejemplo, `class Producto` o `class Ubicacion`).
- Dentro de esta clase, defines las variables o atributos estáticos que cada punto del mapa debe tener obligatoriamente de forma interna (como su nombre, su id único o su categoría).
- Este molde **no sabe nada de conexiones todavía**, solo se preocupa por almacenar los datos limpios de la entidad que representa.

## 🗺️ Paso 3: Crear el Contenedor Global (La Clase Grafo)

Ahora necesitas un "cerebro" o una estructura contenedora que controle a todos los nodos juntos.

- Creas una segunda **Clase principal** (por ejemplo, `class RedDeRecomendacion` o `class GrafoAlmacen`).
- Al arrancar esta clase, creas una variable vacía en su memoria, por lo general un **Diccionario** o una **Matriz**. Esta variable será el archivador central donde se guardará todo el mapa físico.

## ➕ Paso 4: Programar las Funciones de Crecimiento (Las Acciones)

Un grafo funcional debe ser capaz de expandirse dinámicamente. Dentro de la Clase del Grafo del Paso 3, debes programar obligatoriamente dos funciones esenciales:

- **Función para Registrar Nodos**: Toma un objeto del Paso 2 y lo mete en el archivador central del Paso 3, abriéndole un espacio limpio y único en el mapa.
- **Función para Conectar Aristas**: Recibe el nombre de un punto A y un punto B, dibuja un "túnel" o flecha entre ellos en el código y le asigna un número (el Peso) que indica la fuerza o costo de esa relación.

## 🤖 Paso 5: Programar el Algoritmo de Decisión (La Inteligencia)

Con el mapa ya construido y conectado, necesitas el motor que extraiga valor de esos datos.

- Creas una función final (como tu función de `a_star` o de cálculo de `Bayes`).
- Esta función toma un punto de partida y un objetivo, recorre el diccionario del mapa saltando de nodo en nodo a través de las aristas, evalúa los pesos matemáticos o las probabilidades de los vecinos, y **toma una decisión automatizada** (como mostrar la ruta de recolección más rápida o sugerir el componente de PC ideal).

---

Si dominas este orden mental $$Objetivo \rightarrow \ Nodo \rightarrow \ Grafo \rightarrow \ Conexiones \rightarrow \ Algoritmo$$ podrás estructurar e interpretar cualquier sistema de Inteligencia Artificial basado en redes en tu carrera o tareas.

# Tablas de Probabilidad

**por qué la Inteligencia Artificial no es perfecta ni mágica, sino que se basa en apuestas matemáticas calculadas**. ==La IA no sabe el futuro con un 100% de certeza; lo que hace es usar la teoría de la probabilidad para manejar la **incertidumbre**== (lo que no se puede predecir con exactitud).

Para entenderlo a fondo para tu curso, aquí tienes la explicación detallada de cada concepto aplicado directamente a la IA, tus grafos y tu tienda de componentes de PC:

---

##  ¿Qué nos quiere dar a entender? (La idea clave)

En el mundo real (y en tu negocio de PC), los clientes y los sistemas son impredecibles. No puedes saber con certeza si el próximo cliente que entra va a comprar una RTX 4070 o un mouse. Como no tienes una bola de cristal, usas la **probabilidad**. Recolectas datos del pasado para calcular el porcentaje de opciones y tomar **decisiones bien fundamentadas** en lugar de adivinar al azar.

---

## Desglose detallado de los Conceptos Fundamentales

El texto menciona 4 herramientas matemáticas que la IA necesita meter en sus **Tablas de Probabilidad** (las que vimos en la imagen anterior):

 **A.Espacio Muestral (El universo de opciones)**

Es la lista de **absolutamente todo lo que puede pasar**.

- _En el texto:_ Al lanzar una moneda, el espacio muestral es `{cara, cruz}`.
- _En tu IA de PC:_ Si un cliente entra al carrito de compras, el espacio muestral es `{Comprar, Abandonar el carrito, Seguir navegando}`. No hay más opciones. La IA necesita saber este límite para repartir sus porcentajes.

**B. Eventos (Lo que te interesa medir)**

Es el pedazo específico del espacio muestral que estás investigando.

- _En el texto:_ Sacar un número par en un dado `{2, 4, 6}`.
- _En tu IA de PC:_ El evento de interés para tu negocio es `"El cliente compró"`. La IA rastrea cuántas veces ocurre este evento específico para aprender qué lo provoca.

**C. Probabilidad Condicional (La clave de Bayes)**

Es calcular la probabilidad de algo **sabiendo que ya pasó otra cosa antes**. Se escribe matemáticamente como $$P(A\vert{}B), que\ significa\ Probabilidad\ de\ A\ dado\ que\ ocurriO B$$.

- _En tu IA de PC:_ ¿Cuál es la probabilidad de que un cliente compre un procesador Ryzen (**Evento A**), _dado que_ ya metió una placa madre AMD en el carrito (**Evento B**)? Esta condicional cambia todo, haciendo que la probabilidad suba del 10% al 90%.

**D. Independencia (Cosas que no se afectan entre sí)**

Dos eventos son independientes si lo que pasa en uno no altera para nada al otro.

- _En el texto:_ Lanzar una moneda dos veces. Si sale cara en el primer tiro, el segundo tiro sigue teniendo 50% de probabilidad de ser cruz. A la moneda no le importa el pasado.
- _En tu IA de PC:_ Si el "Usuario 1" compra un teclado en Argentina y el "Usuario 2" compra un monitor en Colombia, son **eventos independientes**. La IA no los cruza en el grafo porque uno no influye en el otro. (A diferencia de "comprar placa" y "comprar procesador", que son **dependientes**).

---

## ¿Para qué sirve esto en la Inteligencia Artificial?

El texto remata diciendo que esta base teórica sostiene los modelos del curso (como las **Redes Bayesianas**). Sirve para tres cosas prácticas:

1. **Manejar la Incertidumbre:** Si un carro autónomo de Tesla ve una silueta borrosa por la cámara debido a la niebla, la probabilidad le ayuda a calcular: _"Hay 80% de probabilidad de que sea un peatón y 20% de que sea una bolsa de basura"_. Basándose en ese entorno incierto, toma la decisión fundamentada de frenar.
2. **Hacer Inferencias en Redes Bayesianas:** Es lo que vimos en tu diapositiva anterior. Al conectar los nodos con probabilidad condicional, si cambia el estado de un nodo inicial, la IA puede "deducir" o inferir qué pasará al final del grafo.
3. **Sistemas que Aprenden:** Los modelos de IA modernos (como Gemini o Grok) se entrenan leyendo millones de datos para ajustar estas probabilidades. Entre más datos ven, más precisos son sus porcentajes.

---

En resumen

Este texto te está dando el diccionario matemático. Un **Grafo Bayesiano** es, literalmente, un mapa de **Espacios Muestrales** y **Eventos**, interconectados por flechas de **Probabilidad Condicional**, que asume que algunas cosas son **Independientes** y otras no, para que la IA pueda tomar decisiones inteligentes cuando el entorno es confuso.

