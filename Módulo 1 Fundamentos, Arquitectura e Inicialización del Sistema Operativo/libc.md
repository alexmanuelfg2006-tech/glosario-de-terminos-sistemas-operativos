>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Biblioteca Estándar de C / Standard C Library (libc)

Según Tanenbaum y Bos (2015), libc es la biblioteca estándar del lenguaje C que implementa las funciones del sistema fundamentales y sirve de puente entre las aplicaciones de usuario y las llamadas al sistema del núcleo (_syscalls_), traduciendo llamadas de alto nivel como printf()o malloc() en código ejecutable de bajo nivel. Es la libreria de C que nos permite realizar tareas basicas


```
ldd --version
ldd /bin/ls
```

```
 ┌─────────────────────────────────────────────────────────┐
 │               Aplicación de Usuario (Ring 3)            │
 │       (Invoca funciones: printf, fopen, malloc)         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Enlace con biblioteca estándar)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │            libc (GNU C Library / glibc / musl)          │
 │  * Proporciona wrappers y optimizaciones en espacio de  │
 │    usuario antes de invocar servicios del núcleo        │
 └────────────────────────────┬────────────────────────────┘
                              │ (Invocación de Syscall / Trap)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                Espacio del Núcleo (Ring 0)              │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson.Capítulo 1