>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Orquestación / Orquestación de Contenedores

Tanenbaum y Bos (2015) definen este concepto como la automatización coordinada del despliegue, escalado, red y alta disponibilidad de contenedores en entornos distribuidos de gran escala. Plataformas como Kubernetes gestionan el ciclo de vida de los contenedores distribuyendo cargas de trabajo sobre clústeres de servidores físicos o virtuales. Supervisan el estado de salud de los servicios, aplican balanceo de carga automático y recuperan instancias caídas sin intervención humana. Garantizan la continuidad operativa de aplicaciones empresariales altamente masivas.
```
 ┌─────────────────────────────────────────────────────────┐
 │       Plano de Control (Master Node / Orchestrator)     │
 └────────────────────────────┬────────────────────────────┘
                              │ (Monitoreo, programación y políticas de estado)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Clúster de Nodos de Trabajo (Workers)           │
 │  * Nodo A: [Contenedor 1] [Contenedor 2]                │
 │  * Nodo B: [Contenedor 3] [Auto-escalado dinámico]      │
 └────────────────────────────┬────────────────────────────┘
                              │ (Balanceo de carga y resiliencia)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Servicio Distribuido Altamente Disponible      │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
