>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Búfer de Traducción Asociativa / Translation Lookaside Buffer

Según Silberschatz et al. (2018), el _Translation Lookaside Buffer_ (TLB) es una memoria asociativa de hardware de alta velocidad utilizada para acelerar significativamente la traducción de direcciones virtuales, almacenando las entradas de la tabla de páginas consultadas con mayor frecuencia. Es una memoria caché especial de hardware de alta velocidad ubicada dentro de la MMU del procesador, encargada de almacenar las traducciones más recientes de páginas virtuales a marcos físicos.


```
 ┌─────────────────────────────────────────────────────────┐
 │               CPU Genera Dirección Lógica               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Consulta paralela en la caché)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         TLB (Translation Lookaside Buffer)              │
 │  * Memoria asociativa de alta velocidad (Hardware)      │
 │  * Almacena pares recientes [Página Virtual ➔ Marco]    │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Si encuentra la entrada)               ▼ (Si no la encuentra)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │         TLB HIT              │          │          TLB MISS            │
 │ (Traducción inmediata en CPU)│          │ (Requiere consultar la RAM)  │
 └──────────────────────────────┘          └──────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9
