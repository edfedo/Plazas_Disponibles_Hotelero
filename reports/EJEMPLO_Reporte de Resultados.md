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

[-] Mean Squared Error (MSE):

- Valor del MSE: 18,190,372.90
- El MSE mide el promedio de los cuadrados de los errores, es decir, la diferencia entre los valores predichos por el modelo y los valores reales. Un MSE más bajo indica un mejor ajuste del modelo a los datos.
En este caso, un MSE de 18,190,372.90 es relativamente alto en términos absolutos, pero su interpretación depende del rango de los datos de plazas disponibles. Dado que estamos trabajando con valores de plazas disponibles que pueden alcanzar decenas de miles, este valor podría ser razonable.


[-] R² Score:

- Valor del R²: 0.9765
- El R² Score, o coeficiente de determinación, mide la proporción de la varianza en la variable dependiente que es predecible a partir de las variables independientes. Su valor varía entre 0 y 1.
Un R² de 0.9765 indica que el 97.65% de la variación en el número de plazas disponibles puede ser explicada por el modelo. Esto sugiere que el modelo tiene un excelente ajuste a los datos.


[-] Interpretación General:

- Modelo Eficiente:
El alto valor de R² (cercano a 1) sugiere que el modelo es muy eficaz en capturar la variabilidad de los datos y que tiene un buen rendimiento predictivo.

- Posibles Mejoras:
Aunque el MSE es relativamente alto, podría deberse a algunos valores atípicos o variabilidad inherente en los datos de plazas disponibles. Sería útil analizar estos valores atípicos y considerar técnicas de preprocesamiento adicionales o modelos más sofisticados si se requiere mejorar aún más la precisión.

- Validación y Pruebas:
Es importante también validar el modelo con un conjunto de datos de prueba separado (aun no lo hice) para asegurarse de que estos resultados no son específicos del conjunto de datos de entrenamiento.

- Análisis Adicional:
Podría ser útil llevar a cabo un análisis residual para comprobar si hay patrones en los errores que el modelo comete. Esto podría proporcionar información sobre posibles mejoras o ajustes necesarios en el modelo.


**Conclusiones Finales**

- El modelo parece ser muy eficaz con un R² Score muy alto, pero el MSE indica que todavía hay margen para mejorar la precisión en términos absolutos. La validación adicional y el análisis residual pueden proporcionar más información sobre cómo perfeccionar el modelo.

- Se recomienda explorar el rendimiento de otros algoritmos de aprendizaje automático.

- Al comparar el rendimiento de diferentes modelos de regresión utilizando el Mean Squared Error (MSE) y el R² Score, podemos obtener una visión más clara de cuál modelo se ajusta mejor a los datos y es más eficaz en la predicción. Aquí tienes un análisis detallado de los resultados para los cuatro modelos: Random Forest, Decision Tree, Linear Regression y Support Vector Regression (SVR).

Random Forest:

MSE: 18,190,372.90
R²: 0.9765
Interpretación: El modelo de Random Forest muestra un MSE relativamente bajo y un R² muy alto, lo que indica que es muy eficaz en capturar la variabilidad de los datos y tiene un buen rendimiento predictivo. Este modelo parece ser el más eficiente entre los cuatro, dado su alto R² y bajo MSE.

Decision Tree:
MSE: 26,065,828.33
R²: 0.9664
Interpretación: El modelo de Decision Tree tiene un MSE más alto y un R² más bajo en comparación con Random Forest. Aunque sigue siendo un buen modelo, su capacidad para predecir con precisión es inferior a la de Random Forest. Esto es esperable ya que Random Forest es una combinación de múltiples Decision Trees, lo que generalmente mejora la precisión.

Linear Regression:
MSE: 19,449,663.73
R²: 0.9749
Interpretación: El modelo de regresión lineal tiene un MSE ligeramente superior al de Random Forest, pero todavía es razonablemente bajo. Su R² también es muy alto, lo que indica un buen ajuste a los datos. Aunque no es tan preciso como Random Forest, sigue siendo un modelo sólido para este conjunto de datos.

Support Vector Regression (SVR):
MSE: 835,893,022.62
R²: -0.0781
Interpretación: El modelo SVR tiene un MSE extremadamente alto y un R² negativo, lo que indica que es un mal ajuste para los datos. El R² negativo sugiere que el modelo está peor que simplemente usar la media de los valores observados como predicción. Esto puede deberse a una incorrecta configuración de los hiperparámetros o a la naturaleza de los datos que no se ajusta bien a un modelo SVR. 


Conclusiones Generales:

Mejor Modelo: Random Forest es claramente el mejor modelo en este análisis, con el MSE más bajo y el R² más alto, lo que indica una excelente capacidad predictiva y ajuste a los datos.

Buen Modelo: Linear Regression también muestra un buen rendimiento, con un MSE bajo y un R² alto. Aunque no tan preciso como Random Forest, sigue siendo una opción viable.

Modelo Aceptable: Decision Tree tiene un rendimiento aceptable, pero no tan bueno como Random Forest o Linear Regression.

Peor Modelo: SVR es claramente el peor modelo para este conjunto de datos, con un MSE muy alto y un R² negativo, indicando un mal ajuste.

Este análisis proporciona una clara indicación de que Random Forest es el modelo preferido para este conjunto de datos, seguido de cerca por Linear Regression.
