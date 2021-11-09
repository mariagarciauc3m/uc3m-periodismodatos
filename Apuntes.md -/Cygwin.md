# CÓMO FUNCIONA LA TERMINAL
## COMANDOS
Entre el comando y los argumentos siempre un espacio
- FILE nombre del archivo te dice que tipo de documento es
- ls: lista archivos que tienes en el sitio donde estas (esto lo sabes poniendo pwd y te parece: users/mariagarciaduque
- ls -l: listar de forma completa
- ls -a
- comando env
- pwd: te dice dónde estás
- cat: se utiliza para concatenar
- mkdir: crear una carpeta (mkdir uno dos tres cuatro cinco: te ha creado cinco carpetas a la vez dentro de “borrar”)
si la carpeta se llama “borrar” y le das a ls borrar y no te sale error, es que existe
- cd: cambiar de directorio
- echo: para crear un archivo de texto
- echo > enviar a un archivo / echo hola > hola.txt
- cat hola.txt hora.txt: los concatena (por ejemplo para juntar los datos del covid del día 1, los del día 2, los del 3, etc)
- brew install … : para instalar cosas##


## RUTAS
- Ruta absoluta: cd ESPACIO/Users/mariagarciaduque/borrar
- Ruta relativa: cd borrar
man cat: esto no se para que es
la q es para salir

## CÓMO SE PRUEBA UN COMANDO
man lolcat
export PATH=bin/::$PATH

## NANO
nano /cygdrive/c/Users/g14…. : ruta absoluta
nano uc3m-periodismo-datos/sesiones/20121… : ruta relativa

- git pull para descargar (clonar)
- git remote -v : para saber a donde envio los datos

- para guardar una parte del archivo de “feliz”: head feliz.csv > 10primeraslineas.csv

- para mandar algo al escritorio > -/

cuándo uso un archivo, en realidad estoy usando un recurso

## Para abrir un archivo en NANO
- Descargar el repositorio: copiando el code y git clone ….
- cd: para meternos en esa carpeta que he descargado
- nano 2021-09 (por ejemplo) y tabulamos dos veces
- nos aparecen todos los archivos que se llaman 2021-09, entonces elegimos el que queremos abrir y: nano 2021-09-28.md

CON CD SALES DE DONDE ESTÉS A TU HOME
