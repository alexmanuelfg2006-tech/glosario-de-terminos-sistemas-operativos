>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Planificador Completamente Justo / Completely Fair Scheduler

Según Bovet y Cesati (2005), el _Completely Fair Scheduler_ (CFS) es un algoritmo de Linux diseñado para maximizar la equidad en la distribución del tiempo de CPU, sustituyendo los quántums de tiempo tradicionales por un modelo basado en ponderación de ejecución representado sobre una estructura de árbol rojinegro. Es el planificador de CPU predeterminado en el núcleo de Linux desde la versión 2.6.23. A diferencia de los algoritmos basados en colas con quántums fijos, el CFS busca emular un procesador ideal multiprocesamiento asignando a cada tarea una proporción equitativa del tiempo del procesador


```
 ┌─────────────────────────────────────────────────────────┐
 │               Procesos Listos en el Sistema             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asignación de vruntime basado en uso de CPU)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Árbol Rojinegro (Red-Black Tree del CFS)        │
 │  * Ordenado por el tiempo virtual (vruntime menor a izq.)│
 │  * El nodo más a la izquierda es seleccionado siempre   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Despacho del nodo izquierdo)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Núcleo de la CPU (Ejecución y Actualización)   │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Bovet, D. P., & Cesati, M. (2005). _Understanding the Linux Kernel_ (3.ª ed.). O'Reilly Media. Capítulo 11