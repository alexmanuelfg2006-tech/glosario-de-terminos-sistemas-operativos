>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
lmkd / Demonio Cazador de Memoria Escasa

Silberschatz et al. (2018) tratan este demonio en Android como el componente responsable de evaluar el estado de la RAM y finalizar los procesos en segundo plano con menor prioridad ante presión de memoria. Interactúa directamente con el kernel a través de métricas PSI (Pressure Stall Information) para detectar agotamiento inminente de recursos. Al alcanzarse umbrales críticos de memoria física disponible, envía señales SIGKILL a las aplicaciones dormidas menos relevantes para evitar bloqueos del sistema. Preserva la fluidez de la interfaz del usuario.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
