>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Colas Multinivel / Multilevel Queue Scheduling

Según Silberschatz et al. (2018), la planificación de colas multinivel divide la cola de procesos listos en varios grupos estáticos independientes según su tipo o jerarquía, aplicando un algoritmo específico dentro de cada cola y fijando relaciones de prioridad absoluta entre ellas. Es una técnica de planificación que clasifica los procesos según sus características y los organiza en varias colas separadas e independientes


```
 ┌─────────────────────────────────────────────────────────┐
 │  Cola de Alta Prioridad (Primer Plano / Interactivos)   │ ──► [ Planificado por Round Robin ]
 ├─────────────────────────────────────────────────────────┤
 │  Cola de Media Prioridad (Procesos del Sistema)         │ ──► [ Planificado por FCFS ]
 ├─────────────────────────────────────────────────────────┤
 │  Cola de Baja Prioridad (Lotes / Batch de Fondo)        │ ──► [ Planificado por FCFS ]
 └────────────────────────────┬────────────────────────────┘
                              │ (Gestión de Prioridad Absoluta entre Colas)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                    Núcleo de la CPU                     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5