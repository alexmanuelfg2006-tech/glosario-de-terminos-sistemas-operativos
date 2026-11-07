>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
LZ4 / Algoritmo de Compresión LZ4

Tanenbaum y Bos (2015) destacan a este algoritmo por ofrecer una velocidad de descompresión extremadamente alta por núcleo de CPU, superando múltiples gigabytes por segundo por hilo. Aunque su tasa de compresión es ligeramente inferior a otros algoritmos pesados, su mínimo costo computacional lo hace idóneo para su uso en tiempo real. Se utiliza ampliamente en módulos del kernel como zRAM, zswap y en sistemas de archivos avanzados como Btrfs y ZFS. Optimiza el consumo de ancho de banda en discos físicos y reduce el uso de memoria RAM.


```
 ┌─────────────────────────────────────────────────────────┐
 │         Páginas Inactivas Enviadas al Sistema Swap      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Interceptadas por el controlador de zRAM)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Bloque Virtual en Memoria RAM               │
 │  * Compresión en tiempo real utilizando algoritmos      │
 │    como LZ4 o ZSTD (Reduce huella de memoria)           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Almacenamiento eficiente sin E/S de disco)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Ahorro Crítico de Espacio sin Lentos Accesos      │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
