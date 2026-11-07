>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Hilos a Nivel de Kernel / Kernel-Level Threads (KLT)

Según Stallings (2017), los hilos de kernel son hilos reconocidos y administrados directamente por el sistema operativo, permitiendo que múltiples hilos del mismo proceso se ejecuten simultáneamente en distintos procesadores de un sistema multiprocesador. Son hilos administrados directamente por el kernel del sistema operativo 


```
 ┌─────────────────────────────────────────────────────────┐
 │               Espacio de Usuario (Ring 3)               │
 │       [Hilo ULT A]              [Hilo ULT B]            │
 └────────────────────────────┬────────────────────────────┘
                              │ (Mapeo directo 1:1 o M:N)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Espacio del Núcleo - Hilos de Kernel (Ring 0)   │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Planificador del Kernel (Scheduler Multi-Core)    │  │
 │  │   [KLT 1 en Core 0]      [KLT 2 en Core 1]        │  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                   Hardware Multiprocesador              │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Stallings, W. (2017). _Operating Systems: Internals and Design Principles_ (9.ª ed.). Pearson.Capítulo 4