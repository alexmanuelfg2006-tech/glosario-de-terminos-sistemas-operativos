>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Semáforo Binario / Binary Semaphore

Según Stallings (2017), un semáforo binario es una variable entera de sincronización cuyo valor oscila únicamente entre 0 y 1, funcionando de forma equivalente a un cerrojo mutex para proporcionar exclusión mutua. Es el mecanismo que toma valores de 1 cuando el recurso compartido esta disponible y 0 cuando el recurso esta siendo usado por otro proceso


```
 ┌─────────────────────────────────────────────────────────┐
 │           Señalizador de Evento / Condición             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Valor interno: 0 o 1)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                Semáforo Binario (Mutex-like)            │
 │  * Valor 1: Recurso libre / Evento cumplido             │
 │  * Valor 0: Recurso ocupado / Hilo en espera (Sleep)    │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Stallings, W. (2017). _Operating Systems: Internals and Design Principles_ (9.ª ed.). Pearson.Capítulo 5