>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Proceso Huérfano / Orphan Process

Según Silberschatz et al. (2018), un proceso huérfano es un proceso en ejecución cuyo proceso padre ha finalizado o sido terminado prematuramente, lo que provoca que sea adoptado automáticamente por el proceso `init` (PID 1) para gestionar su posterior terminación. Son los procesos que su proceso tarde termino su ejecucion antes de que pudieran ser procesados y luego los adopta otro proceso para terminar su ejecucion.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso Padre (Termina abruptamente)      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Desaparece del sistema)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Proceso Huérfano (Hijo Activo)            │
 │    * Queda sin proceso ascendente original              │
 └────────────────────────────┬────────────────────────────┘
                              │ (Intervención del Kernel: Reasignación de PPID)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │        Adopción por Init / Systemd (Nuevo PPID = 1)     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 3