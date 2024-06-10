# Ionic Firebase Chat App

Este proyecto es una aplicación de chat en tiempo real desarrollada con Ionic y Angular, utilizando Firebase como backend. La aplicación permite a los usuarios registrarse, iniciar sesión, y participar el chat en tiempo real.

## Características

- **Registro de Usuarios:** Los usuarios pueden registrarse con su correo electrónico y contraseña.
- **Autenticación:** Los usuarios pueden iniciar sesión con su cuenta previamente creada.
- **Chat:** Los usuarios pueden unirse en el chat y participar en conversaciones en tiempo real.
- **Mensajería en Tiempo Real:** Los mensajes se envían y reciben instantáneamente gracias a la integración con Firebase.

## Tecnologías Utilizadas

- **Ionic Framework:** Para la construcción de la interfaz de usuario de la aplicación móvil.
- **Angular:** Framework de desarrollo web para crear aplicaciones web dinámicas.
- **Firebase:** Plataforma de Google que proporciona una base de datos en tiempo real y autenticación de usuarios.

## Requisitos Previos

Antes de comenzar, asegúrate de tener instalados los siguientes programas en tu máquina:

- Node.js (v12 o superior)
- npm (v6 o superior)
- Ionic CLI
## Instalación

Sigue estos pasos para configurar y ejecutar el proyecto localmente:
```bash

git clone https://github.com/JosephYM07/Chat_Ionic.git
cd ionic-firebase-chat

```
2. **Instalar Dependencias:**

```bash
npm install

```

3. **Configurar Firebase:**
    - Crea un proyecto en Firebase Console.
    - Configura la autenticación por correo electrónico y contraseña.
    - Crea una base de datos Firestore y configura las reglas para permitir la lectura y escritura.
    - Obtén las credenciales de configuración de Firebase y agrégalas en `src/environments/environment.ts`:
        
        ```tsx
        typescriptCopiar código
        export const environment = {
          production: false,
          firebaseConfig: {
            apiKey: "YOUR_API_KEY",
            authDomain: "YOUR_AUTH_DOMAIN",
            projectId: "YOUR_PROJECT_ID",
            storageBucket: "YOUR_STORAGE_BUCKET",
            messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
            appId: "YOUR_APP_ID"
          }
        };
        
        ```
4. **Ejecutar la Aplicación:**
    
    ```bash

    ionic serve
    
    ```
    

## Estructura del Proyecto

- `src/app/`: Contiene los módulos principales de la aplicación.
    - `auth/`: Módulo de autenticación, incluye páginas de inicio de sesión y registro.
    - `chat/`: Módulo de chat, incluye componentes para mostrar y enviar mensajes.
    - `services/`: Servicios de la aplicación, como autenticación y manejo de datos de Firebase.
