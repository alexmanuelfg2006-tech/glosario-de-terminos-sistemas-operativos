>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
SSD / Unidad de Estado Sólido

Tanenbaum y Bos (2015) caracterizan a esta unidad de almacenamiento no volátil por estar constituida por módulos de memoria flash NAND sin componentes mecánicos móviles. Al eliminar los tiempos de búsqueda electromecánicos y la latencia rotacional de los discos rígidos magnéticos, ofrece accesos aleatorios a gran velocidad. El kernel del SO utiliza algoritmos de optimización específicos, como F2FS y el comando TRIM, para gestionar el desgaste de los bloques y maximizar su vida útil. Se conecta habitualmente vía SATA o PCIe NVMe.

![[Pasted image 20261107022937.png]]

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
