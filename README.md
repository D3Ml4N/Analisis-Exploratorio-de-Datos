# Analisis Exploratorio de Datos

# Objetivos
Este proyecto tiene como objetivo proporcionar una comprención de un ejemplo practico del uso del algoritmo de RandomForest 
para resolución de problemas de clasificación y regresión de Machine Learning.

# Descripción
Se trabaja en el entorno de desarrollo de Google Colab, en un cuaderno en formato .ipynb. En la siguiente explicación, 'In[n]' significa las entradas en código del cuaderno jupyter de Google Colab llamado 'Automatizacion_taller2.ipynb1, y Out[n] su respectiva salida.

In[2]: Se importan las bibliotecas 'sqlite3' para la conexión con base de datos SQLite, 'numpy' para operaciones matemáticas y 'pandas' para manipulación y análisis de datos tabulares.
Se carga la base de datos SQLite 'sensores.db' para establecer la conexión, se crea un query de consulta para seleccionar datos de la base de datos.
Los resultados se cargan en un dataframe llamado 'dataset'

Out[2]: Se presenta una tabla con las columnas de 'tamaño', 'sensor_polaris',	'sensor_orion',	'sensor_antares',	'sensor_vega',	'categoria',	'Clasificacion_bin', que contienen los datos de la respectiva consulta query.

In[32]: Se importa la función 'train_test_split' de 'scikit-learn' para dividir los datos en conjuntos de entranamiento y prueba.
Se crean los dataframes individuales que contienen la variable a predecir e índices para el cálculo de las predicciones, siendo X la  que no incluye los ultimos 100 datos faltantes, y Y el index que sí los contiene. El 10% de los datos de las tablas son usados como el conjunto de prueba, usando 1500 árboles de decisión.

Out[33]: Se imprime la tabla correspondiente al 10% de datos para la prueba del modelo.

Out[41]: Se proporciona el array que el modelo predice respecto al test del 10% de los datos, donde '1' corresponde al valor 'Positivo', y '0' al valor 'Negativo'. La precisión del modelo comparando las predicciones con las etiquetas reales en el conjunto de prueba es del 91%.

Out[42]: Finalmente se imprimen el array correspondiente a los últimos 100 valores faltantes que el modelo debía predecir.

In[47]: Se exporta el array de Out[42] con sus respetivas etiquetas en un archivo csv llamado 'Predicciones.csv'
