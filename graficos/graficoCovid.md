## Tendencia de las defunciones por COVID-19 en España 

A partir de los datos publicados por Datos.gob.es y obtenidos del Instituto Nacional de Estadística, se puede observar, en primer lugar, una clara diferencia en el número de defunciones debido a la Covid 19 en el total nacional según el grupo etario; en segundo lugar, se observa que el impacto del virus no ha sido el mismo en todo el territorio nacional, sino que hay significativos contrastes entre comunidades autónomas. 

Respecto a la primera visualización de datos podemos destacar una clara tendencia creciente de defunciones conforme va avanzando la edad. Llama la atención el salto a la inversa cuándo se pasan los 95 años, y habría que añadir que al tratarse de datos absolutos y no de porcentajes, es necesario tener en cuenta que estos dos últimos grupos son minoritarios. Es decir, hay muy poca población que se enmarque en estos dos grupos etarios, por lo que el número de defunciones es, necesariamente, menor. 

Por otra parte, los datos muestran que la Comunidad de Madrid reúne el mayor número de muertos por el virus hasta la fecha, tanto en hombres como en mujeres. Se observa también un mayor impacto en el género masculino en todas las regiones geográficas, siendo, por lo general, mayor esta diferencia cuanto mayor es la cifra de defunciones. Le siguen Cataluña, Andalucía y muy seguido Castilla León. Las ciudades autónomas y los archipiélagos encabezan la lista por abajo, junto con Cantabria, que también muestra “buenos” resultados. 

Es necesario destacar que las cifras que refieren estas visualizaciones muestran únicamente las muertes por cuya causa se confirmó expresamente que fue el virus de la Covid-19, quedan excluidos todos los fallecidos cuya causa se sospechara que fuera Covid. 


# Cómo han sido diseñados estas visualizaciones de datos
Como ya se ha mencionado anteriormente, los datos han sido descargados de la página de Datos.gob.es en formato csv. Una vez descargados, los abrí con Open Refine. 

Para el primer gráfico, como lo que me interesaba era el total nacional de fallecimientos, filtré los datos mediante una faceta de texto sobre la columna de las comunidades. Hice lo mismo con la columna de sexo (incluí solo “ambos), y con la de Covid-19, que tenía tres opciones: defunciones provocadas por el Covid19, sospechosas de haberlo sido y otras; seleccioné solo las comprobadas por Covid19 para una mayor rigurosidad de la información. Una vez tenía una tabla con el número de defunciones en cada grupo etario, tuve que transformar las celdas de la columna de los números, ya que Datawrapper no interpretaba  correctamente los datos numéricos que contenían puntos (indicativo de millares), así que apliqué la función: value.replace("."," "). 

Después descargué los datos en csv y me dirigí a Datawrapper. En esta página seleccioné la opción “hide from visualization” en las columnas de Comunidad Autónoma, Covid19 y Sexo. En este caso empleé este formato porque permitía ver la tendencia dominante en la relación edad-muertes. Finalmente, elegí un color de la gama de los rojos tirando hacia un tono marrón, ya que me parecía un color que transmite seriedad, tiene connotaciones negativas pero al ser más oscuro que un rojo tradicional, no resulta tan alarmante. Después incluí un título adecuado con una breve descripción, mi nombre como creadora del gráfico y la fuente de los datos.

Para el gráfico de barras, primero seleccioné con una faceta de texto todas las Comunidades Autónomas y excluí la fila de total nacional. Con la función de value.replace cambié el nombre de algunas comunidades que no me gustaba como aparecían escritas (por ejemplo, “Asturias, Principado de”, “Rioja, La”, “Navarra, Comunidad Foral de”, etc.). Después, seguí el mismo procedimiento con los números de defunciones que en el primer gráfico para eliminar los puntos. Creé una factea de texto en la columna “Sexo” para eliminar la fila “ambos”. Después eliminé las columnas que no me interesaban (“Covid19” y “Edad”).

Cuando ya tenía todo “bien puesto”, cree una columna nueva basada en la columna “Sexo”; una llamada “Mujeres”. Con la función value.replace(“Hombres”,” “), conseguí que en la nueva columna “Mujeres” solo aparecieran los datos que correspondían a muertes de mujeres, y el resto de celdas en blanco. Repetí el proceso pero a la inversa creando otra columna llamada “Hombres”. Una vez conseguido, descargué los datos en xls y con Excel eliminé las celdas vacías y los valores repetidos (cada Comunidad estaba duplicada), consiguiendo una tabla en la que aparecían las defunciones de cada región separadas por sexo.

Abrí los datos con Datawrapper. Invertí filas y columnas para que las comunidades se colocaran en el eje horizontal y seleccioné un gráfico de barras agrupadas para que se viera a simple vista la diferencia por géneros en cada Comunidad Autónoma. Finalmente escogí el mismo color que en el primer gráfico para un valor y otro en la misma gama pero que hiciera contraste para el otro valor; añadí los mismo datos que en el otro gráfico y descargué la imagen.

![Gráfico creado en DataWrapper a partir de los datos de datos.gob.es](imagenes/graficoCovid1.png)
![Gráfico creado en DataWrapper a partir de los datos de datos.gob.es](imagenes/graficoCovid2.png)

También se puede visualizar desde: https://datawrapper.dwcdn.net/K14yA/1/ y https://datawrapper.dwcdn.net/P2ZiP/1/


