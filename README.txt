# Proyecto Docker: Aplicación Web con Frontend, Backend y Base de Datos

Este proyecto es una aplicación web desplegada con Docker que incluye:

- Frontend: Interfaz HTML/CSS/JS.
- Backend: API desarrollada en Flask.
- Base de datos: PostgreSQL con script de inicialización.

## Estructura del Proyecto

proyecto/
├── docker-compose.yml
├── init.sql
├── backend/
│   ├── app.py
│   ├── db.py
│   ├── Dockerfile
│   └── requirements.txt
└── frontend/
    ├── index.html
    ├── script.js
    ├── style.css
    └── Dockerfile

## Cómo desplegar el proyecto

1. Pre-requisitos:
   - Tener Docker y Docker Compose instalados.

2. Clonar el repositorio:
   git clone https://github.com/xGE0/ProyectoDocker

3. Ejecutar los servicios:
   docker-compose up --build

4. Acceso a la aplicación:
   - Frontend disponible en: http://localhost:8080 (o el puerto configurado).
   - Backend (API Flask) en: http://localhost:5000 (si se expone).

## Seguridad y redes

- Los servicios están conectados mediante una red interna de Docker.
- PostgreSQL no expone puertos al exterior.
- Se recomienda no usar modo debug en producción para Flask.
- Agrega variables de entorno para contraseñas en producción.

## Notas

- El script init.sql inicializa la base de datos al primer arranque.
- Este proyecto es ideal como base para proyectos web con arquitectura de microservicios.
