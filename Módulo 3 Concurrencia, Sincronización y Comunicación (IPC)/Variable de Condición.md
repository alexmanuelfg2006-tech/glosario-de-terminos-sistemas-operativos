>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Variable de Condición / Condition Variable

Según Tanenbaum y Bos (2015), una variable de condición es una primitiva utilizada dentro de los monitores que permite a un hilo bloquearse cuando no se cumple un requisito lógico, liberando el cerrojo para otros. Es un mecanismo de sincronización asociado a un monitor que permite a los hilos suspender su ejecución mientras espera que ocurra un evento


```
 ┌─────────────────────────────────────────────────────────┐
 │         Hilo dentro de Sección Crítica (Monitor)        │
 └────────────────────────────┬────────────────────────────┘
                              │ (Evalúa condición lógica no cumplida, ej. buffer lleno)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Operación de Espera (pthread_cond_wait)         │
 │  * Libera el Mutex automáticamente                      │
 │  * Duerme el hilo en la cola de la Variable de Condición│
 └────────────────────────────┬────────────────────────────┘
                              │ (Otro hilo ejecuta señal / broadcast)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │        Despertar y Re-adquisición del Mutex             │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson.Capítulo 2