>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
ext4 / Cuarto Sistema de Archivos Extendido

Tanenbaum y Bos (2015) revisan la arquitectura de esta estructura de disco predeterminada en múltiples distribuciones Linux, destacando por su uso de extents, journaling y asignación diferida de bloques. La introducción de extents reemplaza los bloques contiguos tradicionales por rangos extensos de almacenamiento, mejorando la velocidad de lectura de archivos grandes. Admite volúmenes de datos de hasta 1 Exabyte y archivos individuales de 16 Terabytes con retrocompatibilidad hacia ext2 y ext3. Su mecanismo de asignación diferida reduce significativamente la fragmentación de la unidad.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
