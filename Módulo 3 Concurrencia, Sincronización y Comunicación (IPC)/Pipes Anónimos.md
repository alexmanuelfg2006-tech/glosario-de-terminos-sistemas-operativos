>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
pipes Anónimos / Anonymous Pipes

Silberschatz et al. (2018) tratan estos canales indicando que permiten la transferencia unidireccional de flujo de bytes entre procesos estrechamente vinculados por parentesco. Los datos escritos en un extremo del tubo se almacenan en un búfer circular en la memoria RAM gestionado por el kernel hasta ser leídos en el otro extremo. Al carecer de una entrada en el sistema de archivos, se destruyen automáticamente una vez que ambos procesos cierran sus descriptores. Representan el fundamento del encadenamiento de comandos en shells de línea de órdenes.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
