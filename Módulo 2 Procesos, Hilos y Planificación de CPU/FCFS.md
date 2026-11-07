>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
FCFS (First-Come, First-Served) / FCFS Scheduling

Según Silberschatz et al. (2018), el algoritmo FCFS (_First-Come, First-Served_) asigna la CPU al proceso que la solicite primero en una cola estrictamente FIFO, representando el esquema de planificación más simple pero vulnerable a tiempos promedio de espera elevados debido al efecto convoy. Es el algoritmo de planificación de CPU más elemental y de carácter no expropiativo. Asigna la CPU a los procesos respetando estrictamente el orden de llegada a la cola de listos. Aunque es simple de implementar utilizando una estructura FIFO


```
 ┌─────────────────────────────────────────────────────────┐
 │       Llegada de Procesos en Cola (Orden de Ingreso)    │
 │       [ P1 ] ──> [ P2 ] ──> [ P3 ]                      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asignación secuencial estricta sin apropiación)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 Algoritmo FCFS (FIFO)                   │
 │  * El primer proceso en llegar es el primero en salir   │
 │  * Ejecución completa hasta terminar (No apropiativo)   │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Procesamiento Secuencial en la CPU                │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5