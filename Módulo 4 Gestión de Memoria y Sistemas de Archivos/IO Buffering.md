>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
I/O Buffering / Búferes de Entrada/Salida

Silberschatz et al. (2018) exponen cómo esta técnica consiste en la reserva temporal de regiones de memoria para intermediar la transferencia de datos entre componentes con velocidades o bloques dispares. Permite que la CPU devuelva el control a la aplicación inmediatamente después de escribir en el búfer de RAM, sin esperar a que la unidad SSD o disco físico complete la operación lenta. Asimismo, agrupa múltiples lecturas de pequeño tamaño en transferencias de bloques contiguos a gran velocidad. Mitiga cuellos de botella y optimiza el rendimiento del subsistema de archivos.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
