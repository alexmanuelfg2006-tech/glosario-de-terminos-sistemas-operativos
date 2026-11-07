>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
PML5 / Nivel 5 de Tabla de Páginas

Tanenbaum y Bos (2015) detallan esta ampliación de la paginación a 5 niveles en procesadores x86-64 para direccionar hasta 128 PiB de memoria virtual y 4 PB de RAM física con buses de 57 bits. Agrega un quinto nivel de tabla jerárquica sobre el esquema PML4 tradicional para satisfacer las demandas de memoria extremas de centros de datos de supercomputación. Permite a servidores de hipervisores y bases de datos gigantescas gestionar terabytes de RAM sin agotar los límites del espacio de direcciones virtual. Requiere soporte explícito del procesador y kernel.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Registro CR3 (Arquitectura LA57)          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Índice extendido para direccionamiento de 57 bits)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 Tabla PML5 (Nivel 5)                    │
 │  * Amplía el límite de memoria virtual hasta 4 Petabytes│
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta a la jerarquía PML4 estándar)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │            Jerarquía Completa (PML4 ➔ PDPT ➔ PD ➔ PT)   │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
