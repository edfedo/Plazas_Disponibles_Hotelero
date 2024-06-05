

![Ushuaia_TIerra_Del_Fuego](https://github.com/edfedo/Plazas_Disponibles_Hotelero/blob/main/reports/figures/Front.png)

<p align="left">
    <a href="https://www.lonelyplanet.com/argentina/tierra-del-fuego/ushuaia">
    <img src="https://img.shields.io/badge/copyright_photo-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white" alt="copyright photo" />
  </a>
</p>

**Degree:** Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial.

**Institution:** Politécnico Malvinas Argentinas.  https://politecnico.tdf.gob.ar/

**Subject:** Aprendizaje Automático / Machine Learning

**Year:** 2024

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=edfedo" alt="Vistas de perfil" />
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT" />
  </a>
</p>

------------

**cookiecutter.project:** Plazas Disponibles Hotelero / Available Places Hotelier

**Developed by:** Federico D'Oliveira

------------

**cookiecutter.description:**

| Español       | English       |
| ------------- | ------------- |
| El objetivo principal de este proyecto es aplicar técnicas de Aprendizaje Automático para analizar y predecir la oferta hotelera y parahotelera en Ushuaia, utilizando datos históricos de establecimientos, plazas disponibles y habitaciones/unidades disponibles. Este análisis busca proporcionar insights valiosos para los interesados en la industria del turismo, permitiendo una mejor planificación y toma de decisiones.  | The main objective of this project is to apply Machine Learning techniques to analyze and predict the hotel and parahotel offer in Ushuaia, using historical data on establishments, available places and available rooms/units. This analysis seeks to provide valuable insights for those interested in the tourism industry, allowing for better planning and decision making.|

------------

**DataSet:** 

| Español       | English       |
| ------------- | ------------- |
| El mismo fue obtenido desde la web del Instituto Provincial de Analisis E Investigacion, Estadistica y Censos | It was obtained from the website of the Provincial Institute of Analysis and Research, Statistics and Censuses.|

<p align="left">
    <a href="https://ipiec.tierradelfuego.gob.ar">
    <img src="https://img.shields.io/badge/Link_WEB_IPIEC-FFA500?style=for-the-badge&logo=Google-chrome&logoColor=white" alt="Link WEB IPIEC" />
  </a>
</p>

<p align="left">
    <a href="https://ipiec.tierradelfuego.gob.ar/estadisticas-economicas-2/">
    <img src="https://img.shields.io/badge/Link_WEB_IPIEC_DATASET-4285F4?style=for-the-badge&logo=Google-chrome&logoColor=white" alt="Link WEB IPIEC DATASET" />
  </a>
</p>

------------

[-] **Preguntas de Investigacion del Proyecto:**


| Español       | English       |
| ------------- | ------------- |
| ¿Cuáles son los patrones estacionales en la oferta de plazas disponibles en el sector hotelero y parahotelero de Ushuaia?
Propósito: Identificar los períodos de alta y baja demanda para optimizar la gestión de recursos y la planificación estratégica.
¿Qué variables (por ejemplo, número de establecimientos, habitaciones disponibles) influyen más significativamente en la disponibilidad de plazas en ambos sectores?
Propósito: Determinar los factores clave que afectan la disponibilidad de plazas para mejorar las predicciones y la gestión de la oferta.
¿Es posible predecir la cantidad de plazas disponibles en el sector hotelero y parahotelero para futuros períodos utilizando modelos de aprendizaje automático?
Propósito: Desarrollar un modelo predictivo que ayude a anticipar la demanda y ajustar la oferta de manera proactiva.
¿Cómo varía la precisión de las predicciones al usar diferentes técnicas de aprendizaje automático?
Propósito: Comparar el rendimiento de varios modelos de aprendizaje automático para seleccionar el más adecuado.
¿Cuál es el impacto de eventos específicos (por ejemplo, ferias, festivales, condiciones climáticas) en la oferta y demanda de plazas?
Propósito: Analizar cómo eventos específicos afectan la disponibilidad de plazas y ajustar las estrategias de planificación en consecuencia. | What are the seasonal patterns in the supply of available places in the hotel and parahotel sector of Ushuaia? Purpose: Identify periods of high and low demand to optimize resource management and strategic planning.
What variables (for example, number of establishments, available rooms) most significantly influence the availability of places in both sectors?
Purpose: Determine key factors affecting seat availability to improve predictions and supply management.
Is it possible to predict the number of beds available in the hotel and para-hotel sector for future periods using machine learning models?
Purpose: Develop a predictive model that helps anticipate demand and proactively adjust supply.
How does prediction accuracy vary when using different machine learning techniques?
Purpose: Compare the performance of various machine learning models to select the most suitable one.
What is the impact of specific events (e.g. fairs, festivals, weather conditions) on the supply and demand of places?
Purpose: Analyze how specific events affect seat availability and adjust planning strategies accordingly.|













¿Cuáles son los patrones estacionales en la oferta de plazas disponibles en el sector hotelero y parahotelero de Ushuaia?

Propósito: Identificar los períodos de alta y baja demanda para optimizar la gestión de recursos y la planificación estratégica.

¿Qué variables (por ejemplo, número de establecimientos, habitaciones disponibles) influyen más significativamente en la disponibilidad de plazas en ambos sectores?

Propósito: Determinar los factores clave que afectan la disponibilidad de plazas para mejorar las predicciones y la gestión de la oferta.

¿Es posible predecir la cantidad de plazas disponibles en el sector hotelero y parahotelero para futuros períodos utilizando modelos de aprendizaje automático?

Propósito: Desarrollar un modelo predictivo que ayude a anticipar la demanda y ajustar la oferta de manera proactiva.

¿Cómo varía la precisión de las predicciones al usar diferentes técnicas de aprendizaje automático?

Propósito: Comparar el rendimiento de varios modelos de aprendizaje automático para seleccionar el más adecuado.

¿Cuál es el impacto de eventos específicos (por ejemplo, ferias, festivales, condiciones climáticas) en la oferta y demanda de plazas?

Propósito: Analizar cómo eventos específicos afectan la disponibilidad de plazas y ajustar las estrategias de planificación en consecuencia.

------------

[-] **Diferentes Etapas del Proyecto:**

[-] **Metodología Extracción y Preparación de Datos**

**Extracción de Datos:** Los datos se extrajeron de un archivo y se convirtieron a un DataFrame de pandas.

**Preprocesamiento:** Incluye la conversión de la columna Periodo a un formato de fecha, manejo de valores nulos y escalamiento de los datos si es necesario.
Análisis Exploratorio de Datos (EDA)

**Visualización de Datos:** Utilización de gráficos para entender la distribución de las variables.

**Estadísticas Descriptivas:** Cálculo de medias, medianas, desviaciones estándar y otras estadísticas relevantes.

**Correlación:** Análisis de la correlación entre las diferentes variables para identificar relaciones importantes. 

[-] **Modelado Predictivo**

**Selección de Modelos:** Elección de modelos de aprendizaje automático adecuados, como regresión lineal, árboles de decisión o redes neuronales.

**Entrenamiento de Modelos:** Dividir los datos en conjuntos de entrenamiento y prueba, y entrenar los modelos utilizando el conjunto de entrenamiento.

**Evaluación de Modelos:** Medir el rendimiento de los modelos utilizando métricas apropiadas como MAE, MSE, RMSE o R2.

[-] **Optimización y Validación**

**Optimización de Hiperparámetros:** Ajuste de los hiperparámetros del modelo para mejorar su rendimiento.

**Validación Cruzada:** Uso de técnicas de validación cruzada para asegurar que el modelo generaliza bien a datos no vistos.

[-] **Interpretación y Comunicación de Resultados**

**Interpretación de Resultados:** Análisis de los resultados obtenidos para extraer conclusiones significativas.

**Visualización de Resultados:** Presentación de los resultados a través de gráficos y visualizaciones claras y comprensibles.

**Informe Final:** Elaboración de un informe detallado que resuma los hallazgos y las recomendaciones basadas en el análisis.

[-] **Resultados Esperados**

**Patrones de Temporada:** Identificación de patrones estacionales en la oferta hotelera y parahotelera.

**Predicciones de Oferta:** Modelos predictivos que puedan estimar la disponibilidad futura de plazas y habitaciones.

------------

**Languages ​​and Tools**

<div id="header" align="left">
<img src="https://img.shields.io/badge/Cookiecutter-D4AA00?style=for-the-badge&logo=Cookiecutter&logoColor=white" />
</a>
<img src="https://img.shields.io/badge/conda-342B029.svg?&style=for-the-badge&logo=anaconda&logoColor=white" />
</a>
<img src="https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white" />
</a>
<img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" />
</a>
<img src="https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white" />
</a>
<img src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue" />
</a>  
<img src="https://img.shields.io/badge/DataSet-05192D?style=for-the-badge&logo=datacamp&logoColor=65FF8F" />
</a> 
<img src="https://img.shields.io/badge/Microsoft_Excel_CSV-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white" />
</a> 
<img src="https://img.shields.io/badge/machine learning-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" />
</a>
<img src="https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white" />
</a> 
</div>

------------

<p align="left">
    <a href="https://github.com/alexandresanlim/Badges4-README.md-Profile#-contact-">
    <img src="https://img.shields.io/badge/Badges_4_README_Profile-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white" alt="Badges 4 README Profile" />
  </a>
</p>

------------

Project Organization

------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
