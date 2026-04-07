🚀 Cloud Data Analytics Capstone — TheLook Fintech
📌 Overview

Proyecto final del Google Cloud Data Analytics Professional Certificate (Google Cloud × Coursera).

En este proyecto asumí el rol de Cloud Data Analyst, trabajando con datos de TheLook Fintech, una empresa de préstamos para e-commerce.

El objetivo fue resolver problemas reales del área de Tesorería aplicando el ciclo completo de datos en la nube:

Collect → Process → Store → Analyze → Activate

🎯 Business Problem

El equipo de Tesorería necesitaba visibilidad sobre 3 áreas clave para la salud financiera:

💰 Flujo de caja
Asegurar que los ingresos superen los préstamos otorgados mensualmente
📊 Propósito de los préstamos
Identificar los motivos de solicitud (relacionados con el riesgo de repago)
🌎 Distribución geográfica
Detectar concentraciones de riesgo por región
🧰 Tech Stack
Herramienta	Uso
BigQuery	Exploración, transformación y almacenamiento
SQL	JOINs, agregaciones, CTAS, deduplicación
Google Cloud Storage	Ingesta de datos externos
Looker Enterprise	Dashboard interactivo
LookML	Modelado de métricas y dimensiones
Google Sheets	Exportación de datos
🏗️ Data Pipeline Architecture

El proyecto cubre todo el flujo de datos en la nube:

Ingesta → Dataset fintech + CSV externo (regiones)
Procesamiento → Transformaciones SQL en BigQuery
Almacenamiento → Tablas optimizadas (CTAS)
Análisis → Modelado en Looker
Activación → Dashboard interactivo
⚙️ Data Processing (BigQuery)
🔍 Exploración
Identificación de métricas clave:
loan_amount
issued_date
📥 Ingesta de datos externos
Importación de CSV con regiones de EE.UU.
Creación de tabla enriquecida para análisis geográfico
🔗 Transformación y joins
Consolidación de datos en una única tabla:
loan_id
loan_amount
region_name
🏗️ Materialización (CTAS)
Uso de CREATE TABLE AS SELECT
Generación de tablas listas para análisis y exportación
🧩 Datos anidados
Extracción del campo purpose desde estructuras anidadas
🧹 Limpieza de datos
Eliminación de duplicados en purpose
Mejora de calidad e integridad de datos
📈 Reporte de flujo de caja
Agregación de préstamos por día y año
Base para monitoreo financiero
📊 Dashboard — Loan Insights

Dashboard interactivo desarrollado en Looker para responder preguntas de negocio.

🔴 KPI principal — Total de préstamos vigentes
Indicador con formato condicional
🔴 Alerta visual si supera $3B
🥧 Distribución por estado
Préstamos por categoría:
Al día
Atrasado
Default
Pagado, etc.
📍 Top 10 estados con mayor riesgo
Identificación de concentración geográfica
👤 Top 10 clientes por ingreso
Segmentación de clientes de alto valor
⚡ Features del Dashboard
🔄 Cross-filtering (interactividad total)
⏱️ Actualización automática
KPIs críticos: cada hora
Resto: cada 24h
🧠 Skills Demonstrated
Cloud Data Analytics end-to-end
SQL avanzado (JOINs, CTAS, nested data)
Data cleaning & deduplication
Integración de múltiples fuentes
Data storytelling con dashboards
Traducción de negocio → solución técnica
Diseño de KPIs y alertas visuales
📈 Results & Impact

El proyecto entregó:

✅ Pipeline completo de datos en la nube
✅ Reportes claros sobre:
Flujo de caja
Propósito de préstamos
Distribución geográfica
✅ Dashboard interactivo para toma de decisiones
🎓 Certification

Este proyecto forma parte del:

Google Cloud Data Analytics Professional Certificate
Google Cloud × Coursera

👉 (https://www.coursera.org/account/accomplishments/professional-cert/K73Z32MVDVJZ)
