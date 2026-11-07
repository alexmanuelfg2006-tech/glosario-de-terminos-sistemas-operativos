>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Principio de Menor Privilegio / Regla de Privilegios Mínimos

Silberschatz et al. (2018) exponen esta norma de seguridad como la regla que limita los permisos otorgados a un usuario, proceso o servicio a los estrictamente requeridos para su tarea operativa. Exige restringir el acceso a archivos, llamadas de sistema y servicios de red únicamente durante el tiempo que dure la operación autorizada. Su aplicación previene que el compromiso de un servicio secundario permita tomar el control completo del sistema operativo anfitrión. Fundamenta el uso de Linux Capabilities, AppArmor, SELinux y contenedores.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
