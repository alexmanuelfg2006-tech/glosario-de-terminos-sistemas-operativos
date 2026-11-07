>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Retención y Espera / Hold and Wait

Según Silberschatz et al. (2018), la condición de retención y espera ocurre cuando un proceso que ya tiene recursos asignados solicita nuevos recursos y permanece a la espera sin liberar los que posee. Es una condición de interbloqueo donde un proceso mantiene en su poder al menos un recurso asignado mientras se encuentra a la espera de otros recursos


```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso en Ejecución Activa               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Adquiere y retiene)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Recurso A (Asignado y Retenido por el Proceso)  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Solicita adicionalmente y se bloquea)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │    En Espera de Recurso B (Ocupado por otro proceso)    │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 8