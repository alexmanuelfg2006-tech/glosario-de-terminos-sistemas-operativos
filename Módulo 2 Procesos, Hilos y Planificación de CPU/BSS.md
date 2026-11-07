>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Segmento BSS (Bloque Comenzado por Símbolo / BSS Segment (Block Started by Symbol)

Según Stallings (2017), el segmento BSS es la región del espacio de memoria de un programa reservada para las variables globales y estáticas no inicializadas, las cuales son puestas a cero por el sistema operativo antes de comenzar la ejecución. es una parte de un archivo ejecutable que almacena variables globales y estaticas que no han sido inicializadas o que se inicializan en 0


```
 ┌─────────────────────────────────────────────────────────┐
 │       Declaración de Variables Globales / Estáticas     │
 │                (Sin valor inicial asignado)             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asignación en imagen de memoria durante el arranque)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Segmento BSS en Memoria Virtual              │
 │    * Variables globales y estáticas no inicializadas    │
 │    * Inicializadas automáticamente a cero (0) por el OS │
 │    * Permisos de memoria configurados como: RW-         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Modificación dinámica durante la ejecución)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Escritura y Asignación en Runtime           │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Stallings, W. (2017). _Operating Systems: Internals and Design Principles_ (9.ª ed.). Pearson.Capítulo 3