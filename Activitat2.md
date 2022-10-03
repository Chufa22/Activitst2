# Activitat 2: Owncloud

SMX-B MP08

####  Alumnes
* Marc Muria 
* Corneliu Miron

#### Professor
* Javier Sancho 

# Índex
##### Instalar Apache
##### Instalar MariaDB
##### Crear la base de datos de owncloud
##### Instalar PHP y sus módulos necesarios
##### Instalamos Owncloud
##### Configurar Apache
##### Acceder a Owncloud desde fuera de nuestro equipo

# Instalar Apache
##### Instalar el servidor Apache:
![imatge](com1.png)

##### Desactivamos el listado de directorios del servidor:
![imatge](com2.png)

# Instalar MariaDB

##### Instalamos MariaDB:   
![imatge](com3.png)

##### Y configuramos la instalación:
![imatge](com4.png)

##### Aquí es interesante:

* Deshabilitar usuarios anónimos.
* Deshabilitar acceso remoto como root.
* Eliminar las bases de datos de testeo y el acceso a las mismas.
* Actualizar las tablas de privilegios.

##### Por último reiniciamos el servidor MariaDB.
![imatge](com5.png)

# Crear la base de datos de owncloud

##### Entramos en MariaDB:
![imatge](com6.png)

##### Creamos la base de datos:
![imatge](com7.png)

##### Creamos un usuario llamado ownclouduser con una contraseña que podría ser Admin1234.
![imatge](com8.png)

##### Le damos acceso al usuario a la base de datos creada:
![imatge](com9.png)

##### Aplicamos los cambios y salimos:
![imatge](com10.1.png)
![imatge](com10.2.png)

# Instalar PHP y sus módulos necesarios
![imatge](com11.1.png)

##### Actualizamos los paquetes con el repositorio añadido:
![imatge](com11.2.png)

##### Instalamos PHP y los módulos necesarios:

##### Hemos de tener en cuenta los requisitos de Owncloud antes de instalar los módulos.
![imatge](com11.3.png)

##### Después de la instalación editamos el fichero php.ini y cambiaremos algunos valores:
![imatge](com11.4.png)

##### Los valores que hemos de cambiar son los siguientes:
* file_uploads = On
* allow_url_fopen = On
* memory_limit = 256M
* upload_max_filesize = 100M
* display_errors = Off
* date.timezone = Europe/Madrid

# Instalamos Owncloud

##### Descargamos la última versión del programa y descomprimimos los ficheros, además movemos los archivos de Owncloud a "/var/www/html/owncloud".
![imatge](com12.png)

##### Cambiamos propietario y permisos de los directorios de owncloud. www-data para que los pueda usar Apache, 755 para que los pueda ejecutar y leer cualquier usuario de Linux:
![imatge](com13.png)

# Configurar Apache:

##### Vamos a configurar Apache:
![imatge](com14.1.png)

##### Debemos dejar un fichero como el siguiente, pero cambiando el ServerName y el ServerAlias por los nombres y alias de nuestro propio dominio.
![imatge](com14.2.png)

##### Habilitamos owncloud y el módulo rewrite:
![imatge](com15.png)

##### Reiniciamos Apache:
![imatge](com16.png)
