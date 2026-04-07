Cloud Data Analytics Capstone — TheLook Fintech
Descripción general
Proyecto capstone del Google Cloud Data Analytics Professional Certificate (Google Cloud × Coursera).
El proyecto simula un rol real de Cloud Data Analyst en TheLook Fintech, una empresa fintech de préstamos a comerciantes online. El objetivo fue dar respuesta a preguntas de negocio concretas del departamento de Tesorería, cubriendo las cinco etapas del ciclo de datos en la nube: recopilar → procesar → almacenar → analizar → activar.

Problema de negocio
El departamento de Tesorería necesitaba visibilidad sobre tres áreas críticas para la salud financiera de la empresa:

Flujo de caja: monitorear que los fondos recibidos superen los préstamos otorgados cada mes
Propósito de los préstamos: identificar las razones principales por las que los clientes solicitan préstamos, dado que existe correlación entre el motivo declarado y la probabilidad de repago
Distribución geográfica: entender cómo se distribuyen los préstamos por región para mitigar el riesgo de defaults concentrados


Herramientas y tecnologías
HerramientaUsoBigQueryExploración, transformación y almacenamiento de datosSQLConsultas, joins, deduplicación, agregaciones, CTASGoogle Cloud StorageFuente de datos e importación de archivos externosLooker EnterpriseAnálisis visual y construcción del dashboard interactivoLookMLDefinición de dimensiones y métricas en LookerGoogle SheetsExportación y reporte de datos procesados

Estructura del proyecto
Parte 1 — Recopilación, procesamiento y almacenamiento en BigQuery
Exploración del dataset
Análisis del dataset fintech en BigQuery para identificar tablas, esquemas y columnas relevantes. Se localizaron las métricas clave: monto total de préstamos (loan_amount) y fecha de emisión (issued_date).
Importación de datos externos
Se importó un archivo CSV con la clasificación de estados de EE.UU. por región y subregión, generando una nueva tabla estándar en BigQuery para enriquecer el análisis geográfico.
Transformación y joins
Se realizó un JOIN entre la tabla de préstamos y la tabla de regiones para consolidar en un único reporte los campos loan_id, loan_amount y region_name, combinando datos de múltiples fuentes.
Creación de tablas con CTAS
Se utilizó CREATE TABLE AS SELECT para materializar los resultados del JOIN en una nueva tabla exportable, facilitando el trabajo posterior del equipo en Google Sheets.
Trabajo con datos anidados
Se extrajo la columna purpose almacenada como dato anidado dentro del registro de solicitud, para identificar los motivos declarados por los prestatarios al solicitar un préstamo.
Deduplicación
Se detectaron y eliminaron registros duplicados en el campo purpose (por ejemplo, el motivo "wedding" aparecía múltiples veces), garantizando la integridad de los datos para el análisis.
Reporte de flujo de caja
Se construyó una consulta que produce el monto total de préstamos emitidos por día y año, generando una tabla que permite al equipo de Tesorería monitorear el flujo de caja en el tiempo.

Parte 2 — Análisis y activación con Looker Enterprise
Se desarrolló el dashboard interactivo "Loan Insights" con cuatro visualizaciones orientadas a responder las preguntas de negocio del equipo de Tesorería.
Visualización 1 — Total de préstamos vigentes
Métrica de valor único con formato condicional: fondo rojo automático cuando el total supera el umbral de $3.000.000.000, permitiendo al equipo identificar de inmediato si la exposición financiera excede el límite responsable definido.
Visualización 2 — Distribución por estado de préstamo
Gráfico de torta que muestra el porcentaje de préstamos vigentes por categoría de estado (al día, atrasado, en default, cancelado, pagado, en período de gracia), para monitorear la salud del portfolio de préstamos.
Visualización 3 — Top 10 estados con mayor concentración de préstamos
Gráfico de barras limitado a los 10 estados con mayor cantidad de préstamos vigentes, para identificar concentraciones geográficas de riesgo y orientar decisiones de distribución.
Visualización 4 — Top 10 clientes por ingreso
Tabla con los 10 clientes de mayor ingreso individual que son propietarios de vivienda y tienen préstamos vigentes, incluyendo ID de cliente, ingreso anual, estado y tasa de interés.
Funcionalidades avanzadas del dashboard

Cross-filtering habilitado para filtrado dinámico entre visualizaciones
Actualización automática configurada: métricas críticas cada hora, otras visualizaciones cada 24 horas


Habilidades demostradas

Exploración y comprensión de datasets en entornos cloud
Escritura de consultas SQL complejas: JOINs, agregaciones, CTAS, manejo de datos anidados
Deduplicación y limpieza de datos para garantizar integridad analítica
Integración de fuentes de datos heterogéneas (dataset interno + CSV externo)
Construcción de dashboards interactivos orientados a decisiones de negocio
Traducción de requerimientos de stakeholders en soluciones técnicas concretas
Aplicación de formato condicional y alertas visuales para monitoreo de KPIs
Configuración de actualizaciones automáticas para visibilidad en tiempo real


Resultados
El proyecto entregó al departamento de Tesorería de TheLook Fintech:

Un pipeline de datos completo desde la recopilación hasta la visualización
Reportes estructurados sobre flujo de caja, propósito de préstamos y distribución geográfica
Un dashboard interactivo y actualizable con las métricas clave para la toma de decisiones


Certificación
Este proyecto forma parte del Google Cloud Data Analytics Professional Certificate
Emitido por Google Cloud × Coursera
Ver certificado
