>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Llamada al sistema `fork()` / `fork()` System Call

Según Tanenbaum y Bos (2015), `fork()` es la llamada al sistema estándar en sistemas tipo UNIX mediante la cual un proceso genera un proceso hijo clonando casi de manera idéntica su espacio de direcciones y contexto de ejecución. esta llamada duplica un proceso creando un proceso hijo  de un proceso existente excepto por el valor que retorna


```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso Padre (Ejecutándose)              │
 └────────────────────────────┬────────────────────────────┘
                              │ (Invoca llamada al sistema fork())
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Duplicación en el Kernel (Copy-on-Write)        │
 │  * Se crea un nuevo PCB con un PID único                │
 │  * Se clonan los descriptores de archivos y memoria     │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Retorno para el Padre)                 ▼ (Retorno para el Hijo)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │ Retorna el PID del hijo      │          │ Retorna 0                    │
 │ (Proceso original)           │          │ (Proceso clonado)            │
 └──────────────────────────────┘          └──────────────────────────────┘
```

### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson.Capítulo 2