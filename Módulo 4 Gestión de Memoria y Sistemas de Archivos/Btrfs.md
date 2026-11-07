>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Sistema de Archivos B-tree / B-tree File System

Silberschatz et al. (2018) destacan las propiedades de este sistema de archivos avanzado Copy-on-Write (CoW) para Linux que integra soporte nativo para snapshots, subvolúmenes y compresión al vuelo. Emplea estructuras de datos B-trees para organizar metadatos y bloques de datos con suma de comprobación (checksumming) continua para detectar corrupción silenciosa. Su arquitectura permite extender o reducir volúmenes de almacenamiento en caliente sin desmontar las particiones activas. Además, proporciona capacidades de autorreparación y deduplicación ideales para servidores de almacenamiento masivo.

---
**Referencia:**
 Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
