>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Espera Circular / Circular Wait

Según Silberschatz et al. (2018), la espera circular es una cadena cerrada de procesos en la cual cada proceso aguarda por un recurso que se encuentra retenido y controlado por el siguiente en la estructura. Cadena cerrada de dos o más procesos en la cual cada elemento espera un recurso retenido por el siguiente miembro de la secuencia, cerrando un ciclo de dependencias.



```
        ┌─────────────────────────────────────────┐
        ▼                                         │
 ┌──────────────┐                        ┌──────────────┐
 │  Proceso A   │                        │  Proceso C   │
 │  espera a B  │                        │  espera a A  │
 └──────┬───────┘                        └──────────────┘
        │                                         ▲
        │                                         │
        │                ┌───────────────┐        │
        └──────────────► │   Proceso B   │ ───────┘
                         │  espera a C   │
                         └───────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 8