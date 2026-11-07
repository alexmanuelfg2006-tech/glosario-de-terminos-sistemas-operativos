>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Tiempo de Espera / Waiting Time

Según Silberschatz et al. (2018), el tiempo de espera es la cantidad total de tiempo que un proceso pasa retrasado dentro de la cola de listos esperando a que se le asigne la CPU, siendo el criterio central empleado para optimizar el rendimiento de la planificación. Es la sumatoria de todos los intervalos de tiempo acumulados que un proceso pasa aguardando pasivamente dentro de la cola de listos a la espera de que el planificador le otorgue un turno de uso de la CPU.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso Ingresa a Cola de Listos          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Acumula tiempo esperando turnos de CPU)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Cálculo del Tiempo de Espera                │
 │  * Waiting Time = Tiempo de Retorno - Tiempo de Ráfaga  │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │      Asignación Definitiva al Núcleo del Procesador     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5

