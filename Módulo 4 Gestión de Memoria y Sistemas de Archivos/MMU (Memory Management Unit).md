>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Unidad de Gestión de Memoria / Memory Management Unit

Según Silberschatz et al. (2018), la MMU (_Memory Management Unit_) es un dispositivo de hardware especializado que efectúa en tiempo de ejecución el mapeo dinámico entre direcciones lógicas virtuales y direcciones físicas en la memoria principal. Es un componente de hardware integrado en el procesador responsable de realizar la traducción en tiempo real de las direcciones lógicas solicitadas por la CPU a las direcciones físicas reales de la RAM


```
 ┌─────────────────────────────────────────────────────────┐
 │               CPU Genera Dirección Lógica               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Envía dirección virtual)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │       Unidad de Gestión de Memoria (MMU Hardware)       │
 │  * Consulta rápida en caché TLB (Translation Lookaside Buffer) │
 │  * Traducción de dirección lógica a dirección física    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Acceso a dirección física traducida)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Memoria Física (RAM del Sistema)            │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9