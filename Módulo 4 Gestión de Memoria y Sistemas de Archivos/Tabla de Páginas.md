>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Tabla de Páginas / Page Table

Según Silberschatz et al. (2018), la tabla de páginas es la estructura de datos mantenida por el núcleo que mapea la representación virtual de las páginas de un proceso con las ubicaciones reales de los marcos en la memoria física. Es la estructura de datos que mantiene el sistema operativo por cada proceso activo para registrar la correspondencia entre sus páginas virtuales y los marcos físicos de la memoria RAM donde se ubican realmente.

```
 ┌─────────────────────────────────────────────────────────┐
 │               Número de Página Virtual                  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Consultado como índice en la tabla)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                     Tabla de Páginas                    │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Página 0 ──► Marco Físico 4  [Bit Presente: 1]    │  │
 │  │ Página 1 ──► Marco Físico 9  [Bit Presente: 1]    │  │
 │  │ Página 2 ──► En Disco / Swap [Bit Presente: 0]    │  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Obtención de la dirección física real)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │              Dirección Física en Memoria RAM            │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9