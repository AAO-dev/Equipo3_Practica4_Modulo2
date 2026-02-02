# Práctica 4 – Predicción de Churn de Clientes  
**Diplomado en Ciencia de Datos – Módulo 2 (Modelos Supervisados) - Equipo 3**


## Descripción del proyecto
En esta práctica se aborda el problema de **abandono de clientes (churn)** en una empresa de telecomunicaciones utilizando técnicas de **aprendizaje supervisado**.  
El objetivo es identificar clientes con alta probabilidad de cancelar el servicio, con el fin de apoyar la toma de decisiones para estrategias de retención.

El proyecto incluye análisis exploratorio de datos (EDA), ingeniería de características, entrenamiento y evaluación de distintos modelos de clasificación, así como la selección del modelo con mejor desempeño desde una perspectiva técnica y de negocio.

---

## Dataset
- **Fuente:** Telco Customer Churn (IBM / Kaggle)
- **Observaciones:** Clientes de una empresa de telecomunicaciones
- **Variable objetivo:** `Churn`  
  - `Yes`: el cliente abandonó el servicio  
  - `No`: el cliente permaneció

El dataset contiene información demográfica, contractual, de servicios contratados y de facturación.

---

## Metodología

### 1. Análisis Exploratorio de Datos (EDA)
- Distribución de variables numéricas y categóricas
- Análisis univariado y bivariado respecto al churn
- Identificación de patrones de abandono asociados a:
  - Antigüedad (tenure)
  - Tipo de contrato
  - Método de pago
  - Servicios contratados

### 2. Ingeniería de Características
- Conversión de la variable objetivo a formato numérico
- Escalamiento de variables numéricas
- Codificación One-Hot de variables categóricas
- Construcción de pipelines de preprocesamiento

### 3. Modelado Supervisado
Se entrenaron y evaluaron los siguientes modelos:
- Regresión Logística (baseline)
- Árbol de Decisión
- Random Forest
- Red Neuronal (MLP)

Los modelos fueron comparados utilizando métricas enfocadas en la detección de churn, considerando el desbalance de clases.

---

## Evaluación de Modelos
Las métricas principales utilizadas fueron:
- Precision
- Recall
- F1-score
- ROC-AUC

Se dio especial importancia al **recall de la clase churn**, debido al mayor costo asociado a no detectar clientes que abandonan el servicio.

---

## Modelo Seleccionado
El **Random Forest** fue seleccionado como modelo final al presentar:
- La mayor capacidad de discriminación global (ROC-AUC)
- Un recall alto para la clase churn
- Buen equilibrio entre desempeño predictivo y robustez

---

## Implicación práctica
El modelo puede utilizarse como una herramienta de apoyo operativo para:
- Generar un ranking de clientes según su probabilidad de churn
- Priorizar clientes en riesgo para acciones de retención
- Reducir la pérdida de clientes aceptando un número controlado de falsos positivos

---

---

## Autores
- Myrna Miguel de la Torre
- Luis Manuel Álamo Díaz
- Andre Arellano Ortiz
- Erik Osvaldo Burciaga Piña
- Aldo A. Rodriguez Flores
- Pascual Enrique Juárez Luna