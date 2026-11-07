>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Chroot Jail / Entorno Aislado Chroot

Silberschatz et al. (2018) evalúan la operación de cambio del directorio raíz de un proceso (chroot), confinándolo a un subárbol específico para impedir su navegación por el sistema real. El proceso confinado y sus hilos hijos perciben la nueva ruta como la raíz absoluta /, perdiendo acceso a los archivos fuera de dicha ubicación. Aunque ofrece una forma básica de aislamiento para servicios de red, no proporciona un confinamiento seguro por sí solo frente a usuarios con privilegios. Se utiliza como capa complementaria en entornos de pruebas y compilación de software.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
