# ToCupboard WordPress Website

## Descripción

Este repositorio contiene el código fuente del sitio web de **ToCupboard**, una plataforma de e-commerce creada durante los primeros meses de la pandemia de Covid-19. El sitio web facilita la compra de productos de primera necesidad apoyando a pequeños comerciantes y fue desarrollado utilizando **WordPress** como CMS.

El propósito principal del repositorio es alojar y versionar los archivos necesarios para desplegar el sitio web, incluyendo el tema personalizado, configuraciones de seguridad bajo el modelo **DevSecOps**, y una simulación de una pasarela de pagos.

## Contenido del Repositorio

- **wp-admin/**: Archivos de administración de WordPress.
- **wp-content/**: Contiene los temas personalizados, plugins, y archivos subidos.
- **wp-includes/**: Archivos esenciales de WordPress.
- **index.php**: Archivo principal que carga el contenido del sitio.
- **wp-config.php**: Archivo de configuración para la base de datos y otras opciones.
- **.htaccess**: Archivo de configuración de Apache para URL amigables y reglas de seguridad.

## Requisitos Previos

Para ejecutar este proyecto, necesitarás:

- **Servidor Web** con soporte para PHP (como Apache).
- **Base de datos MySQL/MariaDB**.
- **WordPress** (descargado o clonado en el servidor).
- Acceso a una herramienta de gestión de bases de datos (como phpMyAdmin).
- Git (para clonar este repositorio).

## Pasos para Revisar y Ejecutar el Sitio Web

### 1. Clonar el Repositorio

Primero, clona este repositorio en el servidor donde deseas ejecutar el sitio:

``bash
git clone https://github.com/usuario/repositorio-wordpress.git

### 2. Subir los Archivos al Servidor
- Si trabajas en un servidor remoto, puedes subir los archivos utilizando FTP (como FileZilla) o clonar directamente en el servidor.
- Si trabajas en un servidor local (como XAMPP, WAMP, MAMP), copia los archivos al directorio correspondiente (por ejemplo, htdocs o www).

### 3. Configurar la Base de Datos
Crear la base de datos:

Usa phpMyAdmin u otra herramienta para crear una base de datos MySQL.
Importa el archivo .sql de la base de datos que fue exportado del sitio original (puedes encontrarlo en la carpeta /database/backup.sql).
Configurar wp-config.php:

Abre el archivo wp-config.php y ajusta las siguientes líneas con la información de la base de datos:

define('DB_NAME', 'nombre_base_datos');
define('DB_USER', 'usuario_base_datos');
define('DB_PASSWORD', 'contraseña_base_datos');
define('DB_HOST', 'localhost'); // O el servidor que estés utilizando

### 4. Configurar el Entorno de Seguridad
Certificado SSL: Asegúrate de que tu servidor esté configurado para utilizar HTTPS.
Plugins de Seguridad: El sitio viene preconfigurado con plugins de seguridad. Revisa las configuraciones en el panel de administración de WordPress.

### 5. Acceder al Sitio Web
Después de haber subido los archivos y configurado la base de datos, accede a la URL de tu servidor para verificar el correcto funcionamiento del sitio:

Si es un servidor remoto: (https://tocupboardponce.free.nf/shop/).
Si es un servidor local: [http://localhost/tocupboard](https://tocupboardponce.free.nf/shop/).

### Información Adicional
DevSecOps y Seguridad
Este proyecto sigue el modelo de DevSecOps con las siguientes características de seguridad:

- Integración de pruebas de seguridad automatizadas en el ciclo de desarrollo.
Cifrado HTTPS para la protección de datos.
Uso de plugins de seguridad para WordPress.
Configuraciones de acceso seguro a la base de datos.

- Simulación de Pasarela de Pagos
El sitio incluye una simulación de una pasarela de pagos que permite a los usuarios realizar pruebas de compras sin transacciones reales. 
La simulación valida la información de manera ficticia para asegurar el flujo de compra.
