>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Entrada de la Tabla de Páginas / Page Table Entry

Según Silberschatz et al. (2018), una PTE (_Page Table Entry_) representa cada uno de los registros individuales de la tabla de páginas, albergando el número de marco asignado junto con diversos bits de estado y protección asociados. Es la celda o entrada individual dentro de una tabla de páginas que almacena el número de marco de página físico correspondiente a una página virtual.

```
 ┌─────────────────────────────────────────────────────────┐
 │       Estructura Interna de una PTE (Page Table Entry)  │
 ├────────────────────────────┬────────────────────────────┤
 │ Número de Marco Físico     │ Bits de Estado y Control   │
 │ (Dirección base en RAM)    │ (Presencia, Dirty, R/W...) │
 └────────────────────────────┬────────────────────────────┘
                              │ (Interpretado por la MMU en cada acceso)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Traducción y Verificación de Permisos             │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
ilberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9