# Healthcare-SQL-Reporting

![Status: Maintained](https://img.shields.io/badge/Status-Maintained-brightgreen?style=for-the-badge)
![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![Spark SQL](https://img.shields.io/badge/Spark_SQL-E25A1C?style=for-the-badge&logo=apache-spark&logoColor=white)

Análisis avanzado de datos sanitarios utilizando el motor de procesamiento distribuido de Databricks para optimizar la eficiencia hospitalaria y la gestión pública.

## 🏥 Sobre el Proyecto
Este repositorio contiene la resolución de un caso analítico y modelado de datos basado en información de **Salud Pública de la Ciudad de Rosario, Santa Fe** (enunciados y requerimientos provistos por la consultora **Lovelytics**). El objetivo es transformar registros en bruto de internaciones, pacientes y hospitales en métricas clave para la toma de decisiones directivas.

A través de **Spark SQL**, se resuelven desafíos analíticos reales del sector de la salud, implementando limpieza de datos, modelado relacional y lógica de negocio compleja.

## 📊 Arquitectura de Datos y Entidades



![DER-Salud](https://github.com/user-attachments/assets/e4236ecb-1e9d-410b-aed1-0075746e49cc)


El modelo centraliza el análisis en la capacidad operativa y la demografía hospitalaria, abarcando:

* **Pacientes:** Perfiles demográficos (edad, sexo, nacionalidad).
* **Hospitales:** Infraestructura, capacidad de camas y ubicación por distritos.
* **Internaciones:** Registro de ingresos, días de estadía, motivos de egreso y diagnósticos.
* **Diagnósticos y Sectores:** Clasificación médica y áreas específicas de atención.

## 🛠️ Fases del Desarrollo Analítico (SQL)

El script principal despliega distintas técnicas de ingeniería y análisis de datos:

### 🔹 Fase 1: Data Cleaning & Transformación
- Tratamiento defensivo de valores nulos utilizando funciones `COALESCE` para garantizar la integridad de los reportes.
- Normalización de cadenas de texto y direcciones mediante funciones escalares (`TRIM`, `INITCAP`).

### 🔹 Fase 2: Modelado Relacional & Agregaciones
- **Gestión de Capacidad:** Cálculo de métricas de ocupación y disponibilidad de camas por distrito mediante agrupaciones complejas.
- **Análisis Temporal:** Identificación de estacionalidad mensual y años pico a través de funciones de extracción de fechas (`EXTRACT`, `YEAR`, `MONTH`).

### 🔹 Fase 3: Lógica de Negocio Avanzada
- **Segmentación Dinámica:** Clasificación etaria de pacientes y niveles de urgencia médica (Urgencias vs. Programadas) mediante estructuras `CASE WHEN`.
- **Data Marting:** Generación de vistas pre-calculadas (`CREATE OR REPLACE VIEW`) para agilizar el consumo de métricas de mortalidad e internación por herramientas de BI.

## 🚀 Tecnologías Utilizadas
* **Motor:** SQL / Spark SQL.
* **Plataforma:** Databricks.
* **Fuente de Datos:** [Portal de Datos Abiertos de la Municipalidad de Rosario](https://datos.rosario.gob.ar/).

---
👨‍💻 **Juan Manuel Landa** — *Computer Engineer | Data Analyst & BI Consultant*  
🔗 [LinkedIn](https://ar.linkedin.com/in/juan-manuel-landa/en) • 🌐 [Portfolio](https://juan-manuel-landa.netlify.app/) • ✉️ [Contacto](mailto:jmlanda93@gmail.com)
