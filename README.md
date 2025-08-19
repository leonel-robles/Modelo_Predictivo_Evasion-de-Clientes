# Proyecto de Predicción de Cancelación de Clientes - Telecom X

## Descripción del Proyecto

Este proyecto tiene como objetivo desarrollar modelos predictivos para identificar a los clientes de Telecom X con alta probabilidad de cancelar sus servicios. La empresa busca anticiparse al problema de la cancelación para implementar estrategias de retención proactivas.

El proyecto abarca las siguientes etapas:
1.  **Extracción y Carga de Datos**: Carga del dataset de clientes de Telecom X.
2.  **Preprocesamiento de Datos**: Limpieza, transformación y preparación de los datos para el modelado. Esto incluyó la eliminación de columnas irrelevantes, la codificación de variables categóricas (One-Hot Encoding) y el escalamiento de características numéricas.
3.  **Análisis Exploratorio de Datos (Visualización)**: Exploración de la relación entre variables clave (como Gasto Total y Tiempo de Contrato) y la cancelación.
4.  **Balanceo de Clases**: Aplicación de técnicas como SMOTE para abordar el desbalance significativo entre las clases de clientes que cancelaron y los que no.
5.  **Modelado Predictivo**: Entrenamiento de modelos de clasificación (Regresión Logística y Random Forest) para predecir la cancelación.
6.  **Evaluación del Modelo**: Evaluación del rendimiento de los modelos utilizando métricas como Exactitud, Precisión, Recall, F1-score, AUC y la Matriz de Confusión.
7.  **Análisis de Importancia de Variables**: Identificación de las características más relevantes para la predicción de cancelación según cada modelo.
8.  **Identificación de Factores Clave y Estrategias de Retención**: Análisis de los resultados para determinar los principales impulsores de la cancelación y proponer acciones de retención basadas en estos hallazgos.

## Datos

El dataset utilizado se obtuvo de la siguiente URL:
`https://raw.githubusercontent.com/leonel-robles/Modelo_Predictivo_Evasion-de-Clientes/refs/heads/main/data/Telecom_X`

Contiene información sobre los clientes de Telecom X, incluyendo datos demográficos, servicios contratados, información de facturación y si el cliente canceló o no.

## Resultados Principales

### Factores Clave de Cancelación

Basado en el análisis exploratorio y la importancia de las variables en los modelos, los principales factores que influyen en la cancelación incluyen:

*   **Tipo de Contrato**: Clientes con contratos mes a mes son más propensos a cancelar.
*   **Gasto Total**: Clientes con menor gasto total tienden a cancelar más.
*   **Antigüedad**: Clientes con mayor antigüedad son menos propensos a cancelar.
*   **Servicios Adicionales**: La ausencia de servicios como seguridad online y soporte técnico está asociada a una mayor probabilidad de cancelación.
*   **Método de Pago**: El método de pago 'Electronic check' mostró una mayor asociación con la cancelación en la Regresión Logística.
*   **Cargos Mensuales**: También son un factor relevante en la predicción.

### Rendimiento del Modelo

Se entrenaron y evaluaron dos modelos: Regresión Logística y Random Forest. Ambos modelos mostraron un rendimiento razonable en la predicción de la cancelación, con diferentes fortalezas en las métricas evaluadas. El Random Forest tuvo una Exactitud y Precisión ligeramente superiores para la clase minoritaria, mientras que la Regresión Logística obtuvo un Recall más alto, siendo más efectiva para identificar a los clientes en riesgo real de cancelación. La elección del modelo dependerá de los objetivos específicos del negocio.

### Estrategias de Retención Propuestas

Basadas en los factores identificados, se proponen las siguientes estrategias:

*   Implementar programas de fidelización para clientes con contratos mes a mes.
*   Realizar intervenciones tempranas para clientes de bajo gasto, ofreciendo promociones o evaluando satisfacción.
*   Promocionar servicios de valor añadido (seguridad, soporte) para aumentar la lealtad.
*   Investigar y optimizar los métodos de pago asociados a mayor cancelación.
*   Segmentar clientes en riesgo y ofrecerles ofertas o comunicaciones personalizadas.
*   Establecer un monitoreo continuo para identificar clientes en riesgo en tiempo real.

## Cómo Ejecutar el Código

Para replicar este análisis y modelado, puedes seguir los pasos detallados en el notebook de Colab. Asegúrate de ejecutar las celdas en orden para cargar, preprocesar, modelar y evaluar los datos correctamente.

*   Clona este repositorio (si aplica).
*   Abre el notebook en Google Colab o tu entorno Python preferido.
*   Ejecuta las celdas secuencialmente.

## Dependencias

Las principales bibliotecas utilizadas incluyen:

*   pandas: Para manipulación y análisis de datos.
*   numpy: Para operaciones numéricas.
*   scikit-learn: Para división de datos, escalamiento, modelos y métricas de evaluación.
*   imblearn: Para técnicas de balanceo de clases como SMOTE.
*   matplotlib y seaborn: Para visualización de datos.
