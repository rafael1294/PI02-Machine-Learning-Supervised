
# PROYECTO INDIVIDUAL #2 : MACHINE LEARNING


<p align="center">
<img src="https://healthitanalytics.com/images/site/article_headers/_normal/Data_funnel.jpg"  height=250><br><br>

# DESCRIPCIÓN :

Este proyecto tiene como objetivo generar un modelo de ML que pueda predecir si un paciente estará hospitalizado más de 8 dias o no, por lo cual, se dispone de una data de 410000 registros. El objetivo del proyecto es obtener métricas de "recall" y "accuracy" mayores a 70%.<br>
<br>

<img src="https://uploads-ssl.webflow.com/61eeba8765031c95bb83b2ea/61fbec562cf81f62a255f192_61eeb99a54a67e18ce19d47c_0_nyBFE8lLgr8ePAJ_%20(1).jpeg"  height=200><br><br>

# FEATURE ENGINEERING :

-  Importamos los archivos "hospitalizacions_test.csv" y "hospitalizacions_train.csv" de la carpeta "Datasets", se verifica que ambos archivos tienen la misma estructura.
-  EDA: Se realiza la exploracion de cada columna, buscando valores nulos y repetidos para su corrección.
-  Los valores categóricos de ambos archivos serán convertidos a numéricos y así puedan ser tratados correctamente en los modelos de ML.
<br>
<br>

# FEATURE ENCODING :

-  Se han considerado todas las columnas de la data, las razones del porqué se considera cada columna estan descritas en el archivo "Proyecto.ipynb.
- Los valores categóricos son convertidos a numéricos de cada columna (feature), aplicando "One hot encoder" y "label encoder".
- Se genera un heatmap para verificar la correlación de cada feature con la columna de "Stay". La baja correlación de cada feature no es determinante en su descarte para el proceso de entrenamiento y modelado.

<br>
<br>

# MODELING:


- Se divide el Dataframe con split, en una muestra de 70% para entrenamiento y 30% para testeo.
- Se hace uso de los siguientes modelos:
    - Regresión Logística
    - Vecinos más cercanos
    - Árbol de decisión
- Se ha observado que la eliminación de parametros con baja correlacion overfitea nuestros modelos.
- Despues de generar los modelos, se observa que, la mejores métricas se generan con el "Árbol de decisión".

    - Accuracy: 0.758569105691057
    - Recall:  0.8043583345309172

- Estas métricas superan el valor esperado del 70%, de esta manera seleccionamos ese modelo y procedemos a generar el archivo "pred".

<br><br>


# RESULTADOS : 

- En la carpeta "pred", se encuentra el archivo "rafael1294.csv", generado a partir de la predicción del mejor modelo.

<img src="https://colegiodemedicina.es/wp-content/uploads/2022/08/methods-section-750x300-1.jpg"  height=150><br><br>
