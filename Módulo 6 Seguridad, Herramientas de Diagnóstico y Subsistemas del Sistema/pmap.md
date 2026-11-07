>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
pmap / Herramienta de Mapeo de Memoria

Tanenbaum y Bos (2015) revisan la utilidad de esta herramienta diseñada para mostrar la distribución detallada de las regiones de memoria asignadas a un proceso en ejecución. Detalla el tamaño exacto, permisos (lectura, escritura, ejecución) y el mapeo de archivos o bibliotecas dinámicas asignadas a cada segmento del procesador. Permite a ingenieros de software e investigadoras de seguridad identificar fugas de memoria, sobreutilización del heap y segmentos vulnerables. Analiza directamente la información expuesta por /proc/pid/maps.

![[Pasted image 20261107022853.png]]

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
