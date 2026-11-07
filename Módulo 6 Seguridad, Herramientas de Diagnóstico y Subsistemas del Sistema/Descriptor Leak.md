>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Descriptor Leak / Fuga de Descriptores

Silberschatz et al. (2018) abordan esta condición anómala generada cuando un sistema o aplicación omite cerrar descriptores de archivos o sockets abiertos tras concluir su uso. Al acumular descriptores sin liberar, el proceso agota paulatinamente la capacidad de su tabla interna y alcanza el límite máximo asignado por el kernel (ulimit). Como consecuencia, cualquier intento posterior de abrir archivos, crear conexiones de red o instanciar tuberías fallará rotundamente. Su detección requiere el uso de herramientas de inspección como lsof o procfs.


```
 ┌─────────────────────────────────────────────────────────┐
 │       Proceso Abre Recurso del Sistema (open/socket)    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asignación de entrada en la Tabla de Descriptores)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │      Descriptor de Archivo Activo en el Kernel          │
 │  * Ausencia de llamada de cierre (close)                │
 │  * Acumulación progresiva de referencias abiertas       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Saturación de la tabla de archivos del proceso)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │    Colapso Operativo: Imposibilidad de Abrir Archivos   │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
