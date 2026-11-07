>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Device Driver / Controlador de Dispositivo

Silberschatz et al. (2018) conceptualizan este módulo de software del kernel como el encargado de abstraer la complejidad del hardware físico y proporcionar una interfaz de control uniforme al SO. Traduce las llamadas genéricas de entrada/salida del VFS en secuencias de comandos de bajo nivel específicas del controlador de hardware. Se ejecuta habitualmente dentro del espacio de direcciones privilegiado del núcleo para tener acceso a las instrucciones del procesador y líneas de interrupción. Su correcto diseño evita que los fallos físicos de los periféricos colapsen el sistema.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
