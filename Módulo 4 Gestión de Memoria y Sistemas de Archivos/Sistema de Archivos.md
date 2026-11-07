>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Sistema de Archivos / Organizador de Almacenamiento

Silberschatz et al. (2018) conceptualizan esta estructura lógica como el conjunto de algoritmos que organiza, nombra, guarda y recupera la información física guardada en almacenamiento secundario. Traduce las lecturas y escrituras de archivos conceptuales en direcciones de sectores o bloques físicos de la unidad SSD o disco duro. Gestiona el espacio libre, la estructura de directorios, los metadatos y la recuperación ante fallos mediante journaling o Copy-on-Write. Ejemplos prominentes son ext4, Btrfs, NTFS y ZFS.


```
 ┌─────────────────────────────────────────────────────────┐
 │             Solicitudes de Aplicaciones / Usuarios      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Llamadas a la API del Kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Capa del Sistema de Archivos                │
 │  * Directorios, Nombres de Archivo, Inodos y Metadatos   │
 │  * Traducción lógica a bloques físicos de disco         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Operaciones de bloques)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Dispositivo de Almacenamiento (HDD / SSD)   │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
