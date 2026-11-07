>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Buffer Overflow / Desbordamiento de Búfer

Tanenbaum y Bos (2015) exploran esta falla de seguridad producida cuando un programa escribe datos más allá de los límites del búfer reservado en la memoria física o virtual. Al sobrepasar la capacidad del arreglo, los datos adicionales corruptos alteran los registros adyacentes de la pila, incluyendo la dirección de retorno de funciones. Los atacantes explotan esta vulnerabilidad inyectando instrucciones maliciosas para modificar el flujo de ejecución del programa y obtener privilegios de root. La mitigación requiere el uso de canarios de pila y compilación con protección ASLR/NX.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
