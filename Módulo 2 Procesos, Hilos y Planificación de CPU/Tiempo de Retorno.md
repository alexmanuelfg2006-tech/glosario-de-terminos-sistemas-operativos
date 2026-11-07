>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
**Tiempo de Retorno / Turnaround Time

Según Silberschatz et al. (2018), el tiempo de retorno (_turnaround time_) es el período completo que abarca desde la presentación inicial de un proceso para su procesamiento hasta la entrega total de sus resultados y posterior terminación. Es el intervalo de tiempo total transcurrido desde el momento exacto en que un usuario somete un proceso al sistema para su ejecución hasta el instante preciso en que este completa


```
 ┌─────────────────────────────────────────────────────────┐
 │       Instante de Llegada del Proceso al Sistema        │
 └────────────────────────────┬────────────────────────────┘
                              │ (Transcurso del tiempo: Espera + Ejecución + E/S)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Cálculo del Tiempo de Retorno                │
 │  * Turnaround = Tiempo de Finalización - Tiempo de Llegada│
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Instante de Finalización del Proceso           │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5