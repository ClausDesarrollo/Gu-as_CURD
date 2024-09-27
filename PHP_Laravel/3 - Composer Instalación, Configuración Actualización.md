# **Guía de Instalación, Configuración y Actualización Composer**

---

## **¿Qué es Composer y para qué sirve?**

**Composer** es un gestor de dependencias para PHP que permite instalar, actualizar y manejar las bibliotecas y paquetes necesarios para un proyecto. 
Funciona a través de un archivo `composer.json` que especifica las dependencias del proyecto, garantizando que todas las bibliotecas utilizadas estén en las versiones correctas y funcionando sin conflictos.
---

## **1. Instalación de Composer en Windows 11 Home Single Language**

**Tiempo estimado:** 10 a 15 minutos (dependiendo de la velocidad de descarga)

---

### **Paso 1: Requisitos Previos - Instalar PHP**

1. **Tiempo estimado:** 5-10 minutos.
   - **Composer requiere PHP** para funcionar, por lo que es importante que tengas instalado PHP en tu sistema. Si no lo has hecho ya, sigue los pasos anteriores para [instalar PHP](https://www.php.net/downloads).
   - Asegúrate de que PHP esté configurado correctamente y que puedas verificar la instalación ejecutando en la consola de **cmd**:
     ```bash
     php -v
     ```

### **Paso 2: Descargar el Instalador de Composer**

1. **Tiempo estimado:** 2-5 minutos.
   
   - Visita el sitio oficial de Composer en [https://getcomposer.org/](https://getcomposer.org/).
   - Haz clic en "Download" y luego selecciona el **instalador de Composer para Windows**.
   - Se descargará un archivo ejecutable: `Composer-Setup.exe`.

### **Paso 3: Ejecutar el Instalador de Composer**

1. **Tiempo estimado:** 3-5 minutos.
   
   - Abre el archivo descargado (`Composer-Setup.exe`).
   - Durante el proceso de instalación, selecciona la ubicación del archivo **PHP.exe** (usualmente se encuentra en `C:\php\php.exe` o dentro de XAMPP en `C:\xampp\php\php.exe`).
   - Composer intentará detectar la ubicación de PHP automáticamente. Si no lo hace, selecciona manualmente la ruta del ejecutable PHP.
   - Completa la instalación siguiendo los pasos del asistente.

### **Paso 4: Verificar la Instalación de Composer**

1. **Tiempo estimado:** 1-2 minutos.
   
   - Abre **cmd** y ejecuta el siguiente comando para asegurarte de que Composer se haya instalado correctamente:
     ```bash
     composer
     ```
   - Deberías ver una lista de comandos y opciones disponibles de Composer si la instalación ha sido exitosa.

---

## **2. Configuración de Composer en Windows 11**

**Tiempo estimado:** 5-10 minutos

---

### **Paso 1: Configurar Variables de Entorno**

1. **Tiempo estimado:** 3-5 minutos.
   
   - Abre **cmd** y escribe el siguiente comando para abrir el editor de variables de entorno:
     ```bash
     rundll32 sysdm.cpl,EditEnvironmentVariables
     ```
   - En "Variables del sistema", busca la variable `Path` y asegúrate de que la ruta donde instalaste **Composer** esté incluida (por ejemplo: `C:\ProgramData\ComposerSetup\bin` o `C:\Users\[TU_USUARIO]\AppData\Roaming\Composer\vendor\bin`).
   - Si no está, agrega la ruta a la lista de variables.

### **Paso 2: Verificar la Configuración**

1. **Tiempo estimado:** 1-2 minutos.
   
   - Abre una nueva consola de **cmd** y ejecuta:
     ```bash
     composer
     ```
   - Verifica que **Composer** funcione correctamente mostrando la lista de comandos. Esto confirmará que la configuración de variables de entorno está bien configurada.

---

## **3. Actualización de Composer en Windows 11**

**Tiempo estimado:** 5-10 minutos

---

### **Paso 1: Comprobar la Versión Actual de Composer**

1. **Tiempo estimado:** 1-2 minutos.
   
   - Para verificar la versión actual de Composer instalada, abre **cmd** y ejecuta:
     ```bash
     composer -V
     ```
   - Esto te mostrará la versión instalada de Composer.

### **Paso 2: Actualizar Composer desde la Consola**

1. **Tiempo estimado:** 3-5 minutos.
   
   - Si deseas actualizar Composer a la última versión, abre **cmd** y ejecuta el siguiente comando:
     ```bash
     composer self-update
     ```
   - Composer buscará la última versión estable y actualizará automáticamente. Si todo funciona correctamente, recibirás un mensaje de éxito.

### **Paso 3: Verificar la Nueva Versión**

1. **Tiempo estimado:** 1-2 minutos.
   
   - Después de la actualización, puedes verificar que tienes la última versión ejecutando nuevamente:
     ```bash
     composer -V
     ```
   - Asegúrate de que la versión mostrada sea la más reciente.

---

## **Resumen de Tiempo Estimado Total:**
- **Instalación de Composer**: 10-15 minutos.
- **Configuración de Composer**: 5-10 minutos.
- **Actualización de Composer**: 5-10 minutos.
