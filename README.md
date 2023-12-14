# Analisis Exploratorio de Datos

# Objetivos
Este proyecto tiene como objetivo proporcionar una comprención de un ejemplo practico del uso del algoritmo de RandomForest 
para resolución de problemas de clasificación y regresión de Machine Learning.

Se trabaja en el entorno de desarrollo de Google Colab, en un cuaderno en formato .ipynb.
Se importan las bibliotecas 'sqlite3' para la conexión con base de datos SQLite, 'numpy' para operaciones matemáticas y 'pandas' para manipulación y análisis de datos tabulares.
Se carga la base de datos SQLite 'sensores.db' para establecer la conexión, se crea un query de consulta para seleccionar datos de la base de datos.
Los resultados se cargan en un dataframe llamado 'dataset' y se imprimen.

Se importa la función 'train_test_split' de 'scikit-learn' para dividir los datos en conjuntos de entranamiento y prueba.
Se crean los dataframes individuales que contienen la variable a predecir e índices para el cálculo de las predicciones que no incluyan los ultimos 100 datos faltantes.
El 10% de los datos de las tablas son usados como el conjunto de prueba, usando 1500 árboles de decisión.
La precisión del modelo comparando las predicciones con las etiquetas reales en el conjunto de prueba es del 91%.
.
