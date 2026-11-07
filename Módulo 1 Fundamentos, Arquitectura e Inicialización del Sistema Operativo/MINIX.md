>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Minix

Según Tanenbaum y Woodhull (2006), MINIX es un sistema operativo didáctico de código abierto fundamentado estrictamente en una arquitectura de micronúcleo, creado con el propósito expreso de estudiar las tripas del software de sistemas de manera comprensible. Es un sistema operativo basado en unix creado en 1987 con fines educativos



```
# psft (Process State Table en MINIX)
 PID   USER  PR  NI VIRT RSS  STATE   NAME
   0   root   0   0    0   0  IDLE    kernel
   1   root   1   0  512 256  RUN     pm (Process Manager)
   2   root   1   0  768 384  RUN     fs (File System)
   3   root   1   0 1024 512  RUN     rs (Reincarnation Server)
```

```
 ┌─────────────────────────────────────────────────────────┐
 │               Aplicaciones de Usuario (Ring 3)          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Paso de mensajes IPC)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Servidores Modulares de MINIX (Espacio de Usuario)│
 │  [Servidor de Archivos]  [Servidor de Memoria]  [Drivers]│
 └────────────────────────────┬────────────────────────────┘
                              │ (Mensajes IPC seguros)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │           Minimicronúcleo de MINIX (Ring 0)             │
 │          (Control de interrupciones, hilos y scheduling)│
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                     Hardware Físico                     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
anenbaum, A. S., & Woodhull, A. S. (2006). _Operating Systems: Design and Implementation_ (3.ª ed.). Pearson.Capítulo 1