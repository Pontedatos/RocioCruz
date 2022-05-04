A continuación comentaré todos los pasos que he realizado para la creación de esta web. 

## Creación del nuevo repositorio:
Antes de comenzar el camino para la creación de la nueva web, me metí en mi cuenta de Github. Tras esto, accedí a unirme a la organización "Pontedatos" (Clase de Periodismo de Datos en doble grado de Humanidades y Periodismo de UC3M). En este paso, cree un nuevo repositorio posicionando mi puntero en el apartado de color verde "new". Después de realizar esto, se abrió una pestaña nueva donde indicaba lo que tenía que hacer para crear un nuevo repositorio dentro de "PonteDatos". A continuación, cree mi nuevo repositorio con mi nombre de usuario de Github "Rocío Cruz". Indique que mi repositorio fuera público y le dí a "Create repository". 

## Compilación de los trabajos realizados a lo largo del curso:
Una vez realizado este primer paso, seguí todos los pasos de creación de un repositorio desde la terminal. Los pasos que he realizado para la creación del repositorio desde la terminal son: 
- Empleo del comando `git clone` para clonar el repositorio en una carpeta nueva de mi ordenador (creada a partir de `mkdir`). Esta carpeta es un repositorio git en mi ordenador, en *localhost*, que tiene el mismo contenido que el de la dirección desde donde lo he clonado.
- En el interior de este repositorio se encuentra un archivo README.md vacío. Por lo que, para copiar todos los trabajos que pide el profesor, los he tenido que copiar desde mi repositorio personal a la organización "Pontedatos". Para ello, he usado el comando `cp`. Este comando se emplea para copiar un documento en un lugar nuevo.  Después de `cp` especifique  la dirección del archivo que quiero copiar en la nueva carpeta, y después del espacio incluí la dirección de la carpeta donde quería copiar el archivo.
- Antes de reunir las prácticas en esta carpeta, he borrado el README.md creado anteriormente para que pueda ser sustituido por el README.md ya existente en mi repositorio personal. Para ello, he utilizado el comando `rm` (rm README.md).

Una vez compiladas las prácticas en esta carpeta, he actualizado los cambios en GitHub. Para ello, he empleado varios comandos en el siguiente orden: 
- `mi casa` para ir al lugar donde tengo el repositorio. 
- `cd` para cambiar el directorio a la carpeta conectada a Github.
- `git status` para conocer los archivos que tengo en el ordenador, pero no en GitHub.
-  `git add . `para añadir todos los elementos nuevos al repositorio. 
-  Para darle un nombre a este cambio, he escrito `git commit -m`“cambio1”. 
-  Con `git pull` he actualizado de modo remoto el cambio. 
-  Para acabar, he empleado el comando `git push` y he subido los cambios que he realizado a GitHub (después de introducir mi usuario de GitHub y mi token).

## Creación de una estructura para la página web:
Una vez comprobado en GitHub que los cambios se han hecho con éxito, me he introducido en la sección "Settings" del repositorio y he aprovechado la funcionalidad "Pages" de Github que permite la creación de una web con el contenido del repositorio. La estructura de la web es la del propio repositorio. Este repositorio no contiene carpetas, todos los archivos están en el propio repositorio al mismo nivel. También he escogido un tema para mi página web.
