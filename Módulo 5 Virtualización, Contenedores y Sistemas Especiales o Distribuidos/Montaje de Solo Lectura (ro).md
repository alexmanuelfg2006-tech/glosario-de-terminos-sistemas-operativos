>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Montaje de Solo Lectura (ro) / Montaje Protegido de Solo Lectura

Silberschatz et al. (2018) analizan esta propiedad de montaje de un sistema de archivos indicando que prohíbe cualquier operación de modificación, creación o eliminación de datos en la partición. Cualquier llamada al sistema que intente escribir en la estructura es rechazada de inmediato por el kernel con un error de protección. Esta configuración preserva la integridad de imágenes de sistemas operativos inmutables, particiones de rescate y medios de respaldo. Previene la alteración accidental o maliciosa del sistema base.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
