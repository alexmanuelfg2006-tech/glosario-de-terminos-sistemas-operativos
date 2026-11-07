>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
MMIO / Entrada/Salida Mapeada en Memoria

Tanenbaum y Bos (2015) estudian este método de comunicación donde la CPU interactúa con los periféricos utilizando direcciones de memoria reservadas dentro del mismo bus de datos. Los registros de control y búferes del dispositivo de hardware son asignados a rangos específicos del espacio de direcciones de memoria. La CPU lee o escribe en estas ubicaciones utilizando instrucciones de memoria convencionales sin requerir instrucciones I/O dedicadas. Agiliza la transferencia de comandos y datos con tarjetas gráficas y placas de red.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
