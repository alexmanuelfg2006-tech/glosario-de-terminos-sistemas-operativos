>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
zRAM / Módulo de Intercambio en RAM

Tanenbaum y Bos (2015) explicitan el funcionamiento de este módulo que crea un dispositivo de bloques virtual en RAM para comprimir al vuelo los datos enviados al área de intercambio (swap). Al redirigir las páginas de memoria inactivas hacia este búfer comprimido, multiplica la capacidad efectiva de la RAM disponible en dispositivos con recursos limitados. Evita los severos retardos de entrada/salida provocados por el swap hacia discos magnéticos o memorias eMMC lentas.

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
