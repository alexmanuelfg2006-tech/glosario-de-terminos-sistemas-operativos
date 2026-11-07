>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Mesa DRI / Infraestructura de Renderizado Directo

Silberschatz et al. (2018) explican el papel de este conjunto de bibliotecas abiertas que implementa las APIs gráficas OpenGL y Vulkan facilitando el paso directo de órdenes a la GPU. Actúa como la capa intermedia entre las aplicaciones gráficas en espacio de usuario y los controladores del kernel mediante la interfaz DRM/KMS. Traduce los comandos de sombreado y dibujado 3D en instrucciones nativas de la tarjeta aceleradora gráfica. Permite ejecutar entornos de escritorio modernos y juegos 3D de alta complejidad sobre Linux.


```
 ┌─────────────────────────────────────────────────────────┐
 │    Aplicación Gráfica (OpenGL / Vulkan / Aplicación)    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Llamadas a la API gráfica estándar)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │           Biblioteca Mesa DRI (Espacio de Usuario)      │
 │  * Traduce las llamadas a comandos nativos de la GPU    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Acceso directo a memoria de video / GEM)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │             Controlador DRM en el Kernel                │
 └─────────────────────────────────────────────────────────┘
```


---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
