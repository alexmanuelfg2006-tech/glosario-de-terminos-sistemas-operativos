>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Subsistema Gráfico Linux / Pila de Software Gráfico

Tanenbaum y Bos (2015) estudian la organización de este conjunto coordinado de controladores de kernel, bibliotecas de abstracción, servidores de despliegue y APIs para el procesamiento gráfico. Integra componentes clave como DRM/KMS en el kernel, la implementación de OpenGL/Vulkan en Mesa, y servidores o compositores como X11 o Wayland. Coopera para transformar los comandos de dibujo 3D de las aplicaciones en señales de vídeo enviadas al monitor. Garantiza aceleración por hardware con alta eficiencia.

```
 ┌─────────────────────────────────────────────────────────┐
 │       Aplicaciones de Usuario (Toolkits / OpenGL)       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Llamadas de renderizado y presentación)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Capa de Presentación (Servidor X o Wayland)     │
 └────────────────────────────┬────────────────────────────┘
                              │ (Interfaz de comandos con el núcleo)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │     Subsistema DRM / KMS (Direct Rendering Manager)     │
 │  * Gestión de recursos de pantalla y modos de video     │
 └────────────────────────────┬────────────────────────────┘
                              │ (Controlador de hardware)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Controlador Gráfico de Hardware (GPU)          │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
