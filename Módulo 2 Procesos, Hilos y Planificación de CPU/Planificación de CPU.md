>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Planificación de CPU / CPU Scheduling

Según Silberschatz et al. (2018), la planificación de la CPU es la base de los sistemas operativos multiprogramados, encargada de seleccionar un proceso de la memoria que esté listo para ejecutarse y asignarle la unidad central de procesamiento para optimizar la utilización global del sistema. Es la función fundamental del sistema operativo encargada de decidir qué proceso o hilo en estado listo obtendrá el control de la unidad de procesamiento a continuación.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Cola de Procesos Listos (RAM)             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Algoritmo de decisión del Scheduler)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 Planificador de CPU                     │
 │  * Asigna quántum de tiempo o prioridades de ejecución  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Despacho / Dispatcher)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Núcleo del Procesador (CPU / Running)          │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5