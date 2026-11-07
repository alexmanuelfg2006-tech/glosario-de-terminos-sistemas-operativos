>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Estado Ejecutando / Running State

Según Silberschatz et al. (2018), el estado Ejecutando corresponde a la fase del ciclo de vida en la que las instrucciones de un proceso están siendo procesadas activamente por la unidad central de procesamiento (CPU). Es el estado en el que esta un proceso mientras esta siendo procesado por la cpu


```
 ┌─────────────────────────────────────────────────────────┐
 │               Cola de Procesos Listos                   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asignación por el Dispatcher / Scheduler)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │               Estado Ejecutando (Running)               │
 │    * Uso activo de los registros de la CPU y la ALU     │
 │    * Ejecución de instrucciones de código               │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Si agota quántum o hay interrupción)   ▼ (Si solicita E/S o espera)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │       Retorno a Listos       │          │      Transición a Estado     │
 │        (Preempción)          │          │      Bloqueado (Waiting)     │
 └──────────────────────────────┘          └──────────────────────────────┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 3