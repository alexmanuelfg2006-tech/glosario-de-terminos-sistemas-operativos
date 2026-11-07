>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Colas Paralelas NVMe / Paralelismo de E/S NVMe

Silberschatz et al. (2018) hacen hincapié en la arquitectura de hardware presente en el protocolo NVMe que soporta hasta 64,000 colas de órdenes simultáneas con 64,000 comandos cada una. Esta tecnología rompe el embotellamiento histórico de los controladores AHCI de una sola cola, aprovechando al máximo la arquitectura multinúcleo de los procesadores modernos. Cada núcleo de CPU puede enviar peticiones de lectura y escritura a la unidad SSD de forma independiente sin requerir bloqueos mecánicos. Esto maximiza las IOPS y reduce sensiblemente las latencias de E/S.


```
 ┌─────────────────────────┬───────────────────────────────┐
 │  Núcleo de CPU 1        │  Núcleo de CPU 2              │
 └────────────┬────────────┴───────────────┬───────────────┘
              │ (Cola de Envío 1)          │ (Cola de Envío 2)
              ▼                            ▼
 ┌─────────────────────────────────────────────────────────┤
 │           Controlador NVMe (Múltiples Colas I/O)        │
 │  * Cola de Envío y Recepción por cada núcleo de CPU     │
 │  * Procesamiento concurrente sin contención de bus      │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Ejecución Simultánea en Canales de Flash       │
 └─────────────────────────────────────────────────────────┘
```
---
### Referencia
 Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
