>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Network Namespace / Aislamiento de la Pila de Red

Tanenbaum y Bos (2015) explicitan cómo este espacio de nombres otorga a los procesos su propio conjunto aislado de interfaces de red, direcciones IP, tablas de enrutamiento y reglas de cortafuegos. Permite que múltiples contenedores en una misma máquina utilicen los mismos puertos de red (como el puerto 80) sin generar conflictos de binding. El kernel interconecta estos espacios de nombres independientes mediante pares de interfaces virtuales (veth) vinculadas a puentes de red de software. Es clave para la arquitectura de red de Docker y Kubernetes.

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
