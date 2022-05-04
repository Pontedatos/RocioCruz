# Documentación del proceso de aprendizaje: 
A continuación, detallaré lo aprendido a lo largo del curso en la asignatura Periodismo de Datos.

## Instalación de un programa de emulación de la terminal:
Antes de resumir lo aprendido respecto a la instalación de un programa de emulación de la terminal, cabe señalar que mi ordenador pertenece a la familia de distribuciones de software para PC Windows, por lo que durante el curso tuve que instalar y configurar distintos programas de emulación de la terminal, los cuales expondré a continuación.

### Terminal WSL (Windows Subsystem for Linux)
En primer lugar, me instalé WSL [Windows Subsystem for Linux](https://docs.microsoft.com/es-es/windows/wsl/). Esta herramienta la utilice para que el desarrollador de mi ordenador pudiera ejecutar un entorno de GNU/Linux. Según [Microsoft Build](https://docs.microsoft.com/es-es/windows/wsl/about), WSL es el “subsistema de Windows para Linux permite a los desarrolladores ejecutar un entorno de GNU/Linux, incluida la mayoría de herramientas de línea de comandos, utilidades y aplicaciones, directamente en Windows, sin modificar y sin la sobrecarga de una máquina virtual tradicional o una configuración de arranque dual."

### Ubuntu
En mi caso la virtualización de la distribución de Linux fue Ubuntu. Esta última incluye, principalmente, software libre y de código abierto. Creo que el profesor nos recomendó Ubuntu porque está orientado al usuario promedio, y a su vez, tiene un fuerte enfoque en la facilidad de uso. De esta forma, accedí a Ubuntu en su versión `cli`. Esto quiere decir, una versión sin interfaz gráfica, solo mediante la terminal. 

#### WSL: instalación de Ubuntu 
En primer lugar, la instalación de la terminal WSL la realicé a través de la PowerShell de Windows. Según [Microsoft Build](https://docs.microsoft.com/es-es/powershell/scripting/overview?view=powershell-7.2), PowerShell es “una solución de automatización de tareas multiplataforma formada por un shell de línea de comandos, un lenguaje de scripting y un marco de administración de configuración”. Los pasos que seguí para su instalación fueron:
- Abrí una nueva sesión como administradora.
- Ejecuté el comando `wsl --install -d Ubuntu`. Con el comando `(--install)` estaba indicando que quería instalar y con la distribución `(-d)` Ubuntu. 

Cuando se instaló, hice lo siguiente: 
- Reinicié el ordenador. 
- Conduje mi puntero hacia el escritorio y busqué Ubuntu en “descargas” para poder ejecutarlo y desplazarlo al menú de Inicio de mi ordenador.
Una vez ya instalado, introduje unos datos (Usuario y contraseña) para la creación de un usuario UNIX. Así evité acceder al sistema como “superusuario” (*root*). Finalmente, después de seguir todos estos pasos indicados por el profesor, obtuve con éxito la instalación nueva de Ubuntu a través de WSL.

### Terminal Cygwin 
Otro día, el profesor nos recomendó la instalación de Cygwin, otra forma de ejecutar aplicaciones nativas de Linux en Windows. Este último, proporciona un comportamiento similar a los sistemas Unix en Microsoft Windows. A diferencia de WSL, no instalamos un sistema operativo, sino solo una terminal Unix dentro de nuestro sistema. De esta manera, volvíamos a tener una capa de emulación y una colección de herramientas que nos brindaban la apariencia y la sensación de Linux.

#### Instalación de Cygwin
A mediados de curso el profesor nos recomendó instalarnos Cygwin. Esta vez lo descargue directamente desde su [página web oficial](https://www.cygwin.com/) ya que no pertenece a las herramientas nativas de Microsoft, sino a un programa desarrollado por Cygnus Solutions en un primer momento, y posteriormente por Red Hat cuando esta compró a la primera.

Una vez instalado, me dirigí a las “descargas” de mi ordenador y ejecuté el archivo de Cygwin (setup-x86_64.exe). Tras esto, seguí una serie de pasos para continuar con la ejecución:
1. Al hacer clic en ejecutar el archivo, me preguntó acerca de dónde quería instalarlo. Seleccioné la opción que recomendó el profesor: “Instalar desde Internet”.
2. Para instalar el archivo, la propia documentación de Cygwin nos aconseja instalarlo en una partición diferente a C:\, la raíz de Windows, pero para aquellas personas que solo tenemos una partición, tuve que instalarlo fuera de la raíz del sistema, así que dejé la ruta por defecto.
3. A continuación, apareció en mi pantalla una lista con todos los *mirrors* (servidores espejos repartidos por todo el mundo para garantizar la máxima velocidad y disponibilidad a cualquier usuario del planeta, así que podemos elegir uno cercano a España) desde donde se puede descargar el archivo.
4. Realicé una búsqueda en dicha lista, concretamente del dominio `.es` o de otro país cercano como Italia `(.it)`.

Finalmente, tras seguir estos pasos, el archivo me preguntó si quería instalar paquetes antes de terminar la instalación. Para instalar estos paquetes, dirigí mi puntero hacia la opción “Full” dentro de la pestaña “View”. A través del recuadro de búsqueda, instale los paquetes: `libcur14`, `wget`, `ca-certificates-letsencrypt`, `lynx`, `nano` y `openssl`. En cada paquete, bajo la columna “New” le dí a la flecha del paquete que quería instalar y seleccioné la última opción que me ofrecían. Con todo esto, terminé también con éxito la instalación de Cygwin.

## Configuración del programa:
Lo primero que realicé tras finalizar las instalaciones anteriores, fue configurar los programas, tanto WSL primero, como Cygwin después. Los cambios que configuré fueron respecto a la "Home", al `git` o a algún alias. 

Para **configurar el alias en la terminal** y así poder prescindir de escribir la ruta completa de mi carpeta de Periodismo de datos cada vez que me meta, configuré el comando `mi casa`. De esta forma, en lugar de escribir ‘/mnt/c/Users/rocio/Documentos/Escritorio/Universidad/5/PERIODISMODEDATOS/’ introducía el comando `mi casa` y me llevaba directamente al directorio que yo quería establecer como principal.

Sin embargo, para llegar a este paso, antes tuve que editar el archivo de configuración de Bash (un intérprete de comandos). Según [Emc2net](https://e-mc2.net/blog/bash-i-introduccion-y-ficheros-de-configuracion/#:~:text=Estos%20ficheros%20permiten%20al%20usuario,bash_profile%20%2C%20.), Bash “ha sido escrito por el Proyecto GNU y pertenece a la categoría de interfaz de usuarios en modo carácter o texto”. 

Esto quiere decir, situarse en el directorio “casa” de mi usuario a través del comando `$HOME/.bashr.` Cabe señalar que edité el archivo `.bashrc` desde `nano` (editor de texto para la terminal). Aunque también se podía hacer directamente desde la línea de comandos.

Después de esto, finalicé la sesión de mi terminal a través del comando `exit`. Para comprobar si los cambios realizados eran correctos, volví a abrir la sesión en mi terminal, pero esta vez escribiendo el comando configurado `micasa`. Realicé con éxito la configuración. Para ver el archivo de configuración utilicé el comando `cat $HOME/.bashrc`. Para editar el archivo, el comando `nano $HOME/.bashrc`. 

Por otro lado, tuve que modificar la "Home" en la terminal Cygwin. Para ello, cambié la ruta de “casa” de mi usuario para que fuera la de Windows. Para conseguir esto tuve que realizar varios pasos:
- Editar el archivo `nsswith.conf` con el intérprete de comandos `nano`: `nano /etc/nsswith.conf`. 
- Al final del archivo escribí `db_home: windows`.
- Guardé en `nano` mediante las teclas CTRL + O y cerré con las teclas CTRL + X. 

Cómo realicé con la configuración anterior (la del alias), volví a cerrar y a abrir la terminal para comprobar que el cambio se había realizado correctamente. Para eso, utilicé el comando `pwd` y apareció `/cygdrive/c/Users/Rociocruz`.

Por último, **configure mi usuario de Github en la terminal**. De esta forma, tenía la posibilidad de vincular los cambios que hiciera en mis archivos locales con mi repositorio en la nube (Github) cada vez que realizara una práctica. Seguí los siguientes pasos para hacerlo:
- Abrí mi terminal y escribí el comando `git config --global user.name ROCIOCRUZZ`.
- Después, escribí el comando `git config --global user.email correogithub`. En este caso, escribí el email con el que me dí de alta en la plataforma de Github. Como en mi caso, anteriormente había hecho algún * commit *, tuve que deshacerlo utilizando el comando `git commit --amend --reset-author`.
Para configurar mi usuario y mi correo de Github, escribí `git config --global user.name ROCIOCRUZZ`, y luego `git config --global user.email correogithub`.

Con todo esto, conseguí vincular mi carpeta de la asignatura con Github. 

## Configuración de un programa de edición de texto:
En mi caso, el programa de edición de texto que tengo es `nano`. Por lo que la configuración la realicé en este editor. Lo primero que hice fue ajustar el texto a la resolución de la pantalla de mi ordenador. De esta manera, conseguía que apareciera el número de líneas para poder situar correctamente el contenido de mi archivo. Realicé los siguientes pasos:
- Edite `nano` con el comando `nano $HOME/.nanorc`.
- Escribí #Ajustar el texto a pantalla.
- Escribí `set softwrap`.
- Escribí #Numerar las líneas.
- Escribí `set linenumbers`. 
Con todos estos pasos, conseguí ajustar el texto correctamente. 

Para configurar el programa de edición de texto en Cygwin:
- Copié el archivo de configuración de `nano` que se encuentra en el directorio `/etc`.
- Copié este archivo en mi directorio home con `cp /etc/nanorc .nanorc`.
- Edité el archivo con `nano .nanorc`. 
- Busqué con CTRL + W linenumbers, y en su línea, escribí set linenumbers.
- Busqué con CTRL + W softwrap, y en su línea escribí set softwrap.
- Guardé con CTRL + O y cerré con CTRL + X.

## Configuración y funcionamiento de un gestor de paquetes/programas del emulador de la terminal: 
Según [Debian.org](https://www.debian.org/doc/manuals/aptitude/pr01s02.es.html) un gestor de paquetes se considera “al gestor de conjuntos de ficheros que se agrupan y que puede instalar y eliminar como conjunto”. Principalmente para instalar programas y herramientas en sistemas Unix como GNU/Linux. En el caso de Ubuntu su gestor es `apt` y Cygwin tiene el suyo propio, `apt-cyg`, que no procede de fábrica con el programa, a diferencia del primero.

Para instalar `apt-cyg` utilicé `lynx -source rawgit.com/transcode-open/apt-cyg/master/apt-cyg > apt-cyg` y después `install apt-cyg /bin`.

## Versión del lenguaje de SHELL utilizado:
Según los apuntes tomados durante las clases, se denomina Shell al idioma de la terminal (dentro de este idioma se encuentra BASH y el CSH: Windows y Mac respectivamente). 

Para comprobar la versión del lenguaje Shell que he utilizado, utilicé la variable de entorno `$0` la cual consulto con `echo $0`. De esta forma, obtuve el lenguaje de la terminal que utilizo actualmente, Bash. Según mis apuntes, Bash es un lenguaje de programación en sí, pero también un entorno sobre el que trabajamos incluso sin programar. Es el lenguaje de la Shell más popular. Para comprobar la versión de Bash, lo hice a través del propio Bash, especificando la opción `--help`: `bash --help`.

## Valor de la variable de entorno PATH:
Sobre la variable de entorno PATH he aprendido que es la variable de entorno más importante para ejecutar comandos. Según mis apuntes, ruta (PATH) es el camino que hace el ordenador para “darte” lo que le has pedido. Por ejemplo, si yo quiero mis apuntes de periodismo de datos, el ordenador tiene que ir: Carpeta de apuntes 5º de carrera → Carpeta apuntes primer cuatri → Carpeta de periodismo de datos. La ruta puede estar dentro de tu ordenador o puede estar en Internet en general. 

Las variables de entorno se generan con el símbolo `$`. Por ejemplo, `$HOME` significa la ruta de nuestro usuario (/mnt/c/Users/usuaria). `$PATH` nos muestra las rutas donde están los programas que se puedan ejecutar. Para consultar la variable de entorno `PATH`, usé el comando `echo $PATH`. La terminal nos devolverá las rutas en las que se encuentran los programas instalados que puede ejecutar la terminal. Separados por dos puntos `(:)`, aparecen los directorios donde la terminal va a buscar los programas para ejecutarlos cuando lo indiquemos así a través de los comandos.

## Comandos utilizados y ejemplos:
A continuación cito y explico los comandos que he aprendido y utilizado a lo largo del curso en clase: 

- `pwd`: comando que he utilizado al abrir la terminal para saber dónde me encuentro.
- `cd`: comando que he utilizado para cambiar el directorio (con `cd` y un espacio, te lleva a home).
- `ls`: comando que he utilizado para listar. Por ejemplo, qué tengo en una carpeta. Ejemplo: ls -l significa lístame con más detalle. 
- `nano`: comando que he utilizado para editar archivos .md de texto.
- `mkdir`: comando que he utilizado para crear carpetas.
- `&&`: comando que he utilizado para unir comandos, es decir, hacer dos comandos de una vez. Ejemplo: mkdir (crear carpeta) && cd (cambiar de directorio).
- `push`: comando que he utilizado para realizar descargas.
- `mnt`: comando que he utilizado para relacionar el programa (wsl, la terminal) con Windows. 
- `cat`: comando que he utilizado para concatenar (unir o enlazar) cosas y para leer archivos (o para previsualizar). Por ejemplo, pongo cat README.md para previsualizar mi archivo readme.
- `mv`: comando que he utilizado para mover las cosas de un sitio a otro. También lo he empleado para cambiar de nombre un archivo o carpeta. Ejemplos: mv capeta/ nuevo destino/. (“nuevo destino” es donde muevo “carpeta”). mv carpeta/ carpetita para cambiar de nombre. mv [origen] [destino] para mover (cortar) las carpetas o archivos de sitio, pero también para renombrarlos. 
- `echo`: comando que he utilizado para que la terminal responda a lo que escribo. Por ejemplo, echo “hola mundo”.
- `echo $HOME`: comando que he utilizado para que la terminal me diga cual es mi home. 
- `cp`: comando que he utilizado para copiar un archivo o carpeta a otra. Por ejemplo, cp nombre de la carpeta/nombre del archivo.md  carpeta a donde lo quieres mover/.
- `../`: comando que he utilizado para ir al repositorio anterior.
- `git init`: comando que he utilizado para que una carpeta tenga las mismas “propiedades” que una carpeta de github. 
- `touch`: comando que he utilizado para crear un archivo en blanco.
- `rm`: comando que he utilizado para borrar.
- `whoami`: comando que he utilizado para que me diga quién soy.
- `git clone`: comando que he utilizado para clonar en la carpeta.
- `man`: comando que he utilizado para mostrar información sobre el comando que queramos.
- `env`: comando que he utilizado para que me muestre las variables de entorno. 
- `grep`: comando que he utilizado para  buscar palabras dentro de archivos de texto desde la terminal.
-  `wget`: comando que he utilizado para descargar un archivo/contenido de una web. 
- `cat.bash_history`: comando que he utilizado para ver el historial de comandos. 
- `git status`: comando que he utilizado para conocer los archivos que tengo en el ordenador, pero no en GitHub.
- `git add .`: comando que he utilizado para añadir todos los elementos nuevos al repositorio.
- `git commit -m`: comando que he utilizado para darle un nombre al cambio.
- `git pull`: comando que he utilizado para actualizar de modo remoto el cambio.
- `git push`: comando que he utilizado para subir los cambios realizados a Github.
