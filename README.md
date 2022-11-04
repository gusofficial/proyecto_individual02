# Proyecto individual 02

## Datathon

El proyecto individual 02 se basa en el desarrollo de un modelo de machine learning para estudiar ciertas características del mercado inmobiliario en Colombia. El modelo debía evaluar los precios de diferentes inmuebles y predecir si el precio era caro o barato. La clasificación entre estas categorías se debía hacer tomando en cuenta la media de los precios. Si el precio superaba la media se considera que el inmueble es caro. Si el precio es menor a la media se considera el inmueble barato. 

## Notebook

El notebook "machine_learning_pi_02.ipynb" posee toda la información referente al tratamiento de los datos, su procesamiento y la visualización de las variables respectivas. Luego se presenta una prueba de diferentes modelos para discriminar cuáil sería utilizado para realizar las predicciones. Por último, se encuentra las predicciones realizadas con el modelo que arrojó mejores resultados. Los resultados fueron guardados en un archivo csv.

### EDA

En el proceso de EDA se realizaron varias transformaciones a los datos contenidos en el documento "properties_colombia_train.csv". Se identificaron las columnas con valores únicos. Estas columnas fueron descartadas ya que no proveían información útil para el desarrollo del modelo.

Luego se normalizaron los datos de la columna de precios. Los precios estaban presentados en dos monedas distintas: dólares estadounidenses (USD) y pesos colombianos (COP). Se transformaron aquellos valores que se encontraban expresados como USD tomando como referencia el promedio de la tasa de cambia USD-COP del año 2020. Se descartaron los outliers de la columna precio. Luego, se completaron los valores faltantes con la media de los datos.

Luego se realizó un gráfico para ver la localización geográfico de los puntos de latitud y longitud registrado en la data. Se pudo constatar que existían diferentes puntos fuera del territorio colombiano. Estos puntos "outliers" también fueron descartados. Los valores faltantes de latitud y longitud fueron llenados utilizando la información contenida en la columna l2. 

De la columna de descripciones se extrajo la data necesaria para completar los valores faltantes de la columna "bathrooms."

### Entrenamiento del modelo

Se probaron dos modelos: Random Forest y Gradient Boosting. Al realizar las pruebas se comprobó que el modelo de Random Forest arrojaba mejores valores de recall y accuracy. Se escogió Random Forest como modelo para la predicción.

### Predicción de los datos

Se implementó el modelo de obtenido sobre los datos contenidos en el archivo "properties_colombia_test.csv". Los resultados fueron guardados en un archivo csv. 



