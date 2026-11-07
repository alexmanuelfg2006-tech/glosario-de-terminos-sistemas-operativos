>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Stack Canaries / Valores Canario de Seguridad

Silberschatz et al. (2018) detallan el uso de estos valores numéricos de verificación aleatorios insertados entre los búferes locales de la pila y la dirección de retorno de las funciones. Antes de que la función retorne, el procesador verifica si el valor del canario ha sido modificado por un intento de desbordamiento de búfer. Si detecta una discrepancia en el valor del canario, el sistema aborta de inmediato la ejecución del programa emitiendo una excepción de seguridad. Evita la ejecución de exploits inyectados en la pila.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
