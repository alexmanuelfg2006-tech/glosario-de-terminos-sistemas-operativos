>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Identificador de Proceso / Process Identifier (PID)

Según Tanenbaum y Bos (2015), el PID es un valor numérico entero único asignado por el sistema operativo a cada proceso activo para identificarlo unívocamente dentro de la tabla de procesos del sistema durante todo su ciclo de vida. Es el identificador numerico que se le asigna a cada proceso mientras se ejecuta para identificarlo


```
 ┌─────────────────────────────────────────────────────────┐
 │           Solicitud de Nuevo Proceso (fork)             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Consulta de asignador de identificadores)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Asignador de PIDs del Kernel (PID Allocator)    │
 │  * Busca el siguiente entero libre (hasta pid_max)     │
 │  * Evita colisiones y reutiliza PIDs antiguos           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asigna valor entero único)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Registro en el PCB y Árbol Genealógico (PID/PPID) │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson. Capítulo 2
