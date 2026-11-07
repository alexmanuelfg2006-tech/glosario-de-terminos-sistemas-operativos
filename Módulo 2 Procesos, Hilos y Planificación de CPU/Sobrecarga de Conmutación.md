>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Sobrecarga por cambio de contexto / Context Switching Overhead

Según Tanenbaum y Bos (2015), la sobrecarga de conmutación es el tiempo de CPU consumido en tareas administrativas (guardado/restauración de registros, invalidación de memorias caché y TLB) durante un cambio de contexto, representando un desperdicio de capacidad de cálculo útil. Es el tiempo y los recursos de cpu que se pierden guardando el estado de un proceso y cargando el del siguiente

```
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso A en Ejecución (Ring 3)           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Interrupción / Fin de Quántum)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Sobrecarga de Cambio de Contexto (Ring 0)       │
 │  * Guardado y restauración de registros en PCBs         │
 │  * Actualización de punteros de páginas (CR3 / MMU)     │
 │  * Invalidación parcial de cachés de CPU y TLB          │
 └────────────────────────────┬────────────────────────────┘
                              │ (Restauración de control)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │               Proceso B en Ejecución (Ring 3)           │
 └─────────────────────────────────────────────────────────┘
```
### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson.Capítulo 2