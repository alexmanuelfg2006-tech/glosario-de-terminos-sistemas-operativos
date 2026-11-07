>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Hiperpaginado / Thrashing

Según Silberschatz et al. (2018), el hiperpaginado (_thrashing_) es una condición patológica en la cual un sistema operativo pasa la mayor parte de su tiempo realizando operaciones de transferencia de páginas hacia el disco secundario debido a la insuficiencia crónica de marcos libres en la RAM. Es un estado crítico de degradación severa del rendimiento en un sistema operativo con memoria virtual.


```
 ┌─────────────────────────────────────────────────────────┐
 │        Procesos con Exceso de Páginas Activas           │
 └────────────────────────────┬────────────────────────────┘
                              │ (La RAM no puede contener el Working Set)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Bucle Crítico de Hiperpaginado               │
 │  * Fallos de página masivos y continuos                 │
 │  * CPU saturada esperando operaciones de E/S de disco   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Degradación severa del rendimiento global)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Colapso Operativo / Rendimiento Prácticamente 0 │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 10
