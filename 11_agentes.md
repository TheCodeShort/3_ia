```toc
title: Redes neuronales
style: nestedOrderedList
minLevel: 1
maxLevel: 6
```


# Actuadores
Los actuadores son las respuestas que el agente va a dar. En este caso, el actuador se refiere a la acción, a la actuación sobre lo que se está solicitando. La parte de función de agente es el punto principal, es el núcleo del comportamiento, porque allí es donde se define la función de decisión. Es decir, a partir de la entrada que recibe, aplicando esa función de agente, él es capaz de actuar de forma lógica, aplicando el razonamiento esperado.

# Tipos de agentes
percibe el ambiente, procesa información, genera resultados

## Reactivo 
se basa en reglas y dependiendo en esta regalas toma decisiones inmediatas y  tiene actuadores que es cuando toma la decisión 

## Basados en modelos 
situaciones dinámicas, modelos de ambiente que es cuando esta en el lugar y actúa en ese ambiente y trabaja con histórico ósea trabaja con una memoria 

## Objetivos 
se definen metas o guiados por metas claras y toma decisiones enfocadas en el alcance de las metas y sus decisiones se basan en llegar a esas metas 

## Basados en su utilidad 
evalúan posible acciones y evalua la calidad para llegar a ellos una función para eso y después la toma de decisiones avanzadas son de mayor nivel 

# Agentes Inteligentes en app Web 
selección y organización de contenido personalizado básicamente es sugerir comprar en el caso de una tienda online y son basados en objetivos 

# Agentes de IA: entiende la próxima frontera de la automatización

![](https://www.aluracursos.com/_next/image?url=https%3A%2F%2Fcdn-wcsm.alura.com.br%2F2026%2F07%2F16183133%2Fagentes-de-ia.jpg&w=1200&q=100)

Si en los últimos años hemos quedado maravillados con la capacidad de la inteligencia artificial para generar textos, imágenes y códigos, prepárate para la próxima gran revolución: los agentes de IA.

Estos representan la evolución natural de la IA generativa, pasando de ser herramientas que responden a comandos a sistemas autónomos que ejecutan tareas complejas de principio a fin.

Pensemos en un escenario para ilustrar esta idea. Imagina darle un objetivo a un asistente digital, como "planifica mis vacaciones de una semana en familia para el Nordeste con un presupuesto de R$ 5.000".

Sin embargo, este no solo regresa con sugerencias, sino que se pone a investigar vuelos, comparar precios de hoteles, verificar el pronóstico del tiempo, armar un itinerario y, además, te presentará las opciones de reserva para tu aprobación.

Esta es la promesa de los agentes autónomos.

Pero, en la práctica, ¿qué son exactamente estos agentes inteligentes? ¿Cómo funcionan y qué impacto tendrán en el futuro del trabajo y la tecnología?

Si quieres entender esta que es una de las tendencias más importantes en IA, esta guía completa es tu punto de partida.

Vamos a desentrañar el concepto, explorar sus aplicaciones prácticas y mostrar cómo puedes prepararte para esta nueva era de la automatización.

## ¿Qué son los agentes de IA?

En líneas generales, un agente de IA es un software diseñado para percibir su entorno, tomar decisiones de forma autónoma y ejecutar acciones para alcanzar un objetivo específico.

A diferencia de un chatbot o de un modelo de lenguaje que solo responde a una pregunta, un agente tiene la capacidad de crear y seguir un plan de múltiples etapas para completar una tarea.

Piensa en ChatGPT como un cerebro brillante en un frasco: tiene un conocimiento inmenso, pero no tiene "manos" para actuar en el mundo.

Un agente de IA conecta ese cerebro a "manos y piernas" digitales; es decir, la capacidad de usar herramientas, navegar por internet, interactuar con otras aplicaciones y ejecutar comandos.

En resumen, mientras que la IA generativa tradicional funciona en el ciclo "humano ordena → IA responde", los agentes de IA operan en un ciclo más autónomo:

"humano define objetivo → IA planifica → IA actúa → IA aprende → IA informa".

## ¿Cómo funcionan los agentes de IA?

La arquitectura de un agente de IA, aunque compleja, puede entenderse a través de sus componentes centrales, que trabajan en conjunto para crear un ciclo de acción autónoma.

### Percepción

El agente utiliza "sensores" para recopilar información sobre su entorno. En el mundo digital, estos sensores pueden ser el acceso a una página web, la lectura de una base de datos, el análisis de una hoja de cálculo o la interpretación de un correo electrónico.

### Razonamiento y planificación

Este es el "cerebro" del agente, generalmente potenciado por un poderoso modelo de lenguaje (LLM). Basándose en el objetivo definido por el usuario y la información percibida, el agente descompone la tarea compleja en una secuencia de pasos lógicos y más pequeños.

Por ejemplo, para "organizar un viaje", los pasos serían: 1. Investigar destinos. 2. Filtrar por presupuesto. 3. Buscar vuelos. 4. Buscar hoteles. 5. Armar itinerario.

### Acción

El agente utiliza "actuadores" para ejecutar los pasos del plan. Estos actuadores representan la capacidad de interactuar con otras herramientas: navegar en un sitio web, completar un formulario, enviar una consulta a una API, ejecutar un script de código o escribir en un archivo.

### Memoria y aprendizaje

Los agentes de IA poseen memoria a corto y largo plazo. Recuerdan lo que ya hicieron, el resultado de sus acciones y el feedback recibido. Esto les permite aprender de los errores, ajustar el plan en tiempo real y mejorar su rendimiento con cada nueva tarea.

## Tipos de agentes de IA

Los agentes pueden clasificarse en diferentes niveles de complejidad e inteligencia. La teoría clásica de la inteligencia artificial los divide en algunas categorías principales:

### Agentes de reflejo simple

Son los más básicos. Operan basados en una regla simple de "condición-acción": si sucede X, entonces haz Y. No tienen memoria del pasado y reaccionan solo al estado actual del entorno. Un termostato que enciende el aire acondicionado cuando la temperatura supera los 25 °C es un ejemplo de agente de reflejo simple.

### Agentes de reflejo basados en modelos

Un poco más avanzados, estos agentes mantienen un "modelo" interno de cómo funciona el mundo. Utilizan ese modelo para tomar decisiones. Pensemos ahora en el universo automotriz. Un ejemplo sería el de un coche autónomo que, además de ver al coche de adelante (percepción actual), sabe que frenar bruscamente puede causar una colisión trasera (modelo de mundo). Esto es lo que significa, de manera muy sencilla, decir que está operando basándose en un modelo.

### Agentes basados en metas

Estos agentes son capaces de tomar decisiones basadas en un objetivo futuro. No solo reaccionan al entorno, sino que simulan diferentes secuencias de acciones para elegir aquella que los acerque más a su meta. Un sistema de GPS que calcula la mejor ruta hacia tu destino, basándose en información sobre el tráfico en las vías, es un ejemplo clásico.

### Agentes de aprendizaje

Son los más sofisticados y la base de los agentes autónomos modernos. Además de tener una meta, poseen un "elemento de aprendizaje". Pueden analizar el resultado de sus acciones, recibir feedback y modificar su propio comportamiento para tomar mejores decisiones en el futuro. Aquí es donde entra en juego el machine learning, permitiendo que el agente mejore con la experiencia.

## Beneficios de los agentes de IA

La implementación de agentes digitales promete una serie de beneficios transformadores para empresas e individuos, los cuales surgen principalmente en relación con:

- **Aumento de la eficiencia operativa:** automatizan tareas complejas y lentas, liberando a los profesionales humanos para concentrarse en actividades más estratégicas y creativas.
- **Reducción de errores:** al automatizar procesos basados en reglas y datos, los agentes minimizan la posibilidad de error humano en tareas repetitivas.
- **Operación 24/7:** a diferencia de un equipo humano, los sistemas inteligentes pueden operar continuamente, sin interrupciones, garantizando que los procesos críticos nunca se detengan.
- **Toma de decisiones basada en datos:** los agentes pueden analizar volúmenes masivos de datos en tiempo real para tomar decisiones optimizadas, algo imposible para un ser humano.
- **Personalización a escala:** pueden usarse para crear experiencias altamente personalizadas para los clientes, como un asistente de compras virtual que entiende sus preferencias y busca las mejores ofertas.

## Aplicaciones prácticas de los agentes de IA

La aplicabilidad de los agentes de IA se extiende por todos los sectores de la economía, como por ejemplo:

- **Atención al cliente:** asistentes virtuales y chatbots avanzados que no solo responden preguntas, sino que resuelven problemas complejos, como reprogramar un vuelo o procesar una devolución, interactuando con múltiples sistemas.
- **E-commerce:** agentes que monitorean los precios de la competencia y ajustan los precios de tu tienda en tiempo real para maximizar la competitividad.
- **Recursos humanos:** agentes que realizan el filtrado de currículums, programan entrevistas con los candidatos más calificados e incluso conducen las primeras fases del proceso de selección.
- **Desarrollo de software:** agentes de software que pueden recibir una tarea de un backlog (ej.: "crea una pantalla de inicio de sesión con autenticación de Google"), escribir el código, crear las pruebas y enviarlo para la aprobación de un desarrollador humano.
- **Finanzas:** agentes que monitorean el mercado financiero, identifican oportunidades de inversión basadas en criterios predefinidos y ejecutan órdenes de compra y venta.

## Paso a paso de cómo usar e implementar agentes de IA

![](https://cdn-wcsm.alura.com.br/2026/07/16183430/img1.webp)

  
_La estructura de un agente de IA está compuesta por capas complejas de procesamiento y aprendizaje, permitiendo que perciba, razone y ejecute acciones de forma inteligente._

La buena noticia es que no necesitas ser un experto en IA para comenzar a usar agentes. Plataformas como GPT-5 de OpenAI (que incluso puso a disposición un “modo agente” recientemente), ya permiten la creación de "GPTs" personalizados e integraciones con plataformas de terceros.

Para una empresa que desea una implementación de IA más robusta, el camino generalmente involucra:

- **Identificar el caso de uso:** comienza con un proceso de negocio bien definido, repetitivo y que se beneficiaría de la automatización.
- **Elegir la plataforma:** utiliza plataformas en la nube como AWS (con Amazon Bedrock) o Google Cloud (con Vertex AI), que ofrecen las herramientas y los modelos base para construir agentes.
- **Conectar las herramientas:** dale a tu agente acceso a las "herramientas" que necesita, como la API de tu sistema de CRM, tu base de datos de productos o acceso a internet.
- **Definir las metas y restricciones:** sé claro sobre el objetivo del agente y, fundamentalmente, sobre sus limitaciones y "barreras de seguridad" (guardrails) para garantizar que actúe de forma segura y ética.
- **Probar e iterar:** comienza con un piloto en un entorno controlado, monitorea el comportamiento del agente, recopila feedback y refina su desempeño antes de lanzarlo a  
    producción.

## Tendencias y futuro de los agentes de IA

El futuro de la automatización está intrínsecamente ligado a la evolución de los agentes de IA. Las principales tendencias apuntan hacia:

- **Multi-agentes:** sistemas donde múltiples agentes de IA, cada uno con su especialidad (un agente de investigación, un agente de codificación, un agente de redacción), colaboran para resolver un problema aún más complejo.
- **Democratización:** la creación de plataformas low-code y no-code que permiten que cualquier persona, incluso sin conocimientos técnicos, pueda crear y configurar sus propios agentes digitales para automatizar sus tareas diarias.
- **Agentes proactivos:** en lugar de esperar una orden, los agentes del futuro serán proactivos. Podrán, por ejemplo, analizar tu agenda y tus correos electrónicos y sugerir autónomamente la preparación de un resumen para tu próxima reunión.
- **Impacto en el trabajo:** el ascenso de los agentes acelerará la transformación digital y redefinirá muchas profesiones. El enfoque del trabajo humano se moverá cada vez más de la "ejecución" a la "estrategia, creatividad y supervisión" de las tareas ejecutadas por los agentes.

## Manos a la obra: herramientas prácticas para crear agentes de IA

Aunque la teoría detrás de los agentes de IA es fascinante, la buena noticia es que no necesitas ser un experto en aprendizaje automático para comenzar a construir tus propios sistemas autónomos.

Una nueva generación de herramientas y frameworks está haciendo que la creación de agentes sea más accesible que nunca. Vamos a explorar dos herramientas poderosas que representan enfoques diferentes, pero complementarios: n8n y CrewAI.

### n8n: automatización y orquestación con low-code

Piensa en n8n como una plataforma de automatización de flujos de trabajo superpoderosa, una especie de "Lego" digital para conectar diferentes aplicaciones y servicios. Te permite crear automatizaciones complejas de forma visual, conectando "nodos" que representan acciones en diversas herramientas (Gmail, Slack, Google Sheets, bases de datos, etc.).

#### ¿Cómo se convierte esto en un agente de IA?

La magia ocurre cuando insertas nodos de IA (como los de OpenAI, Claude o Google Gemini) en tus flujos de trabajo. Con esto, puedes crear "agentes" para tareas específicas sin necesidad de programación profunda. n8n es ideal para quienes buscan crear agentes de automatización que integren múltiples herramientas digitales, orquestando tareas de forma inteligente con un enfoque visual y de bajo código (low-code).

### CrewAI: Construyendo equipos de agentes autónomos con Python

Si n8n es como un Lego para conectar herramientas, CrewAI es un framework para construir un verdadero "equipo" de agentes de IA especializados que colaboran para resolver problemas más complejos. Es una biblioteca en Python, lo que significa que está orientada a quienes ya programan y desean crear sistemas de agentes más sofisticados.

CrewAI funciona basándose en algunos conceptos centrales:

- **Agents (Agentes):** Defines agentes con roles, objetivos e incluso una "historia de fondo" (backstory). Por ejemplo, un "Agente Investigador de Mercado".
- **Tasks (Tareas):** Describes las tareas específicas que cada agente debe ejecutar.
- **Crews (Equipos):** Armas un "equipo" con tus agentes y defines el proceso de colaboración entre ellos (ej.: secuencial o jerárquico).

El sistema gestiona el paso de información entre los agentes hasta que se completa la tarea final. Es una herramienta perfecta para quienes buscan explorar el poder de los sistemas multi-agente, simulando un equipo de especialistas autónomos para resolver problemas que requieren diferentes habilidades y etapas.

## ¿Cómo aprender y prepararse para la era de los agentes de IA?

La llegada de los agentes de IA no es una amenaza, sino una oportunidad inmensa para quienes estén preparados. Entender los fundamentos de la inteligencia artificial aplicada y del machine learning se convierte en un diferencial competitivo en cualquier área.

En Alura encontrarás el ecosistema de aprendizaje más completo para profundizar en este universo.

Comienza por la **Formación en Inteligencia Artificial**, que te dará la base conceptual para entender cómo funcionan estos sistemas.

Para quienes quieran poner manos a la obra y aprender a construir los "cerebros" detrás de los agentes, la **Formación en Machine Learning** es el camino ideal.

Y para quienes quieran estar a la vanguardia de la aplicación de estas tecnologías, el **Posgrado en Inteligencia Artificial, Machine Learning & Deep Learning** de la FIAP es la inmersión más profunda que puedes tener en el tema.

La era de los agentes inteligentes apenas comienza. Prepárate para ser la persona que no solo usa, sino que también comprende y construye las herramientas que definirán el futuro.

¿Quieres estar a la vanguardia de la innovación tecnológica? ¡Explora los cursos de IA de la Escuela de Inteligencia Artificial de Alura y domina las habilidades que están moldeando el futuro del trabajo!

## FAQ | Preguntas frecuentes sobre agentes de IA

¿Aún tienes dudas después del contenido? ¡No te preocupes, consulta las más frecuentes a continuación!

### ¿Qué son los agentes de IA?

Un Agente de IA es un sistema de software que puede percibir su entorno, tomar decisiones de forma autónoma y ejecutar acciones para alcanzar un objetivo específico. A diferencia de un chatbot que solo responde a un comando, un agente puede crear y seguir un plan con múltiples pasos, como investigar información, interactuar con otras herramientas y autocorregirse para completar una tarea compleja.

### ¿Cuál es la diferencia entre un agente de IA y ChatGPT?

Piensa en ChatGPT como un "cerebro" poderoso: procesa información y genera respuestas. Un Agente de IA es ese cerebro conectado a "manos y piernas" digitales. Es decir, además de razonar, el agente puede actuar, ejecutando tareas como navegar por sitios web, enviar correos electrónicos, crear archivos o interactuar con APIs, todo de forma autónoma para alcanzar una meta.

### ¿Cuáles son los tipos de agentes de IA?

Los agentes se clasifican por su complejidad. Los más simples son los agentes de reflejo, que reaccionan a reglas directas (si X, entonces Y). Los más avanzados son los agentes de aprendizaje, que poseen memoria, aprenden de sus acciones y optimizan su comportamiento a lo largo del tiempo para alcanzar sus metas de forma más eficiente. Los agentes modernos generalmente se encuadran en esta última categoría.

### ¿Cuáles son algunos ejemplos de agentes de IA?

Ya interactúas con agentes simples en el día a día: el asistente de voz de tu celular (Siri, Google Assistente), el sistema de recomendación de Netflix, e incluso un bot de spam que filtra tus correos. Los agentes más avanzados, que ejecutan tareas complejas, están surgiendo en áreas como asistentes de compras que comparan precios en varios sitios o agentes que gestionan tu calendario de forma proactiva.

### ¿Dónde puedo crear agentes de IA?

La creación de agentes se está volviendo más accesible. Plataformas de automatización visual como n8n permiten crear agentes simples que conectan diferentes aplicaciones. Para construir sistemas más complejos y con múltiples agentes colaborativos, frameworks de programación como CrewAI son herramientas poderosas para quienes ya desarrollan.

### ¿Qué hace un profesional de IA?

Un profesional de IA es quien diseña, desarrolla y entrena los sistemas de inteligencia artificial. Su trabajo puede involucrar desde el análisis de datos para entrenar modelos y la programación de algoritmos de machine learning, hasta la construcción de la arquitectura de sistemas complejos como los agentes de IA. Es una función que exige sólidos conocimientos en programación, estadística y lógica.

### ¿Son los agentes de IA el futuro del trabajo?

Son una parte fundamental del futuro del trabajo y de la automatización. Los agentes de IA no deberían reemplazar completamente a los humanos, sino aumentar sus capacidades, asumiendo tareas repetitivas y complejas. Esto permitirá que los profesionales se concentren en actividades que requieren creatividad, pensamiento estratégico e inteligencia emocional, trabajando en colaboración con estos sistemas inteligentes.

# Cómo los agentes potencian el rendimiento de las LLMs

![agente llama](https://www.aluracursos.com/_next/image?url=https%3A%2F%2Fcdn-wcsm.alura.com.br%2F2026%2F07%2F16224517%2Fcomo-agentes-podem-ajudar-llms2.jpeg&w=1200&q=100)

---

## Índice de contenidos

Quienes estudian tecnología ya conocen muy bien el poder de generación de texto de las LLMs y que su uso no se limita solo a chatbots llenos de certezas.

Desde mediados de 2022, quienes están cerca de los medios digitales en su día a día laboral ya han sentido la llamada Cuarta Revolución Industrial en su propia piel.

Con la llegada de la IA de Meta a WhatsApp en octubre de 2024, la tendencia es que esta tecnología se popularice aún más y pase a formar parte de la vida de personas que aún no la conocían.

En la ola de la industria 4.0, por las vivencias con Internet de las Cosas e incluso por inspiración de películas de Ciencia Ficción, imaginamos un futuro en el que la Inteligencia Artificial se integre al cotidiano teniendo conocimiento sobre información importante en tiempo real y siendo responsible de la realización de tareas repetitivas. Déjame decirte algo: ¡estamos en camino!

Los agentes de IA pueden ser la pieza que transforme radicalmente nuestra interacción con la tecnología.

En este artículo, vamos a explorar el concept de agentes de IA, sus características y aplicaciones prácticas, además de reflexionar sobre los impactos que esta herramienta puede tener en la industria.

## ¿Qué son los agentes?

Los agentes actúan como controladores de la lógica y las acciones de un sistema modular de IA. Con una LLM sirviendo como “cerebro”, un agente toma decisiones y ejecuta tareas de forma autónoma.

Si eres un chef de cocina experimentado y necesitas preparar una cena, no necesitas seguir una receta estrictamente de principio a fin. Mientras te dedicas al plato principal, puedes pedirle a alguien que prepare la mesa, a otra persona que pique el perejil y a una tercera que higienice la ensalada.

Ahora, si nunca has cocinado antes, necesitarás seguir las instrucciones con cuidado y gastar mucho más tiempo para concluir la comida.

Cuando construimos un sistema de IA basado en agentes, el agente funciona como ese chef de cocina experimentado, con la capacidad de planificar, actuar y delegar tareas.

La lógica del sistema está bajo su control: él decide qué hacer con base en los datos que tiene a mano y en cómo organizarlos mejor para alcanzar el objetivo.

Esto se diferencia de los sistemas que, incluso usando LLMs para realizar tareas, siguen condiciones exactas impuestas por la persona que programó el sistema.

En resumen, lo que diferencia el uso de una LLM en agentes de un sistema tradicional programado por humanos es que, en lugar de decisiones preprogramadas o reglas fijas, el modelo de lenguaje usa su capacidad de entendimiento para decidir dinámicamente qué camino seguir, lo que otorga mayor flexibilidad y adaptabilidad al sistema.

## ¿Cuáles son las capacidades de los agentes?

De forma general, las capacidades de los agentes son:

- Recuperación de datos de diferentes tipos (no estructurados, semiestructurados, estructurados) y realización de búsquedas automáticas.
- Interacción con APIs de servicios externos, procesando o almacenando datos para uso futuro.
- Mantener y analizar historiales de conversaciones.
- Ejecutar tareas de datos complejas.

## ¿Y cuáles son las principales características de los agentes?

Ahora que entendemos las capacidades esenciales de los agentes, vamos a profundizar en las características que los tornan tan adaptables y eficazes para diversas aplicaciones.

- **Autonomía:** Los agentes son capaces de tomar decisiones y ejecutar tareas por cuenta propia, sin necesidad de intervención humana constante.
- **Capacidad de Planificación:** Un agente no solo reacciona a inputs, sino que también anticipa etapas futuras, organizando una secuencia lógica de acciones para alcanzar el objetivo. Calcula qué necesita hacerse y en qué orden, considerando la situación actual.
- **Delegación y Coordinación:** En un sistema modular, un agente puede distribuir tareas entre otros agentes o componentes del sistema, coordinando el trabajo de manera eficiente.
- **Adaptación y Flexibilidad:** A diferencia de los sistemas tradicionales que siguen reglas preprogramadas, los agentes pueden ajustar sus acciones con base en las condiciones y el contexto. Esto permite que el sistema maneje situaciones imprevistas o variables.
- **Uso de LLMs para la Toma de Decisiones:** La lógica del sistema es controlada por un modelo de lenguaje, que actúa como "cerebro" del agente. Este LLM procesa información, entiende el contexto y elige la mejor respuesta o acción.
- **Orquestación de Tareas:** Un agente puede servir como orquestador en un sistema complejo, garantizando que todas las partes del sistema cooperen de manera eficaz. Puede gestionar múltiples agentes más pequeños o tareas paralelas, asegurando que el trabajo fluya.

## ¿Cómo toman decisiones los agentes?

La toma de decisión autónoma es una de las mayores ventajas de los agentes de IA en comparación con los sistemas tradicionales.

A diferencia de simples autómatas que siguen una programación rígida, los agentes de IA toman decisiones de forma adaptativa y dinámica.

Este proceso, llamado ciclo de decisión autónomo, es una secuencia que involucra:

- **Análisis del estado actual:** El agente recopila datos o interpreta un contexto específico, ya sea un mensaje recibido, una nueva entrada de sensor o un dato externo.
- **Planificación de acciones:** Con base en su objetivo, el agente considera el conjunto de herramientas y datos a su disposición, planificando una secuencia de acciones.
- **Ejecución y Evaluación:** El agente realiza la acción planificada y, si es necesario, ajusta el plan conforme al feedback, creando un sistema que mejora con la práctica.

Un enfoque utilizado en este ciclo es el ReAct (Reason + Act: Razonamiento + Acción). En lugar de simplemente seguir comandos, ReAct permite que el agente alterne entre razonar sobre un problema y realizar acciones para resolverlo.

Así, el agente logra reflexionar sobre cada etapa antes de actuar, lo que aumenta la precisión de su respuesta y la adaptabilidad del sistema.

![diagrama de flujo](https://cdn-wcsm.alura.com.br/2026/07/16222603/diagrama-de-fluxo2-765x1024.jpeg)

## ¿Cómo sería un sistema multi-agentes?

En un sistema multi-agentes, cada agente está especializado en una tarea o área, y la colaboración entre ellos potencia el funcionamiento del sistema.

Considera un ejemplo donde la empresa utiliza un sistema multi-agentes para monitorear y gestionar las operaciones de una fábrica inteligente.

- **Agente de Monitoreo:** Recopila datos de sensores distribuidos por la fábrica y detecta problemas, como el calentamiento excesivo de una máquina.
- **Agente de Diagnóstico:** Recibe la alerta del Agente de Monitoreo y realiza un análisis para determinar la causa probable, pudiendo consultar historiales y datos técnicos.
- **Agente de Mantenimiento:** Planifica una intervención, si es necesario, y organiza los pasos que un operador humano u otro agente mecánico deben seguir para resolver el problema.
- **Agente de Logística:** Coordina el reabastecimiento de piezas o componentes que puedan ser necesarios para la intervención, organizando el flujo de materiales en la fábrica.

Así, el sistema multi-agentes opera en conjunto, con cada unidad enfocada en una tarea, pero colaborando de forma coordinada. Este tipo de sistema ya encuentra aplicaciones en industrias avanzadas, haciendo que la automatización sea más inteligente y adaptable a los cambios del entorno de producción.

Sin embargo, no todos los agentes necesitan ser complejos o responsables de una amplia gama de decisiones. Los agentes simples también tienen su importancia y pueden componer un sistema al ser responsables de la ejecución de una sola tarea o de un conjunto muy restringido de acciones. Por ejemplo, en un sistema de atención automatizado de una tienda virtual, podemos tener:

- **Agente de Verificación de Inventario:** Al recibir una consulta sobre un producto, este agente verifica la cantidad disponible en el inventario y responde sobre la disponibilidad.
- **Agente de Cotización de Envío:** Responsable de calcular el valor del flete de acuerdo con la dirección del cliente y las opciones de entrega disponibles. Este agente devuelve el valor calculado y las posibles fechas de entrega.
- **Agente de Emisión de Factura:** Después de que se finaliza una compra, este agente emite la factura y la envía al cliente.

## Coordinación entre agentes simples y complejos

En sistemas multi-agentes más sofisticados, los agentes simples son frecuentemente coordinados por un agente orquestador o agente principal, que tiene una visión más amplia y puede dirigir a los agentes especializados según sea necesario. Este orquestador puede ser responsable de:

- Delegar tareas a diferentes agentes simples, garantizando que todos los pasos del proceso se ejecuten en la secuencia correcta.
- Gestionar fallas o retrasos, redistribuyendo tareas para que el sistema continúe operando sin interrupciones.
- Supervisar el desempeño de los agentes y ajustar la asignación de tareas según la demanda.

![diagrama de sistemas](https://cdn-wcsm.alura.com.br/2026/07/16223406/diagrama-de-sistema2-1024x572.jpeg)

Sistemas multi-agentes no están limitados a fábricas y operaciones físicas; en el comercio minorista en línea, en la logística e incluso en la salud, estos sistemas coordinados se aplican para optimizar procesos, reduce errores y aumentar la autonomía de las operaciones.

## Cómo aplicar un agente con LlamaIndex

¿Vamos a experimentar con la aplicación de un agente de matemáticas? Utilicé Google Colab para este ejemplo.

Primero, vamos a instalar las bibliotecas necesarias para crear y configurar nuestro agente de IA con LlamaIndex.

```
!pip install llama-index
!pip install llama-index-llms-groq
!pip install llama_index.core.agent
!pip llama_index.core.tools
```

Ahora que instalamos las bibliotecas, el siguiente paso es importar los módulos y clases principales que nos ayudarán a construir el agente.

Aquí, llamamos al `ReActAgent` y `FunctionCallingAgentWorker` de la biblioteca LlamaIndex, además de herramientas específicas para manejar funciones y el modelo Groq, que será responsable de traer el LLM a nuestro entorno. La importación de `userdata` de Google nos permitirá acceder a una clave de API.

```
from llama_index.core.agent import ReActAgent, FunctionCallingAgentWorker
from llama_index.core.tools import FunctionTool
from llama_index.llms.groq import Groq
from google.colab import userdata
```

Ahora, necesitamos una clave de API que permita utilizar Llama. Puedes crear una clave a través del sitio de Groq. Crea tu cuenta, genera la API Key y cópiala.

En Colab, para agregar una clave de API, haz clic en el icono de llave que se encuentra en el menú lateral izquierdo. Luego, dale un nombre (aquí utilicé `GROQ_API`) y, en el valor, pega tu clave. Es necesario permitir el acceso al notebook.

Para acceder a la clave, podemos utilizar el siguiente código:

```
api_key= userdata.get('GROQ_API')
```

Podemos elegir un modelo proporcionado por Groq. Aquí, elegí el Llama3. En la plataforma Groq, puedes consultar una lista de otros modelos disponibles y, dependiendo de tu necesidad, optar por otro modelo ajustando el parámetro `model`.

```
llama3 = Groq(model="llama3-70b-8192", api_key=api_key)
llama3
```

¡Genial! Ahora es el momento de crear las herramientas que el agente podrá utilizar. Con LlamaIndex, estas herramientas se crean como simples funciones de Python y luego cada función se registra como una `FunctionTool`, permitiendo que el agente acceda y ejecute estas operaciones cuando sea necesario.

Creamos una función `multiply` que devuelve la multiplicación de dos números enteros y una función `add` que devuelve la suma de dos números enteros.

```
from llama_index.core.tools import FunctionTool
def multiply(a: int, b: int) -> int:
    """Multiple two integers and returns the result integer"""
    return a * b
multiply_tool = FunctionTool.from_defaults(fn=multiply)
def add(a: int, b: int) -> int:
    """Add two integers and returns the result integer"""
    return a + b
add_tool = FunctionTool.from_defaults(fn=add)
```

Con las herramientas creadas, vamos a configurar el agente usando el modelo ReAct. Le pasamos las herramientas creadas anteriormente y la LLM que también ya configuramos.

El parámetro `verbose=True` permite que el agente muestre los pasos que toma durante el procesamiento de las instrucciones; así, tendremos una visualización muy gráfica de cómo funciona el proceso de razonamiento y acción del agente.

```
react_agent = ReActAgent.from_tools(tools=[multiply_tool, add_tool], llm=llama3, verbose=True)
react_agent
```

¡Genial, agente definido! Así de simple. Ten en cuenta que este es un ejemplo de aplicación muy básica, donde definimos solo dos operaciones matemáticas como herramientas. Sin embargo, la escalabilidad del proyecto puede ocurrir de acuerdo con las necesidades a las que se proponga el sistema, con múltiples agentes y herramientas más complejas.

En esta prueba, le pedimos al agente calcular "¿Cuánto es la suma de 154 y 90 por cinco?". Esta pregunta requiere que interprete correctamente el orden de las operaciones (multiplicación y adición) y utilice las funciones que creamos anteriormente para sumar y multiplicar.

El agente debe realizar la multiplicación primero (90 por 5), pasando los valores en el formato correcto a la herramienta y, a continuación, sumar el resultado a 154, garantizando que la respuesta sea correcta.

```
response = react_agent.chat("Quanto é a soma de 154 e 90 vezes cinco?")
print(str(response))
```

Al ejecutarlo, tenemos la siguiente respuesta:

```
Running step 3ca66650-4add-4593-b036-8d6feaa670a5. Step input: Quanto é a soma de 154 e 90 vezes cinco?
Thought: The current language of the user is: Portuguese. I need to use a tool to help me answer the question.
To calculate 90 times 5, I'll use the multiply tool.
Action: multiply
Action Input: {'a': 90, 'b': 5}
Observation: 450
> Running step 31ae365c-db7d-47ce-b5e4-43de579064ad. Step input: None
Thought: Now I have the result of 90 times 5, which is 450. I need to add 154 to this result.
To add 154 and 450, I'll use the add tool.
Action: add
Action Input: {'a': 154, 'b': 450}
Observation: 604
> Running step d8d71fe6-b6e6-4917-8573-8ae137bac149. Step input: None
Thought: I can answer without using any more tools. I'll use the user's language to answer
Answer: A soma de 154 e 90 vezes 5 é 604.
A soma de 154 e 90 vezes 5 é 604.
```

¡Mira qué interesante! En cada paso, el agente “piensa” en lo que debe hacerse. Primero, detecta que la pregunta se hizo en español (o portugués en el original) y que debe mantener la respuesta en ese idioma. A continuación, interpreta que necesita resolver 90 por 5 antes de sumar, siguiendo el orden de precedencia de las operaciones matemáticas. Con el resultado de la multiplicación en mano, el agente sigue a la siguiente etapa y utiliza la herramienta de adición. Con la respuesta de la herramienta, el agente responde respetando el idioma de entrada.

En LlamaIndex, es posible construir agentes desde cero o utilizar los que ya están construidos en LlamaHub. El flujo de trabajo para la construcción de agentes en LlamaIndex es asíncrono y orientado a eventos (_event-driven_). Puedes aprender más sobre esto en la documentación.

## Conclusión

Por su capacidad de adaptación y flexibilidad, los agentes son ideales para una amplia variedad de sectores. Al permitir la automatización inteligente de procesos complejos, los sistemas basados en agentes pueden contribuir a la eficiencia operativa y la optimización de recursos, aliviando a los profesionales de tareas repetitivas y creando espacio para iniciativas más estratégicas.

¡En este artículo, conocimos cómo funcionan los agentes y cómo pueden llevar la aplicación de LLMs en sistemas a otro nivel! Sin duda, todavía tendremos muchas novedades en este campo de estudio. La comunidad está dedicada a construir siempre mejores soluciones para el uso de IA. ¡Sigue las notificaciones de Alura para estar al tanto de nuestros lanzamientos en datos e IA!