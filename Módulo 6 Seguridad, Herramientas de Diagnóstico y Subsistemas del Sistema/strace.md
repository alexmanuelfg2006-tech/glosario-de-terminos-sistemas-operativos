>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
strace / Rastreador de Llamadas a Sistema

Silberschatz et al. (2018) revisan la funcionalidad de esta herramienta de depuración para Linux que intercepta y registra todas las llamadas al sistema e interrupciones emitidas por un proceso. Muestra en pantalla el nombre de cada syscall invocada, sus argumentos de entrada y el valor de retorno devuelto por el kernel. Permite a los desarrolladores identificar archivos no encontrados, fallos de permisos, bloqueos de sockets y problemas de asignación de memoria sin disponer del código fuente. Se apoya en la interfaz ptrace del núcleo.
![[Pasted image 20261107023003.png]]
---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
