>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Memoria Compartida POSIX / SysV (`shmem`) / Shared Memory (`shmem`)

Tanenbaum y Bos (2015) analizan este subsistema del kernel que administra la reserva e intercambio de segmentos de memoria compartida utilizando internamente una instancia respaldada por tmpfs. Permite a múltiples procesos mapear regiones comunes de RAM sin requerir un archivo físico persistente en disco como respaldo. Ofrece una interfaz de muy alto rendimiento para el intercambio de datos entre aplicaciones cliente-servidor y compositores gráficos. Facilita la asignación rápida y la liberación automática de RAM.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
