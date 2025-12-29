# Cool App - React + TypeScript + Vite + AWS Amplify

Esta aplicación fue creada usando Vite con React y TypeScript, y configurada con AWS Amplify para el backend.

## Pasos de Instalación

### 1. Crear el proyecto con Vite

```bash
PS C:\Users\ecs50\Documents\cool-app> npm create vite@latest .
```

**Configuración seleccionada:**
- Framework: React
- Variant: TypeScript
- Use rolldown-vite (Experimental)?: No
- Install with npm and start now?: Yes

**Resultado:**
```
Scaffolding project in C:\Users\ecs50\Documents\cool-app...
Installing dependencies with npm...
added 222 packages, and audited 223 packages in 24s

45 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

Starting dev server...

> cool-app@0.0.0 dev
> vite

VITE v7.3.0  ready in 534 ms

➜  Local:   http://localhost:5173/
➜  Network: use --host to expose
➜  press h + enter to show help
```

### 2. Agregar AWS Amplify

```bash
PS C:\Users\ecs50\Documents\cool-app> npm create amplify@latest
```

**Configuración:**
- Where should we create your project?: . (directorio actual)

**Proceso de instalación:**
```
1:51:09 PM Installing devDependencies:
1:51:09 PM  - @aws-amplify/backend
1:51:09 PM  - @aws-amplify/backend-cli
1:51:09 PM  - aws-cdk-lib@2.216.0
1:51:09 PM  - constructs@^10.0.0
1:51:09 PM  - typescript@^5.0.0
1:51:09 PM  - tsx
1:51:09 PM  - esbuild

1:51:09 PM Installing dependencies:
1:51:09 PM  - aws-amplify

1:54:36 PM ✓ DevDependencies installed
1:55:02 PM ✓ Dependencies installed
1:55:02 PM ✓ Template files created

Successfully created a new project!

Welcome to AWS Amplify!
 - Get started by running npx ampx sandbox.
 - Run npx ampx help for a list of available commands.
```

## Comandos Disponibles

- `npm run dev` - Inicia el servidor de desarrollo
- `npx ampx sandbox` - Inicia el entorno de desarrollo de Amplify
- `npx ampx help` - Muestra la lista de comandos disponibles de Amplify

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
