>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Algoritmo SCAN Circular / Circular SCAN Algorithm

Tanenbaum y Bos (2015) describen este mecanismo como una técnica avanzada de planificación de peticiones de entrada/salida para discos magnéticos rígidos. El cabezal electromagnético se desplaza en una sola dirección resolviendo todas las solicitudes pendientes a lo largo de los cilindros hasta alcanzar el extremo final. En ese punto, el mecanismo retorna de inmediato al inicio del disco sin realizar lecturas ni escrituras durante el trayecto de regreso. Esta estrategia elimina por completo la inequidad en los tiempos de espera y reduce la variabilidad del servicio frente a algoritmos tradicionales.
![[Pasted image 20261107021058.png]]

### Referencia

Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.