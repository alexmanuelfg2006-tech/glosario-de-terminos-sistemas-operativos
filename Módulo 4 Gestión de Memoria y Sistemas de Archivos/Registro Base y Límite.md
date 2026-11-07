>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Registro Base y Límite / Base and Limit Registers

Según Silberschatz et al. (2018), los registros base y límite son un par de registros de hardware de protección que delimitan el rango de direcciones físicas válidas asignadas a un proceso específico para evitar accesos indebidos a zonas del sistema o de otros procesos. Es un mecanismo de protección de memoria básico implementado por hardware. El registro base almacena la dirección física inicial de la RAM asignada a un proceso, mientras que el registro límite almacena el tamaño máximo de dicho segmento


```
 ┌─────────────────────────────────────────────────────────┐
 │               CPU Genera Dirección Lógica               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Comparación previa en hardware)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Validación en Registros Base y Límite           │
 │  * ¿Dirección < Límite? ➔ Si NO, genera Violación de Mem │
 │  * Dirección Física = Dirección Lógica + Registro Base  │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────    ┴    ────────────────┐
         ▼ (Si es válida)                          ▼ (Si excede el límite)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │    Acceso exitoso a la       │          │  Interrupción por Violación  │
 │     Memoria Física           │          │    de Segmento (SegFault)    │
 └──────────────────────────────┘          └──────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9