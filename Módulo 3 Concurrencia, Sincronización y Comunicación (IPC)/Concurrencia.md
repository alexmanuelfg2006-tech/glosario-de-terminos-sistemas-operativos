>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Concurrencia / Concurrency

Según Silberschatz et al. (2018), la concurrencia es la capacidad del sistema para dar soporte a la ejecución de múltiples tareas realizando progresos de forma intercalada durante el mismo intervalo de tiempo. es la capacidad de gestionar multiples procesos o hilos ya sea intercalando su ejecucion o en un solo procesador


```
 ┌─────────────────────────────────────────────────────────┐
 │               Planificador del Sistema (Scheduler)      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Alterna quántums de tiempo)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Línea de Tiempo Concurrente (Single / Multi Core)│
 │  [ Tarea A ] ➔ [ Tarea B ] ➔ [ Tarea A ] ➔ [ Tarea C ]  │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │            Progreso Lógico Simultáneo de Tareas         │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 4