# Análisis Exploratorio de Datos (EDA) - Manga Dataset MyAnimeList

## Objetivo del trabajo
El objetivo de este proyecto es realizar un Análisis Exploratorio de Datos (EDA) completo sobre un dataset de la plataforma MyAnimeList, aplicando técnicas de limpieza, tratamiento de datos y visualización para responder un conjunto de hipótesis definidas.

## Contexto del dataset
El dataset utilizado recopila información de más de 70.000 mangas registrados en MyAnimeList. Contiene métricas de interacción de la comunidad (puntajes, favoritos, miembros) y características editoriales (volúmenes, capítulos, autores, demografía). 

## Diccionario de datos
* `title`: Título de la obra (String).
* `score`: Puntaje promedio otorgado por la comunidad, de 1 a 10 (Float).
* `volumes`: Cantidad de volúmenes físicos publicados (Integer).
* `chapters`: Cantidad de capítulos totales (Integer).
* `members`: Cantidad de usuarios que agregaron la obra a su lista (Integer).
* `favorites`: Cantidad de usuarios que marcaron la obra como favorita (Integer).
* `authors`: Creador/es de la obra (String).
* `demographics`: Público objetivo, ej. Shonen, Seinen (String).

## Metodología aplicada
Se procedió a la importación del dataset utilizando la librería Pandas. Se realizó una limpieza tratando valores nulos y eliminando duplicados. Posteriormente, se analizaron las distribuciones numéricas y la detección de outliers utilizando Seaborn y Matplotlib, culminando con un análisis de correlación para responder las hipótesis planteadas.

## Conclusiones y hallazgos relevantes
(Ver resultados en el archivo .ipynb principal donde se responden las 5 hipótesis de negocio).
