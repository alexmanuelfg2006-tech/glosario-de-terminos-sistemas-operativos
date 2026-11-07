>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
PML4 / Nivel 4 de Tabla de Páginas

Silberschatz et al. (2018) analizan este esquema de paginación de 4 niveles en la arquitectura x86-64 capaz de mapear hasta 512 GiB de memoria virtual por proceso mediante buses de 48 bits. Traduce las direcciones virtuales emitidas por la CPU en direcciones físicas de RAM navegando progresivamente a través de cuatro niveles de tablas indexadas. Cada tabla PML4 contiene 512 entradas que apuntan a tablas de directorio de páginas secundarias. Constituyó el estándar de paginación de 64 bits en procesadores modernos hasta la llegada de PML5.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Registro CR3 (Dirección Base)             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Bits de índice superior de la dirección virtual)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 Tabla PML4 (Nivel 4)                    │
 │  * Contiene entradas (PML4E) que apuntan a directorios  │
 └────────────────────────────┬────────────────────────────┘
                              │ (PAGD / Directorio de Páginas)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Jerarquía Descendente (PDPT ➔ PD ➔ PT)         │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
