🚀 Cloud Data Analytics Project — TheLook Fintech
🧩 Project Overview

En este proyecto trabajé como Cloud Data Analyst, diseñando e implementando un pipeline de datos end-to-end en Google Cloud para una fintech en crecimiento (TheLook Fintech).

El objetivo fue transformar datos operativos en información estratégica para el equipo de Tesorería, permitiendo monitorear la salud financiera de la empresa y reducir riesgos asociados a la cartera de préstamos.

🎯 Business Challenge

El área de Tesorería enfrentaba tres desafíos clave:

Falta de visibilidad sobre el flujo de caja
Desconocimiento de los factores de riesgo en los préstamos
Riesgo de concentración geográfica

A partir de esto, se definieron tres preguntas críticas:

¿El volumen de préstamos otorgados es sostenible respecto a los ingresos?
¿Qué motivos de préstamo están asociados a mayor riesgo?
¿Cómo se distribuyen los préstamos geográficamente?
🏗️ Solution Design

Se desarrolló una solución basada en el ciclo completo de datos en la nube:

Ingesta → Procesamiento → Almacenamiento → Análisis → Activación

El enfoque no fue solo técnico, sino orientado a resolver necesidades concretas del negocio.

⚙️ Data Engineering & Processing (BigQuery)
🔍 Exploración y entendimiento del dataset
Análisis estructural de múltiples tablas
Identificación de métricas clave:
loan_amount (flujo de salida)
issued_date (temporalidad del flujo)

👉 Decisión clave: definir correctamente estas variables permitió construir métricas confiables de flujo de caja.

📥 Integración de fuentes externas
Importación de archivo CSV con clasificación geográfica
Normalización e incorporación al entorno BigQuery

👉 Valor agregado: enriquecimiento del dataset para habilitar análisis de riesgo geográfico.

🔗 Transformación y modelado de datos
JOIN entre múltiples tablas para consolidar información crítica
Creación de dataset analítico unificado

👉 Problema resuelto: datos fragmentados → dataset listo para análisis

🏗️ Materialización de datos (CTAS)
Implementación de CREATE TABLE AS SELECT
Generación de tablas persistentes listas para consumo

👉 Impacto: mejora en performance + facilidad de exportación y uso por otros equipos

🧩 Manejo de datos complejos
Extracción de información desde estructuras anidadas (purpose)

👉 Insight técnico: capacidad de trabajar con modelos de datos no planos (muy valorado en cloud)

🧹 Data Cleaning & Quality
Identificación y eliminación de duplicados
Estandarización de categorías

👉 Problema resuelto: inconsistencias que afectaban el análisis de comportamiento

📈 Construcción de métricas de negocio
Agregación de préstamos por día y año
Base para monitoreo de flujo de caja

👉 Resultado: dataset preparado para análisis temporal y financiero

📊 Data Analysis & Visualization (Looker)

Se desarrolló el dashboard “Loan Insights”, enfocado en usabilidad y toma de decisiones.

🔴 KPI Crítico — Total Outstanding Loans
Indicador principal de exposición financiera
Formato condicional:
🔴 alerta automática si supera $3B

👉 Valor: permite decisiones rápidas sin necesidad de análisis manual

🥧 Distribución por estado del préstamo
Análisis del portfolio:
Current, Late, Default, Charged-off, etc.

👉 Insight: visibilidad inmediata de la salud de los préstamos

📍 Análisis geográfico (Top 10 estados)
Identificación de concentración de préstamos

👉 Problema resuelto: detección de riesgo sistémico por región

👤 Segmentación de clientes (Top ingresos)
Foco en clientes con:
alto ingreso
vivienda propia
préstamos activos

👉 Valor estratégico: segmentación para decisiones comerciales y de riesgo

⚡ Dashboard Features (UX & Data Experience)
🔄 Cross-filtering (análisis interactivo)
⏱️ Actualización automática:
KPIs críticos → cada hora
Otros insights → diario
🎯 Diseño enfocado en claridad y toma de decisiones

👉 Diferencial: no solo análisis, sino experiencia de usuario (UX en datos)

📈 Business Impact

La solución permitió:

✔️ Monitorear el flujo de caja de forma continua
✔️ Detectar patrones de riesgo en la cartera de préstamos
✔️ Identificar concentraciones geográficas críticas
✔️ Facilitar la toma de decisiones basada en datos
📌 Key Insights (Ejemplo de análisis)
Determinados propósitos de préstamo presentan mayor riesgo de incumplimiento
Existe concentración geográfica en ciertos estados
El volumen de préstamos requiere monitoreo constante para evitar sobreexposición
🧠 Skills Demonstrated
🔹 Técnicas
SQL avanzado (JOINs, CTAS, nested data)
BigQuery (procesamiento en la nube)
Looker & LookML
Modelado de datos
🔹 Analíticas
Data cleaning & data quality
Data storytelling
Definición de KPIs
🔹 De negocio (CLAVE)
Traducción de requerimientos → soluciones técnicas
Pensamiento crítico aplicado a riesgo financiero
Diseño de métricas accionables
🧰 Tech Stack
Google BigQuery
Google Cloud Storage
SQL
Looker Enterprise
LookML
Google Sheets
🎓 Certification

👉 Google Cloud Data Analytics Professional Certificate
