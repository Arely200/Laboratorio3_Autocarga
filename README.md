# LABORATORIO: IMPLEMENTACIÓN DE LA CARGA AUTOMÁTICA (AUTOLOAD) - PSR-4

**Estudiante:** Arely Mendoza  
**Materia:** Desarrollo de Software VII  
**Facultad:** FISC - UTP

---

Este proyecto demuestra la implementación exitosa de un mapa de **CARGA AUTOMÁTICA** utilizando **Composer** y el estándar **PSR-4**, eliminando el uso de `include` y `require` manuales para lograr una **REFACTORIZACIÓN** eficiente del código.

## GUÍA DE INSTALACIÓN
Para que el proyecto funcione correctamente al clonarlo o descargarlo, se debe seguir este paso obligatorio:

1. Abrir la terminal en la carpeta raíz del proyecto (`C:\Users\arely\autocarga`).
2. Ejecutar el siguiente comando para generar localmente la carpeta `vendor/` y el mapa de carga:

```bash
composer dump-autoload
ESTRUCTURA DE ARCHIVOS Y NAMESPACES
Siguiendo el estándar PSR-4, se ha definido la siguiente relación lógico-física en el archivo composer.json:

NAMESPACE PREFIJO: App\ (Nombre lógico para las clases).

RUTA FÍSICA: src/ (Carpeta donde reside el código).

MAPEO: La clase lógica App\Usuario está vinculada directamente al archivo físico src/Usuario.php.

PRUEBA DE EJECUCIÓN
El sistema ha sido refactorizado satisfactoriamente. El archivo index.php actúa como punto de entrada y demuestra la instanciación de objetos sin errores:

PHP
<?php
// Carga del autoloader único
require_once 'vendor/autoload.php';

// Importación de la clase mediante Namespace
use App\Usuario;

// Instanciación exitosa
$user = new Usuario();

// Resultado esperado: ¡La clase Usuario se cargó automáticamente usando PSR-4!
?>
CONCLUSIONES TÉCNICAS
MANTENIBILIDAD: La carga automática permite escalar el proyecto agregando nuevas clases en la carpeta src/ sin necesidad de modificar archivos de configuración globales o añadir múltiples sentencias include en cada script.

EFICIENCIA DE MEMORIA: Mediante el mecanismo de LAZY LOADING, PHP solo carga en memoria los archivos de las clases en el momento exacto en que son instanciadas, optimizando el rendimiento del servidor.

ESTANDARIZACIÓN: El cumplimiento del estándar PSR-4 garantiza la interoperabilidad del código y facilita el trabajo colaborativo, permitiendo que cualquier desarrollador comprenda la estructura del proyecto de forma inmediata.


---

### ¿Cómo lo actualizas en GitHub?

1.  En VS Code, abre el archivo `README.md`.
2.  Borra todo y pega lo que te acabo de dar.
3.  **Guarda el archivo** (`Ctrl + S`).
4.  En la terminal de VS Code, escribe estos 3 comandos para subir el cambio:

