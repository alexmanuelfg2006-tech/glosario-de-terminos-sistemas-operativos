>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
**_brk() / sbrk() / Llamadas a Sistema para el Heap_**

Tanenbaum y Bos (2015) detallan el funcionamiento de este conjunto de llamadas al sistema de UNIX diseñadas para ajustar la posición del límite de datos (program break) aumentando o disminuyendo el heap. Al invocar estas funciones, el proceso solicita al kernel de Linux que incremente el espacio de memoria virtual asignado dinámicamente. Las bibliotecas estándar de C (como malloc) emplean internamente estas llamadas para gestionar la asignación de bloques de memoria a las aplicaciones. Su uso adecuado evita fragmentación y optimiza la liberación de memoria en programas de larga ejecución.

### Referencia

Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.