# 📞 Análisis de Operadores Ineficientes (Telecom)

## 📌 Objetivo del proyecto
Identificar operadores de telecomunicaciones con **patrones de ineficiencia operativa** a partir de métricas clave de desempeño, con el fin de **priorizar acciones correctivas** y apoyar la toma de decisiones gerenciales.

El proyecto combina **análisis exploratorio en Python** y **visualización analítica en Power BI**, culminando en un ranking de operadores más ineficientes.

---

## 📊 Dataset
El análisis se realizó sobre un dataset de operaciones de telecomunicaciones que incluye, entre otras, las siguientes variables:

- `operator_id`
- `total_calls`
- `missed_rate_row`
- `mean_wait`
- `outgoing_calls`

A partir de estas métricas se construyó un **score compuesto de ineficiencia**.

---

## 🧠 Metodología

### 1️⃣ Exploratory Data Analysis (Python)
- Limpieza de datos y validación de tipos
- Análisis de distribuciones y detección de outliers
- Transformaciones (log1p) para estabilizar varianza
- Validación de correlaciones entre métricas

### 2️⃣ Construcción del Inefficiency Score
Se definió un **score compuesto (`ineff_score`)** que resume múltiples dimensiones de ineficiencia operativa:

- Alta tasa de llamadas perdidas
- Tiempos de espera elevados
- Volumen de llamadas salientes
- Carga total de llamadas

Las métricas fueron **normalizadas** para asegurar comparabilidad antes de su agregación.

> 📌 El `ineff_score` no representa un valor absoluto, sino una **medida relativa** que permite rankear operadores dentro del sistema.

---

## 📈 Visualización (Power BI) 

Se desarrolló un dashboard interactivo que incluye:

### 🔹 Top 10 operadores más ineficientes
Ranking basado en `ineff_score`, útil para priorización operativa inmediata.

### 🔹 Heatmap de métricas normalizadas
Comparación visual del comportamiento de cada operador a través de múltiples dimensiones de ineficiencia.

### 🔹 KPIs clave
- Total de llamadas
- Tasa de llamadas perdidas
- Tiempo promedio de espera

> ⚠️ El archivo `.pbix` se incluye en el repositorio.  
> Para visualizarlo, debe abrirse en **Power BI Desktop**.

---

## 🛠️ Herramientas utilizadas

- **Python**
  - pandas
  - numpy
  - seaborn / matplotlib
- **Power BI**
  - Power Query
  - DAX (medidas calculadas)
- **Git & GitHub**
  - Control de versiones
  - Documentación del proyecto

---

## 📂 Estructura del repositorio

├── operators_inefficiency_report.csv
├── top offenders visualizations.pbix
├── notebooks/
│ └── sprint_14_proyecto_final_encontrar_operadores_ineficientes.ipynb
├── README.md 


---

## 🎯 Resultados y conclusiones

- Se identificó un subconjunto reducido de operadores que concentran los mayores niveles de ineficiencia.
- El uso de un **score compuesto** facilita la toma de decisiones frente a múltiples métricas aisladas.
- Power BI permitió traducir análisis estadístico en **insights accionables** para perfiles no técnicos.

---

## 🚀 Próximos pasos posibles
- Ajustar ponderaciones del `ineff_score` según criterios de negocio
- Incorporar análisis temporal (tendencias por operador)
- Automatizar el pipeline de datos

---

## 👤 Autor
Carlos Villa  
Proyecto desarrollado como parte de un proceso de formación en análisis de datos y business intelligence.
