>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Monton / Heap

Según Silberschatz et al. (2018), el montón es la región del espacio de direcciones asignada dinámicamente durante el tiempo de ejecución de un programa mediante solicitudes explícitas del código (como `malloc` en C o `new` en C++). es un area de la memoria donde se asignan detos de forma dinamica pero no es automatica como la pila se tiene que asignar mediante comandos.


```
 ┌─────────────────────────────────────────────────────────┤
 │             Segmento de Datos / BSS                     │
 ├─────────────────────────────────────────────────────────┤
 │          Montículo (Heap - Crecimiento Ascendente)        │
 │    * Memoria dinámica solicitada por el programa        │
 │    * Gestionada mediante llamadas al sistema (brk/sbrk) │
 ├─────────────────────────────────────────────────────────┤
 │                            ↑                            │
 │                   (Espacio Libre / Mapped)              │
 ├─────────────────────────────────────────────────────────┤
 │                        Pila (Stack)                     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 3