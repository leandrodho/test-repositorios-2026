# 💻 Proyecto Sistema de Buscador Unificado de Recursos para Bibliotecas (NexusLib)

**NexusLib** es un buscador unificado diseñado para la biblioteca de la Universidad Privada de Tacna (UPT)[cite: 1]. Centraliza la consulta de material bibliográfico en el inventario físico local y fuentes digitales externas[cite: 1].

---

## 👨‍💻 Integrantes:
- Hurtado Ortiz, Leandro (2015052384)
- Flores Navarro, Eduardo Gino (2023076793)
- Cortez Mamani, Julio Samuel (2023077283)

---

## 📋 Requisitos Previos

Para desplegar este proyecto en una PC nueva, asegúrate de tener:

*   **XAMPP:** Instalado con los módulos de Apache y MySQL activos.
*   **PHP:** Versión ^7.2.5 o ^8.0 (incluida en versiones recientes de XAMPP)[cite: 2].
*   **Composer:** Necesario para descargar las librerías de dependencias[cite: 1].
*   **HeidiSQL o phpMyAdmin:** Para la gestión y ejecución de scripts de base de datos.

## 🚀 Procedimiento de Despliegue Local (XAMPP)

Sigue estos pasos para poner en marcha el proyecto:

1.  **Ubicación del Proyecto:**
    Descarga o clona el repositorio dentro de la carpeta `C:/xampp/htdocs/`.
2.  **Preparación de la Base de Datos:**
    *   Abre **HeidiSQL** o phpMyAdmin.
    *   Crea una base de datos nueva (ej. `db_nexuslib`).
    *   Ejecuta el script SQL incluido en el proyecto para generar las tablas del inventario físico.
3.  **Instalación de Dependencias:**
    Abre una terminal en la ruta `htdocs/ProyectoNexusLib/nexuslib/` y ejecuta[cite: 1]:
    ```bash
    composer install
    ```
    *Esto creará la carpeta `vendor/` con las librerías necesarias para el funcionamiento del sistema[cite: 1, 2].*
4.  **Acceso al Sistema:**
    Abre tu navegador e ingresa a: `http://localhost/ProyectoNexusLib/nexuslib/`

## ⚙️ Parámetros de Configuración (.env)

El sistema requiere un archivo de configuración para conectar con la base de datos y las APIs externas[cite: 1]. Crea un archivo llamado `.env` en la carpeta `nexuslib/` con el siguiente contenido:
```env
# Configuración de Base de Datos Local
DB_HOST=localhost
DB_NAME=db_nexuslib
DB_USER=root
DB_PASS=

# Integración con Google Books API
GOOGLE_BOOKS_API_KEY=tu_clave_aqui

# Entorno de Desarrollo
APP_ENV=development
APP_DEBUG=true
