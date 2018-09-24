# Practica 1
## [Introducción a los Sistemas Inteligentes 2018-2](https://fagonzalezo.github.io/iis-2018-2/)
### Grupos de máximo 2 estudiantes 

Usando el conjunto de datos wine:

Lo puede descargar [aquí](https://drive.google.com/open?id=0B8POkZpAJ5qQRlFzVUZnMlZVakk).
Puede obtener más información del conjunto [aquí](https://archive.ics.uci.edu/ml/datasets/wine).

El conjunto de datos contiene los ejemplos de 178 vinos. Cada uno identificado por 13 propiedades químicas:
* Alcohol
* Malic_acid
* Ash
* Alcalinity
* Magnesium
* Phenols
* Flavanoids
* Nonflavanoid
* Proanthocyanins
* Color
* Hue
* OD280/OD315
* Proline

A cada vino le fue asignada una clase, que corresponde al tipo de vino $[1, 2, 3]$

Resuelva:
* Cargue el conjunto de datos como un DataFrame de Pandas
* Cargue la clase en un arreglo aparte. Eliminela del DataFrame de Pandas
* Genere un histograma para cada propiedad del conjunto de datos
* Use `scatter_matrix` y visualize todas las posibles combinaciones de características
    * ¿Encuentra algún par de características en el que se observan las clases bien separadas?
* Clasificación usando solo dos características y el esquema Multinomial:
    * Entrene un modelo LogisticRegression para categorizar el tipo de vino usando `Proline` contra `Flavonoids`.
    * Entrene otro modelo LogisticRegression para categorizar el tipo de vino usando `Alcalinity` contra `Malic Acid`.
    * Imprima la región de decisión de cada clasificador.
    * Genere la matriz de confusión de cada clasificador.
    * Reporte el accuracy, el error de clasificación, la precisión macro, el recall macro y el F1 score macro.
    * ¿Cual modelo se desempeña mejor? ¿Por qué?
* Clasificación usando todas las características:
    * Entrene un modelo LogisticRegression usando el esquema "*One vs All*".
    * Entrene un modelo LogisticRegression usando el esquema multinomial.
    * Genere la matriz de confusión de cada clasificador.
    * Reporte el accuracy, el error de clasificación, la precisión por clase, el recall por clase y el F1 score por clase.
    * ¿Cual modelo se desempeña mejor? ¿Por qué? ¿Cual clase es más sencilla para el clasificador?