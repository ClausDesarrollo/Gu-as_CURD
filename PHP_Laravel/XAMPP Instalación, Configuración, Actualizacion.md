# **Guía Completa para la Instalación de PHP con XAMPP en Windows 11**

---

## **¿Qué es PHP y para qué sirve?**

**PHP (Hypertext Preprocessor)** es un lenguaje de programación utilizado principalmente en el desarrollo web para crear aplicaciones del lado del servidor. 

---

## **Proceso de Instalación y Configuración de PHP con XAMPP en Windows 11**

**Tiempo estimado:** 10 a 20 minutos (dependiendo de la velocidad de descarga y la instalación)

---

## **1. Instalación de XAMPP en Windows 11**

### **Paso 1: Descargar XAMPP**
1. **Tiempo estimado:** 2-5 minutos.
   
   - Ve al sitio oficial de XAMPP: [https://www.apachefriends.org/es/index.html](https://www.apachefriends.org/es/index.html).
   - Descarga la última versión de XAMPP que incluye PHP, MySQL, y Apache.

### **Paso 2: Ejecutar el Instalador de XAMPP**
1. **Tiempo estimado:** 5-10 minutos.
   
   - Abre el instalador descargado (`xampp-windows-x64-VERSION-installer.exe`).
   - Selecciona los componentes que deseas instalar. Para ejecutar PHP, asegúrate de que las opciones **Apache** y **PHP** estén marcadas.
   - Elige el directorio de instalación (por defecto: `C:\xampp`).

### **Paso 3: Completar la Instalación**
1. **Tiempo estimado:** 2-5 minutos.
   
   - Sigue las instrucciones en pantalla y espera a que finalice la instalación.
   - Una vez completada, abre el **Panel de Control de XAMPP**.

---

## **2. Configuración de PHP con XAMPP**

**Tiempo estimado:** 5-10 minutos

### **Paso 1: Iniciar Apache**
1. **Tiempo estimado:** 1-2 minutos.
   
   - Abre el **Panel de Control de XAMPP**.
   - Haz clic en "Start" en la línea de **Apache** para iniciar el servidor web que manejará las peticiones PHP.

### **Paso 2: Configurar el archivo `php.ini`**
1. **Tiempo estimado:** 5-7 minutos.
   
   - En el **Panel de Control de XAMPP**, haz clic en "Config" junto a **Apache** y selecciona "PHP (php.ini)" para abrir el archivo de configuración de PHP.
   - Realiza las siguientes configuraciones en el archivo `php.ini`:

     - Establecer la zona horaria:
       ```ini
       date.timezone = America/Mexico_City
       ```

     - Configurar el límite de subida de archivos:
       ```ini
       upload_max_filesize = 50M
       ```

     - Habilitar extensiones necesarias como **MySQL**:
       ```ini
       extension=pdo_mysql
       extension=mysqli
       ```

### **Paso 3: Verificar la Instalación de PHP**
1. **Tiempo estimado:** 1-2 minutos.
   
   - Crea un archivo `phpinfo.php` en la carpeta `C:\xampp\htdocs` con el siguiente contenido:
     ```php
     <?php
     phpinfo();
     ?>
     ```
   - Abre tu navegador web y accede a `http://localhost/phpinfo.php`. Deberías ver una página con la información de la configuración de PHP.

---

## **3. Actualización de PHP en XAMPP**

**Tiempo estimado:** 10-15 minutos

### **Paso 1: Descargar la Última Versión de PHP**
1. **Tiempo estimado:** 2-5 minutos.
   
   - Ve al sitio oficial de PHP en [https://windows.php.net/download/](https://windows.php.net/download/) y descarga la última versión en formato **Thread Safe** (compatible con Apache).

### **Paso 2: Actualizar PHP en XAMPP**
1. **Tiempo estimado:** 5-7 minutos.
   
   - Ve a la carpeta de instalación de XAMPP (por ejemplo, `C:\xampp`).
   - Renombra la carpeta `php` a `php_old` como respaldo.
   - Extrae la nueva versión de PHP que descargaste y cópiala en la carpeta `C:\xampp`, renombrando la carpeta extraída a `php`.

### **Paso 3: Actualizar el Archivo `php.ini`**
1. **Tiempo estimado:** 3-5 minutos.
   
   - Copia el archivo `php.ini` que configuraste previamente desde la carpeta `php_old` y pégalo en la nueva carpeta `php`, sobrescribiendo el existente.

### **Paso 4: Reiniciar Apache**
1. **Tiempo estimado:** 1-2 minutos.
   
   - En el **Panel de Control de XAMPP**, detén y vuelve a iniciar Apache para que los cambios surtan efecto.

---

## **Resumen de Tiempo Estimado Total:**
- **Instalación de XAMPP**: 10-20 minutos.
- **Actualización de PHP en XAMPP**: 10-15 minutos.
- **Configuración de PHP**: 5-10 minutos.
