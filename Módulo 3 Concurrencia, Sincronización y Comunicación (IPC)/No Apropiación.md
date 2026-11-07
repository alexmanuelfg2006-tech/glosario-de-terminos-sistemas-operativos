>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
No Apropiación / No Preemption

Según Silberschatz et al. (2018), la no apropiación establece que un recurso no puede ser expropiado de forma forzosa a un proceso; este solo puede ser liberado voluntariamente al completar su tarea. Establece que los recursos que se le fueron asignados a un proceso no pueden ser tomados a la fuerza por el sistema operativo si no que tiene que esperar a que el proceso los libere


```
 ┌─────────────────────────────────────────────────────────┐
 │        Proceso A Posee Recurso Exclusivo (Ej. Impresora)│
 └────────────────────────────┬────────────────────────────┘
                              │ (El Sistema Operativo respeta la posesión)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │          Regla Estricta de No Apropiación               │
 │  * El OS NO puede arrebatar el recurso por la fuerza    │
 │  * El recurso permanece retenido hasta que el proceso   │
 │    lo libere de manera voluntaria                       │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 8