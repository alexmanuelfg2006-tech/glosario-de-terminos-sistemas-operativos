>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Colas de Mensajes / Mensajería Estructurada IPC

Tanenbaum y Bos (2015) caracterizan esta abstracción como un canal de comunicación asíncrono gestionado directamente por el núcleo donde los procesos depositan y leen paquetes de datos estructurados. A diferencia de las tuberías de flujo continuo de bytes, conservan los límites individuales de cada mensaje enviado dentro de una cola interna en el kernel. Varios procesos pueden escribir y leer de la misma cola en función de prioridades o tipos de mensajes previamente asignados. Esta abstracción resulta idónea para coordinar tareas complejas en sistemas distribuidos y arquitecturas cliente-servidor.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
