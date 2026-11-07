>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Commit de Diario / Journal Commit

Silberschatz et al. (2018) identifican esta etapa como la fase final dentro de un sistema de archivos con journaling donde las modificaciones temporales del diario se consolidan como definitivas. El kernel agrupa las operaciones de escritura de metadatos en un bloque de transacción y lo escribe en el registro circular de disco antes de actualizar los bloques reales. Una vez que la marca de commit se graba con éxito, la operación se considera atómica e irreversible frente a caídas repentinas de energía. Esto garantiza la consistencia del sistema de archivos y acelera la recuperación en el arranque.


```
 ┌─────────────────────────────────────────────────────────┐
 │       Transacciones Acumuladas en el Buffer de Diario   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Ejecución de sincronización forzada o por tiempo)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 Commit de Diario (Commit Block)         │
 │  * Sella oficialmente la transacción como atómica       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Autoriza la persistencia definitiva)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Aplicación de Cambios en la Estructura Principal  │
 └─────────────────────────────────────────────────────────┘
```

---
### Referencia
 Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
