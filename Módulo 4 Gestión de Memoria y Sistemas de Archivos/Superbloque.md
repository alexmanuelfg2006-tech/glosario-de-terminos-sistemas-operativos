>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Superbloque / Bloque Maestro de Metadatos

Silberschatz et al. (2018) identifican esta estructura como el bloque maestro que almacena los parámetros globales y la configuración estructural crítica de un sistema de archivos. Guarda información esencial como el tamaño del bloque, el conteo total de inodos y el estado de montaje del volumen. Si el superbloque sufre corrupción física o lógica, el sistema operativo pierde la capacidad de interpretar el volumen de almacenamiento y montar la partición. Por esta razón, se escriben múltiples copias de respaldo a lo largo del disco.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
