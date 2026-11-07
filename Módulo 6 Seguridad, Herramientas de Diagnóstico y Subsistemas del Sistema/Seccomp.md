>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Seccomp / Modo de Computación Segura

Tanenbaum y Bos (2015) estudian este filtro del kernel Linux diseñado para limitar las llamadas al sistema (syscalls) que un proceso determinado tiene permitido invocar. Utiliza filtros BPF (Berkeley Packet Filter) en espacio de kernel para examinar los números y argumentos de cada syscall emitida por un programa en tiempo real. Si el proceso intenta ejecutar una llamada restringida no autorizada, el kernel intercepta la orden y finaliza la tarea con una señal SIGSYS. Se emplea para blindar motores de contenedores.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
