>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
/sys / Sistema de Archivos de Dispositivos

Silberschatz et al. (2018) definen esta interfaz estructurada del kernel Linux como el mecanismo para exponer la jerarquía completa del hardware conectado al equipo. A diferencia de otros subsistemas virtuales, organiza los dispositivos de forma totalmente jerárquica según su bus, controlador y clase física de pertenencia. Esta disposición facilita la consulta detallada y la modificación dinámica de los atributos operativos de los controladores en tiempo de ejecución. Por consiguiente, resulta indispensable para que los demonios de gestión de dispositivos puedan configurar periféricos y responder a eventos de conexión física.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
