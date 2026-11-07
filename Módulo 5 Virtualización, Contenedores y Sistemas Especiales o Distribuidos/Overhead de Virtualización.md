>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Overhead de Virtualización / Penalización por Virtualización

Silberschatz et al. (2018) evalúan esta penalización como la cuota adicional de recursos (latencia, uso de CPU y memoria) absorbida por la capa de abstracción del hipervisor. Corresponde al costo computacional necesario para interceptar instrucciones privilegiadas, traducir direcciones de memoria virtual y emular periféricos. Aunque las extensiones por hardware (VT-x/AMD-V) reducen este impacto a cifras mínimas, sigue siendo superior al overhead imperceptible de los contenedores nativos. Minimizar esta penalización es objetivo constante en hipervisores.

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
