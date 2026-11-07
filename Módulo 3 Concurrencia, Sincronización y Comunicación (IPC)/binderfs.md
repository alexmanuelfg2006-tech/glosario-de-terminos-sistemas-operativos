>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
binderfs / Sistema de Archivos Binder

Tanenbaum y Bos (2015) introducen este sistema de archivos virtual en el kernel de Linux como la solución para instanciar dinámicamente dispositivos Binder independientes en contenedores. Resuelve la limitación histórica de Android donde el nodo /dev/binder era global para todo el sistema, impidiendo el aislamiento multi-tenencia. Gracias a binderfs, cada espacio de nombres de montaje puede poseer su propia instancia privada de IPC sin interferir con otros contenedores. Esto resulta fundamental para ejecutar entornos Android virtualizados sobre servidores Linux convencionales.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
