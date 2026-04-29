# 💻 Proyecto Sistema de Buscador Unificado de Recursos para Bibliotecas Físicas y Virtuales (NexusLib)

**NexusLib** es un buscador unificado diseñado para la biblioteca de la Universidad Privada de Tacna (UPT)[cite: 1]. El sistema permite centralizar la consulta de material bibliográfico tanto en el inventario físico local como en fuentes externas digitales[cite: 1].

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

Para ejecutar este proyecto, es necesario contar con el siguiente entorno:

*   **PHP:** Versión ^7.2.5 o ^8.0[cite: 2].
*   **Composer:** Gestor de dependencias para PHP[cite: 1, 2].
*   **Servidor Web:** Apache o Nginx.
*   **Base de Datos:** MySQL para la gestión del inventario físico local.

## 🚀 Procedimiento de Despliegue

Sigue estos pasos para instalar el proyecto en tu entorno local:

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/tu-repositorio.git](https://github.com/tu-usuario/tu-repositorio.git)
    ```
2.  **Acceder al directorio del proyecto:**
    Navega hasta la carpeta raíz del sistema[cite: 1]:
    ```bash
    cd ProyectoNexusLib/nexuslib
    ```
3.  **Instalar dependencias de Composer:**
    Descarga las librerías necesarias (como `phpdotenv`) definidas en el archivo de configuración[cite: 1, 2]:
    ```bash
    composer install
    ```

## ⚙️ Parámetros de Configuración (.env)

El sistema utiliza la librería `vlucas/phpdotenv` para gestionar variables de entorno de forma segura[cite: 1, 2]. Debes crear un archivo `.env` en la ruta `ProyectoNexusLib/nexuslib/` con los siguientes parámetros:
```env
# Configuración de Base de Datos
DB_HOST=localhost
DB_NAME=nombre_de_tu_bd
DB_USER=tu_usuario
DB_PASS=tu_password

# Claves de API
GOOGLE_BOOKS_API_KEY=tu_clave_aqui

# Entorno
APP_ENV=development
APP_DEBUG=true
