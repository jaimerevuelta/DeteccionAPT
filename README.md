# Diseño de un sistema de detección de APTs basado en las fases del Cyber Kill Chain

### Trabajo Fin de Grado - Grado en Ingeniería de Tecnologías y Servicios de Telecomunicación

_Jaime Revuelta Santiago_

En este proyecto se diseña un sistema de detección de APT que cuenta con 2 modelos de aprendizaje automático y 1 algoritmo de correlación de tráfico. Uno de los modelos se encarga de la detección de los APT y el segundo modelo se encarga de clasificar las fases de los APT detectados por el modelo anterior. También se desarrolla un algoritmo de correlación de tráfico para identificar qué tráfico pertenece a un mismo APT, basándose en las fases APT que clasifica el modelo de clasificación de fases APT.


## Pre-requisitos

* Google Colaboratory
* Numpy
* Pandas
* Scikit-learn
* Matplotlib
* PyDrive

## Instalación

No se requiere instalar ningún paquete o librería puesto que las máquinas virtuales de Google Colaboratory ya tienen todos las herramientas necesarias instaladas.

## Ejecución

Para llevar a cabo la ejecución de los cuadernos, se deben importar los conjuntos de datos que utilizan los modelos a un Dataframe de Pandas. En nuestro caso se han importado desde Google Drive con la herramienta PyDrive de Python.

## Estructura del repositorio

El repositorio se divide en 4 cuadernos de Jupyter.

* *Modelo_APT.ipynb* - Se desarrolla el modelo de detección de APT, llevándose a cabo sus pruebas y su evaluación
* *Model_Search.ipynb* - Implementa el framework Model Search de Google para la búsqueda de modelos basados en redes neuronales profundas.
* *Modelo_APT_ROC.ipynb* - Se calcula la curva ROC de cada clase y el área bajo la curva ROC para el modelo de detección de APT. Se dibujan todas las curvas en una misma gráfica.


* *Modelo_Fases.ipynb* - Se desarrolla el modelo de clasificación de fases APT y se realizan su evaluación y pruebas correspondientes.
* *Modelo_Fases_ROC.ipynb* - Se calcula la curva ROC de cada clase y el área bajo la curva ROC para el modelo de clasificación de fases APT. Se dibujan todas las curvas en una misma gráfica.
*
*
* *Algoritmo_correlacion.ipynb* - Se implementa un algoritmo de correlación de tráfico y se prueba sobre el conjunto de datos 
