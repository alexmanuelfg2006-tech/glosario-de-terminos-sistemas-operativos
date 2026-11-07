>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Instruccion privilegiada / Privileged instruction

Según Silberschatz et al. (2018), una instrucción privilegiada es aquella instrucción de lenguaje máquina que puede alterar la configuración del hardware, modificar mapas de memoria o deshabilitar interrupciones, y que solo puede ser ejecutada con éxito si el procesador se encuentra en modo kernel. La instrucción privilegiada es un comando que afecta directamente al hardware cuando esta en modo kernel 



```
 [ Intento de Ejecución ] ──> [ Validación de CPL (Ring 0 vs 3) ] 
                                    ├── (Ring 3) ──> [ Excepción #GP / Aborto ]
                                    └── (Ring 0) ──> [ Ejecución de Hardware ]
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 1