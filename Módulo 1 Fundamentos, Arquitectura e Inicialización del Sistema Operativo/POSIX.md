>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Posix / Portable Operating System Interface

Según Tanenbaum y Bos (2015), POSIX (_Portable Operating System Interface_) es un estándar definido por el IEEE para establecer un conjunto unificado de APIs y llamadas al sistema que garanticen que el software escrito para un sistema tipo UNIX sea fácilmente compilable en otros. posix es un estandar para mejorar la compatibilidad entre diferentes sistemas operativos unix


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
anenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson. Capítulo 10