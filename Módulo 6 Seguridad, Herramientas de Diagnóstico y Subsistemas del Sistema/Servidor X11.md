>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Servidor X11 / Servidor de Despliegue X Window

Silberschatz et al. (2018) describen este servidor como la entidad encargada del manejo del protocolo gráfico X11 coordinando las peticiones de dibujado y eventos de entrada. Opera bajo un modelo cliente-servidor donde las aplicaciones envían comandos de renderizado a través de sockets locales o de red. Aunque ha garantizado la interfaz gráfica en sistemas UNIX durante décadas, su arquitectura antigua presenta problemas de latencia y seguridad al carecer de aislamiento entre ventanas. Está siendo reemplazado por Wayland.

```
 ┌─────────────────────────────────────────────────────────┐
 │   Cliente X11 A          Cliente X11 B (Aplicaciones)   │
 └───────┬────────────────────────────┬────────────────────┘
         │ (Envía comandos de dibujo primitivos por socket)
         ▼                            ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Servidor Xorg (Servidor Central)             │
 │  * Recibe peticiones, gestiona entradas (Teclado/Mouse) │
 │  * Renderiza y envía los mapas de bits a la pantalla    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Salida gráfica final)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 Pantalla / Monitor Física               │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
