>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
 Operación `sem_post` / `sem_post` Operation

Según Silberschatz et al. (2018), `sem_post` es la función atómica que incrementa en 1 el contador de un semáforo y despierta a uno de los hilos bloqueados a la espera de dicho recurso. Es la funcion que incrementa o desbloquea los semaforos para que pueda continuar con su ejecucion.Si el valor del semáforo era `0` y había uno o más hilos o procesos bloqueados en una llamada `sem_wait()`, la operación `sem_post()` despierta a uno de ellos

Plaintext

```
 ┌─────────────────────────────────────────────────────────┐
 │                 Hilo Llama a sem_post()                 │
 └────────────────────────────┬────────────────────────────┘
                              │ (Incrementa el valor del semáforo)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Actualización y Despertar de Hilos              │
 │  * Incrementa el contador en 1                          │
 │  * Despierta a un hilo en espera (Wake up / Sleep Queue)│
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. (Capítulo 6: _Synchronization Tools_, pp. 267-271).