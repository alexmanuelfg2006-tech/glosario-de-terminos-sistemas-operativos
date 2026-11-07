>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
munmap() / Llamada a Sistema de Desmapeo

Silberschatz et al. (2018) detallan el rol de esta llamada al sistema encargada de liberar la región de memoria virtual previamente reservada o mapeada mediante mmap(). Al ejecutar esta función, el kernel actualiza las tablas de paginación del proceso y desasocia las páginas de memoria física correspondientes. Si las páginas modificadas estaban respaldadas por un archivo en disco, los cambios se confirman en el almacenamiento no volátil. Evita fugas de espacio en la memoria virtual del proceso y optimiza los recursos de RAM.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
