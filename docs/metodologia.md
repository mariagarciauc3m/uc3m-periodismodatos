## MEMORIA TRABAJO FINAL. CREACIÓN DE UNA PÁGINA WEB
Esta página web ha sido creada desde la terminal de mi ordenador y a través de Github. El primer paso fue descargar Pandoc con “brew install pandoc” y después descargar los ejemplos de Bootstrap. Después tuve que situarme en mi repositorio de Github desde mi terminal, utilizando el comando “cd”. Una vez ahí, con el comando mkdir creé una carpeta llamada “docs”. De nuevo con el comando “cd” me situé en la carpeta “docs” y utilizando “nano index.html” y copiando el contenido del archivo con igual nombre de Ponte Datos, creé el html de la página de inicio de mi web. Repetí el proceso con los comandos y archivos: “nano cabecera.html” y “nano pie.html”. El próximo paso fue dirigirme a los ajustes de mi repositorio > Pages, y ahí seleccionar en “Source” la rama main y la carpeta “docs/”. Una vez hecho esto, obtuve el link de mi página.

Una vez obtenido el link, a través de la terminal moví las carpetas “css” y “js”, que se encontraban en los ejemplos de Bootstrap previamente descargados, a la carpeta “docs/”. (mv index.html sticky-footer-header.css docs/). Después: “git add docs/”, “git commit -m docs/” y “git push origin main”. Con esto ya tenía los documentos necesarios en mi repositorio de Github.

Me dirigí de nuevo a mi repositorio y a través del comando “cd” primero entré en mi repositorio y luego en la carpeta donde guardo los dos comentarios de infografías realizados durante el curso, es decir, los ejercicios 1 y 2 (cd uc3m-periodismodatos; cd comentarios). Con el comando “pandoc infografia1.md” obtuve el contenido en lenguaje html, lo copié; después hice “cd ..” para volver a mi repositorio, y “cd docs” para entrar en esa carpeta; a continuación hice “nano index.html” y pegué el texto en html del primer comentario en la parte de “Begin Content”, debajo de la línea 71”. 

A continuación, en la parte de “header” busqué la línea en la que ponía “href=”#”>Home</a>” y sustituyendo la almohadilla por “index.html” y “Home” por “Inicio”, conseguí que en la página web, pulsando sobre “Inicio”, se regresara a la página de inicio. En la línea 45 puse mi nombre, siguiendo este mismo proceso (al lado de la almohadilla y > puse María García”, sustiuyendo a “Fixed navbar”).

Una vez hecho esto, quería conseguir que en la barra superior de la web aparecieran los títulos de cada entrada y que pinchando en ellos se dirigiera al contenido de dicha entrada. Para ello, un poco más abajo de donde puse mi nombre, en la línea 54, lo modifiqué para que me quedara lo siguiente:

li class="nav-item">
            	a class="nav-link" href="ejercicio1.html">Ejercicio 1
Debajo de esto, lo mismo pero en cada línea el html de un ejercicio y su nombre correspondiente 

Hice ^O para guardar el archivo, borré el nombre que aparecía y puse el nombre de “ejercicio1.html”, guardé el fichero con un nombre diferente y con ^X salí de nano. Repetí este proceso con el comentario de la segunda infografía y con los dos gráficos creados con Datawrapper, nombrandolos como “ejercicio2.html”, “ejercicio3.html”y “ejercicio4.html”, de forma que se creara una coherencia en los títulos. Comprobé que el contenido se había guardado correctamente entrando con “nano ejercicio1.html”. Lo mismo hice con el index.html, donde escribí en la línea correspondiente una descripción sobre lo que el lector encontrará en la web para que aparezca como presentación en la página de inicio.

Una vez conseguido esto, añadí todo a Github haciendo “git add ejercicio” y tabulé hasta que me aparecieron los cuatro ejercicios. Lo mismo con el comando “git commit -m”, y después git push origin main. 

Cuando ya tenía todo esto, reparé en que tenía algunos fallos, como por ejemplo que no había puesto mi nombre en la parte donde pone autor, o no había cambiado el generador, no había puesto un título, etc., por lo que lo añadí en la parte de “author”, “content”, “meta name”, “title”, etc. Por ello, añadí los datos. 

Tampoco había borrado una frase que aparece al final de todas mis entradas “Back to the default sticky footer minus the navbar.”, por lo que me dirigí a cada html a través de nano y lo edité para que desapareciera. Por último, añadí el archivo “sticky-footer-navbar.css” a la carpeta “css” porque también me faltaba. 

Una vez actualizado todo en Github, comprobé que la página web quedaba como había previsto. 


