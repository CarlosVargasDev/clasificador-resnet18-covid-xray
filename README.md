# Clasificador de radiografías de tórax para la detección de Covid

## Descripción
El clasificador de este proyecto fue implementado en el siguiente taller de Coursera: https://www.coursera.org/projects/covid-19-detection-x-ray, con la ayuda de la librería de PyTorch, se usa un modelo pre entrenado, el modelo elegido es la red neuronal convolucional residual resnet18 para la clasificación de imágenes por rayos x en alguna de las siguientes categorías: ["normal", "neumonía viral", "covid"]. El conjunto de datos consta de imágenes .png de radiografías etiquetadas como: "normal", "neumonía viral" y "covid". El conjunto de datos puede ser encontrado en la siguiente liga: https://www.kaggle.com/tawsifurrahman/covid19-radiography-database.

El modelo entrenado alcanza una precisión superior al 95%, aunque es una precisión muy alta se debe de tener en cuenta el tamaño de nuestro conjunto de datos, el conjunto de entrenamiento consta de 2815 imágenes mientras que el conjunto de test consta de 90 imágenes, por lo que este modelo no es lo suficientemente robusto como para ser empleado en un entorno médico real y solo tiene fines didácticos.

## Run
El repositorio contiene dos programas escritos en Python, el código en `covid.py` sirve para entrenar el modelo, mientras que el código en `clasificador.py` sirve para cargar y ejecutar el modelo. El modelo entrenado se encuentra dentro de la carpeta `resnet/`

#### Requisitos Previos
1. Tener instalado Python.
2. Tener instalado PyTorch y torchvision, el comando para instalarlo mediante anaconda es el siguiente: `conda install pytorch torchvision cudatoolkit=10.2 -c pytorch`;

- **Nota Extra**: En caso de ejecutar el programa `clasificador.py` es necesario crear una carpeta llamada `resnet_uploads/` y guardar aqui las imagenes a clasificar en formato png.

#### Entrenamiento
1. Clona este repositorio.
2. Descarga el conjunto de datos: https://www.kaggle.com/tawsifurrahman/covid19-radiography-database y guárdala en la carpeta del repositorio.
3. Renombra la carpeta a Radiography
4. Ejecuta el archivo Python `covid.py`.

- Nota Extra: En caso de entrenar el modelo, este sobrescribirá al modelo guardado de la carpeta `resnet/`

**Capturas del Entrenamiento**:
![entrenando Modelo](https://i.postimg.cc/FRZFX2L0/imagen1.png)
![modelo entrenado](https://i.postimg.cc/qB1BbH0T/imagen2.png)
![img consola](https://i.postimg.cc/851D4t0c/imagen-Output.png)


#### Ejecutar Clasificador
Las imágenes que el clasificador usara se deben de guardar en una carpeta llamada `resnet_uploads/` y deben de estar en formato .png
1. Clona este repositorio.
2. Ejecuta el archivo Python `clasificador.py`.

**Capturas de la ejecucion**:
![img test](https://i.postimg.cc/TwM8NQNg/imagen-Tests.png)


#### API

Proximamente ...