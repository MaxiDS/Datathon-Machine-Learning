# <h1 align=center>**`Datathon - Machine Learning`**</h1>
# <h3 align=center> **Proyecto de clasificacion con ML** </h3>
<p align="center">
<img src="https://www.nephrocare.com.ar/fileadmin/user_upload/assets/images/master/professionals/Careers/NC_Team/NC_team_iStock-1045200338.png"  height=400>
</p>

<hr>

## **TABLA DE CONTENIDO**  
+ 1-Introducción.  
+ 2-Objetivo de trabajo.  
+ 3-Principales tecnologías utilizadas.  
+ 4-Plan de Acción. 
+ 5-Observaciones.   
+ 6-Conclusiones.  

<hr>  

## **1-Introducción**  

Hola! 👋 mi nombre es Lucas Maximiliano Seidl y este repositorio contiene mi proyecto individual para el "Datathon - Machine Learning" de la carrera de Data Science en la academia Henry.  
En este trabajo cree un modelo que puede predecir, a partir de ciertos datos, si un paciente va a permanecer en el hospital durante más o menos de 8 días.

<hr>

## **2-Objetivo de trabajo**  

Un importante Centro de Salud lo ha contratado con el fin de poder predecir si un paciente tendrá una estancia hospitalaria prolongada o no. Para ello tenemos dos archivos csv, uno "train" con el cual vamos a entrenar nuestro modelo de ML y "test" en el cual vamos a aplicar el modelo realizado y conseguir las predicciones.  

+ Análisis exploratorio de los datos (EDA).

+ División de dataset en train y test utilizando train_test_split, CV, KFold o similares.

+ Entrenamiento y predicción utilizando un Modelo de Machine Learning adecuado al problema (clasificación o regresión).

+ Utilización de Pipelines en la producción del modelo.

+ Comentarios y redacción con la fundamentación de la solución propuesta, escrita en Markdown en el Jupyter Notebook (.ipynb) o bien en un documento aparte.

<hr>  

## **3-Principales tecnologías utilizadas**  
<p align="center">

<img src="https://anderfernandez.com/wp-content/uploads/2021/01/Como-programar-arbol-de-decision-en-Python.jpg"  height=400>
</p>

- Python 🐍  
Es un lenguaje de programación ampliamente utilizado en las aplicaciones web, el desarrollo de software, la ciencia de datos y el machine learning (ML).  
https://docs.python.org/3/  
  - Scikit-learn 🤖  
    Es una biblioteca de aprendizaje automático de software gratuito para el lenguaje de programación Python. https://scikit-learn.org/stable/  
  - Pandas 🐼 
  Es una librería de Python especializada en la manipulación y el análisis de datos. Ofrece estructuras de datos y operaciones para manipular tablas numéricas y series temporales, es como el Excel de Python. https://pandas.pydata.org/docs/  
  - Numpy 🧮  
  NumPy es una biblioteca para el lenguaje de programación Python que da soporte para crear vectores y matrices grandes multidimensionales, junto con una gran colección de funciones matemáticas de alto nivel para operar con ellas. https://numpy.org/doc/  
  - Matplotlib 📈   
  Es una biblioteca para la generación de gráficos en dos dimensiones, a partir de datos contenidos en listas o arrays en el lenguaje de programación Python.
  https://matplotlib.org/stable/index.html  
  - Seaborn 📊  
  Es una librería de visualización de datos para Python desarrollada sobre matplotlib . https://seaborn.pydata.org/  
  - Scipy 🔬  
  Es una biblioteca libre y de código abierto para Python. Se compone de herramientas y algoritmos matemáticos. https://docs.scipy.org/doc/scipy/  
  - Pipeline ♻  
  La clase Pipeline de Scikit-learn está diseñada como una forma manejable de aplicar una serie de transformaciones de datos seguidas por la aplicación de un estimador 
  https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html  
  
  <hr>  
  
  ## **4-Plan de Acción** 
  
  
<p align="center">
<img src="https://cdn.discordapp.com/attachments/1027950645577261117/1051530466097893427/image.png"  height=200>
</p>
  
   
 Un breve resumen de lo que se comenta en el notebook es que se llevó a cabo un análisis exploratorio de los datos (EDA), en el que se verificaron los valores nulos y duplicados, y se controló la correlación entre las variables mediante la prueba chi2_contingency. Luego, se normalizaron los datos utilizando OneHotEncoder y LabelEncoder.  
 
 Se entrenaron los modelos X e Y, obteniendo mejores resultados con un random_state=32. Se utilizó un Pipeline para comparar el rendimiento de decisiontreeclassifier y regresión logística, y se seleccionó decisiontreeclassifier como el mejor modelo.  
 
 Posteriormente, se utilizó grid search para ajustar los parámetros del modelo y mejorar su rendimiento una vez en producción. Finalmente, se implementó el modelo entrenado para predecir el conjunto de datos "csv test" y se generó un archivo csv con los resultados, que se subió con el nombre "MaxiDS".  
 
  <hr>  
  
   ## **5-Observaciones**  
   
   Se aplicó LabelEncoder en lugar de OneHotEncoder a las columnas "Age" y "Severity of Illness" porque esto mejoró la precisión del modelo. Se decidió no eliminar la columna "Admission_Deposit" después de realizar pruebas ya que esto también mejoró el rendimiento del modelo.  
   
   Cuando se definen X_train e Y_train, se obtienen mejores resultados con un random_state=32. El uso de grid search nos permitió encontrar los siguientes parámetros óptimos para mejorar nuestro árbol de decisión: 'criterion': 'gini', 'max_depth': 19, 'random_state': 32, 'splitter': 'best'.  
   
   Finalmente, nuestro modelo en producción tuvo un rendimiento de Recall del 81,16% y Accuracy del 77,07% cuando se utilizó "csv test" como conjunto de datos de prueba.  
   
   <hr>
   
   ## **6-Conclusiones**  
   
   Este trabajo me permitió ampliar mis conocimientos en programación y en el uso de librerías de machine learning como Sklearn y Scipy. Aprendí a mejorar el rendimiento de un modelo utilizando grid search y a profundizar en el uso de árboles de decisión. Me siento muy satisfecho de haber cumplido con los objetivos propuestos y de haber ampliado mis conocimientos en esta área.  
   <hr>
   
<p align="center">
<img src="https://miro.medium.com/max/1120/1*oZjtmox-nEmcnW1NV5GVbw.gif"  height=200>
</p>
   
   ¡Muchas gracias por leer mi trabajo!😁 Me alegra haber sido de tu interés.  
   Te comparto mi linkedin para que podamos conectarnos y seguir en contacto: https://www.linkedin.com/in/maxi-seidl/  
   ¡Hasta pronto!👋
   
