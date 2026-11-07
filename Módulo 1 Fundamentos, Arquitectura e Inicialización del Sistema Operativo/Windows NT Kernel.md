>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Nucleo windowns nt / windows nt kernel

Según Russinovich et al. (2012), el núcleo de Windows NT es una arquitectura híbrida orientada a objetos que brinda portabilidad, multiprocesamiento simétrico y soporte multi-subsistema mediante abstracciones como el _Executive_ y el _HAL_ (_Hardware Abstraction Layer_). es el nucleo de los sistemas windows actuales y separa la parte de modo usuario y modo kernel


PowerShell

```
Get-CimInstance Win32_OperatingSystem | Select-Object Caption, Version, BuildNumber
```

```
 ┌─────────────────────────────────────────────────────────┐
 │             Aplicaciones Win32 / UWP (Ring 3)           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Llamadas a la API nativa de Windows)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Subsistemas del Núcleo Windows (Ring 0)         │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Windows Executive (Gestión de objetos, seguridad) │  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ NT Kernel (Scheduler, sincronización, traps)      │  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ HAL (Hardware Abstraction Layer) y Drivers (WDM)  │  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                     Hardware Físico                     │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Russinovich, M., Solomon, D., & Ionescu, A. (2012). _Windows Internals_ (6.ª ed., Parte 1). Microsoft Press.Capítulo 1