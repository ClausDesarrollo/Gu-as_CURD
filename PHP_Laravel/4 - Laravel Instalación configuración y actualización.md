# **Guía Completa para la Instalación, Configuración y Actualización de Laravel en Windows 11 Home Single Language**

---

## **¿Qué es Laravel y para qué sirve?**

**Laravel** es un framework de desarrollo web basado en PHP, diseñado para hacer que el proceso de construcción de aplicaciones web sea más simple y rápido.
Proporciona una estructura robusta y herramientas preconstruidas para manejar tareas comunes como:

- enrutamiento
- autenticación de usuarios
- validación de formularios
- interacción con bases de datos

---

## **Objetivo**

Con esta guía detallada, podrás instalar, configurar y actualizar **Laravel** en tu sistema Windows 11 Home Single Language, además de aprender a crear un nuevo proyecto de Laravel rápidamente. El proceso incluye la instalación de PHP, Composer y la creación de tu primer proyecto en Laravel.

---

## **1. Instalación de Laravel en Windows 11 Home Single Language**

**Tiempo estimado:** 20-30 minutos (dependiendo de la velocidad de descarga)

---

### **Paso 1: Requisitos Previos**

1. **Instalar PHP**
   - Laravel requiere **PHP**. Si no lo tienes instalado, sigue los pasos de la [instalación de PHP](#) para hacerlo.
   - Verifica que PHP esté instalado correctamente ejecutando:
     ```bash
     php -v
     ```
   - Asegúrate de tener la versión de PHP recomendada por Laravel (PHP 8.1 o superior).

2. **Instalar Composer**
   - Laravel también depende de **Composer**, un gestor de dependencias de PHP.
   - Si aún no tienes Composer instalado, sigue los pasos de [instalación de Composer](#) para configurarlo.
   - Verifica que Composer esté instalado correctamente ejecutando:
     ```bash
     composer -V
     ```

### **Paso 2: Instalar Laravel a través de Composer**

1. **Tiempo estimado:** 5-10 minutos.
   
   - Abre **cmd** y navega hasta la carpeta donde deseas instalar tu proyecto Laravel. Por ejemplo:
     ```bash
     cd C:\xampp\htdocs
     ```
   - Ejecuta el siguiente comando para instalar el **instalador global de Laravel**:
     ```bash
     composer global require laravel/installer
     ```
   - Composer descargará el instalador de Laravel en tu entorno global, lo que te permitirá crear nuevos proyectos rápidamente.

### **Paso 3: Configurar Variables de Entorno para Laravel**

1. **Tiempo estimado:** 3-5 minutos.
   
   - Asegúrate de que la ruta donde se instaló el ejecutable de Laravel esté en tus variables de entorno. Generalmente, Composer guarda los archivos binarios en:
     ```bash
     C:\Users\[TU_USUARIO]\AppData\Roaming\Composer\vendor\bin
     ```
   - Añade esta ruta a la variable `Path` en las variables de entorno de Windows:
     1. Abre el buscador de Windows y escribe "Variables de entorno".
     2. Selecciona "Editar las variables de entorno del sistema".
     3. En la ventana que aparece, selecciona `Path` y haz clic en "Editar".
     4. Agrega la ruta mencionada anteriormente.

### **Paso 4: Crear tu Primer Proyecto en Laravel**

1. **Tiempo estimado:** 3-5 minutos.
   
   - Una vez configurado Laravel, puedes crear un nuevo proyecto fácilmente. Ve a la carpeta donde quieres crear tu proyecto y ejecuta:
     ```bash
     laravel new nombre-de-tu-proyecto
     ```
   - Este comando descargará Laravel y creará un nuevo proyecto en la carpeta `nombre-de-tu-proyecto`.

### **Paso 5: Iniciar el Servidor de Desarrollo**

1. **Tiempo estimado:** 1-2 minutos.
   
   - Navega a la carpeta del proyecto que acabas de crear:
     ```bash
     cd nombre-de-tu-proyecto
     ```
   - Ejecuta el siguiente comando para iniciar el servidor de desarrollo de Laravel:
     ```bash
     php artisan serve
     ```
   - Deberías ver un mensaje que te indica que el servidor está corriendo en `http://127.0.0.1:8000`. Abre tu navegador y accede a esta URL para ver tu proyecto de Laravel en funcionamiento.

---

## **2. Configuración Adicional de Laravel**

**Tiempo estimado:** 5-10 minutos

---

### **Paso 1: Configurar la Base de Datos**

1. **Tiempo estimado:** 5 minutos.
   
   - Laravel viene configurado por defecto para utilizar bases de datos como **MySQL**. Para configurarla, abre el archivo `.env` en la raíz de tu proyecto y ajusta las siguientes variables:
     ```env
     DB_CONNECTION=mysql
     DB_HOST=127.0.0.1
     DB_PORT=3306
     DB_DATABASE=nombre_de_tu_base_de_datos
     DB_USERNAME=tu_usuario
     DB_PASSWORD=tu_contraseña
     ```
   - Asegúrate de que MySQL esté corriendo en tu sistema y que los valores de conexión sean correctos.

### **Paso 2: Migrar la Base de Datos**

1. **Tiempo estimado:** 2-3 minutos.
   
   - Una vez que configures la conexión, puedes ejecutar las migraciones que Laravel incluye por defecto para crear las tablas necesarias en tu base de datos:
     ```bash
     php artisan migrate
     ```
   - Esto generará las tablas requeridas en tu base de datos MySQL.

---

## **3. Actualización de Laravel**

**Tiempo estimado:** 5-10 minutos

---

### **Paso 1: Verificar la Versión Actual de Laravel**

1. **Tiempo estimado:** 1 minuto.
   
   - Para verificar la versión de Laravel instalada en tu proyecto, abre **cmd** dentro de la carpeta de tu proyecto y ejecuta:
     ```bash
     php artisan --version
     ```

### **Paso 2: Actualizar las Dependencias del Proyecto con Composer**

1. **Tiempo estimado:** 3-5 minutos.
   
   - Si necesitas actualizar Laravel a una nueva versión, primero actualiza todas las dependencias del proyecto ejecutando:
     ```bash
     composer update
     ```
   - Esto actualizará las bibliotecas y paquetes que Laravel utiliza, incluyendo el propio framework si hay nuevas versiones disponibles.

### **Paso 3: Revisar la Documentación de Laravel**

1. **Tiempo estimado:** 1-2 minutos.
   
   - Si actualizas Laravel a una nueva versión, asegúrate de revisar la [documentación oficial de Laravel](https://laravel.com/docs) para ver si hay cambios que debas implementar en tu proyecto.

---

## **Resumen de Tiempo Estimado Total:**
- **Instalación de Laravel**: 20-30 minutos.
- **Configuración de Laravel**: 5-10 minutos.
- **Actualización de Laravel**: 5-10 minutos.

---
