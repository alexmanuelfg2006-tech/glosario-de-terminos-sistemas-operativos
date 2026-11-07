>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
DMA / Acceso Directo a Memoria

Tanenbaum y Bos (2015) presentan esta característica de arquitectura de hardware como la capacidad que permite a los subsistemas de E/S transferir bloques de datos directamente con la RAM sin recargar de trabajo a la CPU. El procesador únicamente inicializa la transferencia configurando las direcciones de origen, destino y el conteo de bytes en el controlador DMA. Una vez parametrizado, el bus realiza la copia a alta velocidad de forma autónoma entre la memoria y el dispositivo periférico. Al finalizar el volcado, el controlador genera una interrupción para notificar la finalización.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
