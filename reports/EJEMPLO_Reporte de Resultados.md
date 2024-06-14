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

Valor del MSE: 18,190,372.90
El MSE mide el promedio de los cuadrados de los errores, es decir, la diferencia entre los valores predichos por el modelo y los valores reales. Un MSE más bajo indica un mejor ajuste del modelo a los datos.
En este caso, un MSE de 18,190,372.90 es relativamente alto en términos absolutos, pero su interpretación depende del rango de los datos de plazas disponibles. Dado que estamos trabajando con valores de plazas disponibles que pueden alcanzar decenas de miles, este valor podría ser razonable.


[-] R² Score:

Valor del R²: 0.9765
El R² Score, o coeficiente de determinación, mide la proporción de la varianza en la variable dependiente que es predecible a partir de las variables independientes. Su valor varía entre 0 y 1.
Un R² de 0.9765 indica que el 97.65% de la variación en el número de plazas disponibles puede ser explicada por el modelo. Esto sugiere que el modelo tiene un excelente ajuste a los datos.


[-] Interpretación General:

Modelo Eficiente:
El alto valor de R² (cercano a 1) sugiere que el modelo es muy eficaz en capturar la variabilidad de los datos y que tiene un buen rendimiento predictivo.

Posibles Mejoras:
Aunque el MSE es relativamente alto, podría deberse a algunos valores atípicos o variabilidad inherente en los datos de plazas disponibles. Sería útil analizar estos valores atípicos y considerar técnicas de preprocesamiento adicionales o modelos más sofisticados si se requiere mejorar aún más la precisión.

Validación y Pruebas:
Es importante también validar el modelo con un conjunto de datos de prueba separado (si no se ha hecho ya) para asegurarse de que estos resultados no son específicos del conjunto de datos de entrenamiento.

Análisis Adicional:
Podría ser útil llevar a cabo un análisis residual para comprobar si hay patrones en los errores que el modelo comete. Esto podría proporcionar información sobre posibles mejoras o ajustes necesarios en el modelo.

El modelo parece ser muy eficaz con un R² Score muy alto, pero el MSE indica que todavía hay margen para mejorar la precisión en términos absolutos. La validación adicional y el análisis residual pueden proporcionar más información sobre cómo perfeccionar el modelo.

#------------------------------------



* La precisión del modelo con una validación cruzada fue: Media de precisión 0.88, desviación estándar 0.04.
* La precisión de entrenamiento fue de 0.865, la precisión de prueba fue de 0.895 mientras que la precisión del set completo de datos fue 0.874
* La matriz de confusión del set de prueba refleja una buena identificación de positivos con una tasa de falsos positivos un poco alta.

#### Regresión Logística
* La precisión del modelo con una validación cruzada fue: Media de precisión 0.87, desviación estándar 0.04.
* La precisión de entrenamiento fue de 96,3%, la precisión de prueba fue de 90,5% mientras que la precisión del set completo de datos fue de 94,5%
* La matriz de confusión del set de prueba refleja una identificación de positivos un poco menos eficiente, pero con una tasa de falsos positivos menor.

[![Matriz de correlación](MapaDeCalor "Matriz de correlación")](https://github.com/VictorVisnuk/MareaRoja/blob/main/reports/figures/Figura3.png "Matriz de correlación")
#### Conclusiones Finales
+ Es posible determinar con un grado de precisión aceptable la aparición de marea roja en base a variables meteorológicas.
+ El modelo de Regresión Logística es mejor para identificar los positivos, pero con una alta tasa de falsos positivos mientras que el de máquina de soporte vectorial tiene menor detección de positivos pero mayor precisión global.
+ Se recomienda explorar el rendimiento de otros algoritmos de aprendizaje automático.
+ Queda explorar el comportamiento del modelo agregando datos oceanográficos (temperatura del agua, salinidad, saturación de oxígeno, etc.)
+ [![Reporte Metricas Precision](Reporte Clasificacion "Reporte Metricas Precision")](https://github.com/VictorVisnuk/MareaRoja/blob/main/reports/figures/Figura4.png "Reporte Metricas Precision")
+ [![Reporte Metricas Precisión](Reporte Clasificacion "Reporte Metricas Precisión")](https://github.com/VictorVisnuk/MareaRoja/blob/main/reports/figures/Figura5.png "Reporte Metricas Precisión")

