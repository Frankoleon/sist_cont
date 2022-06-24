**En esta carpeta debe pegar el archivo o los archivos .sql de las bases de datos de MySQL**

# Importación de datos a tu MySQL local

### 1. Debe tener los archivos dump de las dases de datos que necesite, estas tienen que estar en UTF-8.
* Ir al servidor de amazon/produccion
* Abrir la terminal (puede ser la de VS Code)
* Tienes 2 opciones apartir de aqui
    1. Primer opcion
        * Ejecutar el siguiente comando:
            mysqldump -u root -p [nombre-de-la-database-en-produccion] > [nombre_del_archivo].sql 
        * Abrir el archivo generado en el bloc de notas y guardarlo como UTF-8
    2. Segunda opcion
        * Ejecutar el siguiente comando
            mysqldump -u root -p [nombre-de-la-database-en-produccion] -r [nombre_del_archivo].sql

### 2. Entrar al contenedor de MySQL con el comando bash
    docker exec -it mysql bash

### 3. Irse a directorio docker-entrypoint-initdb.d/
    cd docker-entrypoint-initdb.d/

### 4. Crear las bases de datos
    mysql -u root -p
    test
    create database pedidosalmacen;
    create database sae;
    create database sistemanomina_prueba;
    exit;

### 5. Importar los datos de los archivos .sql a las bases de datos del contenedor MySQL
    mysql -u root -p pedidosalmacen < pedidosalmacen.sql
    test
    mysql -u root -p sae < sae.sql
    test
    mysql -u root -p sistemanomina_prueba < sistemanomina_prueba.sql
    test