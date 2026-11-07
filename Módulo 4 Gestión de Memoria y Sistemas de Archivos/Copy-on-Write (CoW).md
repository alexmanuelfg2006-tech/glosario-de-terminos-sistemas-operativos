>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
 Copy-on-Write (CoW) / Mecanismo de Copia en Escritura

Tanenbaum y Bos (2015) ponderan esta técnica de optimización donde los recursos compartidos de memoria o disco no se duplican físicamente hasta que un proceso intenta modificarlos. Inicialmente, múltiples procesos apuntan a las mismas páginas de memoria física en modo de solo lectura para ahorrar espacio en RAM. Cuando una tarea intenta ejecutar una escritura, el kernel intercepta la excepción, duplica únicamente esa página específica y le otorga una copia privada. Se utiliza ampliamente en la llamada al sistema fork() y en sistemas de archivos modernos.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
