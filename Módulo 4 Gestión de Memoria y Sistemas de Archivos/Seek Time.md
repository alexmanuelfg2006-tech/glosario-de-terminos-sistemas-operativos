>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Seek Time / Tiempo de Búsqueda de Pista

Silberschatz et al. (2018) definen este parámetro mecánico como el intervalo necesario para posicionar el brazo electromagnético de lectura/escritura sobre la pista cilíndrica del disco. Representa la fase más lenta y costosa dentro del proceso global de acceso a datos en unidades magnéticas tradicionales, promediando varios milisegundos. Los planificadores de E/S del kernel intentan minimizar este tiempo reordenando las peticiones pendientes para reducir los desplazamientos físicos del cabezal. Es inexistente en unidades SSD.


```
 ┌─────────────────────────────────────────────────────────┐
 │         Solicitud de Lectores / Escritores              │
 └────────────────────────────┬────────────────────────────┘
                              │ (El brazo actuador inicia movimiento físico)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Seek Time (Tiempo de Búsqueda)              │
 │  * Movimiento mecánico del brazo a lo largo del radio   │
 │  * Depende de la distancia física entre las pistas      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Posicionamiento correcto sobre la pista)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │        Cabezal Alineado en la Pista Destino             │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
