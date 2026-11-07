>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
mmap() / Llamada a Sistema de Mapeo en Memoria

Silberschatz et al. (2018) describen cómo esta función mapea archivos o dispositivos de bloques directamente en el espacio de direcciones virtuales del proceso, agilizando enormemente el acceso a los datos. Permite manipular el contenido de un archivo en disco como si fuera un arreglo contiguo en memoria RAM, omitiendo llamadas a read() y write(). El kernel se encarga de cargar y volcar las páginas a disco de forma transparente mediante el subsistema de paginación por demanda. Se utiliza frecuentemente para cargar bibliotecas compartidas y bases de datos.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
