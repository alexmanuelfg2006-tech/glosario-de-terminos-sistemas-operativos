>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
VFS / Sistema de Archivos Virtual

Tanenbaum y Bos (2015) detallan la arquitectura de esta capa de abstracción del kernel de Linux que permite a los programas de usuario acceder de forma transparente a múltiples sistemas de archivos. Exporta una interfaz POSIX unificada de llamadas al sistema (como open(), read(), write()) ocultando las diferencias estructurales internas entre ext4, NTFS, Btrfs o NFS. Redirige dinámicamente las operaciones a los controladores específicos de cada volumen montado. Simplifica enormemente la gestión de almacenamiento.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
