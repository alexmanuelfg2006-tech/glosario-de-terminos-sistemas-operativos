>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
ZSTD / Algoritmo de Compresión Zstandard

Silberschatz et al. (2018) analizan las métricas de este algoritmo desarrollado para brindar altas tasas de compresión de datos a gran velocidad en Btrfs, zswap y entornos en tiempo real. Ofrece una flexibilidad excepcional permitiendo ajustar niveles de compresión desde modos ultra-rápidos hasta niveles de densidad equivalentes a LZMA. Su algoritmo de descompresión es extremadamente rápido e independiente del nivel de compresión seleccionado. Es la norma en compresión de imágenes y kernels modernos.

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
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
