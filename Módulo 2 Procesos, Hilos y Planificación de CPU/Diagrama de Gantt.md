>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Diagrama de Gantt / Gantt Chart

Según Silberschatz et al. (2018), un diagrama de Gantt es un recurso de representación visual mediante barras temporales que permite modelar y estudiar la asignación secuencial del procesador a los distintos procesos presentes en el sistema.Es un gráfico de barras horizontales utilizado como representación visual del comportamiento de la CPU a lo largo del tiempo.


```
 ┌─────────────────────────────────────────────────────────┐
 │                Línea de Tiempo del Sistema              │
 ├───────────┬───────────┬───────────┬───────────┬───────────┤
 │  P1 (0-3) │  P2 (3-5) │  P3 (5-8) │  P1 (8-10)│   ...     │
 └───────────┴───────────┴───────────┴───────────┴───────────┘
                              │ (Visualización cronológica de turnos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │      Análisis de Solapamientos, Esperas y Quántums      │
 └─────────────────────────────────────────────────────────┘
```
### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5