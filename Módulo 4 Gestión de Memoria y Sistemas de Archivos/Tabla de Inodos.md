>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Tabla de Inodos / Arreglo Maestro de Inodos

Silberschatz et al. (2018) describen este arreglo contiguo y estructurado de inodos asignados dentro de una partición específica del sistema de archivos desde su creación. Ocupa una región reservada del disco no volátil donde se reserva espacio fijo para almacenar los metadatos de cada archivo y directorio computable. El tamaño de la tabla de inodos determina el límite máximo estricto de archivos individuales que la partición puede contener, independientemente del espacio en gigabytes disponible. Se gestiona de forma transparente.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
