>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Paginación / Paging

Según Silberschatz et al. (2018), la paginación es un esquema de organización de la memoria que evita la necesidad de asignación física contigua dividiendo la memoria lógica en bloques del mismo tamaño llamados páginas y la memoria física en marcos. Es una técnica de gestión de memoria que Consiste en dividir el espacio de direcciones lógicas de un proceso en bloques de tamaño fijo llamados páginas, y la memoria física RAM en bloques exactamente de la misma dimensión llamados marcos de página.


```
 ┌─────────────────────────────────────────────────────────┐
 │               CPU Genera Dirección Lógica               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Comparación previa en hardware)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Validación en Registros Base y Límite           │
 │  * ¿Dirección < Límite? ➔ Si NO, genera Violación de Mem │
 │  * Dirección Física = Dirección Lógica + Registro Base  │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────    ┴    ────────────────┐
         ▼ (Si es válida)                          ▼ (Si excede el límite)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │    Acceso exitoso a la       │          │  Interrupción por Violación  │
 │     Memoria Física           │          │    de Segmento (SegFault)    │
 └──────────────────────────────┘          └──────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9