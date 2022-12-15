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
  - Sklearn 🤖  
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
  
   
  Un breve resumen de lo que esta comentado en nuestro notebook:  
  
  - Primero se realizo análisis exploratorio de los datos (EDA) en el cual:
    - Se hizo: verificacion de nulos y duplicados.  
    - Se controlo la correlacion de los datos por medio de chi2_contingency la cual es una herramienta estadística que se utiliza para determinar si hay una relación significativa entre dos o más variables cualitativas.    
    - Una vez encontradas las columnas con las que queriamos trabajar se paso a normalizar los datos mediante "OneHotEncoder" y "LabelEncoder".  
  - Se entreno x e y (dando mejores resutados con un random_state=32).
  
  - Usamos un Pipeline que nos diga que modelo nos daba un mejor rendimiento entre decisiontreeclassifier y regresion logistica, dando por resultado el decisiontreeclassifier. 
  
  - En el proceso de entrenamiento del Arbol dio mejores resultados (depth=19) como parametro, luego lo confirme con cross validation, dandome como resultado:
  `Accuracy de 77% y un Recall de 83%.`
  
  - Con nuestro modelo terminado se lo implemento, prediciendo  "csv test" y se genero el csv con los resultados el cual subimos con el nombre "MaxiDS".  
  <hr>  
  
   ## **5-Observaciones**  
   
   - Se aplico "LabelEncoder" y no OneHotEncoder a la columna "Age" y "Severity of Illness" porque dio un mejor rendimiento en accuracy.  
   - Admission_Deposit (despues de testearlo con y sin esta columna se llego a la conclusion que no se va a eliminar ya que mejora el modelo).
   - cuando se definde X_train e Y_train dan mejor resultados con un random_state=32.  
   - El Arbol da mejor rendimiento con un depth= 19. 
   - Nuestro modelo en produccion usando "csv test" como prueba dio los siguientes resultados: `Recall: 80.96%` y `Accuracy: 77.05`
   
   <hr>
   
   ## **6-Conclusiones**  
   
   Este trabajo me abrió un nuevo horizonte en todo lo que es la programación, hasta este punto no había visto tan en profundidad cómo trabajar con modelos de ML. Aprendí a usar librerías como Sklearn, y Scipy, también consolidar mis conocimientos en Arboles de decisiones🌳. Me voy muy contento de haber podido cumplir con los objetivos propuestos.  
   <hr>
   
<p align="center">
<img src="https://miro.medium.com/max/1120/1*oZjtmox-nEmcnW1NV5GVbw.gif"  height=200>
</p>
   
   Gracias por llegar hasta aca 👋😁  
   Te comparto mi linkedin: https://www.linkedin.com/in/maxi-seidl/
   
