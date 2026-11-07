>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Monitor residente / resident monitor

Según Stallings (2017), el monitor residente fue una forma primitiva de sistema operativo que se mantenía permanentemente cargada en la memoria principal con el propósito de automatizar la carga e iniciación secuencial de los trabajos del sistema por lotes. el monitor residente se encargaba de que las tareas se iniciaran mas rapido manteniendolas cargadas en la memoria

Fragmento de código

```
sequenceDiagram
    autonumber
    participant RAM as Memoria RAM (Alta / Baja)
    participant Monitor as Monitor Residente (Kernel primitivo)
    participant Job as Programa de Usuario

    Note over RAM, Monitor: El monitor reside permanentemente en memoria protegida
    Monitor->>Job: Carga el primer trabajo desde cinta/lector
    Job->>Job: Ejecuta instrucciones de usuario
    Job->>Monitor: Encuentra macro de control (ej. $END / HALT)
    Monitor->>Monitor: Limpia registros, recupera control y carga siguiente trabajo
```

### Referencias
Stallings, W. (2017). _Operating Systems: Internals and Design Principles_ (9.ª ed.). Pearson.Capítulo 2