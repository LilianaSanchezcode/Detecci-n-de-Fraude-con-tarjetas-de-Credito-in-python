# Detecci-n-de-Fraude-con-tarjetas-de-Credito-in-python
Detección de Fraude con tarjetas de Credito


Las empresas y las instituciones públicas se enfrentan a un problema masivo debido a que una enorme cantidad de pérdidas son causadas por actividades fraudulentas. Según el informe  Nilson ( https://nilsonreport.com/ ), las pérdidas debidas al fraude con tarjetas de crédito, tarjetas de débito y tarjetas de prepago alcanzó los $ 16,31 mil millones en todo el mundo en 2015. Y el informe de Nilson de 2018  muestra que la pérdida bruta por fraude alcanzó los 22.800 millones de dólares en este año, es un 4% más que en 2015 y se proyecta que alcancen más de 40 mil millones de dólares en 2027.

Según Statista (https://es.statista.com/), el fraude bruto alcanzó los $ 5.6B en 2012, mientras que en 2018, la pérdida por fraude alcanzó los $ 9.100 millones, que es aproximadamente dos quintas partes de la pérdida total.

En particular, el 70% de estos fraudes son fraudes con tarjeta no presente (CNP) (es decir, fraudes realizado en línea o por teléfono), el 20% son falsificaciones y el 10% restante de casos están relacionados a pérdidas debidas a tarjetas pérdidas o robadas [personal].
Cuando no se puede evitar que se produzca un fraude, debe detectarse lo antes posible. como sea posible, y se deben tomar las acciones necesarias en su contra. La detección de fraude, es el proceso de detectar si una transacción es legítima o no. Sistemas automatizados de detección de fraudes, son necesarios especialmente teniendo en cuenta el enorme tráfico de datos de transacciones, y no es posible humanos para verificar manualmente cada transacción una por una, si es fraudulenta o no. Este proyecto tratará la detección de fraudes mediante técnicas de aprendizaje automático, más específicamente aprendizaje supervisado (modelos de clasificación).


**Datos:**

**Fuente: https://www.kaggle.com/mlg-ulb/creditcardfraud**

El conjunto de datos contiene transacciones realizadas con tarjetas de crédito en septiembre de 2013 por titulares de tarjetas europeos. Este conjunto de datos presenta transacciones que ocurrieron en dos días, donde tenemos 492 fraudes de 284.807 transacciones. El conjunto de datos está muy desequilibrado, la clase positiva (fraudes) representa el 0,172% de todas las transacciones.
Contiene solo variables de entrada numéricas que son el resultado de una transformación PCA. Desafortunadamente, debido a problemas de confidencialidad, no podemos proporcionar las características originales y más información de fondo sobre los datos. Las características V1, V2,… V28 son los componentes principales obtenidos con PCA, las únicas características que no se han transformado con PCA son 'Tiempo' y 'Cantidad'. La característica 'Tiempo' contiene los segundos transcurridos entre cada transacción y la primera transacción en el conjunto de datos. La función 'Importe' es el Importe de la transacción, esta función se puede utilizar para el aprendizaje dependiente de los costos por ejemplo. La característica 'Clase' es la variable de respuesta y toma el valor 1 en caso de fraude y 0 en caso contrario.
Dada la relación de desequilibrio de clases, recomendamos medir la precisión utilizando el área bajo la curva de recuperación de precisión (AUPRC). La precisión de la matriz de confusión no es significativa para la clasificación desequilibrada
________________________________________
**Variables no anonimizadas:**

- Time Contiene los segundos transcurridos entre cada transacción.
- Amount - Valor total de la transacción.
- Class-Es el target, etiqueta dada a las transacciones, donde 0 representa una transacción normal y 1 refiere a una transacción fraudulenta.

**Objetivo: Encontrar el mejor modelo que clasifique a las transacciones de tarjeta de crédito de los clientes, como fraudulenta o no fraudulenta.**


**Qué se aplicará para lograr el objetivo?**

- Identificación de la cantidad de variables y registros del data set
- Identificación de variables categóricas y numéricas 
- Distribución percentilica de las variables: Time, y cantidad
- Histograma de las variables: Time y Amount.
- Matriz de correlación  de las variables 
- Identificación de variables con valores outliers mediante Box Plot
- Escalamiento de características mediante Robust Scaler (robusto ante la presencia de valores atípicos)
- Manejo de datos desequilibrados mediante el método de sobremuestreo de minorías (SMOTE)

- Desarrollo de modelos de aprendizaje supervisado :
  - Logistic Regression
  - KNeighbors  
  - Decision Tree 
  - Random Forest
  - AdaBoost
  - CatBoost 
  - LGBM Classifier.


**Hallazgos:**

Los modelos que presentan mayor rendimiento según su AUC son: 
Modelo de Regresión Logística  con AUC=0.977
El modelo Adaboost con AUC=0.964








