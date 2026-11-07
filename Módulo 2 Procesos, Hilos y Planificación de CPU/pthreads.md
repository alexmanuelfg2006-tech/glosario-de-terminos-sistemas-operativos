>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Hilos POSIX (pthreads) / POSIX Threads (pthreads)

Según Silberschatz et al. (2018), POSIX Threads o `pthreads` representa el estándar IEEE 1003.1c que especifica una API para la creación y manipulación de hilos en lenguaje C, pudiendo implementarse tanto a nivel de usuario como de kernel según el sistema operativo subyacente. Permite que un programa divida su trabajo en varios hilos de ejecucion 


```
 ┌─────────────────────────────────────────────────────────┐
 │             Aplicación de Usuario (C / C++)             │
 │     (Invoca funciones: pthread_create, mutex, join)     │
 └────────────────────────────┬────────────────────────────┘
                              │ (Enlace con biblioteca pthreads)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Biblioteca pthreads (NPTL en Linux)          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Llamadas al sistema subyacentes, ej. clone)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Gestión de Hilos en el Kernel (Ring 0)    │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 4
