>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Punto de Montaje / Mount Point

Silberschatz et al. (2018) definen esta ubicación dentro de la jerarquía de directorios como el nodo a través del cual se accede a un sistema de archivos secundario previamente montado. Al acoplar una partición de disco o unidad de red a una carpeta existente (como /mnt/disco), los contenidos de dicha partición sustituyen visualmente al directorio base. El VFS intercepta las solicitudes a esa ruta para redirigir las operaciones de entrada/salida hacia el controlador del nuevo volumen de datos.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
