>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
SJF (Shortest Job First) / SJF Scheduling

Según Silberschatz et al. (2018), el algoritmo SJF (_Shortest Job First_) asocia a cada proceso la longitud de su siguiente ráfaga de CPU para seleccionar sistemáticamente la tarea más pequeña, resultando ser óptimo al proporcionar el tiempo medio de espera mínimo para cualquier conjunto de procesos dado. Es un algoritmo de planificación que selecciona para su ejecución al proceso presente en la cola de listos que posea la ráfaga de CPU estimada más corta.


```
 ┌─────────────────────────────────────────────────────────┐
 │       Procesos en Cola (Ordenados por Duración de Ráfaga)│
 │       [ P3 (Burst: 2ms) ] ➔ [ P1 (Burst: 5ms) ]         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Selección del trabajo con menor tiempo de CPU)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Algoritmo SJF (Shortest Job First)              │
 │  * No apropiativo: Ejecuta el trabajo hasta terminar    │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Ejecución Secuencial en la CPU                 │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5