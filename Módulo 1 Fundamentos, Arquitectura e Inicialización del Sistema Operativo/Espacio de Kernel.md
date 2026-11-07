>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
**espacio de kernel / kernel space

**Andrew S. Tanenbaum** y **Herbert Bos** (2015) Definen el espacio de kernel como la zona de memoria donde el código se ejecuta con el máximo nivel de privilegios de hardware (Anillo 0). Explican que esta separación divide la computadora en dos mundos: lo que es de confianza y lo que no. El espacio de kernel es donde se encuentra lo mas delicado del sistema operativo por eso si alguna aplicacion de nivel ususario y detiene el programa antes de que se dañe el sistema operativo

```
 Entrada en la Tabla de Páginas (PTE):
 ┌──────────────┬──────────────┬──────────────┬──────────────┬──────────────────┐
 │ Dirección    │ Global (G)   │ No-Ejecutable│ User/Supervisor │ Bit de Presencia │
 │ Física       │              │ (NX / XD)    │ (U/S = 0)    │ (Present = 1)    │
 └──────────────┴──────────────┴──────────────┴──────────────┴──────────────────┘
                                                       │
                                                       ▼
                                         Si un proceso en Ring 3 intenta
                                         leer o escribir donde U/S = 0,
                                         la CPU genera una EXCEPCIÓN DE
                                         FALLO DE PÁGINA (Segmentation Fault).
```

```
 [ Aplicaciones de Usuario (Espacio de Usuario / Ring 3) ]
                           │
                           │ (Invocación mediante Syscall / Interrupción)
                           ▼
 ┌───────────────────────────────────────────────────────────────────┐
 │ ESPACIO DE KERNEL (Ring 0 - Núcleo del Sistema Operativo)         │
 ├─────────────────────────┬─────────────────────────────────────────┤
 │ • Subsistema de Procesos│ Planifica la CPU y gestiona hilos/pids  │
 │ • Gestor de Memoria     │ Administra la MMU, paginación y RAM     │
 │ • Subsistema de E/S     │ Controla drivers, buses y almacenamiento│
 │ • Capa de Red (Stack)   │ Gestiona protocolos TCP/IP y sockets    │
 └─────────────────────────┬─────────────────────────────────────────┘
                           │
                           ▼
 [ Hardware Físico (CPU, Memoria RAM, Discos, Tarjetas de Red) ]
```

### Referencia
Tanenbaum, A. S., y Bos, H. (2015). _Modern operating systems_ (4.ª ed.). Pearson. capitulo 2