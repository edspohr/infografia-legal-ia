Demo de Triage Legal con IA
Este proyecto es una landing page interactiva que demuestra un flujo de trabajo autónomo para la gestión de consultas legales, impulsado por la API de Gemini de Google. La aplicación simula cómo un asistente de IA puede recibir una consulta inicial de un cliente, interactuar automáticamente para recopilar información clave y, finalmente, generar un informe ejecutivo consolidado para un abogado.

La infografía está diseñada para ser presentada a profesionales del derecho, mostrando el potencial de la IA para optimizar la carga administrativa y mejorar la eficiencia de un estudio jurídico.

✨ Características Principales
Diseño de Infografía: La interfaz es una página única (SPA) con un diseño limpio y profesional, construida con HTML y Tailwind CSS.

Flujo de Trabajo Simulado: Demuestra un proceso de dos pasos:

Análisis Inicial: La IA recibe la consulta, la analiza y genera un correo electrónico con preguntas aclaratorias.

Informe Ejecutivo: La IA simula las respuestas del cliente y, con la información enriquecida, redacta un informe final para el abogado.

Integración Segura con la API: Utiliza Vercel Serverless Functions como un proxy seguro para gestionar la clave de la API de Gemini, asegurando que nunca se exponga en el lado del cliente.

Contexto Legal Chileno: Los prompts están diseñados para que la IA actúe con conocimiento de la legislación y terminología legal de Chile.

🚀 Cómo Desplegar tu Propia Versión
Puedes desplegar tu propia instancia de esta aplicación en minutos siguiendo estos pasos.

Prerrequisitos
Una cuenta de GitHub.

Una cuenta de Vercel (puedes registrarte con tu cuenta de GitHub).

Una Clave de API de Gemini.

Pasos
Obtén tu Clave de API de Gemini

Ve a Google AI Studio.

Inicia sesión y haz clic en "Get API key" -> "Create API key in new project".

Copia y guarda tu clave. La necesitarás en el paso 3.

Haz un Fork de este Repositorio

Haz clic en el botón "Fork" en la esquina superior derecha de esta página para crear una copia del repositorio en tu propia cuenta de GitHub.

Despliega en Vercel

Ve a tu panel de control de Vercel y haz clic en "Add New..." -> "Project".

Importa el repositorio del que acabas de hacer fork.

Vercel detectará la configuración automáticamente. Antes de desplegar, ve a la sección "Environment Variables".

Añade la siguiente variable:

Name: VITE_GEMINI_API_KEY

Value: Pega aquí la clave de API que obtuviste en el primer paso.

Haz clic en "Deploy".

¡Y listo! Vercel desplegará tu aplicación y te proporcionará una URL pública para que puedas compartirla.

📂 Estructura del Proyecto
El proyecto es simple y se compone de dos archivos principales:

index.html: Contiene toda la estructura visual (HTML), el estilo (Tailwind CSS) y la lógica del cliente (JavaScript). Este archivo es responsable de capturar la entrada del usuario y mostrar los resultados.

/api/proxy.js: Es una Función Serverless de Vercel. Actúa como un intermediario seguro entre el cliente y la API de Gemini. Recibe la petición del index.html, añade la clave de API secreta (que solo existe en el servidor de Vercel) y reenvía la petición a Google.

✉️ Contacto
Este proyecto fue desarrollado por:

Edmundo Spohr - Gerente Digital Outsourced

Email: edmundo@spohr.cl

WhatsApp: +56965863160
