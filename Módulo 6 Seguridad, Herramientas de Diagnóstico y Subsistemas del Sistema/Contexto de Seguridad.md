>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Contexto de Seguridad / Atributos de Control de Acceso

Tanenbaum y Bos (2015) denominan así al conjunto de variables de etiquetado (usuario, rol, tipo y nivel de confidencialidad) asignadas a procesos u objetos en sistemas MAC. El núcleo del sistema operativo consulta constantemente estas etiquetas para decidir si un proceso posee la autorización requerida para leer o modificar un archivo. En arquitecturas como SELinux, el contexto de seguridad se almacena dentro de los metadatos extendidos del sistema de archivos. Este mecanismo asegura una aplicación incondicional de las políticas de seguridad del administrador.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
