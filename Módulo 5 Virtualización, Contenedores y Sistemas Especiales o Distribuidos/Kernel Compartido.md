>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Kernel Compartido / Arquitectura de Núcleo Compartido

Silberschatz et al. (2018) evalúan este paradigma propio de la tecnología de contenedores donde múltiples espacios de usuario independientes operan sobre una única instancia del kernel anfitrión. A diferencia de la virtualización clásica donde cada VM arranca su propio núcleo, los contenedores utilizan las llamadas al sistema del kernel del host. Esto reduce drásticamente la huella de memoria RAM y el tiempo de arranque de los servicios a escasos milisegundos. Exige mantener el kernel anfitrión actualizado para blindar la seguridad global.


```
 ┌─────────────────────────┬───────────────────────────────┐
 │      Contenedor A       │      Contenedor B             │
 └────────────┬────────────┴───────────────┬───────────────┘
              │ (Aislamiento lógico)       │ (Aislamiento lógico)
              ▼                            ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Kernel Único y Compartido del Host           │
 │  * Programador de CPU, gestión de memoria y drivers     │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Hardware Físico del Servidor                │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
