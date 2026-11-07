>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
conjunto de trabajo / Working Set Model

Según Silberschatz et al. (2018), el modelo del _working set_ (conjunto de trabajo) es una aproximación basada en la localidad de las referencias que delimita el número activo de páginas que un proceso requiere mantener en la memoria física durante una ventana temporal para evitar fallos excesivos. Es un modelo teórico basado en el principio de localidad que define el conjunto exacto de páginas que un proceso necesita tener residentes en la memoria RAM para poder ejecutarse de manera fluida


```
 ┌─────────────────────────────────────────────────────────┤
 │       Secuencia de Referencias de Memoria del Proceso   │
 │       [ Pág 1 ] ➔ [ Pág 3 ] ➔ [ Pág 1 ] ➔ [ Pág 4 ]     │
 └────────────────────────────┬────────────────────────────┘
                              │ (Evaluación en ventana temporal Δ)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Working Set (Conjunto de Trabajo)           │
 │  * Páginas activas necesarias: { Pág 1, Pág 3, Pág 4 }  │
 │  * Requisito: Memoria asignada >= Tamaño del Working Set│
 └────────────────────────────┬────────────────────────────┘
                              │ (Garantía de estabilidad operativa)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Ejecución Fluida sin Fallos Excesivos          │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 10