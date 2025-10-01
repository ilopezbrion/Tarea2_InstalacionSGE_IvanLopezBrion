# Tarea2_InstalacionSGE_IvanLopezBrion
### Instalación ubuntu server:
Para realizar la instalación de wordpress utilcé como sistema operativo base un Ubuntu Server, específicamente la versión LTS 24.04.
Omitiré la explicación de como se realiza este proceso pues lo daré como sabido y no importante en la explicación del proceso de wordpress
Además de la propia instalación de Ubuntu Server instalé la GUI de kubuntu (para esto simplemente instalamos slim que es un gestor de interfaces gráficas y luego utilicé el comando sudo apt install kubuntu-desktop para descargar el entorno gráfico)
### Guía de instalación utilizada: [Cómo instalar Wordpress en 3 minutos Ubuntu 24.04](https://www.youtube.com/watch?v=TequRBpLqLk)
Para realizar la instalación utilicé la siguiente guía en cuestión adecuada a mi versión de Ubuntu Server
### Inicio de la instalación:
En la siguiente imagen se puede observar la versión que anteriormente he detallado que voy a usar
![primera imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_04_12.png)


Primeramente instalaremos wordpress, para acceder a la parte de instalaciones tendremos que clicar en versiones pues la descarga que aparece en grande de la pantalla es para Windows
![segunda imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_05_21.png)

Podremos seleccionar entre 2 opciones de comprimido, .zip y .targz, en mi caso escogí .targz.
![segunda imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_09_17.png)

Para después utilizar el contenido de la careta de manera más sencilla cambiaremos el nombre del comprimido a wordpress y luego lo extraeremos
![tercera imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_10_03.png)

Tras esto instalaremos apache2 y el servidor de mysql con los comandos que se ven en la terminal. (se puede ver que sale que no se han instalado porque me olvidé de hacerle captura cuando lo hice por primera vez)
![cuarta imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_13_39.png)

Iniciaremos sesión en root con el comando "su -" en caso de que ya esté definido el usuario root, en caso de que esto no sea así utilizaremos "sudo su".

Ya una vez como root entraremos como root en mysql, para lo cual no nos hará falta contraseña pues por algo somos los administradores del equipo.
![quinta imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_20_34.png)

crearemos la base de datos wordpress como se puede observar en la imagen: (si no ponemos ";" la orden no se ejecutará solamente indicando salto de linea)
![sexta imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_21_26.png)

Luego cambiaremos el plugin de autentificación del usuario root al tradicional de mysql, haciendo se consigue mejor compatibilidad con algunas herramientas más antiguas.
![septima imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_22_40.png)

Recargamos los privilegios y salimos del gestor mysql.
Procederemos a instalar una serie de dependencias (lo mismo que antes ya las tenía instaladas y se me olvidó hacer capturas por eso tuve que repetir)
![octaba imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_24_03.png)

Nos moveremos hasta la carpeta donde tengamos la carpeta de wordpress por la terminal, en mi caso Descargas.
Luego copiaremos la carpeta en cuestión en la dirección /var/www/html/ y todo su contenido con la opción -R (recursivo)
![novena imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_26_04.png)

Modificaremos los privilegios de acceso de la siguiente forma:
(No estamos intentando hacer un proceso seguro, simplemente la forma más básica de abrir un wordpress)
![decima imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_27_12.png)

Una vez hecho esto abriremos un navegador a nuestra elección y buscaremos "localhost/wordpress" para abrir nuestro servidor local.
Acto seguido clicaremos en continuar
![undecima imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_27_59.png)

Rellenaremos las siguientes cuestiones (importante recalcar que en este caso no hace falta contraseña pues iniciamos sesión como root, si intentamos iniciar con contraseña como en este caso nos dará error de autentificación)
![duodecima imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_30_47.png)

Si hacemos todo bien nos saldrá la siguiente pantalla y simplemente seguiremos adelante
![decimotercera imagen](VirtualBox_ubuntuServer_PracticaSGE_30_09_2025_23_36_24.png)


Rellenaremos otra vez los siguientes campos, podremos poner una contraseña poco segura habilitando la opción en la caja de abajo, no es una práctica nada recomendable sino que este es un ejemplo práctico.
![decimocuarta imagen](VirtualBox_ubuntuServer_PracticaSGE_01_10_2025_01_28_06.png)

Listo!!!. Wordpress queda instalado y podemos iniciar sesión con los datos que hemos rellenado anteriormente.
![decimoquinta imagen](VirtualBox_ubuntuServer_PracticaSGE_01_10_2025_01_28_38.png)
![decimosexta imagen](VirtualBox_ubuntuServer_PracticaSGE_01_10_2025_01_29_00.png)
