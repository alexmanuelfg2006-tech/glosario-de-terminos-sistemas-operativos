>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Arquitectura de Entrada/Salida / Input/Output Architecture 

Tanenbaum y Bos (2015) explican la organización integral de subsistemas de hardware y abstracciones de software dedicadas a transferir datos entre la memoria principal y los periféricos. Se estructura en capas superpuestas que van desde los controladores de bus físico y chips de control hasta los controladores de dispositivos y el VFS del kernel. Esta modularidad aísla a los programas de usuario de las peculiaridades físicas de los dispositivos de almacenamiento o red. El objetivo principal radica en maximizar el ancho de banda y reducir la carga de CPU mediante interrupciones y DMA.

### Referencia
Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson