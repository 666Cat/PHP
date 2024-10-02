# INTEGRANTES:
# Rodrigo Veizaga Guzman
# Karen Lizarazu Colque


# Guía de Instalación y Configuración de XAMPP, PHP y Visual Studio Code

## 1. Instalación de XAMPP

XAMPP es un paquete de software que incluye Apache (servidor web), MySQL (sistema de gestión de bases de datos), PHP y Perl, diseñado para facilitar la configuración de un servidor local para pruebas de desarrollo web.

### Pasos de instalación:

- Descargar XAMPP desde la página oficial: [https://www.apachefriends.org/es/index.html](https://www.apachefriends.org/es/index.html).
- Ejecuta el instalador y sigue las instrucciones del asistente de instalación.
- Selecciona los componentes que necesitas (Apache, MySQL, PHP) y continúa con la instalación.
- Una vez instalado, abre el **Panel de Control de XAMPP** y arranca los servicios de Apache y MySQL.

## 2. Creación de Variables de Entorno

Para que puedas usar PHP desde la línea de comandos en cualquier ubicación, debes configurar las variables de entorno en tu sistema.

### En Windows:

1. Abre el **Panel de control** → **Sistema y seguridad** → **Sistema**.
2. Haz clic en **Configuración avanzada del sistema** → **Variables de entorno**.
3. En **Variables del sistema**, selecciona la variable `Path` y haz clic en **Editar**.
4. Añade una nueva ruta que apunte a la carpeta donde instalaste XAMPP, algo como `C:\xampp\php`.
5. Guarda los cambios y reinicia la terminal para que los cambios surtan efecto.

### En macOS/Linux:

1. Abre el archivo de configuración del terminal (`~/.bashrc`, `~/.zshrc`).
2. Añade la siguiente línea:
    ```bash
    export PATH="$PATH:/Applications/XAMPP/xamppfiles/bin"
    ```
3. Guarda el archivo y ejecuta `source ~/.bashrc` (o el archivo correspondiente).

## 3. Instalación de Visual Studio Code

### Pasos:

- Descargar Visual Studio Code: [https://code.visualstudio.com/](https://code.visualstudio.com/).
- Instálalo y ábrelo.

## 4. Extensiones útiles para Visual Studio Code

- **PHP Extension Pack**: Incluye soporte básico para PHP, autocompletado, resaltado de sintaxis, entre otras cosas. Puedes instalarlo desde la tienda de extensiones o ejecutando:
    1. Ve a **Extensiones** (icono de cuadro con líneas).
    2. Busca "PHP Extension Pack" y haz clic en **Instalar**.
    
- **PHP Intelephense**: Proporciona autocompletado avanzado, soporte para lenguajes de PHP, análisis de código, etc.
- **Live Server**: Abre un servidor en tiempo real en `localhost` para visualizar los cambios de tu código de manera instantánea.
- **Prettier**: Ayuda a dar formato al código automáticamente.

## 5. Configuración del Servidor para localhost

- Abre XAMPP y asegúrate de que el servicio de Apache está en ejecución.
- Por defecto, los archivos que quieras servir en tu servidor local deben estar en la carpeta `htdocs` de XAMPP (ubicada en `C:\xampp\htdocs` en Windows).
- Para acceder a tus archivos en el navegador, escribe `http://localhost/` seguido del nombre del archivo en el navegador (por ejemplo, `http://localhost/mi_archivo.php`).

## 6. Programa básico: "¡Hola mundo!"

Vamos a crear un archivo PHP simple que mostrará "¡Hola mundo!" en tu navegador.

### Pasos:

1. Abre Visual Studio Code y crea un archivo llamado `index.php` dentro de la carpeta `C:\xampp\htdocs` (o la carpeta correspondiente en tu sistema).
2. Escribe el siguiente código:
    ```php
    <?php
      echo "¡Hola mundo!";
    ?>
    ```
3. Guarda el archivo y abre tu navegador web.
4. Ve a `http://localhost/index.php`.

Si todo está configurado correctamente, deberías ver "¡Hola mundo!" en la pantalla del navegador.
