>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Segmento de Datos Inicializados / Data Segment

Según Silberschatz et al. (2018), el segmento de datos es la sección del espacio de direcciones de un proceso que alberga a las variables globales y estáticas que han sido explícitamente inicializadas con un valor por el programador antes de la compilación. Es una region de la memoria virtual donde se almacena las variables globales de un programa y permanecen activas desde que se inicia un programa hasta que se finaliza 

```
 ┌─────────────────────────────────────────────────────────┐
 │          Declaración de Variables Globales / Estáticas  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asignación en imagen de memoria durante el arranque)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Segmento de Datos en Memoria Virtual (Data)     │
 │    * Variables globales y estáticas con valor inicial   │
 │    * Permisos de memoria configurados como: RW-         │
 │    * Persiste durante todo el ciclo de vida del proceso │
 └────────────────────────────┬────────────────────────────┘
                              │ (Acceso y modificación de valores por la CPU)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Operaciones de Lectura / Escritura          │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 3