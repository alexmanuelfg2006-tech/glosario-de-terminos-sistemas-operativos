>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Condiciones de Coffman / Coffman Conditions

Según Stallings (2017), las condiciones de Coffman describen los cuatro axiomas estructurales indispensables que deben coexistir en un sistema para que un escenario de interbloqueo pueda manifestarse. Es un conjunto de cuatro condiciones necesarias y simultáneas (exclusión mutua, retención y espera, no apropiación y espera circular) que deben cumplirse para generar un interbloqueo.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Sistema Multiproceso y Recursos           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Se cumplen simultáneamente las 4 reglas)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 Las 4 Condiciones de Coffman            │
 │  1. Exclusión Mutua (Recursos no compartibles)          │
 │  2. Retención y Espera (Retiene uno y pide otro)        │
 │  3. No Apropiación (No se pueden arrebatar recursos)    │
 │  4. Espera Circular (Cadena cerrada de dependencias)    │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │            ESTADO CRÍTICO DE INTERBLOQUEO               │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Stallings, W. (2017). _Operating Systems: Internals and Design Principles_ (9.ª ed.). Pearson. (Capítulo 6