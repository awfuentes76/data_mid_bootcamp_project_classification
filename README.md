# Análisis de aceptación de ofertas de tarjetas de crédito

## Objetivo del proyecto
El objetivo de este proyecto es comprender las razones por las cuales algunos clientes del banco aceptan ofertas de tarjetas de crédito, mientras que otros no. Además, se busca identificar oportunidades potenciales que el banco pueda aprovechar a partir de los datos disponibles. Este proyecto forma parte del Bootcamp de Ironhack.

## Conjunto de datos
El conjunto de datos consta de información sobre 18,000 clientes actuales del banco. Los datos proporcionan detalles sobre la demografía y otras características de los clientes, así como si aceptaron o no una oferta de tarjeta de crédito.

### Definiciones de las columnas:
| Nombre de columna       | Descripción                                         |
|-------------------------|-----------------------------------------------------|
| Customer Number         | Número secuencial asignado a los clientes           |
| Offer Accepted          | Si el cliente aceptó (Sí) o rechazó (No) la oferta  |
| Reward                  | Tipo de programa de recompensas ofrecido            |
| Mailer Type             | Tipo de correo (Carta o Postal)                     |
| Income Level            | Nivel de ingresos (Bajo, Medio, Alto)               |
| Bank Accounts Open      | Número de cuentas bancarias abiertas                |
| Overdraft Protection    | Protección contra sobregiros (Sí o No)              |
| Credit Rating           | Calificación crediticia (Baja, Media, Alta)         |
| Credit Cards Held       | Número de tarjetas de crédito mantenidas en el banco|
| Homes Owned             | Número de casas propias                             |
| Household Size          | Tamaño del hogar                                    |
| Own Your Home           | Si el cliente posee su casa (Sí o No)               |
| Average Balance         | Saldo promedio de la cuenta                         |
| Q1 Balance              | Saldo promedio del primer trimestre                 |
| Q2 Balance              | Saldo promedio del segundo trimestre                |
| Q3 Balance              | Saldo promedio del tercer trimestre                 |
| Q4 Balance              | Saldo promedio del cuarto trimestre                 |

## Herramientas utilizadas
- Visualización: Power BI
- Análisis exploratorio de datos (EDA): MySQL, Python (Jupyter Notebook)
- Machine Learning: Python (Jupyter Notebook) utilizando regresión logística, KNN y árboles de decisión

## Estructura del proyecto
1. **Importación de librerías y carga de datos:** Inicialización y carga de los datos.
2. **Análisis exploratorio de datos (EDA):** Análisis de variables categóricas y numéricas, distribución de la variable objetivo y matriz de correlación.
3. **Preparación de datos:** Identificación y tratamiento de valores atípicos, codificación de variables categóricas y división de datos.
4. **Construcción y evaluación de modelos:** Entrenamiento y evaluación de modelos de regresión logística, KNN y árboles de decisión, incluyendo la validación cruzada.
5. **Interpretación de resultados:** Comparación de modelos y conclusiones sobre el mejor rendimiento.

### 1. Importación de librerías y carga de datos
- Importación de librerías necesarias.
- Carga del archivo CSV sin encabezados.
- Asignación de nombres a las columnas.
- Descripción inicial de los datos.
- Comprobación de valores nulos.

### 2. Análisis exploratorio de datos (EDA)
- Análisis de la variable objetivo ('Offer Accepted').
- Análisis de las variables categóricas ('Reward', 'Mailer Type', 'Income Level', 'Overdraft Protection', 'Credit Rating', 'Own Your Home').
- Análisis de las variables numéricas ('Bank Accounts Open', 'Credit Cards Held', 'Homes Owned', 'Household Size', 'Average Balance', 'Q1 Balance', 'Q2 Balance', 'Q3 Balance', 'Q4 Balance').
- Matriz de correlación para entender las relaciones entre variables numéricas.

### 3. Preparación de datos
- Identificación y tratamiento de valores atípicos usando el método de IQR.
- Codificación de variables categóricas.
- División de los datos en características (X) y variable objetivo (y).
- Normalización de los datos.

### 4. Construcción y evaluación de modelos
- Verificación de valores faltantes en los conjuntos de datos escalados.
- Imputación de valores faltantes usando el método de la media.
- Entrenamiento y evaluación de los modelos de regresión logística, KNN y árboles de decisión.
- Comparación de los modelos basados en la exactitud en entrenamiento y prueba.

### 5. Validación cruzada
- Realización de validación cruzada para los modelos de regresión logística, KNN y árboles de decisión.
- Interpretación de los resultados de la validación cruzada.

## Conclusiones
- La regresión logística y el KNN mostraron un buen desempeño, con alta capacidad de generalización y precisión. 
- El árbol de decisión mostró una tendencia al sobreajuste y un rendimiento inferior en comparación con los otros dos modelos.
- Se recomienda utilizar la regresión logística por su simplicidad y menor necesidad de ajuste de hiperparámetros en comparación con el KNN.

Para obtener una comprensión más detallada de los resultados y la metodología, consulte los notebooks de Jupyter proporcionados.
