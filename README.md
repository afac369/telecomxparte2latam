# 📊 Predicción de Cancelación de Clientes – TelecomX

Este proyecto resuelve el desafío de desarrollar un modelo de machine learning para anticipar qué clientes tienen mayor probabilidad de cancelar sus servicios en **TelecomX**, una empresa de telecomunicaciones ficticia.

---

## 🎯 Objetivo

- Predecir la probabilidad de cancelación de un cliente (`Churn`).
- Analizar los factores más relevantes que influyen en la decisión.
- Ofrecer recomendaciones estratégicas basadas en los datos.

---

## 📦 Datos

El archivo `TelecomX_Data.json` contiene la información de 7.267 clientes. Las variables se agrupan en:

- **Datos personales**: género, si es adulto mayor, si tiene dependientes.
- **Servicios**: teléfono, internet, soporte técnico, streaming, etc.
- **Facturación y contrato**: tipo de contrato, facturación electrónica, método de pago, cargos mensuales y totales.
- **Variable objetivo**: `Churn` (1 = canceló, 0 = sigue activo)

---

## 🛠️ Pipeline del Proyecto

1. **Carga y transformación del JSON**
   - Expansión de columnas anidadas en estructuras planas.
2. **Limpieza de datos**
   - Conversión de tipos, manejo de valores nulos.
3. **Preprocesamiento**
   - Codificación de variables categóricas (`get_dummies`)
   - Escalado de variables numéricas (`StandardScaler`)
4. **Modelado**
   - `RandomForestClassifier`
   - `LogisticRegression`
5. **Evaluación**
   - Reportes de clasificación
   - ROC AUC
   - Matrices de confusión y curvas ROC
6. **Interpretación**
   - Análisis de variables más influyentes en la cancelación

---

## 📈 Resultados

| Modelo               | ROC AUC Score |
|----------------------|---------------|
| Random Forest         | 0.82          |
| Logistic Regression   | 0.85 ✅        |

El modelo de **Regresión Logística** tuvo un mejor desempeño, con una capacidad destacada para discriminar entre clientes propensos y no propensos a cancelar.

---

## 💡 Conclusiones Estratégicas

- Los clientes con **contratos mensuales**, **poco tiempo de permanencia**, **cargos altos** y **sin soporte técnico** tienen mayor riesgo de cancelar.
- Recomendaciones:
  - Fomentar contratos anuales.
  - Ofrecer beneficios por permanencia.
  - Mejorar el soporte técnico para servicios de fibra óptica.

---

## 🚀 Cómo usar

1. Sube `TelecomX_Data.json` a tu entorno (Colab o Jupyter).
2. Ejecuta el notebook `Churn_Prediction_RepoOficial.ipynb`.
3. Analiza o ajusta el pipeline según tus necesidades.

---

## 📚 Créditos

Desarrollado como parte del desafío **Data Science LATAM**, basado en el repositorio oficial:  
🔗 [afac369/challenge2-data-science-LATAM](https://github.com/afac369/challenge2-data-science-LATAM)
