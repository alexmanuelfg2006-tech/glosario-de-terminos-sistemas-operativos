>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Inversión de Prioridades / Priority Inversion

Según Silberschatz et al. (2018), la inversión de prioridades es un fallo de sincronización en el que un hilo prioritario espera a que concluya uno de baja prioridad que retiene un cerrojo compartido. Es la anomalía de planificación donde un hilo de alta prioridad queda bloqueado indirectamente porque un hilo de baja prioridad retiene un recurso necesario.


```
 ┌─────────────────────────────────────────────────────────┐
 │  Proceso Alta Prioridad (Bloqueado esperando Recurso)   │
 └────────────────────────────▲────────────────────────────┘
                              │ (Espera que libere el cerrojo)
 ┌────────────────────────────┴────────────────────────────┐
 │  Proceso Baja Prioridad (Posee el Mutex, pero preemptado)│
 └────────────────────────────▲────────────────────────────┘
                              │ (Bloqueado por interrupción o carga)
 ┌────────────────────────────┴────────────────────────────┐
 │  Proceso Media Prioridad (Ejecutándose activamente en CPU)│
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 6