>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Condición de Carrera / Race Condition

Según Tanenbaum y Bos (2015), una condición de carrera es una situación anómala donde dos o más hilos leen o escriben datos compartidos concurrentemente y el resultado final depende del orden exacto e impredecible de ejecución de sus instrucciones. es un fallo que ocurre cuando dos o mas procesos acceden a un recurso compartido al mismo tiempo y el resultado final es impredecible


```
 ┌─────────────────────────────────────────────────────────┐
 │               Hilos Concurrentes (A y B)                │
 └───────┬─────────────────────────────────────────┬───────┘
         │ (Lectura simultánea de variable global) │
         ▼                                         ▼
 ┌──────────────┐                          ┌──────────────┐
 │  Hilo A Lee  │                          │  Hilo B Lee  │
 └──────┬───────┘                          └──────┬───────┘
        │ (Modifica y escribe)                    │ (Modifica y escribe)
        ▼                                         ▼
 ┌─────────────────────────────────────────────────────────┐
 │      Colisión de Escritura en Recurso Compartido        │
 │       (El último en escribir sobrescribe y corrompe)    │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson. Capítulo 2
