# Cool App - React + TypeScript + Vite + AWS Amplify

Esta aplicación fue creada usando Vite con React y TypeScript, y configurada con AWS Amplify para el backend.

## Instalación

```bash
npm create vite@latest . # React + TypeScript
npm create amplify@latest # AWS Amplify backend
```

## Configuración Inicial del Proyecto

### 1. Configurar Amplify en la aplicación

Después de crear el sandbox, debes registrar Amplify en tu aplicación React. 

En `src/main.tsx`, agrega las siguientes importaciones y configuración:

```typescript
import { StrictMode } from 'react'
import { createRoot } from 'react-dom/client'
import './index.css'
import App from './App.tsx'
import { Amplify } from 'aws-amplify'
import outputs from "../amplify_outputs.json"

Amplify.configure(outputs)

createRoot(document.getElementById('root')!).render(
  <StrictMode>
    <App />
  </StrictMode>,
)
```

**Pasos esenciales para cada proyecto nuevo:**
1. Vite init o framework init
2. `npm create amplify@latest` - agregar Amplify al proyecto
3. `npx ampx sandbox` - crear sandbox de Amplify
4. Registrar Amplify en la app:
   - `import { Amplify } from 'aws-amplify'`
   - `import outputs from "../amplify_outputs.json"`
   - `Amplify.configure(outputs)`

## Comandos Disponibles

- `npm run dev` - Inicia el servidor de desarrollo
- `npx ampx sandbox` - Inicia el entorno de desarrollo de Amplify
- `npx ampx help` - Muestra la lista de comandos disponibles de Amplify

## Configuración del Sandbox

Una vez ejecutado `npx ampx sandbox`, se creará automáticamente:

```
Amplify Sandbox
Identifier:   ecs50
Stack:        amplify-coolapp-ecs50-sandbox-2260eb92d6
Region:       us-east-1

✔ Backend synthesized in 3.66 seconds
✔ Type checks completed in 10.74 seconds
✔ Built and published assets
✔ Deployment completed in 204.475 seconds

AppSync API endpoint = https://bldvau6mpfcsbgjdsku3dx75vu.appsync-api.us-east-1.amazonaws.com/graphql

[Sandbox] Watching for file changes...
File written: amplify_outputs.json
```

El sandbox:
- Genera automáticamente `amplify_outputs.json` con la configuración
- Crea un endpoint de GraphQL API
- Queda en modo watch para detectar cambios en archivos
- Usa el identificador del usuario del sistema por defecto

## Estructura del Proyecto

- `/src` - Código fuente de React
- `/amplify` - Configuración del backend de AWS Amplify
- `/public` - Archivos estáticos

## Notas

Amplify recopila datos de telemetría anónimos sobre el uso general del CLI. La participación es opcional y puedes desactivarla usando:

```bash
npx ampx configure telemetry disable
```

Para más información sobre telemetría, visita: https://docs.amplify.aws/react/reference/telemetry
