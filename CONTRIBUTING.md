# Flujo de trabajo de GitHub

**NUNCA MODIFICAR DIRECTAMENTE CODIGO DESDE PRODUCCION EN NINGUNA RAMA, NI TAMPOCO MODIFICAR LA RAMA master DE NINGUN REPOSITORIO**

### Palabras clave

* **Repositorio Remoto Publico (RRPU)**: Es lo que se encuentra en este repositorio remoto
* **Repositorio Remoto Personal (RRPE)**: Es lo que se genera cuando alguien hace un fork, cada desarrolador tendra el suyo.
* **Repositorio Local Personal (RLP)**: Es lo que tienes cuando haces clone de tu RRPE
* **Produccion**: Es el repositorio que se encuentra en los servidores donde se aloja cebsapp
* **PR**: Pull Request
* **Feature**: Funcionalidad

### Flujo

1. Para contribuir en este repositorio tendras que hacer un **fork**.
2. Despues tendras que **clonar** tu RRPE a tu computadora.
3. Realiza tus cambios para despues hacerles **commit** con una clara descripcion (en este commit tendras que escribir el numero de issue que solucionaste, si esto aplica)
4. Estos commit les daras **push** a tu RRPE
5. Ya con el RRPE actualizado, haras un **pull request** al RRPU
6. Si es aprovado tu PR, se hara un **merged** con tus cambios
7. Agregar el repositorio remoto de RRPU en tu RLP
   * git remote add RRPU https://github.com/Cebsa-inc/cebsapp
8. Crear la rama develop en tu RLP desde la rama del RRPU
   * git checkout -b develop rrpu/develop
9. Subir la rama develop de tu RLP a tu RRPE
   * git push -u origin develop

Con lo anterior podras hacer fetch de la rama develop de master con lo que tendras los cambios mas recientes y no te quedarás atrás con los commits, se seguiria la siguiente estructura de contribucion.

![Alt](https://i.stack.imgur.com/Lx7do.png)

### Encontraste un bug

1. Asegurate que el bug no haya sido reportado ya en un issue
2. Si no encuentras ningun issue con el bug que encontraste, entonces crea un nuevo issue. Asegura que el titulo y la descripcion tengan un clara descripcion, si crees que una screenshot ayudaria a entender el bug, porfavor adjuntala

### Proponer un feature o cambiar alguna existente

1. Comentalo con tus compañeros desarrolladores
2. No crees un issue hasta haber recibido un visto bueno. Los issue generalmente se crean cuando hay errores

### Actualizar RLP si esque RRPU se le agregaron commits

    git  pull rrpu develop

### Tarea programa que actualiza produccion

    git fetch url-repositorio
    git merge develop
    git push

### Guias de estilo

Estas guias de estilo solo son **SUGERENCIAS** de como debe ser escrito el codigo, esto para mejorar la lectura y evitar codigo duplicado.

* PHP
  * [PSR-1 basic coding standard](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md)
  * [PSR-2: Coding Style Guide](https://www.php-fig.org/psr/psr-2/)
* JS:
  * [Code Conventions for the JavaScript ](https://www.crockford.com/code.html)
  * [Google JavaScript Style Guide](https://google.github.io/styleguide/javascriptguide.xml)
* HTML/CSS:
  * [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html)
