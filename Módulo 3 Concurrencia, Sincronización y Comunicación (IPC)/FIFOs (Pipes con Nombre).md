>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
FIFOs (Pipes con Nombre) / Tubería Persistente en Disco

Tanenbaum y Bos (2015) caracterizan estas tuberías como un tipo de archivo especial que implementa comunicación unidireccional IPC entre procesos sin parentesco a través de la jerarquía del sistema de archivos. Aunque figuran como entradas de directorio visibles en el sistema, los datos transmitidos no se escriben en el disco físico sino que fluyen por un búfer del kernel. Un proceso abre el archivo en modo de escritura mientras otro lo abre en modo de lectura, bloqueándose hasta que ambas partes se conecten. Conservan el orden estricto de entrada y salida de datos.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
