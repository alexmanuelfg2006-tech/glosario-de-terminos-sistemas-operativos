>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Spinlock (Espera Activa) / Spinlock

Según Silberschatz et al. (2018), un _spinlock_ es un mecanismo de bloqueo de baja sobrecarga donde la CPU consume ciclos manteniendo un bucle de espera activa, eficiente solo cuando los tiempos de retención son cortos. Tipo de cerrojo en el que un hilo, al no poder adquirir el recurso, permanece ejecutando un bucle continuo de comprobación hasta que el recurso queda libre.


```
 ┌─────────────────────────────────────────────────────────┐
 │              Hilo Intentando Adquirir Spinlock          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Intenta bloqueo atómico test_and_set)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 Bucle de Espera Activa (Polling)        │
 │  * ¿El cerrojo está libre?                              │
 ├────────────────────────────┬────────────────────────────┤
 │ Si NO (Ocupado)            │ Si SÍ (Libre)              │
 │ ▼                          │ ▼                          │
 │ Gira en bucle consumiendo  │ Adquiere el cerrojo y      │
 │ ciclos de CPU (Active wait)│ entra a sección crítica    │
 └────────────────────────────┴────────────────────────────┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 6