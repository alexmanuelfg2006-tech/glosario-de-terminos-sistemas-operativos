>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Sistema Operativo Inmutable / SO de Solo Lectura

Tanenbaum y Bos (2015) explican este paradigma de diseño donde la partición raíz del sistema operativo permanece montada estrictamente en modo de solo lectura durante el funcionamiento. Evita que las aplicaciones del usuario, virus o administradores alteren los archivos binarios y bibliotecas del sistema base. Las actualizaciones del sistema se aplican de forma atómica descargando una imagen completa en una partición secundaria con reinicio seguro. Es utilizado en sistemas para contenedores como Flatcar y Talos Linux.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
