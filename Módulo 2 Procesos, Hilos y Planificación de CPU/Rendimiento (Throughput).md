>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Rendimiento  / Throughput

Según Silberschatz et al. (2018), el rendimiento o _throughput_ representa el número neto de procesos finalizados con éxito por unidad de tiempo, siendo una métrica cuantitativa fundamental para evaluar la capacidad operativa de los algoritmos de planificación. Es una métrica global utilizada para medir la productividad del sistema operativo en la gestión de procesador.

```
 ┌─────────────────────────────────────────────────────────┐
 │          Ingreso Masivo de Procesos al Sistema          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Procesamiento concurrente y paralelo)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │          Métrica de Rendimiento (Throughput)            │
 │  * Conteo de tareas finalizadas por segundo (Jobs/sec)  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Salida de resultados)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Procesos Ejecutados Exitosamente               │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. (Capítulo 5
