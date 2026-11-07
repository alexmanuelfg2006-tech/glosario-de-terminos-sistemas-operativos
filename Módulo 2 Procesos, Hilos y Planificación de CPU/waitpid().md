>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Llamada al sistema `waitpid() / waitpid()` System Call

Según Silberschatz et al. (2018), `waitpid()` es la llamada al sistema que suspende la ejecución del proceso invocador hasta que un proceso hijo específico cambie de estado o termine, permitiendo la recolección de su código de retorno y la limpieza de su registro en la tabla de procesos. Esta llamadas suspende al proceso llamado hasta que un proceso hijo termine su ejecucion o cambien de estado


```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso Padre en Ejecución                │
 └────────────────────────────┬────────────────────────────┘
                              │ (Invoca waitpid(pid_hijo, &status, opciones))
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Evaluación de Estado en el Kernel (Ring 0)      │
 │  * ¿El hijo ya terminó?                                 │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Si el hijo sigue activo)               ▼ (Si el hijo ya finalizó)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │    Proceso Padre se bloquea  │          │  Se recupera el código de    │
 │     en espera del evento     │          │    salida y se borra el PCB  │
 └──────────────────────────────┘          └──────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 3