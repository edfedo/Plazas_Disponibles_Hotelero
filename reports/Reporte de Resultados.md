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



