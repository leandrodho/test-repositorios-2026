---
marp: true
theme: default
paginate: true
header: 'Proyecto NexusLib - Patrones de Software'
footer: 'Universidad Privada de Tacna - 2026'
style: |
  section {
    background-color: #f5f5f5;
  }
  h1 {
    color: #1a5276;
  }
---

# 📚 NexusLib
### Buscador Unificado de Recursos para Bibliotecas
**Buscador unificado UPT**[cite: 1]

**Integrantes:**
- Hurtado Ortiz, Leandro
- Flores Navarro, Eduardo Gino
- Cortez Mamani, Julio Samuel

---

# 🎯 Propósito del Proyecto
NexusLib resuelve la dispersión de información bibliográfica en la **UPT**, centralizando:

*   **Inventario Físico Local:** Consulta en tiempo real de libros en estantería (MySQL)[cite: 1].
*   **Recursos Digitales:** Integración directa con **Google Books API**[cite: 1].
*   **Acceso Rápido:** Una sola interfaz moderna para el estudiante.

---

# ✨ Características Clave
*   **Búsqueda Unificada:** Consulta simultánea en BD local y nube.
*   **Gestión de Disponibilidad:** Saber si un libro está prestado o disponible antes de ir a la biblioteca.
*   **Filtros Avanzados:** Por autor, título, categorías e ISBN.
*   **Arquitectura Escalable:** Basado en patrones de software.

---

# 🛠️ Stack Tecnológico
Para garantizar rapidez y estabilidad, utilizamos:

- **Backend:** PHP (^7.2.5 / ^8.0).
- **Gestor de Dependencias:** Composer[cite: 1].
- **Base de Datos:** MySQL para el inventario institucional.
- **Seguridad:** Variables de entorno (.env) con `phpdotenv`[cite: 1].
- **Escaneo de Vulnerabilidades:** Snyk Security.

---

# 📋 Requerimientos Funcionales (v1.0)
| Código | Requerimiento | Descripción |
| :--- | :--- | :--- |
| **RF-01** | Búsqueda unificada | Consulta en MySQL y Google Books[cite: 1]. |
| **RF-02** | Visualización | Datos completos y portadas. |
| **RF-03** | Disponibilidad | Stock físico en tiempo real. |
| **RF-04** | Filtrado | Refinamiento por criterios. |

---

# 🗺️ Roadmap (Hoja de Ruta)
El proyecto está diseñado para evolucionar:

1.  **v1.0 (MVP):** Núcleo del buscador e integración con Google Books[cite: 1].
2.  **v2.0 (Gestión):** **Módulo administrativo (CRUD)** para el inventario local.
3.  **v3.0 (Social):** Recomendaciones personalizadas y perfiles de usuario.

---

# 🚀 Despliegue y Demo
El entorno es **Plug & Play** para facilitar la revisión docente:

1.  Mover carpeta a `htdocs/`.
2.  Importar `schema.sql`.
3.  Configurar `.env` con credenciales de BD.
4.  Acceso vía: `http://localhost/nexuslib/public/`

---

# ¡Gracias por su atención!
### ¿Dudas o preguntas?
