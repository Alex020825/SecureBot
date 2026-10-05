# SecurBot - Auditor de Ciberseguridad Interactivo

SecurBot es un asistente virtual impulsado por Inteligencia Artificial diseñado para actuar como un auditor de código y arquitectura. Analiza fragmentos de código, detecta vulnerabilidades clásicas (como Inyecciones SQL o XSS) y sugiere soluciones aplicando las mejores prácticas de ciberseguridad.

## Stack Tecnológico
* **Frontend:** React, TypeScript, TailwindCSS, Vite.
* **Backend:** NestJS, TypeScript, Prisma (ORM).
* **Base de Datos:** PostgreSQL.
* **Comunicación en Tiempo Real:** WebSockets (Socket.io) para respuestas en streaming.

##  Características Principales
- **Auditoría en Streaming:** La IA procesa y devuelve el análisis en tiempo real (letra por letra), mejorando la experiencia del usuario.
- **Persistencia de Contexto:** Almacenamiento del historial de chats en PostgreSQL mediante Prisma, permitiendo a la IA recordar mensajes anteriores en la misma sesión.
- **Arquitectura Modular:** Separación clara entre el cliente y el servidor mediante un monorepositorio.

##  Cómo levantar el proyecto en local
1. Clona el repositorio.
2. Configura tu base de datos PostgreSQL local y actualiza el archivo `.env` del backend con tu `DATABASE_URL`.
3. En la carpeta `backend`, instala las dependencias (`pnpm install`) y ejecuta las migraciones (`npx prisma migrate dev`).
4. Levanta el servidor del backend (`pnpm run start:dev`).
5. En la carpeta `frontend`, instala las dependencias y levanta el entorno de Vite (`pnpm run dev`).