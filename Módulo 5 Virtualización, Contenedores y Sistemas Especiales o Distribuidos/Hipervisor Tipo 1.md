>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Hipervisor Tipo 1 / Hipervisor Bare-Metal

Silberschatz et al. (2018) analizan este tipo de hipervisor indicando que se instala y ejecuta directamente sobre el hardware físico de la máquina sin requerir un sistema operativo anfitrión intermedio. Al tomar el control exclusivo del procesador y la memoria desde el arranque, ofrece un rendimiento óptimo y una latencia de virtualización mínima. Soluciones como VMware ESXi, KVM y Xen pertenecen a esta categoría, siendo la norma en centros de datos enterprise. Los sistemas operativos invitados se ejecutan como procesos supervisados con acceso directo a extensiones VT-x/AMD-V.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
