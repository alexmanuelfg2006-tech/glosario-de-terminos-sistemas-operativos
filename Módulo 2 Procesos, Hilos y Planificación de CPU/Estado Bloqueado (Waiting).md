>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Estado Bloqueado / Waiting State

Según Silberschatz et al. (2018), el estado Bloqueado o de Espera se da cuando un proceso no puede continuar su ejecución inmediata debido a que aguarda la ocurrencia de un evento externo, como la finalización de una operación de entrada/salida o la recepción de una señal. Es el estado en el que esta un proceso cunado ocurre un error en su procesamiento y no puede seguir con su ejecucion hasta que se solucione el error


```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso en Estado Ejecutando              │
 └────────────────────────────┬────────────────────────────┘
                              │ (Solicita E/S o recurso no disponible)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Estado Bloqueado (Waiting)                │
 │    * Fuera de la cola de CPU (Inactivo en espera)       │
 │    * Vinculado a una cola de eventos o dispositivos     │
 └────────────────────────────┬────────────────────────────┘
                              │ (El evento o E/S se completa / Interrupción de hardware)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Retorno a la Cola de Listos (Ready State)      │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 3
