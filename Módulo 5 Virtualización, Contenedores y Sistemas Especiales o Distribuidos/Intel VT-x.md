>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Intel VT-x / Tecnología de Virtualización Intel

Tanenbaum y Bos (2015) revisan este conjunto de extensiones de arquitectura en procesadores Intel diseñadas para acelerar el procesamiento de instrucciones privileged en máquinas virtuales. Introduce el concepto de ejecución en modos VMX Root y Non-Root, permitiendo que el hipervisor y el sistema invitado compartan la CPU de forma segura. Elimina la necesidad de paravirtualizar el kernel invitado o recurrir a la traducción binaria por software. Optimiza la latencia de conmutación entre máquinas virtuales y reduce la penalización sobre el procesador.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
