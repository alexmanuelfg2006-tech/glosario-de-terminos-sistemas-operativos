>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
User Namespace / Aislamiento de IDs de Usuario

Silberschatz et al. (2018) explicitan el funcionamiento de este espacio de nombres que mapea los identificadores de usuario y grupo (UID/GID) del contenedor a identificadores sin privilegios en el host. Permite que una aplicación se ejecute con el UID 0 (root) dentro del contenedor aislado para gestionar sus archivos, mientras que a nivel del kernel anfitrión representa a un usuario estándar sin facultades. Evita que un escape de contenedor conceda acceso administrativo real sobre la máquina anfitriona.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
