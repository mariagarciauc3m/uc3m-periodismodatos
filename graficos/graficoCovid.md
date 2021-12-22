## TENDENCIA DE LAS DEFUNCIONES POR COVID-19 EN ESPAÑA

A partir de los datos publicados por Datos.gob.es y obtenidos del Instituto Nacional de Estadística, se puede observar, en primer lugar, una clara diferencia en el número de defunciones debido a la Covid 19 en el total nacional según el grupo etario; en segundo lugar, se observa que el impacto del virus no ha sido el mismo en todo el territorio nacional, sino que hay significativos contrastes entre comunidades autónomas. 

Respecto a la primera visualización de datos podemos destacar una clara tendencia creciente de defunciones conforme va avanzando la edad. Llama la atención el salto a la inversa cuándo se pasan los 95 años, y habría que añadir que al tratarse de datos absolutos y no de porcentajes, es necesario tener en cuenta que estos dos últimos grupos son minoritarios. Es decir, hay muy poca población que se enmarque en estos dos grupos etarios, por lo que el número de defunciones es, necesariamente, menor. 
![graficocovid1](https://user-images.githubusercontent.com/90327355/147096957-6a2418b4-55b6-41f3-a2df-38fae46cee11.png)

Por otra parte, en la segunda visualización los datos muestran que la Comunidad de Madrid reúne el mayor número de muertos por el virus hasta la fecha, tanto en hombres como en mujeres. Se observa también un mayor impacto en el género masculino en todas las regiones geográficas, siendo, por lo general, mayor esta diferencia cuanto mayor es la cifra de defunciones. Le siguen Cataluña, Andalucía y muy seguido Castilla León. Las ciudades autónomas y los archipiélagos encabezan la lista por abajo, junto con Cantabria, que también muestra “buenos” resultados. 
![graficocovid2](https://user-images.githubusercontent.com/90327355/143928817-60f685cc-c169-48ae-9a38-f36796c7819e.png)

Es necesario destacar que las cifras que refieren estas visualizaciones muestran únicamente las muertes por cuya causa se confirmó expresamente que fue el virus de la Covid-19, quedan excluidos todos los fallecidos cuya causa se sospechara que fuera Covid. 


### Cómo han sido diseñados estas visualizaciones de datos
Como ya se ha mencionado anteriormente, los datos han sido descargados de la página de Datos.gob.es en formato csv. Una vez descargados, los abrí con Open Refine. 

Con el [primer gráfico](https://datawrapper.dwcdn.net/K14yA/1/) quería mostrar la diferencia en el impacto del Covid-19 según la edad en el conjutno del territoio nacional. Por ello, filtré los datos mediante tres facetas de texto. Para aplicar la primera me coloqué sobre la columna "Comunidades Autónomas por lugar de Defunción" y seleccioné únicamente las filas con el valor "Total Nacional". La segunda faceta de texto la apliqué sobre la columna de sexo e incluí solo el valor “ambos"; la tercera la generé sobre la columna "Covid-19", que tenía tres opciones: defunciones provocadas por el Covid19, sospechosas de haberlo sido y otras; seleccioné solo las comprobadas por Covid19 para una mayor rigurosidad de la información. Una vez tenía una tabla con el número de defunciones en cada grupo etario, me dirig a la columnacon las cifras de las defunciones, seleccioné la opción "edit cells" y después "to number". Sin embargo, cuando abri los datos con Datawrapper, el programa interpretaba los puntos que indican millares como decimales, por lo que tuve que volver a abrir Open Refine y editar esa columna. Sobre la columna de cifras, le di a "Edit cells" > "Transforma" y apliqué la función value.replace("."," "). 

Descargué los datos en forrmato .csv y me dirigí a Datawrapper. Comprobé que el programa interpretaba los datos correctamente. Seleccioné la opción “hide from visualization” en las columnas de Comunidad Autónoma, Covid-19 y Sexo. Seleccioné un formato que permitía a simple vista ver la tendencia de defunciones según iba avanzando la edad. Finalmente, elegí un color de la gama de los rojos tirando hacia un tono marrón, ya que es color que transmite seriedad, tiene connotaciones negativas pero al ser más oscuro que un rojo tradicional, no resulta tan alarmante. Después incluí un título adecuado con una breve descripción, mi nombre como creadora del gráfico y la fuente de los datos.

Para el [gráfico de barras](https://datawrapper.dwcdn.net/0A8K1/1/), volví a Open Refine, fui al historial de cambios y pulsé sobre la primera versión para volver a la tabla incial de datos que había descargado de datos.gob.es. Primero apliqué una faceta de texto en la columna de "Comunidades Autónomas" y  y excluí la fila de "Total Nacional", ya que en este caso quería mostrar la información que no había mostrado en el primer gráfico y observar las diferencias entre comunidades y sexo. En la misma columna, seleccioné la opción "Edit cells" > "Transformations" y con la función de value.replace cambié el nombre de algunas comunidades que no me gustaba como aparecían escritas. En concreto:
- value.replace(“Asturias, Principado de”,"Asturias)
- value.replace(“Rioja, La”,"La Rioja")
- value.replace(“Navarra, Comunidad Foral de”,"Navarra"
- value.replace("Madrid, Comunidad de","Madrid")
- value.replace("Murcia, Región de","Murcia")
- value.replace("Balears, Illes","Baleares")

Después, seguí el mismo procedimiento con los números de defunciones que en el primer gráfico para eliminar los puntos. Una vez conseguido esto, creé una factea de texto en la columna “Sexo” para eliminar la fila “ambos”. Después eliminé las columnas que no me interesaban (“Covid19” y “Edad”).

Cuando ya tenía todo “bien puesto”, pinché en la columna "Sexo", seleccioné la opción "Edit column" > "Add column based on this column" y la llamé  “Mujeres”. Con la función value.replace(“Hombres”,” “), conseguí que en la nueva columna “Mujeres” solo aparecieran los datos que correspondían a muertes de mujeres, y el resto de celdas en blanco. Repetí el proceso pero a la inversa creando otra columna llamada “Hombres” y aplicando esta vez la función value.replace(“Mujeres”,” “). Una vez conseguido, descargué los datos en xls y con Excel eliminé las celdas vacías, consiguiendo una tabla en la que aparecían las defunciones de cada región separadas por sexo.

Abrí los datos con Datawrapper. Comprobé que los datos habían sido interpretados de manera correcta e invertí filas y columnas para que las comunidades se colocaran en el eje horizontal. Después, seleccioné un gráfico de barras agrupadas para que se viera a simple vista la diferencia por sexo en cada Comunidad Autónoma. Finalmente escogí el mismo color que en el primer gráfico para un valor (Hombres) y otro en la misma gama pero que hiciera contraste para el otro valor (Mujeres); añadí los mismo datos que en el otro gráfico (Título, descripción, autor y fuente de los datos) y descargué la imagen en formato PNG.





