>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
F2FS / Sistema de Archivos Flash-Friendly

Silberschatz et al. (2018) evalúan este sistema desarrollado específicamente para optimizar el rendimiento y preservar la vida útil de unidades basadas en memoria NAND flash (SSD y dispositivos móviles). Utiliza una estructura orientada a registros (Log-Structured File System) que agrupa las escrituras en bloques contiguos para minimizar el desgaste físico por ciclos de borrado. Incorpora mecanismos dinámicos de recolección de basura y alineación estricta con la arquitectura geométrica de las celdas flash. Se emplea ampliamente en teléfonos inteligentes y dispositivos embebidos.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
