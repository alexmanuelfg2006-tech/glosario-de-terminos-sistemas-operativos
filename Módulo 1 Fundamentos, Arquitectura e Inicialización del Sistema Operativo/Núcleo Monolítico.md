>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---

**Núcleo monolítico / Monolithic kernel

Según Tanenbaum y Bos (2015), un núcleo monolítico es una arquitectura en la cual la totalidad del sistema operativo (gestión de memoria, planificador, controladores) se compila y ejecuta dentro de un único espacio de direcciones integrado con acceso total en modo kernel. un nucleo monolitico ejecuta todos los procesos en un unico espacio del nucleo

```
 ┌─────────────────────────────────────────────────────────┐
 │               Aplicación de Usuario (C / C++)           │
 │       (Utiliza llamadas estándar: fork, read, pthread)  │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Capa de Interfaz POSIX (IEEE 1003)          │
 │    (Definición estandarizada de cabeceras y funciones)  │
 └──────┬─────────────────────┬─────────────────────┬──────┘
        │                     │                     │
        ▼                     ▼                     ▼
 ┌──────────────┐      ┌──────────────┐      ┌──────────────┐
 │ Núcleo Linux │      │ Núcleo *BSD  │      │  macOS XNU   │
 │  (Syscalls)  │      │  (Syscalls)  │      │  (Syscalls)  │
 └──────────────┘      └──────────────┘      └──────────────┘
```

### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson.Capítulo 1