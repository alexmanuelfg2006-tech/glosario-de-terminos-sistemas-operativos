>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
 E/S por Interrupciones / Interrupt-Driven I/O

Silberschatz et al. (2018) estudian este esquema donde los periféricos envían señales eléctricas de interrupción a la CPU únicamente cuando requieren atención, liberando al procesador de la espera activa. Al emitir una orden de lectura o escritura, el hilo ejecutante entra en estado de reposo mientras la CPU realiza otras tareas productivas. Cuando el dispositivo periférico completa la transferencia de datos, activa la línea IRQ asociada para pausar temporalmente el procesador. La CPU ejecuta el manejador de interrupción y reanuda el proceso suspendido.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
