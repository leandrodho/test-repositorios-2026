# **UNIVERSIDAD PRIVADA DE TACNA**
**FACULTAD DE INGENIERÍA** **Escuela Profesional de Ingeniería de Sistemas**

![Logo UPT](Aspose.Words.6a57f384-4a85-43ff-84b9-2798e0a9b150.001.png)

**Sistema NexusLib** **Curso:** Patrones de Software  
**Docente:** Ing. Patrick Cuadros Quiroga  

**Integrantes:** * **Hurtado Ortiz, Leandro (2015052384)** * **Flores Navarro, Eduardo Gino (2023076793)** * **Cortez Mamani, Julio Samuel (2023077283)** **Tacna – Perú** **2026**

---

## **CONTROL DE VERSIONES**

| Versión | Hecha por | Revisada por | Aprobada por | Fecha | Motivo |
| :---: | :--- | :--- | :--- | :--- | :--- |
| 1.0 | LDHO | LDHO | LDHO | 02/04/2025 | Versión Original |

---

# **ÍNDICE GENERAL**

1. [Descripción del proyecto](#1-descripción-del-proyecto)  
   1.1. [Nombre del proyecto](#11-nombre-del-proyecto)  
   1.2. [Duración del proyecto](#12-duración-del-proyecto)  
   1.3. [Descripción](#13-descripción)  
   1.4. [Objetivos](#14-objetivos)  
      1.4.1. [Objetivo general](#141-objetivo-general)  
      1.4.2. [Objetivos específicos](#142-objetivos-específicos)  
2. [Riesgos](#2-riesgos)  
3. [Análisis de la situación actual](#3-análisis-de-la-situación-actual)  
   3.1. [Planteamiento del problema](#31-planteamiento-del-problema)  
   3.2. [Consideraciones de hardware y software](#32-consideraciones-de-hardware-y-software)  
4. [Estudio de Factibilidad](#4-estudio-de-factibilidad)  
   4.1. [Factibilidad Técnica](#41-factibilidad-técnica)  
   4.2. [Factibilidad Económica](#42-factibilidad-económica)  
      4.2.1. [Costos de software](#421-costos-de-software)  
      4.2.2. [Costos de recursos humanos](#422-costos-de-recursos-humanos)  
      4.2.3. [Costos generales de Administración](#423-costos-generales-de-administración)  
      4.2.4. [Tabla general de costos](#424-tabla-general-de-costos)  
   4.3. [Factibilidad Operativa](#43-factibilidad-operativa)  
   4.4. [Factibilidad Legal](#44-factibilidad-legal)  
   4.5. [Factibilidad Social](#45-factibilidad-social)  
   4.6. [Factibilidad Ambiental](#46-factibilidad-ambiental)  
5. [Análisis Financiero](#5-análisis-financiero)  
   5.1. [Justificación de la Inversión](#51-justificación-de-la-inversión)  
      5.1.1. [Beneficios del proyecto](#511-beneficios-del-proyecto)  
         5.1.1.1. [Beneficios tangibles](#5111-beneficios-tangibles)  
         5.1.1.2. [Beneficios intangibles](#5112-beneficios-intangibles)  
      5.1.2. [Criterios de Inversión](#512-criterios-de-inversión)  
         5.1.2.1. [Costo inicial](#5121-costo-inicial)  
         5.1.2.2. [Costo anual de operación](#5122-costo-anual-de-operación)  
         5.1.2.3. [Tiempo de elaboración](#5123-tiempo-de-elaboración)  
         5.1.2.4. [Tasa de interés](#5124-tasa-de-interés)  
         5.1.2.5. [Relación Beneficio/Costo](#5125-relación-beneficiocosto)  
         5.1.2.6. [Valor actual neto](#5126-valor-actual-neto)  
         5.1.2.7. [Tasa Interna de Retorno (TIR)](#5127-tasa-interna-de-retorno-tir)  
6. [Conclusiones](#6-conclusiones)

---

# **Informe de Factibilidad**

# 1. Descripción del proyecto
## 1.1. Nombre del proyecto
Sistema de Buscador Unificado de Recursos para Bibliotecas Físicas y Virtuales

## 1.2. Duración del proyecto
**Inicio:** 25 de Marzo  
**Fin:** 24 de junio

## 1.3. Descripción
El proyecto consiste en el diseño y desarrollo de una plataforma web integral orientada a centralizar el acceso a la información bibliográfica. El sistema permitirá a los usuarios realizar búsquedas simultáneas en dos entornos: el catálogo de inventario físico y el repositorio de recursos digitales. La solución se desarrollará bajo el patrón **ASP.NET MVC**, utilizando **SQL Server** para la gestión de datos y **Terraform** para la provisión de infraestructura en **Azure**.

## 1.4. Objetivos
### 1.4.1. Objetivo general
Desarrollar una plataforma web unificada que optimice la localización y el acceso a recursos bibliográficos físicos y digitales, mejorando la gestión de información para la comunidad académica de la UPT.

### 1.4.2. Objetivos específicos
* Diseñar un sistema de búsqueda multicanal por título, autor y categoría.
* Implementar un módulo de gestión de inventario físico.
* Integrar un repositorio digital seguro para archivos electrónicos.
* Configurar la infraestructura como código (IaC) mediante Terraform en Azure.
* Establecer un sistema de autenticación diferenciado.
* Garantizar la escalabilidad del sistema.

# 2. Riesgos
* **Desincronización de Inventario Físico:** Que la base de datos no refleje en tiempo real la toma de libros.
* **Complejidad en la Integración de Recursos:** Afectación en tiempos de respuesta por archivos digitales pesados.
* **Limitación de Créditos en la Nube:** Agotamiento de la cuota gratuita de Azure antes de finalizar pruebas.
* **Curva de Aprendizaje en IaC:** Errores en scripts de Terraform que afecten la provisión de recursos.

# 3. Análisis de la situación actual
## 3.1. Planteamiento del problema
La falta de una plataforma centralizada que combine el inventario físico con el repositorio virtual limita la eficiencia en la investigación. Los usuarios deben consultar sistemas fragmentados, lo que genera desmotivación y pérdida de tiempo.

## 3.2. Consideraciones de hardware y software
**Hardware:**
* **CPU:** 2 vCPU mínimo.
* **RAM:** 4 GB.
* **Almacenamiento:** SSD para base de datos y logs.

**Software:**
* **IDE:** Visual Studio 2022 (ASP.NET).
* **BD:** SQL Server & Azure SQL Database.
* **IaC:** Terraform v1.x.
* **Versiones:** GitHub.

# 4. Estudio de Factibilidad
## 4.1. Factibilidad Técnica
El proyecto es técnicamente viable ya que el equipo domina el stack tecnológico propuesto (C#, .NET, SQL Server). La automatización con Terraform en Azure asegura un despliegue profesional.

## 4.2. Factibilidad Económica
### 4.2.1. Costos de software
| N° | Descripción | Precio Unitario (S/.) | Tiempo | Costo (S/.) |
| :--- | :--- | :---: | :---: | :---: |
| 1 | Visual Studio Professional 2022 | 180 | 3 meses | 540 |
| 2 | Azure SQL Database | 120 | 3 meses | 360 |
| 3 | Azure App Service Plan | 90 | 3 meses | 270 |
| 4 | Certificado SSL / Dominio | 150 | 1 año | 150 |
| | **Total** | | | **1,320** |

### 4.2.2. Costos de recursos humanos
| N° | Descripción | Precio Unitario (S/.) | Horas | Costo (S/.) |
| :--- | :--- | :---: | :---: | :---: |
| 1 | Desarrollo Backend | 35 | 100 | 3,500 |
| 2 | Desarrollo Frontend | 35 | 80 | 2,800 |
| 3 | Pruebas y QA | 30 | 40 | 1,200 |
| | **Total** | | | **7,500** |

### 4.2.3. Costos generales de Administración
| N° | Descripción | Precio Unitario (S/.) | Meses | Costo (S/.) |
| :--- | :--- | :---: | :---: | :---: |
| 1 | Internet alta velocidad | 120 | 3 | 360 |
| 2 | Energía Eléctrica | 70 | 3 | 210 |
| 3 | Gastos Oficina | 50 | 3 | 150 |
| | **Total** | | | **720** |

### 4.2.4. Tabla general de costos
| Categoría | Costo (S/.) |
| :--- | :---: |
| Costos de Software | 1,320 |
| Costos de Recursos Humanos | 7,500 |
| Costos Generales de Administración | 720 |
| **Costo Total del Proyecto** | **9,540** |

## 4.3. Factibilidad Operativa
El sistema es intuitivo y se adapta perfectamente al entorno académico sin requerir capacitación compleja para los usuarios finales.

## 4.4. Factibilidad Legal
Se cumple con la **Ley N.° 29733 (Protección de Datos Personales en el Perú)** y se utiliza software bajo licencias corporativas o de libre uso.

## 4.5. Factibilidad Social
Fomenta la democratización de la información y mejora los hábitos de estudio mediante una herramienta de búsqueda de vanguardia.

## 4.6. Factibilidad Ambiental
Reduce la huella ecológica al minimizar el uso de papel y optimizar el consumo eléctrico mediante servicios en la nube.

# 5. Análisis Financiero
## 5.1. Justificación de la Inversión
La inversión de **S/ 9,540** se justifica por la modernización de los procesos de investigación y la eficiencia operativa lograda mediante la infraestructura como código.

### 5.1.1. Beneficios del proyecto
#### 5.1.1.1. Beneficios tangibles
* Ahorro en materiales de oficina.
* Reducción de costos en servidores locales.
* Optimización del tiempo administrativo.

#### 5.1.1.2. Beneficios intangibles
* Incremento en la motivación estudiantil.
* Fortalecimiento de la imagen institucional de la facultad.

### 5.1.2. Criterios de Inversión
* **5.1.2.1. Costo inicial:** S/ 9,540.
* **5.1.2.2. Costo anual de operación:** Evaluado a 5 años.
* **5.1.2.3. Tiempo de elaboración:** 3 meses.
* **5.1.2.4. Tasa de interés:** 3% anual.
* **5.1.2.5. Relación Beneficio/Costo:** **1.44**.
* **5.1.2.6. Valor actual neto (VAN):** **S/ 4,199.12**.
* **5.1.2.7. Tasa Interna de Retorno (TIR):** **17%**.

# 6. Conclusiones
* El proyecto NexusLib es viable en todas las dimensiones evaluadas.
* Los indicadores **VAN** y **TIR** garantizan que es una inversión financieramente sólida.
* El uso de **Terraform** permite un control preciso de costos, alineado con las exigencias académicas actuales.
