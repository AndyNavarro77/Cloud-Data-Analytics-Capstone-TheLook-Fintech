# 🚀 Cloud Data Analytics Project — TheLook Fintech

---

## 🧩 Project Overview

En este proyecto trabajé como **Cloud Data Analyst**, diseñando e implementando un pipeline de datos end-to-end en Google Cloud para una fintech en crecimiento (**TheLook Fintech**).

El objetivo fue transformar datos operativos en **información estratégica** para el equipo de Tesorería, permitiendo monitorear la salud financiera de la empresa y reducir riesgos asociados a la cartera de préstamos.

---

## 🎯 Business Challenge

El área de Tesorería enfrentaba tres desafíos clave:

- Falta de visibilidad sobre el flujo de caja  
- Desconocimiento de los factores de riesgo en los préstamos  
- Riesgo de concentración geográfica  

A partir de esto, se definieron tres preguntas críticas:

- ¿El volumen de préstamos otorgados es sostenible respecto a los ingresos?  
- ¿Qué motivos de préstamo están asociados a mayor riesgo?  
- ¿Cómo se distribuyen los préstamos geográficamente?  

---

## 📊 Data Understanding

El análisis se basó en un dataset de préstamos que incluye:

- Información de préstamos (monto, estado, fecha de emisión)
- Datos de clientes (ingresos, propiedad de vivienda)
- Datos geográficos (estado, región)

### Consideraciones clave:
- Presencia de datos anidados (campo `purpose`)
- Necesidad de integrar fuentes externas (clasificación regional)
- Inconsistencias en categorías (duplicados en motivos de préstamo)

👉 Se realizaron procesos de exploración, validación y limpieza para asegurar la calidad de los datos antes del análisis.

---

## 🏗️ Solution Design

Se desarrolló una solución basada en el ciclo completo de datos en la nube:
Ingesta → Procesamiento → Almacenamiento → Análisis → Activación


El enfoque fue completamente orientado a negocio.

---

## ⚙️ Data Engineering & Processing (BigQuery)

### 🔍 Exploración y entendimiento del dataset
- Análisis estructural de múltiples tablas  
- Identificación de métricas clave:
  - `loan_amount`
  - `issued_date`

---

### 📥 Integración de fuentes externas
- Importación de archivo CSV con clasificación geográfica  
- Normalización e integración en BigQuery  

---

### 🔗 Transformación y modelado de datos
- JOIN entre múltiples tablas  
- Consolidación en un dataset analítico unificado  

---

### 🏗️ Materialización (CTAS)
- Uso de `CREATE TABLE AS SELECT`  
- Generación de tablas listas para análisis y exportación  

---

### 🧩 Manejo de datos anidados
- Extracción del campo `purpose` desde estructuras complejas  

---

### 🧹 Data Cleaning
- Eliminación de duplicados  
- Mejora de calidad e integridad de datos  

---

### 📈 Construcción de métricas
- Agregación de préstamos por día y año  
- Base para análisis de flujo de caja  

---

## 📊 Data Analysis & Visualization (Looker)

Se desarrolló el dashboard **"Loan Insights"** enfocado en toma de decisiones.

---

### 🔴 KPI Principal — Total Outstanding Loans
- Indicador de exposición financiera  
- Alerta visual automática si supera $3B  

---

### 🥧 Distribución por estado del préstamo
- Current, Late, Default, Paid, etc.  

---

### 📍 Top 10 estados con mayor concentración
- Identificación de riesgo geográfico  

---

### 👤 Top 10 clientes por ingreso
- Clientes con alto ingreso + vivienda propia + préstamos activos  

---

## ⚡ Dashboard Features

- Cross-filtering (interactividad)  
- Actualización automática:
  - KPIs → cada hora  
  - Otras métricas → diario  

---

## 📈 Business Impact

El proyecto permitió:

- Monitorear el flujo de caja de forma continua  
- Detectar patrones de riesgo en préstamos  
- Identificar concentraciones geográficas críticas  
- Mejorar la toma de decisiones basada en datos  

---

## 📌 Key Insights

- Determinados propósitos de préstamo presentan mayor riesgo de default  
- Existe concentración geográfica en ciertas regiones  
- El volumen de préstamos requiere monitoreo constante  

---

## 🧠 Skills Demonstrated

### Técnicas
- SQL avanzado (JOINs, CTAS, nested data)  
- BigQuery  
- Looker & LookML  
- Modelado de datos  

### Analíticas
- Data cleaning  
- Data storytelling  
- Definición de KPIs  

### De negocio
- Traducción de requerimientos a soluciones técnicas  
- Pensamiento crítico  
- Análisis de riesgo financiero  

---

## 🧰 Tech Stack

- Google BigQuery  
- Google Cloud Storage  
- SQL  
- Looker Enterprise  
- LookML  
- Google Sheets

---

## 🧠 Analytical Approach

El enfoque del análisis estuvo guiado por las necesidades del negocio:

- Definición de métricas clave alineadas a Tesorería  
- Transformación de datos para responder preguntas específicas  
- Priorización de claridad y usabilidad en la visualización  

Se buscó no solo analizar datos, sino **traducirlos en información accionable**.

---

## 🚀 Conclusion

Este proyecto demuestra la capacidad de:

- Diseñar soluciones de datos orientadas a negocio  
- Trabajar con datos en entornos cloud de forma eficiente  
- Transformar datos complejos en insights claros  
- Construir herramientas que facilitan la toma de decisiones  

Además, sienta las bases para futuras mejoras, como:

- Modelos predictivos de riesgo de default  
- Automatización de pipelines de datos  
- Integración con más fuentes externas  

👉 El enfoque estuvo siempre en generar impacto real mediante datos, no solo en realizar análisis técnicos.

---

## 🎓 Certification

https://www.coursera.org/account/accomplishments/professional-cert/K73Z32MVDVJZ

---

## 🔥 Nota

Este proyecto representa un caso práctico completo de análisis de datos en la nube, enfocado en resolver problemas reales de negocio y generar impacto mediante datos.
