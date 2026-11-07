>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Tiempo de Respuesta / Response Time

Según Silberschatz et al. (2018), el tiempo de respuesta es el intervalo temporal medido desde la formulación de una solicitud por parte del usuario hasta la emisión de la primera respuesta interactiva por parte de la aplicación. En entornos interactivos y de tiempo compartido, es la cantidad de tiempo que transcurre desde que un usuario emite un mandato o entrada al programa hasta que el sistema genera la primera respuesta visible o retroalimentación inicial en pantalla.

```
 ┌─────────────────────────────────────────────────────────┐
 │               Llegada de Proceso Interactivos           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Espera hasta la primera asignación de CPU)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Cálculo del Tiempo de Respuesta             │
 │  * Response Time = Tiempo de 1ra Ejecución - Llegada    │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │        Primera Interacción / Salida Generada            │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5