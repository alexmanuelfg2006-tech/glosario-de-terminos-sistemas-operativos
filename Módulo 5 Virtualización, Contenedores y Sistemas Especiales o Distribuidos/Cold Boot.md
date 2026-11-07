>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Cold Boot / Arranque en Frío del Sistema

Tanenbaum y Bos (2015) analizan la secuencia completa de encendido e inicialización de la máquina partiendo desde un estado de apagado eléctrico total sin datos en caché. Durante este proceso, la placa madre ejecuta la rutina de POST del firmware (BIOS/UEFI) para verificar la integridad física del procesador y la memoria RAM. Posteriormente, se carga el gestor de arranque en memoria virtual, el cual inicializa la imagen comprimida del kernel del sistema operativo. Al carecer de datos remanentes en memoria, requiere la configuración completa de todos los controladores.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
