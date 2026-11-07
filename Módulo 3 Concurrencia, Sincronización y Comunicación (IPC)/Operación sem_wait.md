>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Operación `sem_wait` /  `sem_wait` Operation

Según Silberschatz et al. (2018), `sem_wait` es la función atómica sobre un semáforo que decrementa su valor en 1; si el valor resultante es negativo, el hilo invocador se bloquea hasta que el semáforo sea incrementado por otro hilo. Es una operacion para la sincronizacion de hilos y procesos mediante semaforos que lo decrementa si su valor es 1


```
 ┌─────────────────────────────────────────────────────────┐
 │                 Hilo Llama a sem_wait()                 │
 └────────────────────────────┬────────────────────────────┘
                              │ (Evalúa valor del semáforo > 0)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Evaluación del Contador                     │
 ├────────────────────────────┬────────────────────────────┤
 │ Si Valor > 0               │ Si Valor == 0              │
 │ ▼                          │ ▼                          │
 │ Decrementa contador y avanza│ Bloquea hilo en cola de espera│
 └────────────────────────────┴────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 6
