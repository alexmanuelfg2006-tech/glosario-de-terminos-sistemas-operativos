>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Interbloqueo (Deadlock) / Deadlock

Según Silberschatz et al. (2018), el interbloqueo es una situación en la cual un conjunto de procesos se bloquea permanentemente debido a que cada proceso posee un recurso y espera adquirir otro retenido por otro. Estado de bloqueo permanente en el que un conjunto de procesos se encuentra inactivo de forma indefinida debido a que cada uno espera un recurso retenido por otro miembro del grupo.


```
 ┌──────────────────────┐                     ┌──────────────────────┐
 │       Hilo A         │                     │       Hilo B         │
 │  * Posee: Recurso 1  │                     │  * Posee: Recurso 2  │
 │  * Espera: Recurso 2 │                     │  * Espera: Recurso 1 │
 └──────────┬───────────┘                     └──────────▲───────────┘
            │                                            │
            └─────────────► [ BLOQUEO CIRCULAR ] ────────┘
                    (Ninguno puede avanzar ni liberar)
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 8