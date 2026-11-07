>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Página Virtual / Virtual Page

Según Silberschatz et al. (2018), una página virtual es una unidad contigua de tamaño uniforme perteneciente al espacio de direcciones lógicas de un programa, susceptible de ser reubicada o transferida entre la memoria secundaria y la principal. Es un bloque de memoria de tamaño fijo en el que se subdivide el espacio de direcciones lógicas de un proceso en un sistema paginado.


```
 ┌─────────────────────────────────────────────────────────┐
 │             Memoria Virtual del Proceso                 │
 └────────────────────────────┬────────────────────────────┘
                              │ (División en bloques contiguos de tamaño fijo)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Página Virtual (Ej. 4 KB)                 │
 │  * Número de Página (Bits altos para índice de tabla)   │
 │  * Desplazamiento / Offset (Bits bajos para posición)   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Enviado a la Tabla de Páginas / MMU)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Traducción a Marco Físico                 │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 10