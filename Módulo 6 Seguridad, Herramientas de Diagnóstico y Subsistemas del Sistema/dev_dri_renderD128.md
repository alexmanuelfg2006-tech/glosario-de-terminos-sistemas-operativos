>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
 /dev/dri/renderD128 / Nodo de Renderizado de GPU

Silberschatz et al. (2018) constituye la interfaz directa en el kernel de Linux para que las aplicaciones accedan a las capacidades de cómputo y renderizado fuera de pantalla de la GPU. Al omitir totalmente los gestores de ventanas convencionales y los servidores de visualización, permite a los procesos enviar órdenes de ejecución sin sobrecarga gráfica. Esta abstracción resulta vital en entornos de renderizado acelerado por hardware, procesamiento paralelo con GPGPU y aceleración de contenedores. Asimismo, garantiza un aislamiento estricto de privilegios entre las tareas de cálculo pesado y la gestión de la pantalla principal.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
