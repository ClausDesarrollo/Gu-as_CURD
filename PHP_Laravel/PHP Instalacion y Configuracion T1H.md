# 🏢 **Guía Completa para la Instalación y Configuración de PHP en Windows 11**

---

## **¿Qué es PHP y para qué sirve?**

**PHP (Hypertext Preprocessor)** es un lenguaje de programación de propósito general, orientado principalmente al desarrollo web del lado del servidor. Es compatible con bases de datos como MySQL, PostgreSQL, y SQLite.

---

# **Proceso de Instalación y Configuración de PHP en Windows 11 (usando cmd)**

**Tiempo estimado:** 15 a 30 minutos 

---

## **1. Instalación de PHP en Windows 11**

### **Paso 1: Descargar PHP**
1. **Tiempo estimado:** 2-5 minutos.
   
   - Visita la página oficial de PHP en [https://windows.php.net/download/](https://windows.php.net/download/).
   - Descarga la última versión estable de PHP en formato ZIP (**Thread Safe** si piensas usar Apache).

### **Paso 2: Extraer PHP**
1. **Tiempo estimado:** 1-2 minutos.
   
   - Extrae el archivo ZIP descargado en una carpeta (ejemplo: `C:\php`).

### **Paso 3: Configurar Variables de Entorno en Windows (cmd)**

1. **Tiempo estimado:** 3-5 minutos.
   
   - Abre la consola de comandos (`cmd`) y ejecuta el siguiente comando para abrir el editor de variables del sistema:
     ```bash
     rundll32 sysdm.cpl,EditEnvironmentVariables
     ```
   - Busca la variable `Path` en "Variables del sistema" y agrega la ruta de la carpeta donde has instalado PHP (ejemplo: `C:\php`).

### **Paso 4: Verificar la Instalación**

1. **Tiempo estimado:** 1-2 minutos.
   
   - Abre una nueva consola de **cmd** y escribe:
     ```bash
     php -v
     ```
   - Si todo está bien, verás la versión de PHP instalada.

---

## **2. Actualizar PHP a la Última Versión (desde cmd)**

**Tiempo estimado:** 10-15 minutos

### **Paso 1: Verificar la Versión Actual**
   
   - Abre **cmd** y ejecuta:
     ```bash
     php -v
     ```
   - Esto te mostrará la versión actual de PHP instalada.

### **Paso 2: Descargar la Última Versión**
1. **Tiempo estimado:** 2-5 minutos.
   
   - Ve a la página oficial de PHP y descarga la última versión en formato **Thread Safe**.

### **Paso 3: Extraer y Actualizar Variables de Entorno**
1. **Tiempo estimado:** 5-7 minutos.
   
   - Extrae la nueva versión de PHP en una carpeta diferente (ejemplo: `C:\php-8.2`).
   - Modifica las **Variables de Entorno** para que apunten a la nueva carpeta:
     ```bash
     rundll32 sysdm.cpl,EditEnvironmentVariables
     ```
   - Cambia la ruta anterior de PHP (`C:\php`) por la nueva (`C:\php-8.2`).

### **Paso 4: Verificar la Nueva Versión**
1. **Tiempo estimado:** 1-2 minutos.
   
   - Abre una nueva consola **cmd** y ejecuta:
     ```bash
     php -v
     ```
   - Deberías ver la nueva versión instalada.

---

## **3. Configuración de PHP**

**Tiempo estimado:** 10-15 minutos

### **Paso 1: Configurar el archivo `php.ini`**
1. **Tiempo estimado:** 5-7 minutos.
   
   - Renombra `php.ini-development` a `php.ini` en la carpeta donde has instalado PHP.
   - Abre el archivo `php.ini` con un editor de texto y realiza las siguientes configuraciones:

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

### **Paso 2: Verificar Configuraciones**
1. **Tiempo estimado:** 2-3 minutos.
   
   - Ejecuta el siguiente comando en **cmd** para ver todas las configuraciones activas:
     ```bash
     php -i
     ```

### **Paso 3: Probar PHP con el Servidor Local**
1. **Tiempo estimado:** 2-3 minutos.
   
   - Ejecuta en **cmd** el siguiente comando para iniciar el servidor local embebido de PHP:
     ```bash
     php -S localhost:8000
     ```

   - Accede en tu navegador a `http://localhost:8000` y asegúrate de que PHP esté funcionando correctamente.

---

## **Resumen de Tiempo Estimado Total:**
- **Instalación de PHP**: 15-30 minutos.
- **Actualización de PHP**: 10-15 minutos.
- **Configuración de PHP**: 10-15 minutos.

