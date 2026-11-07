>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Contenedor / Unidad de Software Aislada

Silberschatz et al. (2018) definen esta unidad de software como un entorno ejecutable liviano que empaqueta una aplicación y sus dependencias compartiendo el kernel del sistema anfitrión bajo aislamiento de namespaces. A diferencia de las máquinas virtuales, no requiere emular componentes de hardware ni ejecutar un sistema operativo invitado completo sobre la CPU. Cada contenedor opera en un espacio de procesos aislado con límites de memoria y almacenamiento gestionados por cgroups. Esto permite desplegar cientos de aplicaciones de forma altamente eficiente y portable en infraestructuras de nube.


```
 ┌─────────────────────────────────────────────────────────┐
 │     Aplicación y Dependencias (Espacio de Usuario)      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Aislamiento mediante Namespaces y cgroups)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                        Contenedor                       │
 │  * Sin la sobrecarga de un Sistema Operativo Invitado   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Acceso directo controlado)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Kernel Compartido del Host OS               │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
