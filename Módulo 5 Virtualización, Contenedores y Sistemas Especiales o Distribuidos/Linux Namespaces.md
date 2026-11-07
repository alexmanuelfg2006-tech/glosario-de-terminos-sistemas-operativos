>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Linux Namespaces / Mecanismos de Aislamiento Namespaces

Tanenbaum y Bos (2015) abordan esta tecnología del kernel de Linux que ofrece vistas privadas e aisladas de los recursos del sistema (PID, red, montajes) a grupos de procesos. Permite que un grupo de tareas perciba su propio árbol de procesos comenzando desde el PID 1 o su propia pila de red independiente. Constituye el componente fundamental de la tecnología de contenedores para aislar aplicaciones entre sí sin el overhead de una máquina virtual. Se dividen en namespaces de PID, Mount, Net, IPC, User y UTS.


```
 ┌─────────────────────────────────────────────────────────┐
 │        Procesos Ejecutándose en el Espacio de Usuario   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Filtrado y particionamiento mediante Namespaces)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │          Subsistemas de Namespaces en el Kernel         │
 │  * PID (Aislamiento de identificadores de procesos)     │
 │  * NET (Pilas de red y tarjetas virtuales independientes)│
 │  * MNT (Tablas de puntos de montaje de archivos)        │
 │  * UTS, IPC y USER (Aislamiento de host, memoria y UID) │
 └────────────────────────────┬────────────────────────────┘
                              │ (Resultado: Vista privada y segura de los recursos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                Entorno de Contenedor Aislado            │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
