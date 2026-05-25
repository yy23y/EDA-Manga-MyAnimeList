# Análisis Exploratorio de Datos (EDA) - Manga Dataset MyAnimeList

## Objetivo del trabajo
El objetivo de este proyecto es realizar un Análisis Exploratorio de Datos (EDA) completo sobre un dataset de la plataforma MyAnimeList, aplicando técnicas de limpieza, tratamiento de datos y visualización para responder un conjunto de hipótesis definidas.

## Contexto del dataset
El dataset utilizado recopila información de más de 80.000 mangas registrados en MyAnimeList. Contiene métricas de interacción de la comunidad (puntajes, favoritos, miembros) y características editoriales (volúmenes, capítulos, autores, demografía).
Link de descarga oficial: https://www.kaggle.com/datasets/patelris/anime-and-manga-dataset-2026/data

## Hipótesis planteadas
1. **Relación Extensión-Calidad:** ¿Existe una correlación directa entre la cantidad de capítulos de un manga y su puntaje final (score)?
2. **Centralización de Popularidad:** ¿Las obras con mayor cantidad de miembros en la comunidad son inevitablemente las que acumulan más favoritos absolutos?
3. **Análisis Demográfico:** ¿Los mangas orientados al público "Seinen" obtienen, en promedio, un puntaje (score) superior a los orientados al público "Shounen"?
4. **Formato Físico vs. Popularidad:** ¿Existe una relación positiva entre la cantidad de volúmenes físicos publicados y la base de usuarios (members) que siguen la obra?
5. **Retención de Autores Consagrados:** ¿Las obras de mangakas aclamados por la crítica (como Naoki Urasawa o Takehiko Inoue) presentan una proporción de "favoritos por miembro" significativamente mayor que la media general del dataset?

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
A partir del Análisis Exploratorio de Datos (EDA) realizado, se pudieron constatar los siguientes hallazgos que dan respuesta a las hipótesis planteadas:

* **Sobre la Extensión y la Calidad:** No se observa una correlación lineal perfecta entre capítulos y score. Si bien las obras extremadamente largas suelen tener comunidades consolidadas, existe un punto de saturación; muchas obras logran puntajes de excelencia con una cantidad contenida de capítulos y volúmenes, demostrando que alargar la historia no garantiza mejor recepción.
* **Comunidad y Favoritos:** La matriz de correlación confirma una relación directa y muy fuerte entre la cantidad de `members` y `favorites`. La popularidad tracciona fuertemente el fanatismo absoluto.
* **Comportamiento Demográfico:** Al analizar las demografías, los mangas "Seinen" tienden a concentrar puntajes promedio ligeramente más altos que los "Shounen", a pesar de tener, en términos generales, comunidades numéricamente más reducidas. Esto sugiere un público más de nicho pero que califica de manera más favorable.
* **Volúmenes y Tracción:** Se comprobó una tendencia donde los mangas con mayor cantidad de volúmenes físicos impresos coinciden con un alto número de miembros, indicando que el éxito sostenido en ventas físicas es un buen predictor de la popularidad en plataformas digitales.
* **El Peso de los Autores:** Al aislar obras de autores consagrados, se detectó que la tasa de conversión (cuántos miembros terminan marcando la obra como favorita) supera ampliamente la media del dataset, evidenciando un nivel de fidelidad y calidad percibida muy superior al manga promedio.
