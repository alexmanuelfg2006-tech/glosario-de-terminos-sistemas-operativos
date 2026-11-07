>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Paralelismo / Parallelism

Según Silberschatz et al. (2018), el paralelismo es la propiedad de un sistema donde dos o más tareas o hilos se ejecutan de manera estrictamente simultánea en el tiempo al disponer de múltiples núcleos físicos o procesadores dedicados. es la capacidad de ejecutar varias tareas de forma simultanea utilizando varios procesadores o nucleos de la cpu

```
 ┌─────────────────────────────────────────────────────────┐
 │         Procesador Físico Multinúcleo (Multi-Core)      │
 ├────────────────────────────┬────────────────────────────┤
 │      Núcleo de CPU 1       │      Núcleo de CPU 2       │
 │   [ Ejecución Tarea A ]    │   [ Ejecución Tarea B ]    │
 └─────────────┬──────────────┴─────────────┬──────────────┘
               │                            │
               ▼                            ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Progreso Físico Simultáneo Real             │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 4