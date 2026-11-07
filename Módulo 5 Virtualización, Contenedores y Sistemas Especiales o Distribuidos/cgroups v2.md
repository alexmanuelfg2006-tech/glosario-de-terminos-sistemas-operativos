>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
cgroups v2 / Grupos de Control Versión 2

Tanenbaum y Bos (2015) estudian la estructura del kernel Linux que organiza los procesos en una jerarquía unificada para supervisar y restringir los recursos del sistema. A diferencia de la versión 1, establece una estructura de árbol único que evita conflictos en la asignación paralela de CPU, memoria RAM y operaciones de disco. Permite a los administradores fijar límites estrictos de consumo y cuotas de ancho de banda a grupos de procesos o contenedores. Constituye la columna vertebral sobre la cual motores como Docker y Kubernetes aplican aislamiento de recursos.

![[Pasted image 20261107021143.png]]

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
