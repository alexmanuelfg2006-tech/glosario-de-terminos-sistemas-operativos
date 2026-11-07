>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Detección de Interbloqueos / Deadlock Detection

Según Silberschatz et al. (2018), la detección de interbloqueos implica el uso de algoritmos de análisis estructural que evalúan las tablas de estado para identificar si se ha formado un bloqueo operativo real. es un método algorítmico ejecutado por el sistema operativo para examinar el estado de las asignaciones e identificar si se ha materializado un bloqueo mutuo entre procesos.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Operación Libre del Sistema               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Ejecución periódica del algoritmo de detección)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Auditoría de Recursos y Solicitudes             │
 │  * Construcción de matrices de asignación y peticiones  │
 │  * Verificación de bloqueos circulares activos          │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Si NO hay interbloqueo)                ▼ (Si SÍ hay interbloqueo)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │   El sistema continúa su     │          │    Activación de Protocolo   │
 │        operación normal      │          │     de Recuperación (Kill)   │
 └──────────────────────────────┘          └──────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 8

