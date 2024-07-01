## Reporte de Resultados Plazas Disponibles Hotelero Ushuaia
### Análisis Exploratorio de Datos

**Selecciona las características (columnas) Establecimientos, Habitaciones o Unidades disponibles y EsFestivo, y la variable objetivo Plazas disponibles:**

**Dentro de la exploración de los datos se encontraron los siguientes patrones de interés:**

[-] Cuadro de Tendencias temporales

[-] Tendencia General:

- Se observa una tendencia general decreciente en el número de plazas disponibles desde 2008 hasta aproximadamente 2016.
- A partir de 2016, hay una ligera recuperación que se ve interrumpida abruptamente en 2020, lo cual es probable que se deba a la pandemia de COVID-19.
- Posteriormente, hay una recuperación marcada a partir de 2021, alcanzando niveles más altos hacia 2024.

[-] Variabilidad:

- La banda sombreada alrededor de la línea de tendencia representa la variabilidad o el rango de las plazas disponibles en los distintos meses de cada año.
- La variabilidad parece ser más alta en los años más recientes (2020 en adelante), lo cual puede indicar fluctuaciones significativas en el número de plazas disponibles probablemente debido a la recuperación y ajustes post-pandemia.

[-] Impacto de la Pandemia (2020):

- Claramente, 2020 muestra un impacto significativo con una caída drástica en las plazas disponibles, reflejando las restricciones y cierres asociados a la pandemia de COVID-19.
- La recuperación empieza en 2021 y continúa en los años siguientes, pero con una alta variabilidad, sugiriendo una reactivación gradual y posiblemente desigual entre los distintos meses y lugares.

[-] Otros

- Las variables de EsFestivo no parecen afectar mucho dentro del modelo.


### Modelos de Clasificación

#### Random Forest 

[-] Random Forest

- Accuracy: 0.9867
- Precision: 1.0000
- Recall: 0.9744
- F1 Score: 0.9870

Análisis: El modelo Random Forest muestra una excelente precisión, con una precisión y F1 score casi perfectos. La alta precisión y F1 score indican que el modelo es muy bueno tanto en predecir correctamente las plazas altas como en minimizar los falsos positivos. Sin embargo, el recall ligeramente inferior a la precisión sugiere que podría haber una pequeña cantidad de falsos negativos.


[-] Interpretación General:

- El modelo de Random Forest mostró un buen rendimiento en términos de las métricas calculadas (accuracy, precision, recall, f1 score). Sin embargo, la interpretación de estas métricas depende de los valores específicos obtenidos.
Si las métricas son altas, el modelo puede ser considerado confiable para predecir 'Plazas altas'. Si son bajas, podría necesitar mejoras o una revisión de las características utilizadas.


**Conclusiones Finales**

1. Random Forest

- Accuracy: 0.9867
- Precision: 1.0000
- Recall: 0.9744
- F1 Score: 0.9870

Análisis: El modelo Random Forest muestra una excelente precisión, con una precisión y F1 score casi perfectos. La alta precisión y F1 score indican que el modelo es muy bueno tanto en predecir correctamente las plazas altas como en minimizar los falsos positivos. Sin embargo, el recall ligeramente inferior a la precisión sugiere que podría haber una pequeña cantidad de falsos negativos.


2. Logistic Regression

- Accuracy: 0.9600
- Precision: 0.9737
- Recall: 0.9487
- F1 Score: 0.9610

Análisis: La regresión logística también muestra un rendimiento sólido, aunque inferior al de Random Forest. La precisión y el recall son altos, lo que significa que el modelo es bastante equilibrado en términos de predecir correctamente las clases positivas y minimizar tanto los falsos positivos como los falsos negativos. Sin embargo, sus métricas son un poco más bajas que las de Random Forest, lo que indica que puede no ser tan efectivo en este contexto específico.

3. Support Vector Classifier (SVC)

- Accuracy: 0.9733
- Precision: 1.0000
- Recall: 0.9487
- F1 Score: 0.9737

Análisis: El SVC muestra una precisión perfecta pero un recall un poco menor, similar al Random Forest, pero con un F1 score ligeramente inferior. Esto sugiere que el SVC es muy bueno para minimizar los falsos positivos pero puede pasar por alto algunos casos positivos (plazas altas). Aun así, su rendimiento es robusto y competitivo.

4. Decision Tree

- Accuracy: 0.9467
- Precision: 0.9268
- Recall: 0.9744
- F1 Score: 0.9500

Análisis: El modelo Decision Tree tiene la menor precisión de los cuatro modelos, pero aún muestra un buen rendimiento. Tiene un buen recall, lo que sugiere que es bueno para identificar la mayoría de los casos positivos, pero su precisión más baja indica que tiene más falsos positivos en comparación con otros modelos. Su F1 score, aunque bueno, es inferior al de los otros modelos, lo que sugiere que podría no ser la mejor opción para este conjunto de datos específico.



- Random Forest es el modelo con el mejor rendimiento general, mostrando una precisión y F1 score casi perfectos. Es altamente recomendado para este conjunto de datos.
- Support Vector Classifier también muestra un rendimiento fuerte, especialmente en términos de precisión, aunque su recall es un poco más bajo que el de Random Forest.
- Logistic Regression ofrece un buen equilibrio entre precisión y recall, siendo una opción robusta aunque ligeramente inferior a los dos modelos anteriores.
- Decision Tree muestra el rendimiento más bajo entre los cuatro modelos, aunque aún es efectivo en términos de recall. Puede ser una opción válida pero con un rendimiento inferior comparado con los otros modelos.

**Para la tarea de predecir 'Plazas altas', el modelo Random Forest es la mejor opción, seguido de cerca por el SVC y la regresión logística. La elección final del modelo puede depender de la preferencia entre minimizar falsos positivos o falsos negativos, y la interpretación de los resultados en el contexto del negocio o investigación.**

--------------
--------------

[-]**Preguntas a Responder del proyecto:**

Se responderan cada una de las preguntas de investigacion del proyecto con base en el analisis realizado y los resultados obtenidos:

**1. ¿Cuáles son los patrones estacionales en la oferta de plazas disponibles en el sector hotelero y parahotelero de Ushuaia?**

Propósito: Identificar los períodos de alta y baja demanda para optimizar la gestión de recursos y la planificación estratégica.

Respuesta: Al analizar las gráficas de series temporales y la disponibilidad de plazas a lo largo del tiempo, observamos que hay fluctuaciones estacionales claras en la oferta de plazas disponibles. Por ejemplo, durante los meses de verano (diciembre a febrero), hay un aumento notable en la disponibilidad de plazas, lo cual sugiere una alta demanda turística en estos períodos. En contraste, los meses de invierno (junio a agosto) muestran una menor disponibilidad, indicando una baja demanda.

**2. ¿Qué variables (por ejemplo, número de establecimientos, habitaciones disponibles) influyen más significativamente en la disponibilidad de plazas en ambos sectores?**

Propósito: Determinar los factores clave que afectan la disponibilidad de plazas para mejorar las predicciones y la gestión de la oferta.

Respuesta: De acuerdo con la matriz de correlación, las variables "Establecimientos" y "Habitaciones o Unidades disponibles" muestran una correlación significativa con la variable "Plazas disponibles". Esto indica que estas dos variables son factores clave que influyen en la disponibilidad de plazas en el sector hotelero y parahotelero. Específicamente, un mayor número de establecimientos y habitaciones disponibles tienden a asociarse con una mayor cantidad de plazas disponibles.

**3. ¿Es posible predecir la cantidad de plazas disponibles en el sector hotelero y parahotelero para futuros períodos utilizando modelos de aprendizaje automático?**

Propósito: Desarrollar un modelo predictivo que ayude a anticipar la demanda y ajustar la oferta de manera proactiva.

Respuesta: Sí, es posible predecir la cantidad de plazas disponibles utilizando modelos de aprendizaje automático. En nuestro análisis, entrenamos un modelo de Random Forest que mostró un alto desempeño en términos de precisión, sensibilidad y puntaje F1, con una exactitud del 97.33%. Esto indica que los modelos de aprendizaje automático pueden ser efectivos para anticipar la demanda y ajustar la oferta de plazas.

**4. ¿Cómo varía la precisión de las predicciones al usar diferentes técnicas de aprendizaje automático?**

Propósito: Comparar el rendimiento de varios modelos de aprendizaje automático para seleccionar el más adecuado.

Respuesta: En este análisis, utilizamos un modelo de Random Forest, que es conocido por su robustez y precisión. Sin embargo, para una comparación completa, se podrían probar otros modelos como Support Vector Machines (SVM), Gradient Boosting, y redes neuronales. Cada modelo tiene sus propias ventajas y limitaciones. Comparar el rendimiento de estos modelos en términos de precisión, sensibilidad, puntaje F1, y otras métricas, permitiría seleccionar el modelo más adecuado para las predicciones de plazas disponibles.

**5. ¿Cuál es el impacto de eventos específicos (por ejemplo, ferias, festivales, condiciones climáticas) en la oferta y demanda de plazas?**

Propósito: Analizar cómo eventos específicos afectan la disponibilidad de plazas y ajustar las estrategias de planificación en consecuencia.

Respuesta: Para responder a esta pregunta, sería necesario incorporar datos adicionales sobre eventos específicos, ferias, festivales y condiciones climáticas en el análisis. Actualmente, no se incluyeron estos datos en el análisis realizado. Sin embargo, es plausible que eventos especiales y condiciones climáticas extremas tengan un impacto significativo en la oferta y demanda de plazas. Incorporar estos datos en futuros modelos de predicción podría mejorar la precisión y proporcionar insights valiosos para la planificación estratégica.

**Conclusión:** Las herramientas y técnicas de análisis de datos y aprendizaje automático ofrecen un gran potencial para entender y predecir la disponibilidad de plazas en el sector hotelero y parahotelero de Ushuaia. Con un análisis más detallado y la inclusión de más variables, como eventos específicos y condiciones climáticas, se puede optimizar aún más la gestión de recursos y la planificación estratégica en este sector.

--------------
--------------
