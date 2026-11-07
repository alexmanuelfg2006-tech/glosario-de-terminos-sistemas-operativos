>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Bit sucio / Dirty Bit

Según Silberschatz et al. (2018), el _dirty bit_ o bit de modificación es una marca de hardware en la tabla de páginas que registra si una página ha sido alterada en memoria, evitando escrituras innecesarias en el almacenamiento secundario durante un reemplazo de página. Es un bit de control en la PTE que la unidad de gestión de memoria activa automáticamente con un 1 en el momento en que se efectúa cualquier operación de escritura sobre esa página.


```
 ┌─────────────────────────────────────────────────────────┐
 │         Operación de Escritura sobre la Página          │
 └────────────────────────────┬────────────────────────────┘
                              │ (El hardware actualiza la PTE)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Dirty Bit (Bit de Modificación)             │
 │  * Bit = 0: La página no ha sido modificada desde su carga│
 │  * Bit = 1: La página fue alterada (Dirty) y requiere   │
 │             escribirse de vuelta en el disco (Swap)     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 10