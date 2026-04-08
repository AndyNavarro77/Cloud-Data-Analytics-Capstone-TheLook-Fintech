# ⚙️ Data Processing & Storage — BigQuery

---

## 📌 Overview

En esta etapa del proyecto se trabajó sobre las primeras fases del ciclo de datos en la nube:

> **Recopilar → Procesar → Almacenar**

El objetivo fue preparar los datos necesarios para responder a los requerimientos del área de Tesorería, asegurando calidad, integridad y disponibilidad para análisis posteriores.

---

## 📥 Ingesta de datos externos

Se importó un archivo CSV desde Google Cloud Storage que contiene la clasificación de estados de EE.UU. por región y subregión. Esta información permitió enriquecer el dataset original para análisis geográficos.

```sql
LOAD DATA OVERWRITE fintech.state_region
(
  state     STRING,
  subregion STRING,
  region    STRING
)
FROM FILES (
  format = 'CSV',
  uris   = ['gs://sureskills-lab-dev/future-workforce/da-capstone/temp_35_us/state_region_mapping/state_region_*.csv']
);
```

> 👉 **Resultado:** creación de la tabla `state_region`, lista para ser utilizada en procesos de transformación.

---

## 🔗 Integración de datos (JOIN)

Para responder a los requerimientos del negocio, se integraron datos provenientes de distintas tablas. El objetivo fue construir un dataset unificado que contenga:

- ID del préstamo
- Monto del préstamo
- Región geográfica

```sql
SELECT
  lo.loan_id,
  lo.loan_amount,
  sr.region
FROM fintech.loan lo
INNER JOIN fintech.state_region sr
  ON lo.state = sr.state;
```

> 👉 **Resultado:** consolidación de información clave en una única consulta para análisis.

---

## 🏗️ Materialización de datos (CTAS)

Se utilizó la técnica **CREATE TABLE AS SELECT (CTAS)** para almacenar los resultados del JOIN en una nueva tabla persistente. Esto permite:

- Mejorar la performance
- Facilitar el acceso a otros equipos
- Habilitar la exportación a herramientas como Google Sheets

```sql
CREATE OR REPLACE TABLE fintech.loan_with_region AS
SELECT
  lo.loan_id,
  lo.loan_amount,
  sr.region
FROM fintech.loan lo
INNER JOIN fintech.state_region sr
  ON lo.state = sr.state;
```

> 👉 **Resultado:** creación de una tabla analítica lista para consumo.

---

## 🧹 Limpieza de datos (Deduplicación)

Se detectaron duplicados en los valores del campo `purpose`, lo cual podía afectar la calidad del análisis. Para resolverlo, se creó una tabla con valores únicos:

```sql
CREATE TABLE fintech.loan_purposes AS
SELECT DISTINCT application.purpose
FROM fintech.loan;
```

> 👉 **Resultado:** dataset limpio y consistente para análisis de comportamiento.

---

## 📊 Agregación de datos

Se construyó una tabla agregada para analizar la evolución de los préstamos en el tiempo:

```sql
CREATE TABLE fintech.loan_count_by_year AS
SELECT
  issue_year,
  COUNT(loan_id) AS loan_count
FROM fintech.loan
GROUP BY issue_year;
```

> 👉 **Resultado:** base estructurada para análisis temporal y métricas de negocio.

---

## 📈 Impacto en el negocio

Las transformaciones realizadas permitieron:

- Mejorar la calidad e integridad de los datos
- Integrar múltiples fuentes en un dataset unificado
- Preparar información clave para análisis de flujo de caja
- Facilitar el acceso a datos para otros equipos

---

## 🚀 Conclusión

En esta etapa se logró construir una base sólida de datos mediante:

- Ingesta de fuentes externas
- Transformación e integración de datos
- Limpieza y validación
- Creación de tablas analíticas

> 👉 Este proceso fue fundamental para habilitar el análisis posterior y la construcción de dashboards orientados a la toma de decisiones.
