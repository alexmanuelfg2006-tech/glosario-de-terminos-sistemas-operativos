>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Journaling / Registro de Transacciones en Disco

Tanenbaum y Bos (2015) explican este mecanismo como el proceso que registra las operaciones de archivo no confirmadas en una bitácora antes de plasmarlas en la estructura principal para evitar fallos por cortes. Si el sistema sufre una interrupción eléctrica inesperada, el kernel examina el diario durante el arranque para completar las transacciones pendientes o revertir los cambios incompletos. Evita la necesidad de ejecutar análisis extensivos del disco completo mediante fsck tras un colapso. Garantiza la consistencia estructural del sistema de archivos.


```
 ┌─────────────────────────────────────────────────────────┐
 │          Operación de Modificación de Archivos          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Escribe primero la intención de la transacción)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Área de Diario (Journal / Log en Disco)         │
 │  * Registro secuencial de cambios pendientes            │
 └────────────────────────────┬────────────────────────────┘
                              │ (Una vez registrado de forma segura, se aplica)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │        Escritura Definitiva en el Sistema de Archivos   │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
