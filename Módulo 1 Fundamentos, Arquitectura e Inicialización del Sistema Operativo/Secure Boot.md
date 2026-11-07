>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Arranque seguro / Secure Boot

Según Silberschatz et al. (2018), _Secure Boot_ es un estándar de seguridad integrado dentro del firmware UEFI que verifica mediante firmas criptográficas digitales la autenticidad e integridad del gestor de arranque antes de cederle el control del hardware. Impide la ejecución de cualquier software que no sea seguro al encenderse

```
 ┌─────────────────────────────────────────────────────────┐
 │               Arranque del Sistema (UEFI)               │
 └────────────────────────────┬────────────────────────────┘
                              │ (Carga del binario de arranque, ej. GRUB / Kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Validación de Firma Criptográfica              │
 │  * Compara certificado del binario con Base de Datos    │
 │    Autorizada (db) y Claves de Plataforma (PK / KEK)    │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Firma Válida / Coincide)               ▼ (Firma Inválida / No Autorizada)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │     Ejecución Autorizada     │          │    Bloqueo de Seguridad      │
 │  (El sistema continúa boot)  │          │    (Fallo de Secure Boot)    │
 └──────────────────────────────┘          └──────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 1