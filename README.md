# Instrucciones

### 1.- Tener instalado composer y docker

https://docs.docker.com/desktop/windows/install/

* Docker Desktop se tiene que ejecutar como administrador
* Descargue el paquete de actualizacion del kernel de Linux
  https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-using-the-repository

### 2.- Crear archivo de seguridad

* En la raiz del directorio crear un archivo llamado **security.php** y adentro de él declarar la informacion sensible de las conexiones a la base de datos y cualquier otro tipo de información. Ejemplo:

```php
<?php
    $MYSQL_ROOT_PASSWORD= 'PONER VALOR AQUI';
  
    $FIREBIRD_ROOT_PASSWORD = 'PONER VALOR AQUI';
    $FIREBIRD_HOST = 'PONER VALOR AQUI';
    $FIREBIRD_USER = 'PONER VALOR AQUI';
    $FIREBIRD_PATH = 'PONER VALOR AQUI';

    $KMAIL_PASSWORD = 'PONER VALOR AQUI';
?>
```

### 3.- Pegue los archivos .sql al directorio dump/  e importelos con ayuda del archivo /dump/README.md

### 4.- Inicialice los contenedores:

    docker-compose up --build

### 5.- Configurar tu administrador de bases de datos para conectarte a MySQL local.

* Los datos de conexion estan en el archivo docker-compose.yml
* En el archivo .dbp viene los datos de conexion de las bases de datos para DBeaber

### Comandos utiles:

    docker ps:
        Muestra los contenedores activos
    docker-compose stop:
        Detiene los contenedores activos
    docker-compose up:
        Inicia los contenedores

# Links:

http://localhost:8001/index.html
