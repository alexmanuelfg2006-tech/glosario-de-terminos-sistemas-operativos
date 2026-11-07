>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
udev / Gestor de Dispositivos de Linux

Tanenbaum y Bos (2015) tratan este demonio dinámico encargado de crear, nombrar o remover los nodos de dispositivo en el directorio /dev ante eventos de conexión o desconexión física. Escucha los eventos uevent emitidos por el kernel de Linux cuando un periférico es detectado por los buses del sistema. Aplica reglas de configuración personalizables para asignar permisos de acceso, crear enlaces simbólicos y cargar los controladores correspondientes de forma transparente. Gestiona la conexión Plug and Play en tiempo real.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
