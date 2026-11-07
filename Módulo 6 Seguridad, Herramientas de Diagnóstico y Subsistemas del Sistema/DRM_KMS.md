>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
DRM/KMS / Gestor de Renderizado Directo

Tanenbaum y Bos (2015) describen la función de este subsistema de Linux encargado de arbitrar el acceso directo al hardware gráfico y configurar resoluciones y frecuencias de actualización a nivel de kernel. Kernel Mode Setting (KMS) permite al núcleo establecer modos de pantalla desde la fase temprana del arranque sin depender del servidor gráfico en espacio de usuario. Direct Rendering Manager (DRM) gestiona la asignación de búferes de memoria de vídeo y coordina la cola de comandos enviada a la GPU. Juntos proporcionan la base para compositores Wayland y OpenGL.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
