>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Afinidad de CPU / CPU Affinity

Según Silberschatz et al. (2018), la afinidad de CPU describe la tendencia de un sistema operativo a mantener la ejecución de un proceso dentro de un mismo núcleo físico para minimizar la sobrecarga derivada del fallo de caché y de la migración de contexto a través del bus de datos. Es la política del planificador en sistemas multiprocesador que procura mantener a un proceso ejecutándose de manera continua sobre el mismo núcleo o procesador físico durante su ciclo de vida.

```
 ┌─────────────────────────────────────────────────────────┐
 │                Proceso / Hilo Configurado               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Máscara de afinidad de CPU, ej. cores 0 y 1)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Planificador del Kernel (Restricción)           │
 │  * Fuerza al proceso a ejecutarse únicamente en la      │
 │    máscara de núcleos hardware permitidos               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Aprovechamiento de caché L1/L2 local)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Núcleo de CPU Permitido (Core 0 / Core 1)         │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5
