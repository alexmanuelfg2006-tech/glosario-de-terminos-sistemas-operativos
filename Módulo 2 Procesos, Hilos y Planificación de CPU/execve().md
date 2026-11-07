>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Llamada al sistema `execve()` / `execve()` System Call

Según Silberschatz et al. (2018), `execve()` es la llamada al sistema que reemplaza la imagen de memoria actual del proceso en ejecución cargando un nuevo archivo ejecutable, reiniciando los segmentos de texto, datos, montón y pila. Esta llamada sustituye los codigos, los datos, la pila y el monton del proceso actual con los de el nuevo proceso que se va a a cargar


```
 ┌─────────────────────────────────────────────────────────┐
 │            Proceso Actual (Espacio de Memoria Antiguo)  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Invoca execve("/bin/ls", argv, envp))
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Reemplazo de Imagen en el Kernel (Ring 0)       │
 │  * Se limpia el segmento de texto, datos, pila y heap   │
 │  * Se carga el nuevo binario ejecutable desde el disco  │
 │  * El PID del proceso se conserva intacto               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Inicia ejecución desde el nuevo punto de entrada _start)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Nuevo Programa Ejecutándose (Mismo PID)        │
 └─────────────────────────────────────────────────────────┘
```


### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 3