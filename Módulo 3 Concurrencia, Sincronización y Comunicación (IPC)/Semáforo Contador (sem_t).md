>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Semáforo Contador / Counting Semaphore 

Según Silberschatz et al. (2018), un semáforo contador es un primitivo de sincronización que gestiona un entero no negativo para coordinar el acceso a un número finito y determinado de unidades de un recurso compartido. Es un mecanismo que gestiona el acceso a un recurso compartido o a un numero determinado de instancias de un mismo recurso


```
 ┌─────────────────────────────────────────────────────────┐
 │           Petición de Acceso a Recursos Limitados       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Consulta de capacidad disponible)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Semáforo Contador (Valor Entero N >= 0)     │
 │  * Si N > 0: Decrementa y permite acceso                │
 │  * Si N == 0: Bloquea al hilo en cola de espera         │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 6