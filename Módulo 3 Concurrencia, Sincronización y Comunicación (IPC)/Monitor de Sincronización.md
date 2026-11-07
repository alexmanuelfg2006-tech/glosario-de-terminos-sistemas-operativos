>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Monitor de Sincronización / Synchronization Monitor

Según Silberschatz et al. (2018), un monitor es un constructo de sincronización de alto nivel de lenguaje que proporciona un mecanismo seguro y conveniente para compartir datos de forma concurrente entre procesos, garantizando la exclusión mutua por diseño abstracto. Es una estructura de programación de alto nivel que encapsula variables compartidas, procedimientos de sincronización y exclusión mutua, permitiendo que solo un hilo acceda a los datos internos de forma simultánea.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Hilos Concurrentes Externos               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Intentan invocar métodos del monitor)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                Monitor de Sincronización                │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Cerrojo Mutex Interno (Exclusión Mutua Automática)│  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Datos Privados Compartidos y Variables de Condición│  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Acceso exclusivo y seguro)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Ejecución Segura del Método del Monitor        │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 6