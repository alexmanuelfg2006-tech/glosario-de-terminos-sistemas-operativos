>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
acierto de TLB / TLB hit

Según Silberschatz et al. (2018), un _TLB hit_ es el evento favorable en el cual la entrada de traducción de la página virtual buscada se encuentra residente dentro de la caché asociativa de la TLB, permitiendo una resolución de direcciones virtual-a-física de velocidad óptima. Ocurre cuando la MMU busca el número de página virtual en la TLB y encuentra de inmediato su correspondiente dirección física almacenada en la caché


```
 ┌─────────────────────────────────────────────────────────┐
 │        CPU Consulta la Dirección Virtual en la MMU      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Búsqueda en la memoria asociativa)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 TLB HIT (Acierto en Caché)              │
 │  * La traducción existe y es válida en la TLB           │
 │  * Tiempo de acceso ultrarrápido (Sin retraso de RAM)   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Obtención directa del marco físico)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │               Acceso Inmediato a la Memoria             │
 └─────────────────────────────────────────────────────────┘
```
### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9