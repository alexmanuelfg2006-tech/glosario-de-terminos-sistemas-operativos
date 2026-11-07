>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Tabla de Páginas Multinivel / Multilevel Page Table

Según Silberschatz et al. (2018), la tabla de páginas multinivel es un esquema de organización jerárquica de la memoria que descompone el espacio de direcciones virtuales en múltiples niveles de tablas de páginas para reducir el consumo continuo de memoria RAM. Es una estructura jerárquica que fragmenta una tabla de páginas lineal de gran tamaño en múltiples sub-tablas encadenadas.


```
 ┌─────────────────────────────────────────────────────────┐
 │          Acceso de Lectura o Escritura a Página         │
 └────────────────────────────┬────────────────────────────┘
                              │ (El hardware registra el uso)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Referenced Bit (Indicador de Actividad)         │
 │  * Bit = 1: Página accedida recientemente               │
 │  * Bit = 0: Página inactiva (Candidata para reemplazo)  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Revisado periódicamente por el Kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │       Optimización de Reemplazo de Páginas              │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9