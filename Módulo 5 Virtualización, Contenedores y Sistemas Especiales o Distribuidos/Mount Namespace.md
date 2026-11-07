>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Mount Namespace / Aislamiento de Puntos de Montaje

Tanenbaum y Bos (2015) presentan este mecanismo de aislamiento indicando que otorga a cada contenedor una vista privada del directorio del sistema de archivos. Un proceso ejecutado dentro de un mount namespace puede montar o desmontar volúmenes sin alterar la estructura visible por el sistema anfitrión u otros contenedores. Permite construir directorios raíz personalizados (/) para aplicaciones aisladas combinándolo con chroot y OverlayFS. Es una de las capas primordiales para la seguridad de contenedores OCI.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
