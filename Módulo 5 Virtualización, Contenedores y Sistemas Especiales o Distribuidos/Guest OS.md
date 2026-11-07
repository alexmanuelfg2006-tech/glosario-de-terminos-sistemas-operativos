>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Guest OS / Sistema Operativo Invitado

Silberschatz et al. (2018) definen este término para señalar al sistema operativo secundario que se ejecuta dentro del entorno virtualizado proporcionado y administrado por un hipervisor. Opera creyendo de manera transparente que posee el acceso directo al hardware físico de la máquina, aunque sus instrucciones son arbitradas por la capa de virtualización. Posee sus propios controladores, núcleo, espacio de usuario y aplicaciones aisladas de la máquina anfitriona. Se pueden ejecutar múltiples sistemas invitados heterogéneos sobre una misma plataforma física.


```
 ┌─────────────────────────────────────────────────────────┤
 │           Guest OS (Sistema Operativo Invitado)         │
 │  * Su propio Kernel, Procesos, Archivos y Aplicaciones  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Peticiones interceptadas por la capa de virtualización)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Hipervisor / Virtualizador (VMM)            │
 └────────────────────────────┬────────────────────────────┘
                              │ (Traducción hacia los recursos reales)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Recursos Físicos del Host (CPU, RAM, E/S)       │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
