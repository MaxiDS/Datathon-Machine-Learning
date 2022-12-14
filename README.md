# <h1 align=center>**`Datathon - Machine Learning`**</h1>
# <h3 align=center> **Proyecto de clasificacion con ML** </h3>
<p align="center">
<img src="https://www.nephrocare.com.ar/fileadmin/user_upload/assets/images/master/professionals/Careers/NC_Team/NC_team_iStock-1045200338.png"  height=400>
</p>

<hr>

## **TABLA DE CONTENIDO**  
+ 1-Introducci贸n.  
+ 2-Objetivo de trabajo.  
+ 3-Principales tecnolog铆as utilizadas.  
+ 4-Plan de Acci贸n. 
+ 5-Observaciones.   
+ 6-Conclusiones.  

<hr>  

## **1-Introducci贸n**  

Hola! 馃憢 mi nombre es Lucas Maximiliano Seidl y este repositorio contiene mi proyecto individual para el "Datathon - Machine Learning" de la carrera de Data Science en la academia Henry.  
En este trabajo cree un modelo que puede predecir, a partir de ciertos datos, si un paciente va a permanecer en el hospital durante m谩s o menos de 8 d铆as.

<hr>

## **2-Objetivo de trabajo**  

Un importante Centro de Salud lo ha contratado con el fin de poder predecir si un paciente tendr谩 una estancia hospitalaria prolongada o no. Para ello tenemos dos archivos csv, uno "train" con el cual vamos a entrenar nuestro modelo de ML y "test" en el cual vamos a aplicar el modelo realizado y conseguir las predicciones.  

+ An谩lisis exploratorio de los datos (EDA).

+ Divisi贸n de dataset en train y test utilizando train_test_split, CV, KFold o similares.

+ Entrenamiento y predicci贸n utilizando un Modelo de Machine Learning adecuado al problema (clasificaci贸n o regresi贸n).

+ Utilizaci贸n de Pipelines en la producci贸n del modelo.

+ Comentarios y redacci贸n con la fundamentaci贸n de la soluci贸n propuesta, escrita en Markdown en el Jupyter Notebook (.ipynb) o bien en un documento aparte.

<hr>  

## **3-Principales tecnolog铆as utilizadas**  
<p align="center">

<img src="https://anderfernandez.com/wp-content/uploads/2021/01/Como-programar-arbol-de-decision-en-Python.jpg"  height=400>
</p>

- Python 馃悕  
Es un lenguaje de programaci贸n ampliamente utilizado en las aplicaciones web, el desarrollo de software, la ciencia de datos y el machine learning (ML).  
https://docs.python.org/3/  
  - Sklearn 馃  
    Es una biblioteca de aprendizaje autom谩tico de software gratuito para el lenguaje de programaci贸n Python. https://scikit-learn.org/stable/  
  - Pandas 馃惣 
  Es una librer铆a de Python especializada en la manipulaci贸n y el an谩lisis de datos. Ofrece estructuras de datos y operaciones para manipular tablas num茅ricas y series temporales, es como el Excel de Python. https://pandas.pydata.org/docs/  
  - Numpy 馃М  
  NumPy es una biblioteca para el lenguaje de programaci贸n Python que da soporte para crear vectores y matrices grandes multidimensionales, junto con una gran colecci贸n de funciones matem谩ticas de alto nivel para operar con ellas. https://numpy.org/doc/  
  - Matplotlib 馃搱   
  Es una biblioteca para la generaci贸n de gr谩ficos en dos dimensiones, a partir de datos contenidos en listas o arrays en el lenguaje de programaci贸n Python.
  https://matplotlib.org/stable/index.html  
  - Seaborn 馃搳  
  Es una librer铆a de visualizaci贸n de datos para Python desarrollada sobre matplotlib . https://seaborn.pydata.org/  
  - Scipy 馃敩  
  Es una biblioteca libre y de c贸digo abierto para Python. Se compone de herramientas y algoritmos matem谩ticos. https://docs.scipy.org/doc/scipy/  
  - Pipeline 鈾?  
  La clase Pipeline de Scikit-learn est谩 dise帽ada como una forma manejable de aplicar una serie de transformaciones de datos seguidas por la aplicaci贸n de un estimador 
  https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html  
  
  <hr>  
  
  ## **4-Plan de Acci贸n** 
  
  
<p align="center">
<img src="https://cdn.discordapp.com/attachments/1027950645577261117/1051530466097893427/image.png"  height=200>
</p>
  
   
 Un breve resumen de lo que se comenta en el notebook es que se llev贸 a cabo un an谩lisis exploratorio de los datos (EDA), en el que se verificaron los valores nulos y duplicados, y se control贸 la correlaci贸n entre las variables mediante la prueba chi2_contingency. Luego, se normalizaron los datos utilizando OneHotEncoder y LabelEncoder.  
 
 Se entrenaron los modelos X e Y, obteniendo mejores resultados con un random_state=32. Se utiliz贸 un Pipeline para comparar el rendimiento de decisiontreeclassifier y regresi贸n log铆stica, y se seleccion贸 decisiontreeclassifier como el mejor modelo.  
 
 Posteriormente, se utiliz贸 grid search para ajustar los par谩metros del modelo y mejorar su rendimiento una vez en producci贸n. Finalmente, se implement贸 el modelo entrenado para predecir el conjunto de datos "csv test" y se gener贸 un archivo csv con los resultados, que se subi贸 con el nombre "MaxiDS".  
 
  <hr>  
  
   ## **5-Observaciones**  
   
   Se aplic贸 LabelEncoder en lugar de OneHotEncoder a las columnas "Age" y "Severity of Illness" porque esto mejor贸 la precisi贸n del modelo. Se decidi贸 no eliminar la columna "Admission_Deposit" despu茅s de realizar pruebas ya que esto tambi茅n mejor贸 el rendimiento del modelo.  
   
   Cuando se definen X_train e Y_train, se obtienen mejores resultados con un random_state=32. El uso de grid search nos permiti贸 encontrar los siguientes par谩metros 贸ptimos para mejorar nuestro 谩rbol de decisi贸n: 'criterion': 'gini', 'max_depth': 19, 'random_state': 32, 'splitter': 'best'.  
   
   Finalmente, nuestro modelo en producci贸n tuvo un rendimiento de Recall del 81,16% y Accuracy del 77,07% cuando se utiliz贸 "csv test" como conjunto de datos de prueba.  
   
   <hr>
   
   ## **6-Conclusiones**  
   
   Este trabajo me permiti贸 ampliar mis conocimientos en programaci贸n y en el uso de librer铆as de machine learning como Sklearn y Scipy. Aprend铆 a mejorar el rendimiento de un modelo utilizando grid search y a profundizar en el uso de 谩rboles de decisi贸n. Me siento muy satisfecho de haber cumplido con los objetivos propuestos y de haber ampliado mis conocimientos en esta 谩rea.  
   <hr>
   
<p align="center">
<img src="https://miro.medium.com/max/1120/1*oZjtmox-nEmcnW1NV5GVbw.gif"  height=200>
</p>
   
   隆Muchas gracias por leer mi trabajo!馃榿 Me alegra haber sido de tu inter茅s.  
   Te comparto mi linkedin para que podamos conectarnos y seguir en contacto: https://www.linkedin.com/in/maxi-seidl/  
   隆Hasta pronto!馃憢
   
