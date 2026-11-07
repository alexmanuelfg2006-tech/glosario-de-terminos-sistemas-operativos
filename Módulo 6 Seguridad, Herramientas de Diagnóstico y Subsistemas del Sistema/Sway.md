>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Sway / Compositor Wayland Tiling

Tanenbaum y Bos (2015) presentan este compositor para Wayland que organiza las ventanas de manera automática en formato de mosaico no solapado aprovechando al máximo el espacio en pantalla. Diseñado como un reemplazo directo para el gestor de ventanas i3, ofrece una interfaz de usuario orientada al uso intensivo del teclado sin consumo de recursos superfluos. Al operar directamente sobre el protocolo Wayland, elimina los problemas de parpadeo gráfico y ofrece un rendimiento gráfico fluido e ideal para desarrolladores.

```
 ┌─────────────────────────────────────────────────────────┐
 │             Aplicaciones de Usuario (Clientes)          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Protocolo Wayland de superficie)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │           Sway (Compositor Tiling Wayland)              │
 │  * Organiza contenedores y ventanas en mosaico automático│
 │  * Renderizado acelerado por hardware mediante wlroots  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Interacción directa con DRM/KMS del kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Pantalla / Hardware Gráfico               │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
