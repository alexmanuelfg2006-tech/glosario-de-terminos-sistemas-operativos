>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Protocolo NVMe / Especificación NVMe

Tanenbaum y Bos (2015) estudian esta especificación de comunicación en bus PCI Express optimizada específicamente para garantizar accesos de ultra-baja latencia a unidades de estado sólido (SSD). Diseñado desde cero para superar las limitaciones mecánicas del protocolo SATA, soporta paralelismo masivo mediante colas de comandos múltiples. Permite transferir datos a velocidades de varios gigabytes por segundo reduciendo sensiblemente el uso de ciclos de CPU por operación de E/S. Es la norma en almacenamiento moderno de alto rendimiento.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Subsistema del Procesador (CPU)           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Conexión directa a través del bus PCIe)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │          Protocolo NVMe (Non-Volatile Memory Express)   │
 │  * Acceso directo en memoria sin cuello de botella      │
 │  * Paralelismo extremo adaptado a dispositivos flash    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Controlador SSD NVMe)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │           Almacenamiento SSD en Estado Sólido           │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
