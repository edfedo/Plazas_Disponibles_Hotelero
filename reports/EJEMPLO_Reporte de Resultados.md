## Reporte de Resultados Plazas Disponibles Hotelero Ushuaia
### Análisis Exploratorio de Datos

*Selecciona las características (columnas) Establecimientos, Habitaciones o Unidades disponibles y EsFestivo, y la variable objetivo Plazas disponibles:*

Dentro de la exploración de los datos se encontraron los siguientes patrones de interés:

- Cuadro de Tendencias temporales

Tendencia General:

Se observa una tendencia general decreciente en el número de plazas disponibles desde 2008 hasta aproximadamente 2016.
A partir de 2016, hay una ligera recuperación que se ve interrumpida abruptamente en 2020, lo cual es probable que se deba a la pandemia de COVID-19.
Posteriormente, hay una recuperación marcada a partir de 2021, alcanzando niveles más altos hacia 2024.
Variabilidad:

La banda sombreada alrededor de la línea de tendencia representa la variabilidad o el rango de las plazas disponibles en los distintos meses de cada año.
La variabilidad parece ser más alta en los años más recientes (2020 en adelante), lo cual puede indicar fluctuaciones significativas en el número de plazas disponibles probablemente debido a la recuperación y ajustes post-pandemia.
Impacto de la Pandemia (2020):

Claramente, 2020 muestra un impacto significativo con una caída drástica en las plazas disponibles, reflejando las restricciones y cierres asociados a la pandemia de COVID-19.
La recuperación empieza en 2021 y continúa en los años siguientes, pero con una alta variabilidad, sugiriendo una reactivación gradual y posiblemente desigual entre los distintos meses y lugares.

























* En las variables de temperatura la distribución de los positivos esta corrida hacia el lado derecho lo que confirma la suposición de una influencia de las altas temperaturas a la aparición de marea roja.
*
*
* [![Temperatura](Distribucion Temperatura "Temperatura")](https://github.com/VictorVisnuk/MareaRoja/blob/main/reports/figures/Figura2.png "Temperatura")
* En las variables de radiación solar se observa una interesante distribución donde en existe un pico amesetado de positivos en el rango de la mediana de la distribución y su consecuente baja de negativos lo que puede indicar que ese rango de radiación afecta particularmente al fenómeno. [[![Grafico Radiacion](Radiación "Grafico Radiacion")](https://github.com/VictorVisnuk/MareaRoja/blob/main/reports/figures/Figura1.png "Grafico Radiacion")(https://github.com/VictorVisnuk/MareaRoja/blob/main/reports/figures/Figura1.png)
* Las variables de viento no parecen afectar al fenómeno.


### Modelos de Clasificación
#### Regresión Logística
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

