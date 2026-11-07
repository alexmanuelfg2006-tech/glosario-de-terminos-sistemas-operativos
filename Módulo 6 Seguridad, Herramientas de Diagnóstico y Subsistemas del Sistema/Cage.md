>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Cage / Compositor Wayland para Modo Kiosco

Silberschatz et al. (2018) presentan este compositor gráfico minimalista diseñado específicamente para ejecutar una sola aplicación a pantalla completa bajo el protocolo Wayland. Elimina todos los elementos convencionales del entorno de escritorio, como barras de tareas, menús de navegación y gestores de ventanas flotantes. Esta focalización reduce drásticamente el consumo de recursos de memoria y previene la manipulación no autorizada del sistema por parte de los usuarios. Resulta la solución estándar para terminales de punto de venta, cajeros automáticos y paneles informáticos.

```
┌─────────────────────────────────────────────────────────┐
 │            Una Única Aplicación (Cliente Wayland)       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Solicita maximizar superficie única)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Cage (Compositor Wayland Kiosco)             │
 │  * Fuerza a la aplicación a ocupar toda la pantalla    │
 │  * Bloquea la creación de ventanas secundarias          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Control directo del framebuffer)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 Pantalla del Sistema                    │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
