>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Host OS / Sistema Operativo Anfitrión

Silberschatz et al. (2018) identifican a esta entidad como el sistema operativo principal que controla directamente los componentes físicos del hardware y aloja al hipervisor o motor de contenedores. Responsable prioritario de inicializar la plataforma, gestionar las interrupciones físicas y coordinar el consumo de energía del procesador. En plataformas de virtualización Tipo 2 y entornos Docker, proporciona la pila completa de controladores sobre la cual se ejecutan los entornos aislados. Su estabilidad resulta crítica para la disponibilidad de los servicios virtualizados.



```
 ┌─────────────────────────────────────────────────────────┐
 │              Hardware Físico del Servidor               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Control directo de recursos)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Host OS (Sistema Operativo Anfitrión)        │
 │  * Administra Kernel, Drivers, Memoria y Periféricos    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Provee entorno para Hipervisores o Daemons)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │      Capas Superiores (Hipervisores / Contenedores)     │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
