>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Cerrojo de Exclusión Mutua  / Mutual Exclusion Lock)

Según Silberschatz et al. (2018), un cerrojo mutex es un mecanismo de sincronización booleano utilizado para proteger secciones críticas adquiriendo un bloqueo mediante `acquire()` previo al ingreso y liberándolo con `release()` al salir. Es la medida de seguriada que se tiene para asegurar que un solo proceso acceda a un recurso compartido para evitar condiciones de carrera


```
 ┌─────────────────────────────────────────────────────────┐
 │               Hilos Solicitantes del Mutex              │
 │      [Hilo 1]                  [Hilo 2] (Bloqueado)     │
 └───────────┬────────────────────────┬────────────────────┘
             │ (Intenta lock())       │ (En cola de espera)
             ▼                        ▼
 ┌─────────────────────────────────────────────────────────┐
 │                 Estado del Cerrojo Mutex                │
 │    * Propietario actual: Hilo 1                         │
 │    * Estado: Ocupado (Locked)                           │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 6