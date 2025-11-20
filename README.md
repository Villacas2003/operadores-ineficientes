# 🚀 Detección de Operadores Ineficientes

Este proyecto identifica operadores ineficientes en un centro de llamadas mediante análisis estadístico y pruebas de hipótesis en Python.  
El código realiza un pipeline completo: limpieza de datos, métricas clave, ranking de desempeño y recomendaciones automáticas.

---

## 📂 Estructura del proyecto

operadores-ineficientes/
├── sprint_14_proyecto_final_encontrar_operadores_ineficientes.ipynb #Pipeline completo en Python
├── presentacion_resultados_operadores.pdf #Resultados y storytelling
└── README.md #Documentación del proyecto


---

## 🧠 Metodología general
1. **Carga y limpieza de datos**  
   Conversión de tipos, control de valores nulos y normalización de variables clave (`is_missed_call`, `internal`, etc.).
2. **Cálculo de métricas**  
   - Tasa de llamadas perdidas  
   - Duración total y promedio  
   - Score de ineficiencia combinado
3. **Ranking y pruebas estadísticas (Z-test)**  
   Identificación de operadores con tasas de llamadas perdidas significativamente superiores a sus pares.
4. **Recomendaciones automáticas**  
   Priorización de operadores según nivel de riesgo: `HIGH`, `MEDIUM`, `LOW`.
5. **Visualización**  
   Gráficos con Seaborn/Matplotlib (ranking, tasa de omisión, score).

---

## 📈 Resultados principales
- Se detectaron operadores con tasas de pérdida hasta **3 veces** mayores que la media del grupo.
- El test de proporciones (Z-test) confirmó diferencias estadísticamente significativas (p < 0.05).
- Se recomienda **coaching inmediato y revisión de colas de atención** para los operadores de prioridad alta.

---

## 🧩 Tecnologías utilizadas
- Python (Pandas, NumPy, Seaborn, Statsmodels)
- Jupyter Notebook
- Matplotlib
- Scikit-learn (para escalado/normalización)
- PowerPoint para presentación ejecutiva

---

## 🪜 Próximos pasos
- Integrar panel interactivo en **Tableau**.  
- Automatizar la ingesta de datos diarios.  
- Implementar alertas automáticas con umbrales dinámicos.

---

## 👤 Autor
**Carlos Villa**  
📍 Proyecto Sprint 14 – Análisis de desempeño operativo  
📅 Octubre 2025
