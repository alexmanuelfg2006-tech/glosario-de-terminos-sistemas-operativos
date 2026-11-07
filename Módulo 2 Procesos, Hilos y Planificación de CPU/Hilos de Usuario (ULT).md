>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Hilos a Nivel de Usuario / User-Level Threads (ULT)

Según Stallings (2017), los hilos de usuario son aquellos gestionados completamente por una biblioteca en el espacio de usuario sin el conocimiento ni la intervención del núcleo del sistema operativo, lo que permite conmutaciones rápidas pero carece de soporte directo para multiprocesamiento. Son hilos gestionados en el espacio usuario que no intervienen en el kernel del sistema operativo 


```
 ┌─────────────────────────────────────────────────────────┐
 │               Espacio de Usuario (Ring 3)               │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Biblioteca de Hilos (User-Level Scheduler)        │  │
 │  │   [ULT 1]      [ULT 2]      [ULT 3]  (Conmutación)│  │
 │  └────────────────────────────┬──────────────────────┘  │
 └───────────────────────────────┼─────────────────────────┘
                                 │ (Mapeo N:1 - Invisibles para el Kernel)
                                 ▼
 ┌─────────────────────────────────────────────────────────┐
 │            Único Hilo de Kernel / Proceso (Ring 0)      │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Stallings, W. (2017). _Operating Systems: Internals and Design Principles_ (9.ª ed.). Pearson. Capítulo 4