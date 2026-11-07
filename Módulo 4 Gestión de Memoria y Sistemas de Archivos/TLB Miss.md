>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Fallo de TLB /  TLB miss 

Según Silberschatz et al. (2018), un _TLB miss_ representa el fallo de coincidencia en la caché de traducción, lo que obliga al sistema a incurrir en un acceso adicional a la tabla de páginas residente en la memoria principal para recuperar el mapeo físico correcto. Se manifiesta cuando la MMU busca una página virtual en la TLB pero no encuentra su correspondencia porque la entrada no está en la caché.


```
 ┌─────────────────────────────────────────────────────────┐
 │        CPU Consulta la Dirección Virtual en la MMU      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Búsqueda infructuosa)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 TLB MISS (Fallo en Caché)               │
 │  * La traducción no está presente en la TLB             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Acceso obligatorio a la Tabla de Páginas en RAM)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │    Recuperación de PTE en RAM y Actualización de TLB    │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9