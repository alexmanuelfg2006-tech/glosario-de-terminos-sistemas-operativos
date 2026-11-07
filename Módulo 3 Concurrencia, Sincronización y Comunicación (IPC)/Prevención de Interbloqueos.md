>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Prevención de Interbloqueos / Deadlock Prevention

Según Silberschatz et al. (2018), la prevención de interbloqueos consiste en estructurar las reglas de asignación para invalidar preventivamente al menos una de las cuatro condiciones necesarias de Coffman. Conjunto de políticas de diseño destinadas a garantizar que al menos una de las condiciones de Coffman jamás se cumpla, imposibilitando la aparición de interbloqueos.


```
 ┌─────────────────────────────────────────────────────────┐
 │              Diseño Preventivo del Sistema              │
 └────────────────────────────┬────────────────────────────┘
                              │ (Invalida preventivamente al menos una condición)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Estrategias sobre las Condiciones de Coffman    │
 │  * Evitar Exclusión Mutua (Spooling / Recursos compartidos)
 │  * Evitar Retención y Espera (Pedir todos de golpe)     │
 │  * Evitar No Apropiación (Permitir arrebatar recursos)  │
 │  * Evitar Espera Circular (Orden jerárquico estricto)   │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          IMPOSIBILIDAD MATEMÁTICA DE INTERBLOQUEO       │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 8