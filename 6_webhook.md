**Webhook** (se pronuncia _"web-fuk"_)
# 🪝 ¿Qué es un Webhook?

Un Webhook es un mecanismo que permite que **una aplicación le avise a otra automáticamente cuando pasa algo en tiempo real**

- **La analogía**: Imagina que esperas un paquete. Una opción es llamar al cartero cada 5 minutos para ver si llegó (eso se llama _Polling_ y gasta recursos). La opción del Webhook es dejar tu número para que el cartero **te mande un mensaje de texto solo cuando el paquete esté en tu puerta**.

## 🏗️ ¿Cómo es su estructura básica?

En el desarrollo de software, la estructura de un Webhook consta de dos partes principales:

1. **La URL de Destino (Endpoint)**: Una dirección web privada que tú creas en tu servidor (ej. `https://mi-agente-sena.com`). Es el "buzón" donde vas a recibir la información.

2. **La Carga de Datos (Payload)**: La información real que se envía, que casi siempre viaja en formato **JSON** (un formato de texto estándar en desarrollo de software que organiza los datos en clave y valor). 

## 🤖 ¿Para qué sirve en tu Agente de IA del SENA?

Los Webhooks son los que convierten a tu IA en un **Agente Autónomo** que puede interactuar con el mundo real. Por ejemplo:

- **Conexión con GitHub**: Configuras un Webhook en tu repositorio de código del SENA. Cada vez que subas una tarea (un `git push`), GitHub envía un Webhook automático a tu Agente de IA. Al recibirlo, la IA se activa sola, revisa tu código y te escribe por chat: _"Oye, acabo de ver que subiste el diagrama de clases, déjame revisarlo"_.

- **Alertas de entrega**: Si el SENA cambia la fecha de una entrega en su plataforma virtual, esa plataforma podría enviar un Webhook a tu base de datos para que tu Agente actualice su calendario y te avise de inmediato.

## ❌ ¿Qué pasa si NO usas un Webhook? (Agente Pasivo)

Si decides no programar Webhooks, tu Agente seguirá siendo excelente. Funcionará bajo el modelo de **Petición-Respuesta**.

- **Cómo funciona**: La IA se queda dormida en el servidor de Neon o donde la tengas alojada. Solo se despierta cuando tú entras a la página web y le escribes: _"Hola, ayúdame con este código"_.
- **Resultado**: Es un excelente tutor interactivo, pero es **reactivo** (espera a que tú des el primer paso).

## 🚀 ¿Qué pasa si SÍ le pones un Webhook? (Agente Proactivo)

Si le agregas un Webhook, tu aplicación gana la capacidad de **escuchar al mundo exterior**. Tu Agente se vuelve **proactivo**.

- **Cómo funciona**: Ya no tienes que buscarlo tú. Si estás programando tu entrega del SENA en Visual Studio Code y guardas el archivo, un Webhook puede avisarle a tu IA en segundo plano.
	- **Resultado**: El Agente te puede enviar una notificación automática a tu celular o a Discord diciendo: _"Oye, acabo de detectar que tu script de base de datos tiene un error en la línea 12, corrígelo antes de subirlo a la plataforma del SENA"_.