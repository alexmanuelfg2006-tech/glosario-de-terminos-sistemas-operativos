>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Polling / Sondeo Activo de Dispositivos

Tanenbaum y Bos (2015) definen esta técnica como la verificación periódica y síncrona del estado de un dispositivo de E/S por parte de la CPU dentro de un bucle cerrado de consulta. La CPU ejecuta continuamente instrucciones para leer los registros de estado del controlador de hardware hasta que este indique que la transferencia ha concluido. Aunque elimina los retardos asociados al manejo de interrupciones, desperdicia ciclos masivos de procesamiento en esperas activas. Solo resulta eficiente en dispositivos ultra-rápidos de baja latencia.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
