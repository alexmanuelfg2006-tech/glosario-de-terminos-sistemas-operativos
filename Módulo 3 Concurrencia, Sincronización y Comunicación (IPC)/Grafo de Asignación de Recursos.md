>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Grafo de Asignación de Recursos / Resource-Allocation Graph 

Según Silberschatz et al. (2018), el grafo de asignación de recursos es una herramienta gráfica formal utilizada para modelar estados del sistema, donde los ciclos indican la presencia de un interbloqueo. Es el modelo gráfico dirigido compuesto por nodos de procesos y recursos que permite visualizar solicitudes y asignaciones vigentes para detectar posibles interbloqueos.

```
 ┌─────────────────────────────────────────────────────────┐
 │               Modelo de Grafo Dirigido (RAG)            │
 └────────────────────────────┬────────────────────────────┘
                              │ (Estructura de Vértices y Aristas)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │  Leyenda de Elementos:                                  │
 │  * Proceso (P): Círculo [ P1 ]                          │
 │  * Recurso (R): Rectángulo con instancias [ R1 (o) ]    │
 │  * Arista de Solicitud (P ➔ R): Proceso pide recurso    │
 │  * Arista de Asignación (R ➔ P): Recurso otorgado a P   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Análisis de ciclos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │     Detección de Ciclo (Equivalente a Interbloqueo)     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 8