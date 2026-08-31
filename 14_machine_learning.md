```toc
title: Redes neuronales
style: nestedOrderedList
minLevel: 1
maxLevel: 6
```

[Directo al punto: qué es Machine Learning con ejemplos reales | Alura Cursos Online](https://www.aluracursos.com/blog/directo-al-punto-que-es-machine-learning-con-ejemplos-reales#algoritmos-comunes-de-ml)

[[10_grafos]]
![[2_ramas_ia.png]]

# El Machine Learning (Aprendizaje Automático)

es fascinante porque cambia por completo la forma en que programamos software.

En lugar de escribir tú mismo las reglas de lo que es un virus, le das miles de ejemplos al algoritmo y este **"aprende a identificar patrones"** por sí solo usando **Mucha Matemática Aplicada y Estadística**.

---

¿Cómo funciona la mente de un algoritmo de Machine Learning?

Para entenderlo a fondo de forma universal, un modelo de Machine Learning es una máquina que busca una **fórmula matemática** que conecte tus entradas con tus salidas

la clave aquí es **"Muchos datos"**. El algoritmo necesita equivocarse miles de veces con datos históricos para calibrar sus números internos hasta que se vuelve un experto prediciendo el futuro.

---

## Los 3 pilares para aprender Machine Learning a fondo

Para dominar esta rama, necesitas entender que todo el Machine Learning se divide en tres formas de entrenar al algoritmo:

### Aprendizaje Supervisado (Con Profesor)

Le das al algoritmo los datos de entrada **junto con la respuesta correcta**.

- **Ejemplo para tu PC:** Le pasas un registro de 10,000 procesos y a cada uno le pones una etiqueta manual: `[Proceso A = Sano]`, `[Proceso B = Virus]`. El modelo estudia las diferencias matemáticas entre ambos grupos hasta que puede etiquetar procesos nuevos por sí solo.

![[3_apren_supervi.png]]

#### Modelos de Clasificación (Separar en categorías)

Se usan cuando la respuesta que buscas es una **etiqueta, una clase o una categoría discreta**. El algoritmo analiza las características del dato y decide a qué "grupo" pertenece.

- **En tu proyecto de seguridad:** Es el modelo ideal. Su tarea es responder preguntas como: ¿Este proceso es `[Sano]` o es `[Virus]`?
- **Tipos de Clasificación:**
    - **Binaria (Dos opciones):** Eliges entre dos respuestas (ej. Correo deseado vs. Spam, Transacción legítima vs. Fraude).
    - **Multiclase (Más de dos opciones):** Eliges entre varias etiquetas (ej. Clasificar un archivo en `[Documento]`, `[Imagen]` o `[Ejecutable]`).
- **Algoritmos populares:** Árboles de Decisión, Regresión Logística, Máquinas de Vector de Soporte (SVM) y Bosques Aleatorios (Random Forest).

---

#### Modelos de Regresión (Predecir un número exacto)

Se usan cuando la respuesta que buscas es un **valor numérico continuo**. No estás agrupando cosas, estás calculando una cantidad, un precio, un porcentaje o una tendencia en una escala infinita.

- **En tu proyecto de seguridad:** Te serviría para calcular el porcentaje exacto de vulnerabilidad de tu sistema en una escala del `0.00` al `100.00`, o estimar cuántos megabytes de RAM consumirá un proceso sospechoso si lo dejas correr 2 horas más.
- **Otros ejemplos universales:** Predecir el precio de una casa según sus metros cuadrados, estimar la temperatura de mañana o calcular las ganancias de una empresa el próximo mes.
- **Algoritmos populares:** Regresión Lineal, Regresión Polinómica y Regresión de Cresta (Ridge).

Al evaluar un modelo de Machine Learning, utilizamos métricas para medir su desempeño y entender su capacidad de generalización. Algunas de las principales métricas que podemos adoptar cuando utilizamos modelos de regresión son:

- R² (Coeficiente de Determinación): Mide qué tan bien los datos se ajustan al modelo. Un valor cercano a 1 indica un buen ajuste, mientras que valores bajos sugieren que el modelo no está explicando bien los datos.
- MAE (Error Medio Absoluto): Representa la media de los errores absolutos entre las predicciones y los valores reales. Cuanto menor sea el MAE, mejor será el modelo.
- RMSE (Raíz del Error Cuadrático Medio): Similar al MAE, pero otorga más peso a errores mayores, haciéndolo más sensible a outliers.

Además de las métricas, necesitamos garantizar que el modelo generalice bien para nuevos datos, evitando dos problemas comunes:

###### **Overfitting (Sobreajuste)**

El modelo aprende excesivamente los patrones de los datos de entrenamiento, pero tiene un desempeño deficiente en los datos de prueba. Esto ocurre cuando el modelo es demasiado complejo y memoriza los ejemplos en lugar de aprender patrones generales. Podemos identificar el sobreajuste cuando el R² en el entrenamiento es alto, pero en la prueba es bajo.

###### **Underfitting (Subajuste)**

El modelo no logra capturar los patrones de los datos, tanto en el entrenamiento como en la prueba, lo que indica que es demasiado simple para la tarea. Si el R² es bajo en ambos conjuntos, es una señal de subajuste.

Una técnica que podemos adoptar para evaluar el desempeño del modelo sin depender de una única división entre entrenamiento y prueba es la validación cruzada (cross validation). En el código implementado en el video anterior, usamos `cross_val_score(model, features, labels, cv=5, scoring='r2')`, que divide los datos en 5 partes, entrenando el modelo en 4 y probando en la parte restante. Este proceso se repite hasta que todas las partes se utilizan como prueba, y la media de los resultados indica la capacidad del modelo de generalizar para nuevos datos.

Para entender mejor esta técnica, podemos pensar en la analogía con un profesor aplicando varias pruebas para evaluar a un alumno. En lugar de confiar en una única nota de un examen aislado, aplica cinco pruebas diferentes y calcula la media, garantizando una evaluación más justa y representativa del conocimiento del alumno.
#### Ciclo de vida obligatorio

##### Preparamos los Datos (La Limpieza y Etiquetado)

Los algoritmos son matemáticos, por lo que no entienden explicaciones de texto ni datos desordenados. Esta fase consiste en **recolectar la información y ordenarla en una tabla limpia**.

- **¿Qué se hace aquí?** Si tu sensor captura registros vacíos, errores de lectura o textos raros, aquí se eliminan o corrigen.

- **La Clave del Aprendizaje Supervisado:** En este paso es donde dejas lista la "respuesta correcta" (la etiqueta). Creas una columna que dice explícitamente qué renglones corresponden a un comportamiento sano y cuáles a un virus. Si alimentas al modelo con datos mal etiquetados o sucios, la IA aprenderá patrones totalmente falsos.

##### Entrenamos el modelo (La Fase de Estudio)

- **¿Qué ocurre internamente?** El modelo empieza a cruzar las variables (como el uso de CPU y las conexiones de red) con la etiqueta final. Comienza a hacer intentos matemáticos a ciegas, se equivoca, ajusta sus ecuaciones estadísticas y vuelve a intentar.

- **El Objetivo:** El algoritmo repite este proceso miles de veces hasta encontrar la **fórmula matemática exacta** (el patrón) que conecta de forma lógica tus datos de entrada con la respuesta correcta. Al terminar este paso, nace el "cerebro" (el archivo `.pkl` del que hablábamos).

##### Hacemos la Previsión (La Predicción en Vivo)

Una vez que el modelo terminó de estudiar y ya tiene su "cerebro" listo, es hora de ponerlo a trabajar con **datos nuevos que nunca antes ha visto**.

- **¿Cómo funciona?** Tu sensor en la PC detecta un proceso sospechoso en tiempo real y le manda los datos de telemetría al servidor. El servidor no sabe si es un virus o no (no viene etiquetado).

- **La Acción:** El modelo toma esos números nuevos, los pasa a través de la fórmula matemática que descubrió en la fase de entrenamiento y arroja su predicción instantánea: _"Esto califica como un proceso sano"_ o _"Esto tiene un 95% de probabilidad de ser un virus"_.

##### Evaluamos el modelo (El Control de Calidad)

Hacer predicciones no es suficiente; necesitas saber **qué tan bueno es tu modelo y si te puedes fiar de él** antes de darle el control para que borre archivos o bloquee tu PC.

- **¿Cómo se evalúa?** Se toma un pequeño porcentaje de tus datos históricos que guardaste en secreto (datos de los que sí conoces la respuesta correcta) y se los pasas al modelo para ver cuántas veces acierta y cuántas falla.

- **El Análisis de Errores:** Aquí descubres problemas graves como los **Falsos Positivos** (el modelo es tan estricto que confunde tus herramientas de programación con virus) o los **Falsos Negativos** (el modelo es tan blando que deja pasar virus reales por considerarlos sanos). Si los resultados de la evaluación son malos, el ciclo se repite: debes regresar al paso 1 a recolectar mejores datos o cambiar el algoritmo en el paso 2.
#### Algoritmo mas usado 

![[4_algoritmo_importante.png]]

##### Árboles de Decisión (El lado izquierdo de tu imagen)

Este modelo funciona como un **diagrama de flujo de preguntas lógicas**.

- **¿Cómo opera?**: Toma un dato nuevo (en la imagen arriba a la izquierda se ve una fila de "TEST DATA" con las medidas de una flor) y lo hace bajar por el árbol. Cada nodo es una pregunta con un filtro numérico (ej. _¿El ancho del pétalo es menor a 0.8 cm?_). Si la respuesta es Sí, el dato toma el camino de la izquierda; si es No, toma el de la derecha. Al llegar al final (las hojas de colores), el árbol le asigna su etiqueta definitiva (ej. _Iris virginica_).
-
- **Conexión con lo que ya sabes**: Este algoritmo es el que genera los archivos `.pkl` **ultra livianos** de los que hablábamos. Una vez que descubre las preguntas correctas durante el estudio, borra la base de datos y solo guarda ese mapa de preguntas de Sí/No. Es ultra rápido.

---

##### KNN - K-Nearest Neighbors (El lado derecho de tu imagen)

Este algoritmo se basa en el dicho popular: _"Dime con quién andas y te diré quién eres"_. Funciona por **geometría y cercanía espacial**.

- **¿Cómo opera?**: No crea reglas ni preguntas lógicas. En lugar de eso, dibuja todos tus datos históricos en un plano cartesiano (en la gráfica se ven puntos verdes y puntos rojos). Cuando entra un dato nuevo en tiempo real (el **punto negro** del centro), el algoritmo traza un círculo alrededor de él y mira a sus vecinos más cercanos.

- **El significado de K=5**: El parámetro "K" es el número de vecinos que la IA va a consultar para votar. En la imagen dice `K=5`. Si miras dentro del círculo punteado, hay **4 puntos rojos** y solo **1 punto verde**. Como ganan los rojos por mayoría (4 contra 1), el algoritmo deduce al instante: _"El punto negro pertenece al grupo Rojo"_.

---

⚠️ ¡Aquí está el misterio de los 5 GB revelado!

¿Recuerdas que hace un momento hablábamos de por qué un archivo `.pkl` podría llegar a pesar 5 GB por un error de diseño? **KNN es el culpable perfecto de eso.**

A diferencia del Árbol de Decisión, KNN **no aprende ninguna fórmula matemática**. Para poder calcular qué vecinos tiene cerca el punto negro, el algoritmo **necesita guardar absolutamente todos los puntos históricos (los millones de registros) dentro del archivo `.pkl`**.

Si entrenas un KNN con 5 años de datos masivos de telemetría, el archivo `.pkl` va a engordar exponencialmente hasta pesar Gigabytes, porque se ve obligado a cargar toda tu base de datos dentro de la memoria RAM cada vez que quiere hacer una sola predicción. Por eso, para tu mini servidor y tu sensor de PC, el **Árbol de Decisión** es infinitamente superior y más eficiente que el KNN.

---


### Aprendizaje No Supervisado (Sin Profesor)

Le das los datos al algoritmo **sin respuestas ni etiquetas**. El modelo debe buscar patrones escondidos o agrupaciones por similitud por sí mismo.

- **Ejemplo para tu PC:** Le avientas todo el historial de uso de tu computadora. El algoritmo agrupa tus programas normales en un "clúster" o bloque gigante. Si un proceso misterioso actúa de forma totalmente aislada a ese grupo, el modelo lo detecta de inmediato como una anomalía.

### Aprendizaje por Refuerzo (Ensayo y Error)

El algoritmo es un agente que interactúa con un entorno y aprende recibiendo **premios o castigos** según sus acciones. Es como se entrenan las IA para jugar videojuegos o controlar robots.

---