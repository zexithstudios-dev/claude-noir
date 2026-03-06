# Claude Noir — Deploy en Vercel

## Archivos
```
claude-noir/
├── api/
│   └── chat.js          ← Backend proxy (guarda tu API key aquí)
├── public/
│   └── index.html       ← La app completa
└── vercel.json          ← Configuración de rutas
```

## Pasos para publicar gratis en Vercel

### 1. Crea una cuenta
Ve a https://vercel.com y regístrate (gratis).

### 2. Sube los archivos
Opción A — Sin GitHub (más fácil):
- Instala Vercel CLI: `npm i -g vercel`
- En la carpeta del proyecto ejecuta: `vercel`
- Sigue los pasos en pantalla

Opción B — Con GitHub:
- Sube esta carpeta a un repositorio en GitHub
- En Vercel → "Add New Project" → importa el repo
- Vercel detecta todo automáticamente

### 3. Agrega tu API Key (MUY IMPORTANTE)
En el dashboard de Vercel de tu proyecto:
- Ve a **Settings → Environment Variables**
- Agrega una variable llamada: `ANTHROPIC_API_KEY`
- Valor: tu key que empieza con `sk-ant-...`
- Obtén tu key en: https://console.anthropic.com

### 4. Redeploy
Después de agregar la variable, haz click en **Redeploy** para que tome efecto.

### ¡Listo!
Tu app estará en una URL pública tipo `https://claude-noir-xxxx.vercel.app`
Cualquier persona puede usarla sin necesitar su propia API key.

## Seguridad
- La API key **nunca** se expone al navegador
- El backend actúa como proxy invisible
- Vercel guarda las variables de entorno de forma cifrada
