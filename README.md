# Diseño de un sistema de detección de APTs basado en las fases del Cyber Kill Chain

_Jaime Revuelta Santiago_

En este proyecto se diseña un sistema de detección de APT que cuenta con 2 modelos de aprendizaje automático y 1 algoritmo de correlación de tráfico. Uno de los modelos se encarga de la detección de los APT y el segundo modelo se encarga de clasificar las fases de los APT detectados por el modelo anterior. También se desarrolla un algoritmo de correlación de tráfico para identificar qué tráfico pertenece a un mismo APT, basándose en las fases APT que clasifica uno de los modelos.


### Pre-requisitos

* Google Colaboratory
* Numpy
* Pandas
* Scikit-learn
* Matplotlib
* PyDrive

### Instalación

No se requiere instalar ningún paquete o librería puesto que las máquinas virtuales de Google Colaboratory ya tienen todos las herramientas necesarias instaladas.

### Ejecución

Para llevar a cabo la ejecución de los cuadernos, se deben importar los conjuntos de datos que utilizan los modelos a un Dataframe de Pandas. En nuestro caso se han importado desde Google Drive con la herramienta PyDrive de Python.

## Estructura del repositorio

El repositorio se divide en 4 cuadernos de Jupyter.

* *Modelo_APT.ipynb* - se desarrolla el modelo de detección de APT, llevándose a cabo sus pruebas y su evaluación
* *Modelo_APT_ROC-ipynb* - se calcula la curva ROC de cada clase y el área bajo la curva ROC para el modelo de detección de APT. Se dibujan todas las curvas en una misma gráfica.
* *Modelo_Fases.ipynb* - se desarrolla el modelo de clasificación de fases APT y se realizan su evaluación y pruebas correspondientes.
* *Modelo_Fases_ROC.ipynb* - se calcula la curva ROC de cada clase y el área bajo la curva ROC para el modelo de clasificación de fases APT. Se dibujan todas las curvas en una misma gráfica.
* *Algoritmo_correlacion-ipynb* - se implementa un algoritmo de correlación de tráfico y se prueba sobre el conjunto de datos 
