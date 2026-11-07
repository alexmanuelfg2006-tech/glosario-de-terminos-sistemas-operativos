>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
HDD / Unidad de Disco Duro Magnético

Silberschatz et al. (2018) describen este dispositivo de almacenamiento masivo electromagnético que registra datos en platos metálicos giratorios mediante cabezales de lectura/escritura. Las operaciones de lectura implican movimientos mecánicos para posicionar el brazo sobre la pista requerida (Seek Time) y esperar la rotación del sector (Latencia Rotacional). El kernel del SO aplica algoritmos de planificación de disco como SCAN o C-SCAN para reordenar las peticiones y mitigar la lentitud mecánica. Sigue siendo utilizado por su bajo costo por terabyte.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Platos Magnéticos Giratorios              │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Pistas Concéntricas y Sectores Magnéticos         │  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────▲────────────────────────────┘
                              │ (Acceso físico mediante brazo actuador)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Cabezal de Lectura / Escritura Mecánico         │
 │  * Desplazamiento físico sobre la superficie del plato  │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │            Transferencia de Datos por E/S               │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
