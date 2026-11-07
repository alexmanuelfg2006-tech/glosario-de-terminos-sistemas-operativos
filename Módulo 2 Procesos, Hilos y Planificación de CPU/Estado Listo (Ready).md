>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Estado Listo / Ready State

Según Silberschatz et al. (2018), el estado Listo describe a un proceso que se encuentra completamente cargado en memoria con todos sus recursos asignados, a la espera únicamente de que el planificador de la CPU le asigne un tiempo de procesamiento. Es el estado de proceso al que ya se le asignaron recurso y esta a la espera para procesarse



```
 [ Carga / Desbloqueo ] ──> [ Cola de Listos (Ready Queue) ] ──> [ Asignación de CPU (Dispatcher) ]
```

```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso Creado o Desbloqueado             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Pasa a la cola de listos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │              Cola de Procesos Listos (Ready Queue)      │
 │    * Residentes en RAM                                  │
 │    * Esperando asignación de procesador                 │
 └────────────────────────────┬────────────────────────────┘
                              │ (Selección por parte del Planificador / Dispatcher)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Transición a Estado de Ejecución (Running)     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 3
