>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Linux Capabilities / Capacidades Graduales del Kernel

Silberschatz et al. (2018) describen cómo esta funcionalidad descompone el poder absoluto del superusuario root en subconjuntos independientes de privilegios asignables individualmente a cada proceso. En lugar de otorgar control total a un binario, se le asignan únicamente las facultades estrictas que requiere, como CAP_NET_BIND_SERVICE para abrir puertos de red bajos. Esta granularidad evita que un fallo de seguridad en un servicio con privilegios comprometa la totalidad del sistema anfitrión. Refuerza significativamente el principio de menor privilegio.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
