>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Inanición / Starvation

Según Silberschatz et al. (2018), la inanición o bloqueo indefinido es una situación en la cual un proceso permanece en estado listo de manera infinita sin que el planificador le asigne tiempo de CPU. Problema de planificación donde un proceso apto para ejecutarse se ve postergado indefinidamente debido a que otros procesos acaparan los recursos del sistema y no tiene recursos para ejecutarse


```
 ┌─────────────────────────────────────────────────────────┐
 │          Cola de Procesos Listos (Ready Queue)          │
 └────────────────────────────┬────────────────────────────┘
                              │ (El planificador selecciona continuamente tareas prioritarias)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Proceso con Inanición (Starvation / Aging)      │
 │  * Espera indefinida en la cola de listos               │
 │  * Nunca recibe un quántum de CPU                       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Solución tradicional: Envejecimiento / Aging)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │      Incremento Gradual de Prioridad en el Tiempo       │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5