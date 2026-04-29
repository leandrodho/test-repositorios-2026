# 💻 Proyecto Sistema de Buscador Unificado de Recursos para Bibliotecas Físicas y Virtuales (NexusLib)

**NexusLib** es un buscador unificado diseñado para centralizar la consulta de material bibliográfico de la Universidad Privada de Tacna (UPT), integrando el inventario físico local y la Google Books API.

---

## 👨‍💻 Integrantes:

- Hurtado Ortiz, Leandro (2015052384)
- Flores Navarro, Eduardo Gino (2023076793)
- Cortez Mamani, Julio Samuel (2023077283)

---

## 🎯 Curso: Patrones de Software
## 🏫 Universidad Privada de Tacna
## 🗓️ Ciclo 2026-I

---

## 📋 Requisitos Previos

Para ejecutar el proyecto localmente, solo necesitas:
*   **XAMPP:** Con los módulos de **Apache** y **MySQL** iniciados.
*   **Gestor de BD:** HeidiSQL o phpMyAdmin para cargar el esquema.

## 🚀 Procedimiento de Despliegue Local

Dado que el proyecto ya incluye todas las librerías (`vendor/`) y la configuración base, sigue estos pasos:

1.  **Ubicación:** 
    Copia la carpeta `nexuslib` dentro de `C:/xampp/htdocs/`.
2.  **Base de Datos:**
    *   Crea una base de datos llamada `db_library` (o la que indique tu archivo `.env`).
    *   Ejecuta el script SQL ubicado en `nexuslib/database/schema.sql` para crear las tablas necesarias[cite: 1].
3.  **Acceso al Sistema:**
    Abre tu navegador y entra a la siguiente dirección:
    `http://localhost/nexuslib/public/`

## ⚙️ Parámetros de Configuración (.env)

El proyecto ya cuenta con un archivo **`.env`** configurado en la carpeta raíz[cite: 1]. En caso de que tus credenciales de MySQL sean distintas a las predeterminadas (root sin contraseña), puedes editarlas directamente allí:
```env
DB_HOST=localhost
DB_NAME=db_library
DB_USER=root
DB_PASS=

GOOGLE_BOOKS_API_KEY=tu_api_key_aqui
