>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 5| Volver al Módulo 5]]

---
Tablas Anidadas (EPT/NPT) / Paginación Anidada de Hardware

Tanenbaum y Bos (2015) analizan este mecanismo que acelera por hardware la traducción de direcciones virtuales del sistema invitado a direcciones físicas del host sin intervención del hipervisor. Extended Page Tables (Intel EPT) y Nested Page Tables (AMD NPT) incorporan dos niveles de traducción de direcciones gestionados directamente por la MMU de la CPU. Eliminan la necesidad de mantener costosas tablas de paginación en la sombra (shadow page tables) gestionadas por software. Reducen de forma notable la latencia de acceso a memoria RAM en máquinas virtuales.


```
 ┌─────────────────────────────────────────────────────────┐
 │            Dirección Virtual del Guest (VCPU)           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Traducción 1: Guest Virtual ➔ Guest Físico)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │        Tabla de Páginas del Invitado (Guest PT)         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Traducción 2 asistida por hardware: EPT / NPT)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │          Memoria Física Real del Host (RAM)             │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
