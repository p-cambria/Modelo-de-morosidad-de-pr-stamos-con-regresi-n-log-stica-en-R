# Modelo de morosidad de préstamos con R

Este proyecto utiliza regresión logística para estimar la probabilidad de morosidad de préstamos a partir del dataset HMEQ, compuesto por 5,960 registros.

El trabajo incluye exploración de datos, tratamiento de valores faltantes, construcción del modelo y evaluación con datos de prueba. El análisis se desarrolló en R y se documentó en R Markdown.

## Conclusiones

La preparación de los datos fue una parte importante del proyecto. Eliminar los registros incompletos reducía la proporción de préstamos morosos de aproximadamente **20 % a 8.8 %**, alterando la composición de la muestra. Por eso, se conservaron los registros mediante imputación y se incorporaron indicadores de información faltante.

En el conjunto de prueba, el modelo alcanzó un **AUC de 0.903** y una **exactitud del 89.9 %**. Con un umbral de 0.50, identificó correctamente el **65.6 % de los préstamos morosos**.

La comparación de umbrales mostró que es posible detectar más morosos al reducir el punto de corte, aunque esto también aumenta las falsas alertas. La elección del umbral depende del equilibrio que se busque entre ambos tipos de error.

Este ejercicio permitió comprender cómo el tratamiento de los datos y la elección del umbral influyen en los resultados de un modelo de clasificación.

