>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Cambio de Contexto / Context Switch

Según Silberschatz et al. (2018), el cambio de contexto es la operación mediante la cual el núcleo guarda el estado del proceso en ejecución en su PCB y restaura el estado de otro proceso para transferirle el control del procesador. es el proceso mediante el kernel de un sistema detiene la ejecucion de un proceso y guarda su estado para cargar el estado de otro proceso distinto para que varias tareas compartan el procesador


```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso A en Ejecución (Running)          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Ocurre interrupción por Timer o llamada bloqueante)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Conmutación de Contexto por el Núcleo (Ring 0)  │
 │  * Guarda registros, PC, SP y estado del Proceso A en PCB A│
 │  * Restaura registros, PC, SP y estado del Proceso B de PCB B│
 └────────────────────────────┬────────────────────────────┘
                              │ (Restauración de control en CPU)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso B en Ejecución (Running)          │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 3