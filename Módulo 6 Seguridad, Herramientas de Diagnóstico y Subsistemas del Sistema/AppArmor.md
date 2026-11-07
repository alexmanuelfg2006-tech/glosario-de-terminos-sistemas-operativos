>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
AppArmor / Módulo de Seguridad por Perfiles

Silberschatz et al. (2018) conceptualizan este módulo como una capa de control de acceso obligatorio (MAC) en el kernel de Linux basada en rutas absolutas de archivos para restringir programas. A diferencia de SELinux que utiliza etiquetas complejas, AppArmor emplea perfiles legibles en texto plano donde se asocian permisos específicos a binarios ejecutables. Esto impide que una aplicación vulnerada acceda a directorios no autorizados o ejecute llamadas de sistema peligrosas. Se encuentra integrado por defecto en distribuciones como Ubuntu y Debian para blindar servicios críticos.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
