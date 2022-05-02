# Documentación del proceso de creación de esta web:
A continuación comenataré todos los pasos que he realizado para la creación de esta web. 

## Creación del nuevo repositorio:
Antes de comenzar el camino para la nueva web, me introduje en mi cuenta de github. El primer paso que dí fue meterme en la organización "Pontedatos" (Clase de Periodismo de Datos en doble grado de Humanidades y Periodismo de UC3M). Tras esto, cree un nuevo repositorio posicionando mi puntero en el apartado de color verde "new". Después de realizar este paso, se me abrió una pestaña nueva donde se indicaba lo que tenía que hacer para crear un nuevo repositorio dentro de "PonteDatos". A continuación, cree mi nuevo repositorio con mi nombre de usuario de Github "Rocío Cruz". Indique que mi repositorio fuera público y le dí a "Create repository". 

## Compilación de los trabajos realizados a lo largo del curso:
Una vez realizado este primer paso, seguí todos los pasos de creación de un repositorio desde la terminal. Los pasos que he realizado para la creación del repositorio desde la terminal son: 
- Empleo del comando `git clone` para clonar el repositorio en una carpeta nueva de mi ordenador (creada a partir de `mkdir`). Esta carpeta es un repositorio git en mi ordenador, en *localhost*, que tiene el mismo contenido que el de la dirección desde donde lo he clonado.
- En el interior de este repositorio se encuentra un archivo README.md vacío. Por lo que, para copiar todos los trabajos que pide el profesor, los he tenido que copiar desde mi repositorio personal a la organización "Pontedatos". Para ello, he usado el comando `cp`. Este comando se emplea para copiar un documento en un lugar nuevo.  Después de `cp` se debe especificar la dirección del archivo que quiero copiar en la nueva carpeta, y después del espacio se inlcuye la dirección de la carpeta donde quieres copiar el archivo.
- Antes de reunir las prácticas en esta carpeta, he borrado el README.md creado anteriormente para que pueda ser sustituido por el README.md ya existente en mi repositorio personal. Para ello, he utilizado el comando `rm` (rm README.md).

Una vez compiladas las prácticas en esta carpeta, he actualizado los cambios en GitHub. Para ello, he empleado varios comandos en el siguiente orden: 
- `mi casa` para ir al lugar donde tengo el repositorio. 
- `cd` para cambiar a la carpeta que tengo conectada con Github.
- `git status` para conocer los archivos que tengo en el ordenador, pero no en GitHub.
-  `git add . `para añadir todos los elementos nuevos al repositorio. 
-  Para darle un nombre a este cambio, he escrito `git commit -m`“cambio1”. 
-  Con `git pull` he actualizado de modo remoto el cambio. 
-  Para acabar, he empleado el comando `git push` he subido los cambios que he realizado a GitHub (después de introducir mi usuario de GitHub y mi token).

## Creación de una estructura para la página web
