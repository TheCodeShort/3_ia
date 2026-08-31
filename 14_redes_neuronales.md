
```toc
title: Redes neuronales
style: nestedOrderedList
minLevel: 1
maxLevel: 6
```

# Redes neuronales: qué son y cómo funcionan

![Imagen redes neuronales](https://www.aluracursos.com/_next/image?url=https%3A%2F%2Fcdn-wcsm.alura.com.br%2F2026%2F07%2F16190337%2Fredes-neurais.webp_2K_202607161550-scaled.jpeg&w=1200&q=100)

---

## Índice de contenidos

Las redes neuronales han revolucionado el campo de la inteligencia artificial y del Machine Learning, permitiendo avances significativos en áreas como el reconocimiento de voz, procesamiento de imágenes, traducción automática e incluso diagnósticos médicos.

Pero, ¿qué hace que las redes neuronales sean tan poderosas? ¿Y cómo funcionan detrás de escena?

Para responder a estas preguntas, el objetivo de este artículo es reflexionar sobre qué son las redes neuronales, cómo funcionan y cómo pueden aplicarse en diversos contextos desde la previsión de ventas hasta la clasificación de imágenes médicas.

---

## ¿Qué son las redes neuronales?

Imagine poder construir modelos que aprenden y se adaptan a partir de datos complejos, capturando patrones sutiles que escapan a las técnicas tradicionales. Es exactamente eso lo que hacen las redes neuronales.

Están inspiradas en la estructura del cerebro humano y tienen la capacidad de resolver problemas altamente no lineales, convirtiéndose en una herramienta esencial para científicos de datos e ingenieros.

## Escenario práctico: cómo aplicar las redes neuronales para prever ventas

Usted trabaja como científico de datos en una empresa de retail y ha recibido la tarea de desarrollar un modelo para prever las ventas de un determinado producto en los próximos meses.

Su jefe enfatizó que este es un problema altamente no lineal, influenciado por diversos factores, y mencionó que ya había obtenido éxito utilizando redes neuronales. Pero, ¿qué son exactamente las redes neuronales y cómo pueden ayudar?

Al investigar, nota que la biblioteca **Scikit-learn** ofrece métodos para redes neuronales y que existen otras bibliotecas populares como **TensorFlow**, **Keras** y **PyTorch**.

Sin embargo, todo parece muy diferente de los métodos clásicos de machine learning con los que está más familiarizado. Entonces surge la interrogante: ¿por dónde empezar? ¿Y cuál de estas herramientas elegir para dar el primer paso?

---

## La estructura de una red neuronal

Retomando el problema, tenemos una tabla que contiene información relacionada con las ventas de un producto. Las primeras columnas de la tabla corresponden a factores que influyen en las ventas, mientras que la última columna representa la cantidad de productos vendidos.

|Mes|Stock|Precipitación|Dias_Promocion|Ventas|
|---|---|---|---|---|
|7|111|21.3961|2|49.0838|
|4|3|152.206|3|0.0000|
|11|349|108.253|9|115.254|
|8|330|192.598|8|96.4274|
|5|445|68.3744|5|85.4793|
|...|...|...|...|...|
|6|429|97.4312|1|106.739|
|11|269|165.897|0|101.186|
|2|485|57.7175|5|91.7283|
|11|470|116.109|7|126.533|
|3|324|132.022|6|75.7136|

Mostrar menos

Nuestro objetivo es construir un modelo que reciba la información sobre Mes, Stock, Precipitación y Días de Promoción, siendo capaz de prever la cantidad de ventas de un producto.

Para alcanzar este objetivo, utilizaremos una red neuronal, que puede entenderse como un conjunto de "neuronas" artificiales organizadas en capas.

Estas neuronas procesan información y realizan predicciones, permitiendo que la red capture patrones complejos en los datos.

La red que vamos a utilizar puede visualizarse en la siguiente figura:

![](https://cdn-wcsm.alura.com.br/2026/07/16193957/Neural_networK-1024x765.jpeg)

En la figura, vemos una capa de entrada con cuatro entradas que representan el Mes, Stock, Precipitación y Días de Promoción.

A continuación, tenemos dos capas ocultas (_hidden layers_), donde cada círculo (neurona) recibe información de la capa anterior. Estas neuronas aplican una suma ponderada de las entradas y utilizan una función de activación para generar sus salidas, que se pasan a la siguiente capa.

Este proceso continúa hasta llegar a la capa de salida, que, en nuestro caso, posee solo una neurona.

Esta neurona final será responsable de generar la previsión de la cantidad de productos vendidos, tras pasar por su propia función de activación.

Ahora, se estará preguntando: **¿Cómo funcionan estas sumas ponderadas? ¿Qué son estas funciones de activación?**

Exploremos más a fondo los conceptos de sumas ponderadas y funciones de activación, elementos cruciales para el funcionamiento de estas redes.

## Entendiendo pesos y bias en las redes neuronales

Siguiendo con la imagen de la red neuronal, cada valor de entrada está conectado por una línea a cada neurona de la capa siguiente. A cada una de estas conexiones le asignamos un peso, un valor que será multiplicado por la entrada.

Este peso sirve para expresar la importancia que una determinada conexión en la red tendrá en la estructura general.

De forma más detallada, una neurona recibe varias entradas, que pueden ser variables de un conjunto de datos o salidas de otras neuronas en capas anteriores. Cada una de estas entradas (x_1, x_2, ..., x_n) se multiplica por un peso ($w_1, w_2, ..., w_n$) que define la importancia de cada entrada para la neurona.

Las entradas multiplicadas por sus respectivos pesos se suman. Este sumatorio ponderado es esencialmente una combinación lineal de las entradas. Matemáticamente, se expresa mediante la siguiente ecuación:

z = w_1x_1 + w_2x_2 + ... + w_nx_n + b

Donde:

- **x_i** son las entradas.
- **w_i** son los pesos.
- **b** es el bias (sesgo), que ajusta el resultado, garantizando que la neurona tenga flexibilidad incluso con entradas iguales a cero.

### Función de activación

Tras calcular la suma ponderada (z), la neurona aplica una **función de activación**. La función de activación introduce la **no linealidad** en el modelo, permitiendo que la red neuronal capture patrones complejos en los datos.

Las funciones de activación más comunes son:

- **ReLU (Rectified Linear Unit):** Retorna cero para valores negativos y retorna el valor original para valores positivos.
- **Sigmoide:** Convierte el valor z en una probabilidad entre 0 y 1.
- **Tangente hiperbólica (Tanh):** Transforma el valor z en un intervalo entre -1 y 1.

En nuestro problema, estamos tratando con la previsión de ventas, que es un valor continuo y no negativo. Por lo tanto, una función de activación como **ReLU** puede ser adecuada para la capa de salida.

### El proceso de entrenamiento

Al definir la estructura de la red neuronal, aún no conocemos cuáles son los pesos y bias correctos que permiten que la red realice predicciones precisas. Es aquí donde entra el proceso de entrenamiento, en el cual la red aprende a ajustar estos parámetros basándose en los datos de entrenamiento.

#### Propagación (Forward Propagation)

Inicialmente, los pesos se definen de forma aleatoria. Durante la propagación hacia adelante, las entradas pasan a través de la red, capa por capa, hasta llegar a la salida final. En cada neurona, se calcula la suma ponderada de las entradas y se aplica la función de activación.

#### Cálculo del Error

La salida generada por la red se compara entonces con el valor real de las ventas. La diferencia entre la previsión y el valor real es el error (o pérdida), que necesitamos minimizar.

#### Retropropagación (Backpropagation) y Gradiente Descendiente

Para ajustar los pesos y minimizar el error, utilizamos el algoritmo de retropropagación combinado con el gradiente descendiente:

- **Gradiente Descendiente:** Es un método de optimización que ajusta los pesos en la dirección opuesta al gradiente del error en relación con los pesos. Esto significa que estamos moviendo los pesos en la dirección que más reduce el error.
- **Retropropagación:** Es el proceso por el cual calculamos el gradiente del error en relación con los pesos, comenzando por la capa de salida y retrocediendo hasta la capa de entrada. Esta información se utiliza para actualizar los pesos de cada conexión.

Este ciclo de propagación hacia adelante, cálculo del error, retropropagación y actualización de los pesos se repite muchas veces (épocas) hasta que el error se minimiza y la red aprende a realizar predicciones precisas.

## ¿Cuál es la relación entre redes neuronales y regresión lineal?

De hecho, existe una relación. La regresión lineal es un modelo que intenta encontrar la mejor línea recta que describe la relación entre las variables de entrada y la variable de salida, ajustando coeficientes (pesos) para minimizar el error.

En el caso más simple, una red neuronal con una única capa de entrada y una única capa de salida lineal, sin funciones de activación no lineales, equivale a una regresión lineal.

Sin embargo, las redes neuronales destacan por su capacidad de modelar relaciones no lineales gracias a las funciones de activación y a las capas ocultas. Mientras que la regresión lineal se limita a relaciones lineales entre variables, las redes neuronales pueden capturar patrones complejos y no lineales.

No obstante, es importante notar que en la regresión lineal tampoco conocemos los coeficientes correctos que pueden producir la recta que mejor se ajusta a los datos.

Una forma de comenzar es elegir valores aleatorios e ir ajustando esos valores hasta obtener la recta óptima.

![Gif com gráfico de dispersão com uma linha de regressão linear ajustada aos pontos de dados. A linha começa desajustada, mas aos poucos atinge a configuração ótima](https://cdn-wcsm.alura.com.br/2025/04/reta.gif)

## ¿Cuáles son las ventajas y limitaciones de las redes neuronales?

Las redes neuronales ofrecen una serie de ventajas frente a otros métodos tradicionales de Machine Learning, especialmente en problemas que involucran datos complejos y no lineales. Sin embargo, también presentan retos notables.

|Ventajas|Limitaciones|
|---|---|
|Excelente capacidad para identificar y modelar patrones altamente complejos y no lineales.|Requieren grandes volúmenes de datos y un alto costo computacional para ser efectivas.|
|Capacidad para aprender, adaptarse y generalizar con eficacia ante nuevos conjuntos de datos.|El proceso de entrenamiento y ajuste de hiperparámetros suele ser lento y complejo.|
|Eficiencia en tareas en tiempo real gracias al procesamiento en hardware dedicado (GPUs).|Riesgo elevado de _overfitting_ (sobreajuste) si el modelo se entrena en exceso.|
|Ideal para campos como visión computacional, procesamiento de voz y análisis predictivo.|Efecto "caja negra": baja interpretabilidad de cómo se llega a una determinada conclusión.|

Mostrar menos

Por lo tanto, aunque las redes neuronales son extremadamente poderosas, vienen con un conjunto de desafíos que deben enfrentarse para obtener los mejores resultados.

## Conclusión

En este artículo, estudiamos qué son las redes neuronales y cómo funcionan. Pasamos por las siguientes etapas:

- Entendimos la **estructura básica** de capas (entrada, ocultas y salida).
- Exploramos el rol fundamental de los **pesos, bias y funciones de activación**.
- Discutimos el ciclo de entrenamiento mediante el **backpropagation y el gradiente descendente**.
- Evaluamos tanto sus **puntos fuertes** como las **barreras de interpretabilidad** que poseen.

Con un buen entendimiento sobre redes neuronales, estará más preparado para aplicar esta poderosa herramienta en diversos escenarios, como predicciones de ventas, clasificación de imágenes y análisis predictivo en diferentes áreas.