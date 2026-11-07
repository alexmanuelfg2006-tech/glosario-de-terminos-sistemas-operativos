>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
IPC Namespace / Aislamiento IPC

Tanenbaum y Bos (2015) describen la función de este espacio de nombres orientado a proporcionar aislamiento de recursos de comunicación inter-proceso (como colas de mensajes POSIX o memoria compartida System V) entre contenedores. Cada IPC namespace posee su propia tabla independiente de identificadores de recursos IPC, impidiendo que un proceso en un contenedor acceda o modifique segmentos de memoria de otro. Esta separación resulta indispensable para ejecutar múltiples aplicaciones multihilo en el mismo servidor sin riesgo de interferencias cruzadas o colisiones de nombres de sockets.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
