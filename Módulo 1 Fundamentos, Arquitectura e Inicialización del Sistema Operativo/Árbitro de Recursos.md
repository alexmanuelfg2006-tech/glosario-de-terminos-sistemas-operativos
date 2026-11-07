>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---

***Árbitro de recursos (gestor de recursos) / Resource Arbiter (Resource Manager)

**Andrew S. Tanenbaum** y **Herbert Bos** (2015) Explican que la labor del sistema operativo es permitir que múltiples programas compartan de manera ordenada una sola computadora física. **Multiplexación en el tiempo:** Cuando varios programas necesitan usar un único recurso. **Multiplexación en el espacio:** En lugar de tomar turnos, los programas se reparten el recurso simultáneamente. El arbitro es el que se encarga de distribuir los recursos del sistema entre los diferentes programas



```
 [ Solicitudes Concurrentes (Múltiples CPUs, DMAs, Hilos de Usuario) ]
                                   │
                                   ▼
 ┌───────────────────────────────────────────────────────────────────┐
 │ NIVEL 1: ÁRBITRO DE HARDWARE (Controladores de Bus / Memoria)     │
 │ • Resuelve colisiones físicas en líneas de datos, direcciones y   │
 │   control (PCIe, Memoria RAM, Controladoras de E/S).              │
 └─────────────────────────────────┬─────────────────────────────────┘
                                   │
                                   ▼
 ┌───────────────────────────────────────────────────────────────────┐
 │ NIVEL 2: PLANIFICADOR DEL KERNEL (CPU Scheduler / Ring 0)        │
 │ • Arbitra el tiempo de procesamiento de la CPU entre hilos        │
 │   activos mediante algoritmos (Round Robin, Colas de Prioridad).    │
 └─────────────────────────────────┬─────────────────────────────────┘
                                   │
                                   ▼
 ┌───────────────────────────────────────────────────────────────────┐
 │ NIVEL 3: ÁRBITROS DE SINCRONIZACIÓN LÓGICA (Mutex, Semáforos)     │
 │ • Regulan el acceso seguro a bases de datos, archivos, buffers    │
 │   o estructuras de memoria compartida en espacio de usuario/kernel│
 └───────────────────────────────────────────────────────────────────┘
```




```
 [ Hilo A ] ──┐
              ├──► [ Intento de Adquisición de Recurso (Lock/Mutex) ]
 [ Hilo B ] ──┘                            │
                                           ▼
                                 ┌───────────────────┐
                                 │ ¿El recurso está  │
                                 │ libre (Disponible)│
                                 └───────────────────┘
                                      │           │
                                    (Sí)        (No)
                                      │           ▼
                                      │    [ Árbitro del Kernel suspende ]
                                      │    [ al hilo y lo encola (Wait Queue) ]
                                      ▼           │
                           [ Acceso Concedido ] ◄─┘
                           [ Sección Crítica  ]
                                      │
                                      ▼
                           [ Liberación del Recurso (Unlock) ]
                                      │
                                      ▼
                           [ Despertar Siguiente Hilo en Cola ]
```






### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern operating systems_ (4.ª ed.). Pearson. Cap. 1, sec. 1.1.2: The Operating System as a Resource Manager.

