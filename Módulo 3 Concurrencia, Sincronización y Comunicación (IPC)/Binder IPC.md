>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Binder IPC / Mecanismo IPC de Android

Silberschatz et al. (2018) describen la arquitectura del subsistema principal de comunicación entre procesos en la plataforma Android, el cual sustituye a los mecanismos tradicionales de UNIX. Emplea un controlador de kernel dedicado (/dev/binder) y mapeo de memoria compartida para transmitir llamadas RPC entre procesos aislados. Esta arquitectura reduce el costo computacional al evitar la doble copia de datos en memoria durante la transferencia de mensajes. Asimismo, integra verificación estricta de identidades y permisos para asegurar que los componentes de las aplicaciones interactúen de forma segura.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
