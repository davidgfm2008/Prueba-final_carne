# Prueba_final_carne


Proyecto de entrenamiento de un clasificador de la Carne usando redes neuronales convolucional

![image](https://github.com/davidgfm2008/Prueba-final_carne/assets/96543442/493d5405-6d22-44d0-aeb3-a7d4358ccf02)


#Link de acceso de los datos

https://drive.google.com/file/d/1Z5DJ-MVS1TQV1kow9mIFWTec-ZdOLRLF/view?usp=sharing

Se encuentran dos archivos un test y un train

![image](https://github.com/davidgfm2008/Prueba-final_carne/assets/96543442/82419c77-1e30-4fd0-b645-9ee4c5fc9aaf)


# Objetivo 

Crear una matrix de confusión del modelo, la matriz de confusión del error en training y la de
test.

# Librerias utilizadas 
import numpy as np
import os
import re
import matplotlib.pyplot as plt
%matplotlib inline
from sklearn import metrics
from sklearn.model_selection import train_test_split
from sklearn.metrics import classification_report
from sklearn.metrics import ConfusionMatrixDisplay
import tensorflow
from tensorflow.keras.utils import to_categorical
from tensorflow.keras import Sequential,Input,Model
from tensorflow.keras.layers import Dense, Dropout, Flatten
from tensorflow.keras.layers import Convolution2D, MaxPooling2D,BatchNormalization,LeakyReLU

# Instalación de librerias faltantes

Para la insalación de librerias faltantes y abrir ancanda Powershell ingresar los siguientes comandos

pip install tensorflow
code install -c conda-forge keras

# Directorio 

cuando se vaya a cargar las imagenes se debe validar que directorio esta y hacer la carga 

imgpath = os.path.join(os.getcwd(), 'Aqui va el directorio')

# Creación de un set de entrenamiento

El codigo  train_test_split se utiliza para dividir el conjunto de datos y nos ayuda a clasificar 0.2 hace referencia que se utilizará el 20% de los datos para pruebas y el 80% restante se usará para entrenamiento.

# Creamos la red 

Para la creación de la red neuronal usamos Keras

![image](https://github.com/davidgfm2008/Prueba-final_carne/assets/96543442/f0e7f310-41b6-4031-8e44-d0f14f0cc25a)

# Entrenamos la CNN

Con la siguiente linea sport_model.fit()  iniciaremos el entrenamiento de las imagenes

# Evaluación del modelo

En la evaluación del modelo se puede ver que se alcanzo un 90% de reconocimiento de imagenes 

![image](https://github.com/davidgfm2008/Prueba-final_carne/assets/96543442/cbde1d84-b786-49fd-864a-7dec7e3951c7)


# Referencia 
https://www.aprendemachinelearning.com/clasificacion-de-imagenes-en-python/
