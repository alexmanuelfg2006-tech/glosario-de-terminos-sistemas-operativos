>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Proceso / Process

Silberschatz et al. (2018),nos dice que un proceso es una instancia de un programa en ejecución que constituye la unidad de trabajo fundamental dentro de un sistema operativo, la cual incluye su espacio de direcciones de memoria, código, registros y recursos del sistema asignados. Un proceso es un programa al que se le asigna recursos como memoria y tiempo de cpu para alcanzar un resultado final


```
 ┌─────────────────────────────────────────────────────────┐
 │             Bloque de Control de Proceso (PCB)          │
 │   (PID, Estado, Registros de CPU, Punteros de Memoria)  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asociado a)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Espacio de Direcciones Virtuales del Proceso    │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Text/Code (Instrucciones) │ Data (Variables)      │  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Heap (Dinámica)           │ Stack (Pila local)    │  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Ejecución Activa en el CPU (Hilos / Threads)    │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 3