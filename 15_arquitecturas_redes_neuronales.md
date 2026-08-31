```toc
title: Arquitectura resde neuronales
style: nestedOrderedList
minLevel: 1
maxLevel: 6
```
# Arquitecturas de redes neuronales: aplicaciones en la IA

![Imagen IA](https://www.aluracursos.com/_next/image?url=https%3A%2F%2Fcdn-wcsm.alura.com.br%2F2026%2F07%2F16214107%2Farquiteturas-de-redes-neurais2.jpeg&w=1200&q=100)

---

## Índice de contenidos

¿Alguna vez te has preguntado cómo tu smartphone reconoce tu rostro o cómo los asistentes virtuales entienden lo que dices?

¡Todo esto es gracias a las redes neuronales! Inspiradas en el funcionamiento de nuestro cerebro, están revolucionando la Inteligencia Artificial y permitiendo avances increíbles en áreas como el reconocimiento de imágenes, el lenguaje natural y la robótica.

Lo más fascinante es que aprenden patrones complejos a partir de datos brutos, como un rompecabezas que se va armando. Esta poderosa habilidad ayuda a resolver problemas que antes parecían imposibles.

Pero, ¿qué hace que todo esto sea posible? ¡La variedad de arquitecturas de redes neuronales!

Cada tipo tiene sus propias fortalezas y debilidades, adaptándose a diferentes tareas y tipos de datos. Conocer estas diferentes estructuras es esencial para quienes desean aventurarse en el mundo del aprendizaje profundo (_deep learning_) y aplicar estas tecnologías de forma eficaz.

En este artículo, exploraremos las principales arquitecturas de redes neuronales. Comenzaremos por las redes perceptrón e iremos hasta las más avanzadas, como las redes convolucionales y recurrentes.

Descubriremos los principios básicos de cada una, dónde se utilizan más y cuáles son sus ventajas y desventajas con el objetivo de ofrecerte una visión completa y accesible de este universo fascinante.

## Perceptrón Multicapa (MLP)

Las diferentes arquitecturas de redes neuronales pueden adaptarse a una variedad de problemas, dependiendo de las características de los datos y de las tareas a resolver.

La red MLP (_Multilayer Perceptron_) es una de las formas más simples y tradicionales de red neuronal, compuesta por capas densamente conectadas, también conocidas como _fully connected_. Es ampliamente utilizada en tareas de clasificación y regresión, especialmente con datos tabulares.

Con una MLP, es posible construir modelos que estimen valores continuos, como el precio de las casas, basándose en variables geográficas y características de los inmuebles de la región. Además, puede aplicarse en la clasificación de problemas de salud, como predecir si una persona tiene diabetes a partir de los resultados de exámenes médicos.

![](https://cdn-wcsm.alura.com.br/2026/07/16205550/Neural_networK-1024x765.jpeg)

## Redes Neuronales Convolucionales (CNNs)

Aunque la arquitectura MLP es bastante poderosa, encontrar la configuración ideal de neuronas, capas o funciones de activación puede ser un desafío. Sin embargo, al utilizar capas especializadas para el tipo de dato con el que estamos tratando, incluso las configuraciones simples pueden resultar en modelos de alto rendimiento.

Las **Redes Neuronales Convolucionales (CNNs)** están diseñadas exactamente con ese propósito. Introducen capas convolucionales que aplican filtros sobre los datos durante el entrenamiento. Estos filtros son aprendidos por la red y permiten la identificación y el realce de características importantes, mejorando la precisión en tareas como la clasificación y la regresión.

Las CNNs se utilizan ampliamente en visión computacional, como en la clasificación de imágenes y detección de objetos, ya que las operaciones de convolución son altamente eficaces para capturar patrones espaciales y características dentro de una imagen.

![](https://cdn-wcsm.alura.com.br/2026/07/16210248/rede-convolucional.webp)

En el ejemplo presentado, observamos una red donde las primeras capas son convolucionales, combinadas con capas de _max-pooling_. El _max-pooling_ realiza la reducción dimensional, disminuyendo la cantidad de parámetros y la complejidad de la red. Después de estas capas, tenemos capas densas, similares a las usadas en las redes MLP, que finalizan el proceso de aprendizaje y clasificación.

## Redes Neuronales Recurrentes (RNNs)

Algunos tipos de datos poseen un carácter secuencial, como las series temporales. Por ejemplo, el precio de las acciones de una empresa de agronomía puede verse influenciado por factores estacionales, como el clima, o por eventos recientes, como un escándalo político ocurrido el día anterior.

En este tipo de datos, es importante recordar los eventos pasados y considerar que estos pueden repetirse estacionalmente o no. Otro ejemplo de datos secuenciales son los textos. Al escuchar la frase _"Quiero comer una..."_, es mucho más probable que la secuencia se complete con "pizza" que con "taladro".

Para lidiar con estas características, las **Redes Neuronales Recurrentes (RNNs)** poseen una memoria interna que permite capturar dependencias a lo largo de secuencias temporales.

En la ilustración abajo podemos observar la arquitectura de una RNN, donde parte de la información es retroalimentada para la misma neurona, lo que le da a la red su capacidad de tratar datos secuenciales de forma eficaz

![](https://cdn-wcsm.alura.com.br/2026/07/16211143/rede-recorrente.webp)

Existen variantes populares de las RNNs, como las _Long Short-Term Memory_ (LSTM) y las _Gated Recurrent Units_ (GRUs):

- **LSTMs:** Son capaces de capturar dependencias a largo plazo, manejando bien secuencias extensas sin perder información en el camino.
- **GRUs:** Aunque su diseño es más simple que el de las LSTMs, resultan sumamente eficaces en el procesamiento de secuencias largas con un menor costo computacional.

## Redes Neuronales Generativas Adversarias (GANs)

En lugar de querer entrenar una red que realice una tarea de clasificación para discernir entre una información y otra, podrías querer "enseñar" a una red a generar un determinado tipo de información, como una imagen o un texto. Las GANs se utilizan ampliamente en este campo.

Están compuestas por dos redes diferentes que compiten en un juego de suma cero durante el entrenamiento:

- **Red generadora:** Intenta crear datos nuevos (por ejemplo, imágenes) que parezcan completamente reales.
- **Red discriminadora:** Evalúa los datos para determinar si son reales (del conjunto de entrenamiento original) o falsos (creados por el generador).

![](https://cdn-wcsm.alura.com.br/2026/07/16211652/gan.webp)

Este entrenamiento competitivo ocurre hasta que la red generadora es capaz de producir imágenes indistinguibles de las reales. Las GANs han sido responsables de avances impresionantes como el _DeepFake_ (creación de videos realistas), la generación de arte digital, imágenes de alta resolución y modelos en 3D.

## Transformers

Las redes Transformers representan una evolución significativa en el campo del aprendizaje automático, especialmente en tareas relacionadas con el procesamiento de lenguaje natural (NLP).

A diferencia de las RNNs, que procesan secuencias de forma ordenada y secuencial, los Transformers son capaces de **procesar la información en paralelo**. Esto los hace extremadamente rápidos y eficientes, especialmente para entrenarse con volúmenes masivos de datos para tareas como traducción automática y generación de texto y procesamiento de imágenes.

La clave de su éxito reside en el mecanismo de atención, más específicamente en la denominada **self-attention (autoatención)**. Este mecanismo permite que la red asigne diferentes pesos a distintas partes de la secuencia de entrada en base al contexto, sin importar qué tan alejadas estén unas palabras de otras en la frase.

El Transformer estándar está compuesto por dos bloques principales:

- **Codificador (Encoder):** Recibe la secuencia de entrada y genera una representación vectorial interna.
- **Decodificador (Decoder):** Utiliza esa representación para generar la secuencia de salida (por ejemplo, la traducción final).

![](https://cdn-wcsm.alura.com.br/2026/07/16213052/transformers2-1024x572.jpeg)
### Transformers: funcionamiento y beneficios

![](https://www.aluracursos.com/_next/image?url=https%3A%2F%2Fcdn-wcsm.alura.com.br%2F2026%2F07%2F21131318%2Ftransformers-1.webp&w=1200&q=100)

#### Breve historia de la arquitectura Transformers

Actualmente, nos encontramos en un escenario en el que modelos como GPT pueden entender y generar texto de forma casi humana, respondiendo preguntas complejas y participando en conversaciones naturales.

Cuando ChatGPT se popularizó a mediados de 2022, el tema de la Inteligencia Artificial (IA) se volvió ampliamente conocido. Sin embargo, la ciencia detrás de esta tecnología proviene de largos años de investigación.

Los grandes avances recientes son posibles gracias a una innovación llamada **Transformers**, una arquitectura que cambió por completo el juego de la Inteligencia Artificial al ser publicada en 2017 e introducir el mecanismo de atención, el cual elevó considerablemente la capacidad de los modelos de lenguaje para comprender el contexto en el lenguaje natural.

En este artículo, exploraremos cómo funcionan los Transformers y por qué esta tecnología está detrás de los avances más impresionantes en IA.

#### Breve historia de la arquitectura de transformers

La arquitectura Transformers fue propuesta en 2017 en el artículo _Attention is All You Need_ (“La atención es todo lo que necesitas”), escrito por investigadores de Google.

**Este trabajo introdujo el uso de una estructura que revolucionó la forma en que se conducía el Aprendizaje Profundo (_Deep Learning_) hasta ese momento: mecanismos de atención que comprenden el contexto.**

Antes de esto, se utilizaban otros tipos de redes neuronales profundas para resolver tareas de Inteligencia Artificial, como las Redes Neuronales Recurrentes (RNN) y las LSTM. Cada modelo necesitaba un entrenamiento supervisado para solucionar una tarea específica, como la clasificación de texto o el análisis de sentimientos. Estos modelos funcionan en una arquitectura _**sequence-to-sequence**_ (secuencia a secuencia), es decir, trabajan de manera secuencial, analizando una palabra tras otra.

#### Beneficios de los Transformers

Esas arquitecturas anteriores se siguen utilizando hoy en día y se mantienen muy relevantes, pero los mecanismos de atención de los Transformers aportaron el gran beneficio de la **paralelización**.

Con la paralelización, **la oración completa se procesa al mismo tiempo**. Esto aporta una serie de ventajas:

- Mayor velocidad de entrenamiento
- Eficiencia en el reconocimiento de dependencias entre palabras
- Mejora en el reconocimiento de patrones
- Capacidad para analizar problemas no secuenciales

#### GPT y BERT

En 2018, un año después de la publicación del artículo que describe la arquitectura Transformers, se lanzaron los modelos GPT y BERT.

- **GPT** es el acrónimo de **Preentrenamiento Generativo Transformador** (_Generative Pre-trained Transformer_). Este modelo, desarrollado por OpenAI, es la base del GPT ampliamente conocido hoy a través de ChatGPT.
- **BERT**, desarrollado por Google, está presente en el día a día de quienes usan los servicios de esta empresa. A partir de 2019, BERT se implementó en los servicios de búsqueda para la optimización de SEO. Desde entonces, se ha integrado en traducciones automáticas, clasificación de correos electrónicos, interacciones del Asistente de Google, entre otros.

GPT y BERT son representantes importantes entre diversos modelos que siguen la arquitectura Transformers. Este fue solo el comienzo de un gran salto en el área de investigación en Aprendizaje Automático (_Machine Learning_) e Inteligencia Artificial.

Para dimensionar el gran impacto de los modelos Transformers, podemos analizar el número de citaciones que ha recibido el artículo a lo largo de los años desde su lanzamiento.

![](https://cdn-wcsm.alura.com.br/2026/07/21132708/Gemini_Generated_Image_gy9nx7gy9nx7gy9n-1024x776.png)

En 2020, ese número ya estaba en las decenas de miles y, desde entonces, ha crecido rápidamente superando de largo las 100 mil citas.

#### ¿Cómo funciona Transformers?

¡La transformación comienza incluso antes de que el texto entre en la estructura del Transformer!

Imagina que queremos traducir la frase “a Dani le gusta el cafe” al portugues usando el Traductor de Google. Recibimos la respuesta “Dani gosta de café” en un abrir y cerrar de ojos, pero, internamente, suceden muchas cosas.

Cuando se envía el texto de entrada, primero se divide en pequeños fragmentos de palabras que mantienen significado: los **tokens**. Luego, los tokens deben convertirse a un formato numérico, al que llamamos **embeddings**.

**Un _embedding_ es una secuencia numérica que representa el significado de la palabra, su semántica, posición dentro del texto, contexto, etc.** Esta secuencia pasa por diversas transformaciones dentro del modelo.

Con los _embeddings_ creados, estamos listos para entrar propiamente en la arquitectura Transformers.

La arquitectura se compone de dos mecanismos principales: el **encoder** (codificador) y el **decoder** (decodificador). En términos sencillos, el _encoder_ procesa la entrada (por ejemplo, una oración) y el _decoder_ genera la salida (que puede ser una traducción, la continuación de un texto, etc.).

![](https://cdn-wcsm.alura.com.br/2026/07/21135541/transformers-3-1024x360.png)

Cada uno de estos mecanismos se repite varias veces, formando un conjunto de _encoders_ y otro conjunto de _decoders_ que procesan la información de manera sucesiva. Esta repetición hace que el resultado final sea de mayor calidad, ya que con cada iteración los resultados son más precisos.

Además de estos dos componentes, también tenemos una capa llamada _language modeling head_ (cabeza de modelado de lenguaje), responsable del procesamiento final del texto.

> **Dato curioso:** Los modelos basados en Transformers no siempre utilizan todos los componentes. BERT, por ejemplo, utiliza solo el _encoder_, mientras que GPT utiliza únicamente el _decoder_.

### El proceso de codificación - Encoder

La función del _encoder_ es “entender” el texto de entrada. Para ello, dentro del _encoder_ existen dos capas principales:

1. **Self-Attention (Autoatención):** el mecanismo de atención que identifica qué palabras de una oración están más relacionadas entre sí.
2. **Feed Forward:** una red neuronal tradicional que procesa la información extraída de la capa de _self-attention_, refinando la comprensión del contexto.

Además de estas, tenemos dos capas auxiliares:

- **Normalización:** un cálculo que mantiene las salidas de una capa en el formato adecuado para la siguiente.
- **Conexiones residuales:** un mecanismo que “rescata” la entrada original, garantizando que el contexto inicial no se pierda a lo largo del procesamiento.

El _embedding_ inicial pasa por la capa de _self-attention_, se normaliza y recibe conexiones residuales. A continuación, pasa por la capa _feed-forward_, donde nuevamente se normaliza y recibe conexiones residuales.

![](https://cdn-wcsm.alura.com.br/2026/07/21182258/transformers-32123-1024x1024.png)

#### Mecanismo de Self-Attention

El mecanismo de atención permite que el modelo capture las sutilezas de contexto y significado de un texto.

De manera simultánea, calcula la relación de cada palabra individual con todas las demás palabras de la frase. Por ejemplo, en la frase:

> _“Dani gusta mucho del café, pero solo si es filtrado.”_

El modelo necesita entender que "filtrado" está relacionado con "café", y no con "Dani" o "gusta", que están más fuertemente relacionadas entre sí. Atribuye pesos diferentes a cada palabra según estas relaciones. En este caso, "filtrado" recibe un peso mayor en relación con "café", porque esas palabras están conectadas directamente en el contexto de la oración.

El bloque de _self-attention_ funciona como si el modelo observara diferentes aspectos del contexto al mismo tiempo, enfocándose cada uno en detalles específicos. Este mecanismo se llama **multi-headed attention** (atención de múltiples cabezas): en lugar de calcular la relevancia de una palabra para el contexto una sola vez, el modelo lo hace varias veces, analizando la frase desde diferentes perspectivas.

#### Normalización y Conexiones Residuales

Una vez realizado el procesamiento en las "múltiples cabezas de atención", cada una genera una salida individual desde su punto de vista con información semántica y contextual.

Como la siguiente capa necesita una entrada única, la **normalización** compacta toda esa información al formato estándar de las capas de codificación.

En esta etapa también actúan las **conexiones residuales**: los _embeddings_ iniciales sin procesar se suman a las salidas de los mecanismos de atención. Así, el siguiente bloque recibe tanto la información procesada por la atención como la estructura original del texto, evitando que el contexto inicial se diluya.

#### Mecanismo Feed Forward

La red neuronal _Feed Forward_ es una de las arquitecturas más antiguas de _Machine Learning_. La información fluye en una sola dirección a través de múltiples capas de neuronas. En el Transformer, esta capa refina las salidas de los mecanismos de atención, enfocándose en el procesamiento de los datos capturados más que en el análisis de contexto.

Tras pasar por la red _Feed Forward_, se aplica la normalización de nuevo y el proceso se repite en cada uno de los _encoders_ apilados en el modelo.

### El momento de la decodificación - Decoder

Estructurado de forma similar al _encoder_, el _decoder_ se encarga de generar la respuesta mediante los siguientes componentes:

1. **Self-Attention Parcial (Mascara de atención):** se enfoca solo en las palabras generadas previamente.
2. **Encoder-Decoder Attention:** mecanismo de atención que recibe la información proveniente del conjunto de _encoders_.
3. **Feed Forward:** red neuronal que refina las salidas.
4. **Normalización y Conexiones Residuables:** mantienen la estabilidad de los datos y el contexto acumulado.

![](https://cdn-wcsm.alura.com.br/2026/07/21183029/transformer-6-1024x1024.png)

A diferencia del _encoder_ (que procesa la entrada en paralelo), el _decoder_ genera las palabras **una a una, de forma secuencial**.

#### Aquí tienes la traducción del texto al español, manteniendo los términos técnicos y conceptuales del área de Inteligencia Artificial:

### **Self-Attention (Autoatención)**

En esta capa, el mecanismo de _self-attention_ realiza un comportamiento llamado **autorregresivo**.

La atención se enfoca únicamente en las palabras que ya han sido generadas previamente por el _decoder_ (decodificador).

Volviendo al ejemplo de la traducción de la frase _"Dani gosta de café"_ al español, en cada procesamiento el mecanismo de atención tendrá una visión diferente:

- Token especial para iniciar la generación de texto
- "A"
- "A Dani"
- "A Dani le"
- "A Dani le gusta"
- "A Dani le gusta el"
- "A Dani le gusta el café"
- Token especial para finalizar el procesamiento.

Mientras tanto, los _embeddings_ de las palabras que aún no han sido generadas están enmascarados, es decir, ocultos, para que el modelo no vea información futura durante la generación. De esta forma, el modelo respeta el orden de generación del texto.

### **Encoder-Decoder Attention (Atención Codificador-Decodificador)**

Este es el componente que recibe toda la información que proviene del _encoder_ (codificador), el cual procesó la entrada completa.

La atención también se dirige a las palabras que ya fueron generadas, pero con la gran responsabilidad de transformar el contexto inicial del comando en una respuesta consistente y coherente.

### **Normalización, Conexiones Residuales y Feed Forward**

Estas capas funcionan de manera similar a lo que ocurre en el _encoder_. El cálculo de normalización mantiene los _embeddings_ en un formato adecuado y el mecanismo _feed forward_ realiza el refinamiento.

Las conexiones residuales tienen una ligera diferencia. En el _decoder_, continúan entre las capas principales (_self-attention_, _encoder-decoder attention_ y _feed forward_) y conectan la información que fue procesada previamente dentro del propio _decoder_.

Esta secuencia de procesamiento se repite en todos los _decoders_ apilados en el modelo. La salida final es una serie de representaciones numéricas de la interpretación del modelo sobre las palabras que deben ser generadas.

## Language Modeling Head

Es la última capa del Transformer y se compone de dos partes:

- **Linear (Lineal):** mapea las representaciones matemáticas complejas (vectores) generadas por los _decoders_ contra todo el vocabulario disponible en el modelo, asignando una puntuación a cada palabra posible.
- **Softmax:** convierte las puntuaciones en probabilidades porcentuales. La palabra con la probabilidad más alta es elegida como la siguiente en la secuencia.

> **Parámetros y Configuración:** El número de capas, cabezas de atención, tamaño del vocabulario y selección de probabilidades son **hiperparámetros** configurables durante el entrenamiento que determinan el rendimiento final del modelo.

## ¿Cómo se entrena el modelo?

1. **Entrenamiento Autosupervisado (Base):** El modelo aprende a partir de grandes volúmenes de texto sin procesar ni etiquetado humano, identificando patrones estadísticos del lenguaje (predicción de palabras faltantes o siguientes).
2. **Transfer Learning / Aprendizaje por Transferencia (Ajuste Fino):** El modelo base se ajusta mediante datos etiquetados por humanos para realizar tareas específicas como traducción, clasificación o respuestas a preguntas.
3. **Retroalimentación Humana (RLHF):** Muchas arquitecturas modernas aplican técnicas de refinamiento continuo basadas en la evaluación e interacción de usuarios humanos.

## Recursos e Infraestructura

Los modelos Transformers son masivos. Por ejemplo, modelos de la escala de GPT-4 requieren cientos de terabytes de datos de texto y procesan billones de parámetros, demandando semanas o meses de entrenamiento sobre infraestructuras de cómputo de alto rendimiento.

En este ámbito, plataformas como **Hugging Face** juegan un rol clave al alojar repositorios de modelos preentrenados y bibliotecas de código abierto (como la librería `transformers` en Python), facilitando la reutilización de estos modelos sin necesidad de entrenarlos desde cero.

Aunque nacieron para el Procesamiento del Lenguaje Natural (PLN), hoy los Transformers se aplican con éxito en:

- **Visión por Computadora:** Clasificación de imágenes y video (ej. _Vision Transformer_).
- **Procesamiento de Audio:** Conversión de voz a texto y asistentes virtuales.
- **Generación de Código:** Asistentes de programación.
- **Ciberseguridad y Finanzas:** Detección de fraudes y búsquedas semánticas.
## Autoencoders

Los Autoencoders son un tipo de red neuronal utilizada principalmente para la compresión de datos y el aprendizaje no supervisado. Su principal característica es la capacidad de aprender representaciones comprimidas de los datos de entrada, capturando sus componentes clave en un espacio de menor dimensión.

Su arquitectura básica está compuesta por dos partes principales:

- **Codificador (Encoder):** Recibe la entrada y la comprime en una representación de menor dimensión llamada _bottleneck_ (capa latente).
- **Decodificador (Decoder):** Toma esa representación comprimida e intenta reconstruir la entrada original con la menor pérdida de información posible.

Durante el entrenamiento, el Autoencoder se ajusta para minimizar la diferencia entre la entrada y la salida reconstruida. Son sumamente versátiles y se aplican en tareas como la eliminación de ruido en imágenes, la detección de anomalías o mediante su variante _Variational Autoencoders_ (VAEs) para generar nuevas muestras de datos.

## U-Nets y Redes de Difusión

Las U-Nets son un tipo de red neuronal diseñada para tareas que requieren una **segmentación de imágenes precisa**, como la identificación de tumores en imágenes médicas o estructuras en mapas satelitales.

![](https://cdn-wcsm.alura.com.br/2026/07/16213333/diagrama-arquitetura.webp)

Fuente: Mehrdad Yazdani, CC BY-SA 4.0 [https://creativecommons.org/licenses/by-sa/4.0, via Wikimedia Commons](https://creativecommons.org/licenses/by-sa/4.0,%20via%20Wikimedia%20Commons)

La estructura de una U-Net se divide en dos caminos simétricos:

- **Camino de contracción (Encoder):** Reduce la dimensionalidad de los datos extrayendo características mediante convoluciones y max-pooling.
- **Camino de expansión (Decoder):** Reconstruye el mapa de segmentación a través de operaciones de _upsampling_ combinadas con conexiones de salto (_skip connections_), las cuales recuperan detalles de alta resolución del camino del encoder.

### Relación con las Redes de Difusión

Recientemente, las redes de difusión han surgido como una poderosa técnica para la generación de imágenes de alta calidad a partir de ruido (un proceso conocido como "difusión" y "desdifusión").

Las U-Nets a menudo se utilizan como el motor base en la arquitectura de las redes de difusión, ya que su estructura de codificación, decodificación y conexiones de salto permite una reconstrucción altamente eficiente de la imagen preservando los detalles y texturas importantes.

## Physics-Informed Neural Networks (PINNs)

Las **Physics-Informed Neural Networks (PINNs)** son una clase especial de redes neuronales que integran el conocimiento de las leyes de la física directamente en el proceso de aprendizaje.

A diferencia de los modelos tradicionales de Deep Learning, que dependen únicamente de los datos para encontrar patrones, las PINNs utilizan ecuaciones diferenciales parciales (PDEs) como restricciones durante el entrenamiento. Esto permite:

- **Entrenamiento con pocos datos:** Pueden aprender eficientemente en entornos donde la recolección de datos es difícil o costosa.
- **Consistencia Física:** Las predicciones de la red garantizan el respeto a los principios de la física real (por ejemplo, termodinámica o mecánica de fluidos), evitando errores absurdos o inconsistentes.
- **Mejor generalización:** Al estar acotadas por leyes físicas preestablecidas, ofrecen una fiabilidad científica mucho mayor.

## Conclusión

En este artículo, exploramos las principales arquitecturas de redes neuronales, desde las más simples, como las redes MLP, hasta las más avanzadas, como Transformers y PINNs. Cada una de estas arquitecturas tiene su lugar en diferentes tipos de problemas, y entender sus particularidades es esencial para aplicarlas de forma eficaz en el mundo real.