>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Weston / Compositor de Referencia Wayland

Silberschatz et al. (2018) presentan este compositor de referencia oficial desarrollado para demostrar el funcionamiento práctico y las capacidades de las APIs del protocolo Wayland. Proporciona un entorno gráfico básico diseñado para evaluar el rendimiento de renderizado en sistemas embebidos, plataformas automotrices y escritorios Linux. Sirve como base de código abierto a partir de la cual los desarrolladores construyen compositores avanzados más complejos como Mutter o Sway.

```
 ┌─────────────────────────────────────────────────────────┐
 │         Clientes Wayland (Aplicaciones de Prueba)       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Protocolo Wayland puro)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Weston (Compositor de Referencia)           │
 │  * Carga shells y módulos de renderizado estándar       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Salida a través de backends: DRM, X11, Wayland)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Sistema Operativo / Kernel                │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
