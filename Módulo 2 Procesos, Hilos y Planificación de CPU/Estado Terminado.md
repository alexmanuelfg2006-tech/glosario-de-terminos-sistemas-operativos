>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Estado Terminado /  Terminated State

Según Silberschatz et al. (2018), el estado Terminado es la fase final del ciclo de vida de un proceso que ha concluido su ejecución (ya sea normalmente o por un fallo) y cuyos recursos están siendo liberados por el sistema operativo. Es el estado de un proceso cuando se termina su ejecucion ya sea por un error o por que ya se proceso completamente y devuelve los recursos que le fueron asignado para asignarselos a otro


```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso en Ejecución Final                │
 └────────────────────────────┬────────────────────────────┘
                              │ (Ejecuta instrucción de salida / exit() o excepción)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Estado Terminado (Terminated)             │
 │    * Liberación de memoria virtual, archivos y recursos │
 │    * Persistencia temporal del PCB (Estado Zombie)      │
 └────────────────────────────┬────────────────────────────┘
                              │ (El proceso padre ejecuta la llamada wait())
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Eliminación Definitiva del PCB por el Kernel    │
 └─────────────────────────────────────────────────────────┘
```
### Referencias
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 3