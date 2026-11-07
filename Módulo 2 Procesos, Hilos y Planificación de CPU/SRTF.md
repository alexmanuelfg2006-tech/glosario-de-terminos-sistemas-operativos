>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
SRTF (Shortest Remaining Time First) / SRTF Scheduling

Según Silberschatz et al. (2018), SRTF (_Shortest Remaining Time First_) es la versión expropiativa de SJF en la cual, si la llegada de un nuevo proceso presenta un tiempo remanente de CPU menor que el tiempo que le resta al proceso en ejecución, la CPU es expropiada de inmediato para asignarse al nuevo elemento.Es la versión expropiativa del algoritmo SJF. Si mientras un proceso se está ejecutando llega a la cola de listos un nuevo trabajo cuyo tiempo es mas corto de los que estan en la cola se detine el proceso mas largo para completarlo


```
 ┌─────────────────────────────────────────────────────────┐
 │         Llegada de Nuevo Proceso a la Cola              │
 └────────────────────────────┬────────────────────────────┘
                              │ (Comparación de tiempo restante)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Evaluación de Tiempo Restante (SRTF)            │
 ├────────────────────────────┬────────────────────────────┤
 │ Si Restante Nuevo < Actual │ Si Restante Nuevo > Actual │
 │ ▼                          │ ▼                          │
 │ Desaloja (Preempt) al actual y asigna CPU al nuevo      │
 └────────────────────────────┴────────────────────────────┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5