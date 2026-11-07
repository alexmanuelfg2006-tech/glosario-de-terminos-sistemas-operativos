>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Reemplazo FIFO / FIFO Page Replacement

Según Silberschatz et al. (2018), el algoritmo FIFO (_First-In, First-Out_) asocia a cada página el instante exacto de su carga en memoria para expulsar, en caso de un fallo de página, a la estructura que haya permanecido residente durante mayor tiempo. Es un algoritmo de reemplazo de páginas sencillo basado en una cola de tipo First-In, First-Out. Cuando se produce un fallo de página y la memoria está llena, el sistema selecciona y expulsa invariablemente a la página que lleva más tiempo residente en la memoria RAM.

### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 10