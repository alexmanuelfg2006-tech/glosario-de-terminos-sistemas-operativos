>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Stateless OS / Sistema Operativo sin Estado

Tanenbaum y Bos (2015) describen este diseño indicando que reconstruye su entorno completo desde una imagen base limpia guardada en red o memoria en cada arranque sin conservar estados locales. Al reiniciar la máquina, cualquier archivo temporal, configuración o modificación realizada durante la sesión previa es descartada totalmente de la memoria RAM. Garantiza que todos los nodos de un clúster ejecuten exactamente el mismo estado probado de software sin desviaciones de configuración. Simplifica el escalado y la recuperación ante desastres.

```
 ┌─────────────────────────────────────────────────────────┐
 │        Capa Raíz del Sistema Operativo (Inmutable)      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Separación estricta de datos dinámicos)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │        Volúmenes Persistentes Externos (Base de Datos / │
 │         Configuraciones / Logs del Usuario)             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Reinicio limpio garantizado)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │      Instancia Efímera del Sistema (Stateless Host)     │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
