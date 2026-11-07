>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Huge Pages / Bloques Gigantes de Memoria

Tanenbaum y Bos (2015) detallan las ventajas de este mecanismo de gestión de memoria virtual que emplea tamaños de página muy superiores a los 4 KB estándar (típicamente 2 MB o 1 GB). Al utilizar páginas de mayor tamaño, se reduce drásticamente el número de entradas requeridas en las tablas de paginación del proceso. Esto disminuye la probabilidad de fallos en el Translation Lookaside Buffer (TLB) de la CPU, acelerando el acceso a la RAM. Se utiliza frecuentemente en bases de datos de alto rendimiento, hipervisores y motores de analítica masiva.

![[Pasted image 20261107021253.png]]

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
