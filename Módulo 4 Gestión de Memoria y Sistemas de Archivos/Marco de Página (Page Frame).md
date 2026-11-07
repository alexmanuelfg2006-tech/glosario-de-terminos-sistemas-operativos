>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Marco de Página / Page Frame

Según Silberschatz et al. (2018), un marco de página o _page frame_ representa cada una de las divisiones físicas de tamaño fijo que conforman la memoria principal, destinadas a albergar individualmente a las páginas virtuales de los procesos. Es una sección física de tamaño uniforme en la que se divide la memoria RAM principal para dar soporte a la paginación. Su tamaño coincide exactamente con el de las páginas virtuales del sistema


```
 ┌─────────────────────────────────────────────────────────┤
 │         Memoria Física (RAM Dividida en Marcos)         │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Marco de Página 0 (Ocupado por Proceso A)         │  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Marco de Página 1 (Ocupado por Proceso B)         │  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Marco de Página 2 (Libre / Disponible)            │  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asignación gestionada por el Kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Almacenamiento Físico de Datos Reales          │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9