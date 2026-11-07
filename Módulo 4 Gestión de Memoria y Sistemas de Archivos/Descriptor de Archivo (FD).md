>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Descriptor de Archivo (FD) / File Descriptor (FD)

Tanenbaum y Bos (2015) clasifican esta abstracción como la referencia numérica entera no negativa asignada por el kernel POSIX a cada recurso de entrada/salida o archivo abierto por un proceso. Funciona como un índice dentro de la tabla interna de descriptores del proceso que apunta a la estructura del archivo abierto en el sistema. Los procesos utilizan estos enteros simples para invocar operaciones de lectura, escritura y posicionamiento mediante llamadas al sistema. Por convención, el valor 0 corresponde a la entrada estándar, 1 a la salida estándar y 2 al error estándar.


```
 ┌─────────────────────────────────────────────────────────┐
 │        Proceso Ejecutándose en el Espacio de Usuario    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Solicita abrir recurso, ej. open())
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Descriptor de Archivo (FD, ej. 0, 1, 2, 3...)   │
 │  * Índice numérico en la tabla de archivos del proceso  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta a la tabla global de archivos abiertos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Estructura de Datos del Kernel y Inodo          │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
