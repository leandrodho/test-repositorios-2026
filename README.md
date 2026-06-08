# NexusLib - Buscador Unificado de Recursos Bibliográficos

NexusLib es una plataforma web híbrida diseñada para resolver la fragmentación de la información académica en la Universidad Privada de Tacna. El sistema unifica de manera ágil y concurrente las consultas del catálogo físico local con repositorios digitales externos (Alpha Cloud y E-Libro), ofreciendo un espacio personal para estudiantes y un panel administrativo integrado.

---

## 🚀 Características Principales

El sistema implementa **9 Requerimientos Funcionales** estratégicos estructurados bajo patrones de diseño avanzados (*Facade, Adapter y Strategy*):

* **Búsqueda Unificada (RF-01):** Consulta simultánea distribuida entre el inventario local MySQL y las APIs externas.


* **Visualización Detallada (RF-02):** Ficha técnica unificada con metadatos estructurados y portadas.


* **Disponibilidad en Sala (RF-03):** Localización física en tiempo real (Piso y Estante) con control de existencias.


* **Filtrado Avanzado (RF-04):** Segmentación por Origen, Disponibilidad, Temas y Criterios.


* **Acceso Digital (RF-05):** Enlaces directos a visores externos o descargas autorizadas.


* **Gestión Administrativa (RF-06):** Panel protegido para el control de inventario local, usuarios y auditoría en modo lectura.


* **Seguridad y Autenticación (RF-07):** Registro y Login seguro mediante hashing de credenciales y tokens de sesión.


* **Módulo de Favoritos (RF-08):** Guardado persistente de referencias dentro del espacio personal del estudiante.


* **Módulo de Reservas (RF-09):** Separación preventiva de textos físicos en estantería con generación de códigos únicos de recojo.



---

## 📋 Requisitos del Sistema (Prerrequisitos)

Antes de levantar el proyecto de forma local, asegúrate de contar con el siguiente entorno configurado:

* **Servidor Web / Backend:** PHP >= 8.2.12 (con soporte para Programación Orientada a Objetos y tipado fuerte).


* **Extensiones PHP Requeridas:** `pdo_mysql`, `curl`, `json`, `mbstring`.
* **Gestor de Dependencias:** Composer (para la orquestación de librerías).
* **Base de Datos:** MySQL Server >= 8.0.


* **Frontend:** Navegador web moderno compatible con ECMAScript 6 (ES6) y diseño responsivo.



---

## ⚙️ Parámetros de Configuración (`.env`)

El proyecto utiliza variables de entorno para manejar las credenciales de forma segura. Duplica el archivo de ejemplo y configura tus accesos locales:

```bash
cp .env.example .env

```

Abre el archivo `.env` creado y edita las siguientes directrices según tu entorno de desarrollo:

```ini
# Configuración del Entorno de Aplicación
APP_ENV=local
APP_DEBUG=true
APP_URL=http://localhost:8000

# Conexión a Base de Datos Local (MySQL)
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nexuslib_db
DB_USERNAME=tu_usuario_mysql
DB_PASSWORD=tu_contrasena_mysql

# Llave Secreta para Cifrado de Tokens de Sesión
JWT_SECRET=tu_clave_secreta_super_segura_de_32_caracteres

# Credenciales de APIs de Proveedores Digitales Externos
ALPHA_CLOUD_API_KEY=tu_token_de_alpha_cloud
ALPHA_CLOUD_BASE_URL=https://api.alphacloud.exchange/v1

ELIBRO_API_KEY=tu_token_de_elibro
ELIBRO_BASE_URL=https://api.elibro.net/v1

```

---

## 🛠️ Procedimiento de Instalación Paso a Paso

Sigue estas instrucciones cronológicas para compilar y ejecutar el proyecto en tu entorno local:

### 1. Clonar el Repositorio

Obtén una copia local del código fuente oficial del proyecto:

```bash
git clone https://github.com/UPT-FAING-EPIS/proyecto-si889-2026-i-ul-buscador-unificado-biblioteca.git
cd proyecto-si889-2026-i-ul-buscador-unificado-biblioteca

```

### 2. Instalar Dependencias del Backend

Ejecuta el gestor para descargar los componentes de enrutamiento o utilitarios del sistema:

```bash
composer install

```

### 3. Configurar la Base de Datos Local

1. Inicia el servicio de tu servidor MySQL local.


2. Crea una nueva base de datos vacía llamada `nexuslib_db`.
3. Importa los esquemas de tablas transaccionales, índices y datos de prueba provistos ejecutando el siguiente comando en tu terminal (o utilizando herramientas visuales como MySQL Workbench / DBeaver):

```bash
mysql -u tu_usuario_mysql -p nexuslib_db < database/schema.sql

```

> 📌 **Nota de Integridad:** El archivo `schema.sql` inicializará de manera relacional las tablas de `users`, `books`, `physical_books`, `bookmarked_books` y `reserved_books`.
> 
> 

### 4. Inicializar el Servidor de Desarrollo Local

Puedes utilizar el servidor de desarrollo nativo integrado en PHP para levantar la plataforma de manera instantánea:

```bash
php -S localhost:8000 -t public/

```

Una vez ejecutado el comando, abre tu navegador web de preferencia e ingresa a la siguiente dirección: **`http://localhost:8000`**

---

## 📂 Estructura General del Proyecto

A continuación se detalla la distribución modular del repositorio bajo el patrón arquitectónico empleado:

```text
├── config/             # Archivos de configuración del sistema y variables de entorno.
├── database/           # Scripts SQL, esquemas relacionales e inventario inicial UPT.
├── public/             # Punto de entrada de la aplicación (index.php, CSS, JS, Portadas).
└── src/                # Capa Lógica y de Control del Software.
    ├── Boundaries/     # Interfaces y componentes gráficos (Dashboard, Formularios).
    ├── Controls/       # Controladores, Adaptadores (Alpha/E-Libro) y Motores de Búsqueda.
    └── Entities/       # Modelos de dominio y persistencia de datos físicos/usuarios.

```

---

## 🛡️ Pruebas de Calidad y Seguridad Locales

Para asegurar que las entradas de texto se encuentren blindadas contra inyecciones SQL o ataques XSS (conforme al requerimiento **RNF-01**), puedes validar el comportamiento de la lógica ejecutando el script de pruebas unitarias:

```bash
php vendor/bin/phpunit --testsuite=Unit

```
