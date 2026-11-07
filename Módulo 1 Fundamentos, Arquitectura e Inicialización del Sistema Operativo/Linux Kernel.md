>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Nucleo linux / Linux kernel

Según Bovet y Cesati (2005), el _kernel_ de Linux es un núcleo monolítico y modular basado en los estándares UNIX que administra de manera directa los componentes físicos del hardware y distribuye los tiempos de ejecución mediante algoritmos avanzados.es el nucleo de los sistemas operativos tipo unix

Bash

```
uname -r
cat /proc/version
```


```
 ┌─────────────────────────────────────────────────────────┐
 │             Aplicaciones de Usuario (Ring 3)            │
 └────────────────────────────┬────────────────────────────┘
                              │ (Llamadas al Sistema / API POSIX)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │               Espacio del Núcleo Linux (Ring 0)         │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Planificador (CFS)  │ Gestión de Memoria (MMU)    │  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Subsistema VFS (Archivos) │ Red (Netfilter/TCP)   │  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Módulos y Controladores de Dispositivos (Drivers) │  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Control directo de buses y dispositivos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                     Hardware Físico                     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Bovet, D. P., & Cesati, M. (2005). _Understanding the Linux Kernel_ (3.ª ed.). O'Reilly Media. Capítulo 1