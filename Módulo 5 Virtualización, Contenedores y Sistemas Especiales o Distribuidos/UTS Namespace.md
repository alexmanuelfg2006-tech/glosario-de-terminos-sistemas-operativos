>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
UTS Namespace / Aislamiento de Nombres de Dominio

Tanenbaum y Bos (2015) explican que este espacio de nombres permite que un grupo de procesos posea su propio nombre de host (hostname) y nombre de dominio NIS aislado. Las llamadas al sistema como sethostname() invocarán cambios visibles únicamente dentro del espacio de nombres UTS correspondiente al contenedor. Facilita que múltiples servicios de red mantengan identidades de red independientes operando simultáneamente sobre el mismo servidor físico sin colisiones de nombres.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
