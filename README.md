<p align="center">
  <h1 align="center">🔍 FindIt UNAL</h1>
  <p align="center">
    <strong>Plataforma integral para la gestión de objetos perdidos y encontrados en la Universidad Nacional de Colombia</strong>
  </p>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Frontend-React%2018.3-61DAFB?style=for-the-badge&logo=react&logoColor=white" alt="React"/>
  <img src="https://img.shields.io/badge/Backend-Node%20%2B%20Express-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node"/>
  <img src="https://img.shields.io/badge/TypeScript-5.x-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"/>
  <img src="https://img.shields.io/badge/Socket.IO-Realtime-010101?style=for-the-badge&logo=socketdotio&logoColor=white" alt="Socket.IO"/>
</p>

---

## 📑 Tabla de Contenidos

- [📖 Descripción](#-descripción)
- [✨ Funcionalidades del sistema](#-funcionalidades-del-sistema)
- [🏗️ Arquitectura general](#️-arquitectura-general)
- [🛠️ Tecnologías y herramientas](#️-tecnologías-y-herramientas)
- [📁 Estructura del proyecto](#-estructura-del-proyecto)
- [📋 Requisitos previos](#-requisitos-previos)
- [🚀 Instalación](#-instalación)
- [⚙️ Configuración](#️-configuración)
- [▶️ Ejecución](#️-ejecución)
- [🐳 Docker](#-docker)
- [📘 Documentación adicional](#-documentación-adicional)
- [🤝 Contribución](#-contribución)
- [📄 Licencia](#-licencia)

---

## 📖 Descripción

**FindIt UNAL** es un sistema web para reportar, buscar y administrar objetos perdidos y encontrados dentro de la Universidad Nacional de Colombia. La solución está organizada como un conjunto de servicios y aplicaciones que trabajan juntos para ofrecer una experiencia completa: interfaz web, API de negocio, comunicación en tiempo real y administración centralizada.

El proyecto está pensado para cubrir el ciclo completo del sistema:
- publicación de objetos perdidos o encontrados,
- búsqueda y filtrado por criterios útiles,
- mensajería entre usuarios,
- notificaciones en tiempo real,
- moderación y control administrativo.

---

## ✨ Funcionalidades del sistema

### Para estudiantes y usuarios

| Funcionalidad | Descripción |
|---|---|
| 🔐 **Autenticación institucional** | Inicio de sesión con Google y validación de acceso institucional. |
| 📝 **Registro de reportes** | Creación de reportes de objetos perdidos o encontrados con detalles relevantes. |
| 🖼️ **Carga de imágenes** | Asociación de imágenes a los reportes para facilitar la identificación. |
| 🔍 **Búsqueda y filtros** | Exploración por categoría, ubicación, estado, fecha y texto libre. |
| 📄 **Detalle de objetos** | Vista ampliada con información del reporte, imágenes y acciones asociadas. |
| 💬 **Chat en tiempo real** | Comunicación directa entre usuarios vinculados a un caso. |
| 🔔 **Notificaciones** | Alertas sobre mensajes, cambios de estado y actividad relacionada. |
| 👤 **Perfil de usuario** | Consulta y actualización de datos personales y actividad propia. |
| 📋 **Seguimiento de reportes** | Visualización de reportes propios y su estado actual. |

### Para administradores

| Funcionalidad | Descripción |
|---|---|
| 📊 **Dashboard administrativo** | Resumen de métricas y estado general del sistema. |
| 👥 **Gestión de usuarios** | Consulta, control y administración de usuarios registrados. |
| 📋 **Moderación de reportes** | Supervisión y tratamiento de reportes del sistema. |
| 🚨 **Gestión de quejas** | Revisión de quejas y casos que requieren intervención. |
| 📜 **Logs de actividad** | Registro de acciones relevantes dentro de la plataforma. |
| 🧭 **Control de permisos** | Separación de roles y protección de rutas sensibles. |

### Capacidades técnicas del sistema

- API REST para autenticación, objetos, categorías, ubicaciones, imágenes, reportes, notificaciones, quejas y administración.
- Persistencia de datos en MySQL.
- Validación de datos de entrada en backend.
- Comunicación en tiempo real con Socket.IO para chat y notificaciones.
- Documentación técnica disponible para despliegue y referencia.

---

## 🏗️ Arquitectura general

El proyecto está organizado en tres frentes principales:

| Componente | Carpeta | Propósito |
|---|---|---|
| **Frontend** | `finditunal-frontend/` | Interfaz web construida con React + TypeScript. |
| **Backend** | `finditunal-backend/` | API principal con Express + TypeScript y MySQL. |
| **Documentación** | `finditunal-documentation/` | Material de apoyo y notas del proyecto. |

### Flujo general

1. El usuario interactúa desde el frontend.
2. El frontend consume la API del backend.
3. El backend valida, procesa y persiste la información.
4. MySQL almacena usuarios, objetos, reportes, mensajes y notificaciones.
5. Socket.IO mantiene el canal en tiempo real para chat y avisos.

---

## 🛠️ Tecnologías y herramientas

### Frontend

| Tecnología | Uso |
|---|---|
| **React 18.3** | Construcción de la interfaz de usuario. |
| **TypeScript** | Tipado estático y mejor mantenimiento del código. |
| **Vite** | Desarrollo rápido y build moderno. |
| **TailwindCSS** | Estilos utilitarios y diseño responsivo. |
| **Radix UI** | Componentes accesibles de bajo nivel. |
| **TanStack Query** | Estado del servidor, caché y sincronización de datos. |
| **Zustand** | Estado global ligero. |
| **React Router DOM** | Navegación y protección de rutas. |
| **Socket.IO Client** | Conexión en tiempo real con el backend. |
| **Lucide React** | Sistema de íconos consistente. |
| **react-hot-toast** | Notificaciones visuales. |
| **Supabase JS** | Integración opcional con servicios externos. |

### Backend

| Tecnología | Uso |
|---|---|
| **Node.js** | Entorno de ejecución del servidor. |
| **Express** | API HTTP y ruteo. |
| **TypeScript** | Tipado y estructura más mantenible. |
| **MySQL** | Base de datos relacional principal. |
| **mysql2** | Conector MySQL para Node.js. |
| **Socket.IO** | Tiempo real para chat y notificaciones. |
| **Zod** | Validación de esquemas y payloads. |
| **Multer** | Carga y manejo de archivos. |
| **JWT** | Autenticación basada en tokens. |
| **Google Auth Library** | Integración con autenticación de Google. |
| **Swagger** | Documentación de la API. |
| **Docker / Docker Compose** | Contenedorización y despliegue local. |

### Desarrollo y calidad

| Herramienta | Uso |
|---|---|
| **ESLint** | Reglas de calidad estática. |
| **Prettier** | Formato consistente de código. |
| **Nodemon** | Recarga automática en desarrollo backend. |
| **PostCSS** | Procesamiento de estilos. |
| **Autoprefixer** | Compatibilidad CSS entre navegadores. |

---

## 📁 Estructura del proyecto

```text
project/
├── finditunal-backend/         # API principal y lógica de negocio
├── finditunal-frontend/        # Aplicación web principal
├── finditunal-documentation/   # Documentación complementaria
├── FrontEnd/                   # Variante adicional del frontend
├── uniwheels-chat-service/     # Servicio separado de chat
└── tecnologias.txt             # Apuntes de tecnologías y justificación
```

### Estructura relevante del backend

```text
finditunal-backend/src/
├── controllers/   # Controladores HTTP
├── models/        # Modelos de datos
├── routes/        # Definición de endpoints
├── services/      # Lógica de negocio
├── schemas/       # Validación con Zod
├── middlewares/   # Autenticación, roles, errores y validación
├── database/      # Conexión y utilidades de base de datos
└── utils/         # Utilidades generales
```

### Estructura relevante del frontend

```text
finditunal-frontend/src/
├── components/    # Componentes por nivel de complejidad
├── pages/         # Vistas principales
├── routes/        # Configuración de rutas
├── services/      # Consumo de API
├── hooks/         # Hooks personalizados
├── store/         # Estado global con Zustand
├── context/       # Contextos de aplicación
├── types/         # Tipos TypeScript
└── utils/         # Funciones auxiliares
```

---

## 📋 Requisitos previos

Antes de ejecutar el proyecto, asegúrate de tener instalado:

- **Node.js** 18 o superior.
- **npm** 9 o superior.
- **MySQL** 8 o compatible, si no usarás Docker.
- **Docker** y **Docker Compose**, si prefieres levantar toda la solución en contenedores.

---

## 🚀 Instalación

### 1. Clonar el repositorio

```bash
git clone <url-del-repositorio>
cd project
```

### 2. Instalar dependencias del frontend

```bash
cd finditunal-frontend
npm install
```

### 3. Instalar dependencias del backend

```bash
cd ../finditunal-backend
npm install
```

---

## ⚙️ Configuración

### Frontend

Crea un archivo `.env` en `finditunal-frontend/` con variables como estas:

```env
VITE_API_URL=http://localhost:3000
VITE_WS_URL=http://localhost:3000
VITE_GOOGLE_CLIENT_ID=tu_google_client_id.apps.googleusercontent.com
VITE_SUPABASE_URL=https://tu-proyecto.supabase.co
VITE_SUPABASE_ANON_KEY=tu_anon_key
```

### Backend

Configura el archivo `.env` en `finditunal-backend/` con los datos de conexión y autenticación requeridos por el servidor, incluyendo al menos:

```env
PORT=3000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=tu_password
DB_NAME=finditunal
JWT_SECRET=tu_secreto
GOOGLE_CLIENT_ID=tu_google_client_id.apps.googleusercontent.com
```

> Los nombres exactos pueden variar según el entorno local o el archivo de configuración ya definido en el backend.

---

## ▶️ Ejecución

### Frontend

```bash
cd finditunal-frontend
npm run dev
```

### Backend

```bash
cd finditunal-backend
npm run dev
```

### Compilación de producción

Frontend:

```bash
cd finditunal-frontend
npm run build
```

Backend:

```bash
cd finditunal-backend
npm run build
```

---

## 🐳 Docker

El proyecto incluye archivos de Docker Compose para facilitar el despliegue local y el arranque coordinado de servicios.

| Archivo | Propósito |
|---|---|
| `finditunal-backend/docker-compose.yml` | Orquestación del backend y su base de datos. |
| `finditunal-backend/docker-compose.dev.yml` | Entorno de desarrollo. |
| `finditunal-frontend/Dockerfile` | Construcción de la imagen del frontend. |
| `finditunal-backend/Dockerfile` | Construcción de la imagen del backend. |

Si deseas levantar todo por contenedores, revisa primero la configuración de variables de entorno y los puertos expuestos en cada servicio.

---

## 📘 Documentación adicional

- [Documentación del backend](finditunal-documentation/README.md)
- [README del frontend](finditunal-frontend/README.md)
- [Notas de tecnologías](tecnologias.txt)

---

## 🤝 Contribución

Si vas a extender el sistema, procura mantener estas reglas:

- Usa **TypeScript** en nuevas piezas del frontend y backend.
- Respeta la separación entre controladores, servicios, modelos y rutas.
- Mantén componentes reutilizables en la capa adecuada del frontend.
- Agrega validación a cualquier dato que provenga del usuario.
- Documenta cambios grandes en la sección correspondiente del proyecto.

---

## 📄 Licencia

Este proyecto está destinado a uso académico y privado para la Universidad Nacional de Colombia.

---

<p align="center">
  Desarrollado con ❤️ para la comunidad de la <strong>Universidad Nacional de Colombia</strong>
</p>

<p align="center">
  <a href="#-tabla-de-contenidos">⬆️ Volver arriba</a>
</p>
