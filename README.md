# RiskMathics: Crédito y Fraude

Este repositorio contiene el material y ejercicios prácticos del curso de RiskMathics sobre Prevención de Fraude y Propensión de Crédito. A través de estos ejercicios se implementan técnicas avanzadas de aprendizaje automático para resolver problemas financieros.

## Contenido

El repositorio se compone de dos casos de uso principales:

1. **Análisis de Deserción (Attrition Analysis)**
2. **Detección de Fraude** (en desarrollo)

## Caso 1: Análisis de Deserción de Clientes

Este notebook implementa un modelo de predicción para identificar posibles clientes que podrían abandonar los servicios bancarios. 

### Descripción del modelo

El modelo principal utiliza **XGBoost** (Extreme Gradient Boosting), un algoritmo basado en árboles de decisión que:

- Construye árboles secuencialmente, enfocándose en corregir los errores de los árboles anteriores
- Repondera las observaciones después de cada iteración para enfatizar los casos mal clasificados
- Incorpora regularización para evitar el sobreajuste
- Maneja eficientemente datos faltantes
- Ofrece alta velocidad de procesamiento y precisión

También se implementa un modelo de **Árbol de Decisión** para comparación y análisis. Un árbol de decisión:

- Es un modelo de aprendizaje supervisado que segmenta datos mediante decisiones binarias
- Crea una estructura jerárquica donde cada nodo representa una prueba sobre una característica
- Las ramas representan los resultados de la prueba
- Las hojas representan la clasificación final o valor de predicción
- Proporciona alta interpretabilidad visual de las reglas de decisión
- Puede manejar tanto datos numéricos como categóricos sin normalización previa

### Métricas de rendimiento

El modelo XGBoost alcanza:
- Precisión global: 98%
- F1-Score para clientes existentes: 0.99
- F1-Score para clientes que abandonan: 0.92

### Características principales

Las características más importantes para predecir la deserción de clientes son:

1. Número total de transacciones (`Total_Trans_Ct`)
2. Saldo rotativo total (`Total_Revolving_Bal`)
3. Número total de productos (`Total_Relationship_Count`)
4. Monto total de transacciones (`Total_Trans_Amt`)
5. Cambio en número de transacciones Q4-Q1 (`Total_Ct_Chng_Q4_Q1`)

## Requisitos

```
scikit-learn==1.3.0
xgboost==1.7.6
pandas==2.0.3
numpy==1.24.3
matplotlib==3.7.2
seaborn==0.12.2
```

## Instrucciones de uso

1. Clone el repositorio:
```bash
git clone https://github.com/fridaruh/RiskMathics_Credito_y_Fraude.git
```

2. Navegue al directorio del proyecto:
```bash
cd RiskMathics_Credito_y_Fraude
```

3. Abra el notebook correspondiente al caso de uso que desea explorar.

## Próximos pasos

- Incorporación del segundo caso de uso: Detección de Fraude
- Mejora de modelos con técnicas de ensamblaje adicionales
- Adición de técnicas para balance de clases

## Referencias

- Documentación de [XGBoost](https://xgboost.readthedocs.io/)
- Material del curso RiskMathics: Prevención de Fraude y Propensión de Crédito

---

© 2025 Frida Ruh - Materiales del curso RiskMathics
