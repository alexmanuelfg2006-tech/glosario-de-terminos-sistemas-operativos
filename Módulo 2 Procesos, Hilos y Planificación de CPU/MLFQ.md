>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Cola multinivel con realimentación / Multilevel Feedback Queue

Según Silberschatz et al. (2018), la cola multinivel con realimentación (MLFQ) es un esquema dinámico que permite el movimiento de los procesos entre colas en función de la naturaleza de sus ráfagas de CPU, ajustando sus prioridades continuas para evitar la inanición y optimizar la respuesta. Es un algoritmo de planificación avanzado que permite a los procesos desplazarse dinámicamente entre distintas colas de prioridad según su comportamiento histórico.


```
 ┌─────────────────────────────────────────────────────────┐
 │  Cola 0: Alta Prioridad (Quántum corto = 8ms)           │ ◄─── (Promoción por Envejecimiento)
 ├─────────────────────────────────────────────────────────┤
 │  Cola 1: Prioridad Media (Quántum medio = 16ms)         │
 ├─────────────────────────────────────────────────────────┤
 │  Cola 2: Baja Prioridad (Procesamiento por FCFS)        │
 └────────────────────────────┬────────────────────────────┘
                              │ 
                              ▼ (Retroalimentación: Degradación por agotar quántum)
 ┌─────────────────────────────────────────────────────────┐
 │     Migración Dinámica de Procesos entre Niveles        │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5