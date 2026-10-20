# 🤖 Bots de Ventas — Chat con IA

Chat web de una sola página que funciona como **asistente de ventas** para una tienda de equipos electrónicos. Las respuestas se generan con la API de **OpenAI** (Chat Completions).

## ✨ Características

- Interfaz de chat moderna con efecto *glassmorphism* y degradados.
- Burbujas diferenciadas para el usuario y la IA, con animación de aparición.
- Indicador "Escribiendo..." mientras se espera la respuesta.
- `Enter` envía el mensaje · `Shift + Enter` inserta un salto de línea.
- El botón se desactiva durante la consulta para evitar envíos duplicados.
- Manejo de errores con un mensaje visible en el chat.
- Respuestas acotadas por un *prompt* de sistema: el bot solo atiende consultas de la tienda y responde en menos de 30 palabras.

## 🛠️ Tecnologías

| Herramienta | Uso |
|---|---|
| HTML + JavaScript (vanilla) | Estructura y lógica del chat |
| [Tailwind CSS 3.4](https://tailwindcss.com/) (CDN) | Estilos, colores `marca` y animaciones personalizadas |
| [Axios 1.20](https://axios-http.com/) (CDN) | Peticiones HTTP a la API |
| [Google Fonts — Poppins](https://fonts.google.com/specimen/Poppins) | Tipografía |
| [OpenAI API](https://platform.openai.com/docs/api-reference/chat) | Modelo `gpt-5` para generar respuestas |

## 📁 Estructura

```
chat-openai-gitflow2/
├── index.html   # Interfaz, estilos y lógica del chat
└── README.md
```

## 🚀 Cómo usarlo

1. Clona el repositorio:
   ```bash
   git clone https://github.com/alessio034/chat-openai-gitflow.git
   cd chat-openai-gitflow
   ```
2. Abre `index.html` y reemplaza `TOKEN_AQUI` por tu API key de OpenAI:
   ```js
   "Authorization": "Bearer TOKEN_AQUI"
   ```
3. Abre `index.html` en el navegador (doble clic o con una extensión como *Live Server*).
4. Escribe tu consulta y presiona **Consultar** o `Enter`.

## ⚙️ Personalización

- **Comportamiento del bot:** edita el mensaje con `role: "system"` dentro de `consultarChat()`.
- **Modelo:** cambia el valor de `"model"` (por ejemplo, `"gpt-5"`).
- **Colores:** modifica la paleta `marca` en `tailwind.config` dentro del `<head>`.

## ⚠️ Seguridad

La API key se envía directamente desde el navegador, por lo que **cualquiera que abra la página puede verla**. Este enfoque sirve solo para pruebas y aprendizaje:

- No subas tu API key real al repositorio.
- Para producción, usa un pequeño backend (Node/Express, función serverless, etc.) que guarde la clave en una variable de entorno y haga de intermediario con OpenAI.

## 🌿 Flujo de trabajo

Este proyecto se usa para practicar **Git Flow** (ramas `main`, `develop`, `feature/*`, etc.) con GitHub.
