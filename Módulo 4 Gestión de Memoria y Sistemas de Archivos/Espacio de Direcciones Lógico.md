>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Espacio de Direcciones Lógico / Logical Address Space

Según Silberschatz et al. (2018), el espacio de direcciones lógico comprende la totalidad del conjunto de direcciones virtuales emitidas por el procesador durante la ejecución de las instrucciones de un programa determinado. Es el conjunto completo de direcciones de memoria que genera la CPU durante la ejecución de un programa en modo usuario.

```
 ┌─────────────────────────────────────────────────────────┐
 │               Código Compilado del Proceso              │
 └────────────────────────────┬────────────────────────────┘
                              │ (Genera referencias a direcciones lógicas / virtuales)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │          Espacio de Direcciones Lógicas (0 a Max)       │
 │  * Perspectiva interna y abstracta del programa         │
 │  * Completamente independiente de la RAM física         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Enviado a la MMU para traducción)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │            Unidad de Gestión de Memoria (MMU)           │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9