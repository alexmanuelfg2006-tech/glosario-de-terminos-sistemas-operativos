>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
 /dev/binder / Dispositivo Binder

Tanenbaum y Bos (2015) funciona como el punto de acceso central en la arquitectura Android, estando instanciado en el sistema como un nodo de dispositivo virtual especial. A través de este mecanismo, los componentes del sistema y las aplicaciones del usuario intercambian mensajes mediante llamadas a procedimientos remotos (RPC) a máxima velocidad. El kernel intercepta estas operaciones para mapear búferes de memoria compartida entre procesos, lo que elimina la necesidad de realizar copias de datos redundantes en RAM.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
