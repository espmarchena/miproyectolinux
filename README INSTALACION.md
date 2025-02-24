Me he apoyado en [Aprende a instalar PHP Symfony Framework en Linux](https://www.youtube.com/watch?v=Ij4NQ0DHlcE&list=PLDbrnXa6SAzUYxocB3jC81TfvWUynAppf&index=2)

**A continuación detallo paso a paso cómo he realizado la instalación de php, git y symfony y creado mi proyecto en mi VB con Linux**

------

### INSTALAR PHP 

- Con `sudo add-apt-repository ppa:ondrej/php` descargo PHP en mi VB Linux directamente desde un repositorio que mantienen actualizándose y así evito multiples instalaciones de php en mi SO.
![Image](https://github.com/user-attachments/assets/a5a5d6c5-8b4f-438c-9b5e-15290230f6cc)

- Ejecuto `sudo apt update` para refrescar y actualizar los repositorios
- Ejecuto `sudo apt install php7.4` para empezar el proceso de instalación
![Image](https://github.com/user-attachments/assets/12c462f9-0812-46ce-adb8-8b3b8a5ad1dc)

- Me dirijo a la web de [Composer ](https://getcomposer.org/) para descargarlo para Linux donde encuentro el proceso de instalación:

- Comando que me permite descargar el composer setup `php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"`
`pwd` para ver en qué ruta estoy
- Comando `ls` para comprobar que está ahí
- Para validar que el paquete esté bien descargado: `php -r "if (hash_file('sha384', 'composer-setup.php') === 'dac665fdc30fdd8ec78b38b9800061b4150413ff2e3b6f88543c636f7cd84f6db9189d43a81e5503cda447da73c7e5b6') { echo 'Installer verified'.PHP_EOL; } else { echo 'Installer corrupt'.PHP_EOL; unlink('composer-setup.php'); exit(1); }"
`php -v` para verificar que está instalado
- Ejecuto `php composer-setup.php --install-dir=/usr/local/bin --filename=composer` para ejecutar el script e instalar php, especificando el directorio donde se instalará y definiendo el nombre del archivo.
`composer` para verificar la instalación correcta
![Image](https://github.com/user-attachments/assets/4df965b9-eecb-4412-b85e-809b5e8faee3)

------

### INSTALAR GIT

- Ejecuto `sudo apt install git` para instalar git directamente de los repositorios oficiales del SO, que será la siguiente herramienta que necesito antes de proceder con la instalación de Symfony
También uso el comando `sudo apt upgrade` para actualizar los paquetes disponibles de actualización
![Image](https://github.com/user-attachments/assets/355caa72-819f-475d-839d-3fde8fd9a0a4)

-------

### INSTALAR SYMFONY

- Ejecuto `wget https://get.symfony.com/cli/installer -O - | bash` que me facilita la [web oficial de Symfony](https://symfony.com/download)en el apartado de Linux. Este comando descarga el instalador directamente de la url facilitada, y pasa su contenido directamente a Bash para ejecutarlo.
![Image](https://github.com/user-attachments/assets/df3b52df-fa1f-413a-9c1e-505827e7b3a7)

-Lo muevo a la carpeta del sistema con el comando que me ofrece la terminal tras la instalación: `sudo mv /home/codearts/.symfony5/bin/symfony /usr/local/bin/symfony`
-Para validar que se ejecuta correctamente `symfony`
![Image](https://github.com/user-attachments/assets/35a06810-ecad-4133-91f6-0d86036dfea4)

----

### CREAR MI PROYECTO SYMFONY

- Creo un directorio raíz para contener mi proyecto `mkdir miproyectosymfony` y entro en ella con `cd miproyectosymfony`
![Image](https://github.com/user-attachments/assets/b649f61c-dcf5-4aed-baba-8d6db005c66b)

- Creo un nuevo proyecto Symfony `symfony new miproyecto`, lo que va a descargar y configurar Symfony en la carpeta miproyecto,  instalar las dependencias necesarias usando composer y generar la estructura básica del proyecto con los archivos y carpetas recomendadas por Symfony.
![Image](https://github.com/user-attachments/assets/f461277b-e28a-42cc-a235-4261d19f3fe0)

- Podemos ejecutar de nuevo el comando de lectura `ls` para corroborar que se ha creado y `ls -a` para que muestre al detalle, en este caso la estructura que ha creado:
![Image](https://github.com/user-attachments/assets/de04325b-818d-4038-a715-3dd891448205)

- Inicio el proceso de ejecución del symfony cli dentro del proyecto con `symfony server:start` para ver el servidor local en `http://127.0.0.1:8000`
![Image](https://github.com/user-attachments/assets/d5b76399-8bc3-4ff6-ad42-b8edca8f10d0)
