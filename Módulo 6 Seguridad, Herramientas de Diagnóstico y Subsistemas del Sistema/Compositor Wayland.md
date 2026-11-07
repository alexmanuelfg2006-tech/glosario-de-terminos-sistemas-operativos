>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Compositor Wayland / Servidor Gráfico Wayland

Tanenbaum y Bos (2015) asignan a esta entidad la responsabilidad de coordinar las entradas de usuario y componer el renderizado visual de las aplicaciones directamente en pantalla dentro de Wayland. A diferencia del antiguo modelo X11 donde el servidor actuaba como intermediario pesado, el compositor combina el rol de gestor de ventanas y servidor gráfico en un único ejecutable. Cada aplicación renderiza su propio búfer en memoria compartida y le notifica al compositor para la muestra final. Esto elimina el parpadeo de pantalla y mejora la latencia de entrada.

```
 ┌─────────────────────────────────────────────────────────┐
 │   Cliente Wayland (Toolkit con soporte Wayland nativo)  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Renderiza en su propio búfer y avisa al compositor)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │               Compositor Wayland                        │
 │  * Gestiona superficies, entradas y composición visual  │
 │  * Se comunica directamente con el kernel vía DRM/KMS   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Salida directa y sin parpadeos / tearing)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Pantalla / Controlador Gráfico en Kernel        │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
