>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
PID Namespace / Aislamiento de Identificadores de Proceso

Tanenbaum y Bos (2015) describen cómo este espacio de nombres aísla el árbol de IDs de proceso, permitiendo que un contenedor mantenga su propia numeración desde el PID 1. El proceso raíz del contenedor actúa como el init local gestionando a sus hilos hijos, mientras que el kernel anfitrión le asigna un PID totalmente distinto en su árbol global. Esta separación impide que los procesos dentro del contenedor puedan visualizar o enviar señales (kill) a tareas que se ejecutan fuera de su espacio de nombres aislado.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
