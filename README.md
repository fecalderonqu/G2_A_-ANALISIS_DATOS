## 1. Descripción del propósito del dataset
**🌍 World Happiness Report – Análisis de Datos**

El World Happiness Report es un conjunto de datos elaborado a partir de encuestas globales y estadísticas socioeconómicas recopiladas por la ONU y otras instituciones internacionales.
Su propósito es medir y comparar el nivel de felicidad y bienestar en diferentes países a lo largo del tiempo.

El índice de felicidad **(Happiness_score)** se construye en base a factores que influyen en la percepción de calidad de vida, entre ellos:

- PIB per cápita **(gdp_per_capita)** → refleja la riqueza económica.

- Apoyo social **(social_support)** → mide la red de apoyo disponible en momentos de necesidad.

- Esperanza de vida saludable **(life_expectancy)** → refleja la salud pública y calidad del sistema sanitario.

- Libertad para tomar decisiones **(freedom)** → percepción de autonomía individual.

- Generosidad **(generosity)** → disposición a donar y ayudar a otros.

- Percepción de corrupción **(corruption)** → mide la confianza en instituciones y gobierno.

**En resumen:
Este dataset busca responder a la pregunta:**

👉 *¿Qué factores determinan la felicidad de los países y cómo varía a lo largo del tiempo y las regiones del mundo?*

# 2. Explicación de los pasos de limpieza y transformación

El dataset original provenía de diferentes archivos anuales del World Happiness Report. Cada archivo contenía columnas con nombres distintos y en algunos casos con valores nulos o inconsistentes.

### Pasos realizados:

- Descarga de los archivos
  
  Se realiza la descarga desde Kaggle de manera manual y se coloco en el repositorio.
  
- Unificación de archivos
  
  Se combinaron los reportes de distintos años (2015–2019) en un solo dataset.

  Se añadió una nueva columna **`Year`** para identificar el año de cada registro.

- Selección y estandarización de columnas

  Se cambia los nombres de columnas para mantener consistencia:
  
  `Country or region` → **`country`**
  
  `Score` → **`Happiness_score`**

  `GDP per capita` → **`gdp_per_capita`**

  `Healthy life expectancy` → **`life_expectancy`**

  `Freedom to make life choices` → **`freedom`**

  `Perceptions of corruption` → **`corruption`**
  y asi sucesivamente
  
- Tratamiento de valores nulos

  Se detectaron valores faltantes en algunas columnas socioeconómicas.

- Eliminación de duplicados

  Se revisaron filas repetidas entre diferentes fuentes y se eliminaron duplicados exactos.

- Guardado de dataset limpio

  El dataset final se almacenó en la variable **`df`**

### ✅ Resultado

Un dataset consolidado con las siguientes columnas finales:

`['country', 'happiness_score', 'gdp_per_capita', 'social_support', 'life_expectancy', 'freedom', 'generosity', 'corruption', 'year']` 


### Herramientas utilizadas  

- **Python**  
- **Librerías principales**:  
  - `pandas`, `numpy` → limpieza y manipulación de datos.  
  - `matplotlib`, `seaborn`, `plotly` → visualizaciones de los datos.  
  - `folium` → mapa interactivo.  
  - `scikit-learn` → Machine Learning.  


## 3. Principales hallazgos del análisis

## 4. Cualquier insight o conclusión relevante  