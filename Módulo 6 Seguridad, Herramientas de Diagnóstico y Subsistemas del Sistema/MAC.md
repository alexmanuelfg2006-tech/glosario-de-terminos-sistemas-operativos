>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
MAC / Control de Acceso Obligatorio

Tanenbaum y Bos (2015) conceptualizan este modelo de seguridad donde las políticas de acceso son administradas de forma centralizada e incondicional por el núcleo, superando los permisos de usuario. A diferencia del modelo discrecional (DAC), ni siquiera el propietario de un archivo puede modificar los permisos o revocar las reglas definidas por el administrador. El sistema compara etiquetas de seguridad asignadas a sujetos y objetos para conceder o denegar cada llamada al sistema. Previene la propagación de software malicioso y eleva el nivel de blindaje.
```
┌─────────────────────────────────────────────────────────┐
 │       Administrador de Seguridad / Políticas del Kernel │
 └────────────────────────────┬────────────────────────────┘
                              │ (Define reglas estrictas e inalterables)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │          Modelo MAC (Control Obligatorio)               │
 │  * El Kernel evalúa etiquetas de contexto de seguridad  │
 │  * Las decisiones de acceso no pueden ser eludidas      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Filtrado estricto)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Ejecución Restringida bajo Principio de Mínimo Privilegio│
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
