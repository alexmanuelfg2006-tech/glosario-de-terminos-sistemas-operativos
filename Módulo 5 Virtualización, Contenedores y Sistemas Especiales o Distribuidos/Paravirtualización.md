>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Paravirtualización / Virtualización Modificada

Silberschatz et al. (2018) analizan esta técnica donde el sistema operativo invitado es modificado para realizar llamadas directas (hypercalls) al hipervisor mejorando el rendimiento. Al ser consciente de que se ejecuta en un entorno virtualizado, el SO invitado no intenta ejecutar instrucciones de hardware no permitidas, evitando trampas de intercepción costosas. Esta colaboración reduce sustancialmente el overhead de virtualización en E/S y gestión de tablas de paginación. Se utiliza en hipervisores Xen y controladores de entrada/salida virtio.


```
 ┌─────────────────────────────────────────────────────────┐
 │         Kernel Modificado del Sistema Guest             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Emite llamadas cooperativas directas / Hypercalls)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Hipervisor (VMM Cooperativo)              │
 │  * Recibe las solicitudes optimizadas sin necesidad     │
 │    de interceptar instrucciones prohibidas por hardware │
 └────────────────────────────┬────────────────────────────┘
                              │ (Gestión eficiente de recursos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Hardware Físico del Servidor                │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
