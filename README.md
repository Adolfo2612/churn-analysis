# Análisis de Abandono de Clientes (Churn)

## Informes del Proyecto

Los reportes están organizados en tres notebooks principales:

- Limpieza de datos y análisis exploratorio  
- Preprocesamiento e ingeniería de características  
- Entrenamiento, ajuste y evaluación de modelos  

---

## Contexto y Planteamiento del Problema

Este proyecto se basa en un dataset de una compañía de telecomunicaciones que ofrece servicios de telefonía e internet, junto con servicios digitales adicionales (seguridad en línea, respaldo, soporte técnico, streaming, etc.).

El objetivo es construir un modelo predictivo que identifique clientes con alta probabilidad de abandono (churn), utilizando características demográficas, de servicio contratado y comportamiento de pago. Esto permite a la empresa implementar estrategias de retención personalizadas para reducir pérdidas.

---

## Alcance

- Limpieza y corrección de datos, imputación de valores faltantes  
- Análisis exploratorio para descubrir patrones relevantes  
- Ingeniería de características para mejorar la representación de los datos  
- Selección, entrenamiento y ajuste de modelos de Machine Learning e Inteligencia Artificial (regresión logística, random forest, redes neuronales)  
- Evaluación del rendimiento con métricas específicas para clasificación  

---

## Inteligencia Artificial en el Proyecto

Se aplicaron modelos supervisados para predecir el abandono:

- **Regresión logística**: modelo clásico para problemas binarios con interpretabilidad  
- **Random Forest**: para capturar relaciones no lineales y mejorar la robustez  
- **Red neuronal**: para modelar patrones complejos y mejorar la capacidad predictiva  

Se analizaron métricas como **precisión**, **recall**, **f1-score** y **accuracy** para comparar y seleccionar el mejor modelo según el balance entre detectar clientes que abandonan y minimizar falsos positivos.

---

## Resumen Ejecutivo

Se trabajó con más de 20 variables por cliente. Se destacó que:

- Clientes con contratos mensuales, sin servicios adicionales y con cargos mensuales altos presentan mayor abandono  
- Las variables fueron codificadas y normalizadas, reduciendo dimensionalidad y eliminando redundancias  
- Los modelos mostraron desempeño adecuado, con ventajas y limitaciones según la métrica evaluada  

---

## Diccionario de Datos

| Columna            | Tipo               | Descripción                                         |
|--------------------|--------------------|-----------------------------------------------------|
| `customerID`       | Categórica (ID)     | Identificador único del cliente                     |
| `gender`           | Categórica          | Género: `Male` o `Female`                           |
| `SeniorCitizen`    | Numérica binaria    | 1 si es adulto mayor, 0 si no                       |
| `Partner`          | Binaria             | `Yes` si tiene pareja                               |
| `Dependents`       | Binaria             | `Yes` si tiene dependientes                         |
| `tenure`           | Numérica            | Meses con la empresa                                |
| `PhoneService`     | Binaria             | `Yes` si tiene servicio telefónico                  |
| `MultipleLines`    | Categórica          | Múltiples líneas: `Yes`, `No`, `No phone service`   |
| `InternetService`  | Categórica          | Tipo de internet: `DSL`, `Fiber optic`, `No`        |
| `OnlineSecurity`   | Categórica          | Seguridad online: `Yes`, `No`, `No internet service`|
| `OnlineBackup`     | Categórica          | Respaldo online                                     |
| `DeviceProtection` | Categórica          | Protección de dispositivos                          |
| `TechSupport`      | Categórica          | Soporte técnico                                     |
| `StreamingTV`      | Categórica          | Streaming de TV                                     |
| `StreamingMovies`  | Categórica          | Streaming de películas                              |
| `Contract`         | Categórica          | Tipo de contrato                                    |
| `PaperlessBilling` | Binaria             | Facturación electrónica                             |
| `PaymentMethod`    | Categórica          | Método de pago                                      |
| `MonthlyCharges`   | Numérica            | Cargo mensual                                       |
| `TotalCharges`     | Numérica            | Total pagado (puede tener valores vacíos)          |
| `Churn`            | Binaria             | `Yes` si abandonó, `No` si sigue (variable objetivo)|

---

## Librerías Utilizadas

- `numpy`  
- `pandas`  
- `matplotlib`  
- `seaborn`  
- `scikit-learn`  
- `xgboost`  
- `tensorflow` / `keras`  
