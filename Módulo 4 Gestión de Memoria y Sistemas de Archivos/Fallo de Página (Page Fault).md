>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---

Fallo de Página / Page Fault

Según Silberschatz et al. (2018), un fallo de página (_page fault_) es una excepción de hardware generada cuando una referencia a una página virtual apunta a una dirección cuyo bit de validez indica que el bloque no está residente en la memoria física principal. Es una interrupción síncrona generada por el hardware de la MMU cuando un programa intenta acceder a una página virtual cuyo bit de presencia está en cero, lo que indica que no se encuentra cargada en la memoria RAM.


```
 ┌─────────────────────────────────────────────────────────┐
 │       MMU Intenta Traducir Página pero Bit Presencia = 0│
 └────────────────────────────┬────────────────────────────┘
                              │ (Dispara excepción de hardware al Kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Excepción de Fallo de Página (Page Fault)       │
 │  * Pausa la ejecución del proceso actual                │
 │  * Transfiere el control al Kernel del Sistema Operativo│
 └────────────────────────────┬────────────────────────────┘
                              │ (Ejecución de la rutina de gestión)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Carga de Página desde Disco / Swap a la RAM     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 10