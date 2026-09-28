# Proyecto de IA: Predicción de Riesgo de Anemia Infantil y Segmentación

**1. ¿Cuál es el problema?**
La incapacidad de predecir tempranamente el nivel de riesgo de severidad en casos de anemia infantil utilizando enfoques de estadística descriptiva tradicional.

**2. ¿Cuál es el objetivo?**
Desarrollar y evaluar un sistema de Machine Learning compuesto por un modelo de clasificación (Regresión Logística) y uno de agrupamiento (K-Means) para clasificar el riesgo de severidad mayor y segmentar perfiles de casos.

**3. ¿Qué dataset se utilizó?**
Se utilizó el dataset estructurado `ANEMIA_DA.csv`, correspondiente a 59,225 registros clínicos de pacientes pediátricos de la región San Martín (2016-2025).

**4. ¿Cómo obtener los datos?**
Descargando el archivo público directamente desde la Plataforma Nacional de Datos Abiertos del Ministerio de Salud (MINSA) del Perú, o accediendo al archivo `.csv` adjunto en el repositorio.

**5. ¿Cómo instalar el proyecto?**
Se requiere contar con Python 3.x. Para instalar las dependencias necesarias, se debe ejecutar en la terminal el siguiente comando:
`pip install pandas numpy scikit-learn matplotlib seaborn` (o `pip install -r requirements.txt` si se utiliza en entorno local).

**6. ¿Cómo ejecutar el código?**
Abriendo el archivo interactivo `PachecoAnton_Fatima_Parcial_Seccion_A.ipynb` en Google Colab o Jupyter Notebook y ejecutando las celdas de manera secuencial (desde la celda 1 hasta el final).

**7. ¿Cómo entrenar el modelo?**
Los modelos se entrenan automáticamente al correr las celdas de la sección "6. Modelado" en el notebook. El algoritmo utiliza la función `.fit()` de scikit-learn sobre la partición de entrenamiento preprocesada (`X_train_s`).

**8. ¿Cómo reproducir los experimentos?**
Ejecutando el mismo notebook. Para garantizar resultados idénticos, todo el código (las particiones `train_test_split` y los algoritmos) está anclado a una semilla aleatoria fija mediante el parámetro `random_state=42`.

**9. ¿Cómo ejecutar el prototipo?**
El prototipo tecnológico funciona en el mismo entorno de Google Colab. Al ejecutar todas las celdas, el sistema procesa los datos y devuelve visualmente por consola las matrices de confusión y los mapas de segmentación en tiempo real.

**10. ¿Cuáles fueron los resultados?**
El modelo de Regresión Logística superó al Baseline ingenuo, obteniendo un F1-Score de 0.377 y un Recall de 0.625 (logrando detectar 1,595 casos críticos). Por su parte, K-Means logró segmentar espacialmente los casos con un Silhouette Score de 0.470 (con k=4), identificando clústeres con incidencias de severidad que oscilan entre 13.3% y 24.1%.
