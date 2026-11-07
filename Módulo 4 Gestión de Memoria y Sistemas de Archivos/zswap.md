>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
zswap / Caché Comprimida para Swap

Tanenbaum y Bos (2015) definen esta memoria intermedia como una caché comprimida en RAM que intercepta las páginas antes de ser enviadas a la partición de swap en el disco físico. Si una página expulsada por la memoria virtual puede comprimirse con éxito, zswap la almacena en su búfer en RAM evadiendo la costosa operación de escritura en disco. Solo si la caché zswap se llena por completo, se escriben las páginas en el almacenamiento secundario. Acelera notablemente la respuesta del sistema bajo alta presión de memoria.
![[Pasted image 20261107023030.png]]

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
