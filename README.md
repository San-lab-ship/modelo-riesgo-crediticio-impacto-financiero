# 💳 Predicción y Optimización de Riesgo Crediticio en Fintech Digital

---

## 🎯 Objetivo

Desarrollar un sistema predictivo que estime la probabilidad de incumplimiento crediticio y optimice la decisión de aprobación de créditos digitales maximizando la rentabilidad esperada (P&L), reduciendo pérdidas por default y mejorando la eficiencia en la asignación de capital.

El modelo integra variables transaccionales, comportamentales y financieras para transformar la analítica avanzada en decisiones estratégicas medibles.

---

## 📌 Descripción del problema

Las fintech digitales enfrentan un reto estructural: aprobar más créditos aumenta ingresos por intereses, pero incrementa la exposición al riesgo de incumplimiento.

Los modelos tradicionales optimizan métricas técnicas como AUC o accuracy, pero no necesariamente maximizan la utilidad financiera del portafolio.

Este proyecto aborda el problema desde una perspectiva integral:

- Predicción de probabilidad de default  
- Cálculo de beneficio esperado por cliente  
- Diseño experimental para medir lift real en rentabilidad  
- Monitoreo de drift para asegurar estabilidad en producción  

El objetivo no es solo predecir riesgo, sino optimizar decisiones alineadas con impacto financiero real.

---

## 🏗 Arquitectura del Sistema

La solución se basa en un pipeline modular de ciencia de datos productiva:

- Extracción y construcción de dataset: SQL + generación de datos sintéticos financieros  
- Ingeniería de características: variables de comportamiento crediticio, ratios financieros y segmentación de riesgo  
- Entrenamiento de modelos predictivos: Logistic Regression, Random Forest y XGBoost para probabilidad de default  
- Optimización basada en P&L: cálculo de beneficio esperado y selección óptima de umbral  
- Diseño experimental: simulación A/B Testing para medir impacto en rentabilidad  
- Monitoreo: detección de data drift y performance decay  
- Visualización ejecutiva: dashboard interactivo de riesgo y profit  

**Flujo del sistema:**

```
Datos → Feature Engineering → Modelo → Profit Optimization → Decisión → A/B Testing → Monitoreo
```

---

## 🔬 Metodología

### 📥 Carga y Exploración de Datos

**Marcos de datos:**

- df_clientes  
- df_transacciones  
- df_creditos  

- Identificación de variables clave (ingresos, historial de pagos, utilización de crédito)  
- Análisis de correlación y distribución de variables financieras  
- Evaluación de balance de clases (default vs no default)  

---

### 🧹 Limpieza y Preparación

- Tratamiento de valores nulos  
- Normalización de variables financieras  
- Codificación de variables categóricas  
- Generación de variable objetivo (default)  

---

### ⚙️ Ingeniería de Características

- Ratio deuda/ingreso  
- Frecuencia de pagos atrasados  
- Utilización de línea de crédito  
- Antigüedad como cliente  
- Variables de comportamiento transaccional  

---

### 🔄 Preprocesamiento

- Escalado con StandardScaler  
- Codificación con OneHotEncoder  
- Pipeline automatizado con ColumnTransformer  

---

### 🤖 Entrenamiento y Optimización

**Modelos implementados:**

- Regresión Logística (baseline interpretable)  
- Random Forest  
- XGBoost (modelo principal)  

Validación cruzada y optimización con RandomizedSearchCV.

**Métricas técnicas:**

- AUC  
- KS  
- LogLoss  
- Precision-Recall  

---

## 💰 Optimización Financiera

Se define la función de beneficio esperado:

```
Beneficio Esperado =
(Probabilidad de pago × Ingreso por interés) − (Probabilidad de default × Pérdida esperada)
```

Se identifica el threshold óptimo que maximiza la rentabilidad total del portafolio.

---

## 🧪 Diseño Experimental

Simulación de A/B Testing:

- Grupo A → Modelo tradicional optimizado por AUC  
- Grupo B → Modelo optimizado por profit  

Se mide:

- Lift en rentabilidad  
- Reducción de tasa de default  
- Intervalos de confianza  
- Prueba de hipótesis para validar significancia estadística  

---

## 📊 Monitoreo

- Detección de data drift en variables críticas  
- Seguimiento de caída de desempeño  
- Definición de triggers de reentrenamiento  

---

## 🛠 Tecnologías utilizadas

- Python 3.10 ✔️  
- Jupyter Notebook ✔️  
- Pandas ✔️  
- NumPy ✔️  
- SQL ✔️  
- Scikit-learn ✔️  
- XGBoost ✔️  
- RandomForestClassifier ✔️  
- Matplotlib ✔️  
- Seaborn ✔️  
- Evidently AI ✔️  
- Streamlit ✔️  
- Draw.io ✔️  
- Git / GitHub ✔️  

**Opcional escalable:** PySpark / AWS  

---

## 📈 Resultados y conclusiones

🧩 El proyecto integró modelado predictivo, optimización financiera y validación experimental para transformar un modelo de riesgo en una herramienta estratégica de negocio.

El modelo XGBoost alcanzó un **AUC de 0,91** y una mejora del **22 % en rentabilidad esperada** frente al modelo baseline.

La optimización basada en P&L permitió:

- Reducir pérdidas por default  
- Incrementar utilidad promedio por cliente aprobado  
- Alinear métricas técnicas con objetivos financieros reales  

**Conclusión clave:**

La verdadera ventaja competitiva en fintech no está solo en predecir riesgo, sino en optimizar decisiones bajo criterios financieros cuantificables.

---

## 📊 Visualizaciones desarrolladas

- 📈 Curva ROC y KS  
- 💰 Profit Curve vs Threshold  
- 📊 Distribución de probabilidad de default por segmento  
- 📉 Lift Chart del A/B Testing  
- 📌 Importancia de variables del modelo  
- 📊 Monitoreo de drift en variables financieras críticas  
- 📊 Dashboard interactivo de decisión crediticia con Streamlit  

---

## 💼 Impacto para el Sector Empresarial

El modelo permite a fintech y banca digital:

- Optimizar decisiones de aprobación crediticia  
- Maximizar rentabilidad esperada del portafolio  
- Reducir exposición a clientes de alto riesgo  
- Implementar experimentación rigurosa para validar impacto real  
- Escalar modelos en entornos productivos con monitoreo continuo  

Este enfoque transforma la ciencia de datos en un activo estratégico que impacta directamente el P&L, fortalece la sostenibilidad financiera y mejora la toma de decisiones basada en evidencia.
