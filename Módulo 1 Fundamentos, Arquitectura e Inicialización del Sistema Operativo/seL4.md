>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
sel4

Según Klein et al. (2009), seL4 es un micronúcleo de tercera generación formalmente verificado mediante pruebas matemáticas rigurosas, garantizando propiedades estrictas de aislamiento de memoria, ausencia de fallos catastróficos e invulnerabilidad en su código base. el sel4 es un microkernel y protege al sistema de fallas de seguridad y hackeos



```
 [ Familia L4 Microkernel ] ──> [ Verificación Matemática (Isabelle/HOL) ] ──> [ Máxima Seguridad y 
```

```
 ┌─────────────────────────────────────────────────────────┐
 │        Dominios de Aplicaciones Aisladas (Ring 3)       │
 │     [Aplicación Crítica A]      [Aplicación Segura B]   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Control estricto por Capabilities / IPC)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │           Microkernel seL4 (Ring 0 - Minimizado)        │
 │   * Gestión estricta de capacidades de acceso a recursos│
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                     Hardware Físico                     │
 └─────────────────────────────────────────────────────────┘
```

### Referencias
Klein, G., Elphinstone, K., Heiser, G., Andronick, J., Cock, D., Derrin, P., Elkaduwe, D., Engelhardt, K., Kolanski, R., Norrish, M., Sewell, T., Tuch, H., & Winwood, S. (2009). seL4: Formal verification of an OS kernel. _Proceedings of the ACM SIGOPS 22nd Symposium on Operating Systems Principles (SOSP)_. (Sección: _Introduction and Kernel Overview_).