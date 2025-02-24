![Image](https://github.com/user-attachments/assets/9f68a158-6bc8-4f94-87c1-610292444523)

### 📂 Estructura de carpetas de un proyecto Symfony
📁 **miproyecto/** (Directorio raíz del proyecto)
│── 📁 **assets/** → Contiene archivos frontend como CSS, JS e imágenes.
│── 📁 **bin/** → Archivos ejecutables del proyecto, como console para ejecutar comandos de Symfony.
│── 📁 **config/** → Configuraciones de la aplicación (rutas, bases de datos, servicios, seguridad, etc.).
│── 📁 **migrations/** → Archivos de migraciones de la base de datos generados por Doctrine.
│── 📁 **public/** → Punto de entrada público (contiene index.php y assets compilados).
│── 📁 **src/** → Código fuente de la aplicación (controladores, entidades, servicios, etc.).
│── 📁 **templates/** → Vistas en Twig (.html.twig) para la renderización de HTML.
│── 📁 **translations/** → Archivos de traducción para internacionalización (.yaml, .xlf).
│── 📁 **var/** → Archivos temporales como logs, caché y sesiones.
│── 📁 **vendor/** → Librerías de Composer (Symfony y paquetes externos).
│── 📁 **tests/** → Pruebas unitarias y funcionales.
│── 📄 **composer.json** → Dependencias PHP del proyecto (usado por Composer).
│── 📄 **package.json** → Dependencias frontend (si se usa Webpack Encore).
│── 📄 **symfony.lock** → Bloqueo de dependencias para mantener versiones estables.
│── 📄 **.env** → Variables de entorno (base de datos, API keys, configuración).
│── 📄 **.gitignore** → Lista de archivos/carpetas que no deben subirse a Git.
