>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
NTFS / Sistema de Archivos de Nueva Tecnología

Silberschatz et al. (2018) caracterizan este sistema de archivos propietario de Microsoft Windows por su soporte para permisos ACL, cifrado, compresión y journaling. Emplea la Tabla Maestra de Archivos (MFT) para indexar de manera eficiente la ubicación de cada objeto en la unidad de disco. Su mecanismo de registro de transacciones garantiza una recuperación rápida ante cortes de energía, manteniendo la integridad del volumen. Aunque fue diseñado para Windows, el kernel de Linux incluye controladores avanzados (ntfs3) para su lectura y escritura.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
