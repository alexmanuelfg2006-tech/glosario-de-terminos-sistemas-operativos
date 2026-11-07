>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Kernel Monolítico vs Emulado / Monolithic Kernel vs emuled

Un núcleo monolítico ejecuta la totalidad de los servicios del sistema operativo (gestión de memoria, planificador y controladores) dentro de un único espacio de direcciones con privilegios absolutos en el procesador, logrando así un rendimiento óptimo debido a sus llamadas a funciones directas, pero sufriendo de alta fragilidad, ya que un fallo en cualquier módulo colapsa por completo todo el equipo. En contraste, un enfoque emulado o virtualizado interpone una capa de abstracción o hipervisor entre el sistema operativo y el hardware físico real, lo que aísla de manera segura los errores y protege al anfitrión frente a caídas fatales, aunque introduce una notoria penalización en la eficiencia de procesamiento debido a la sobrecarga de las traducciones adicionales.

![[Pasted image 20261107021320.png]]

### Referencia
Desconocido. (2025).Micronúcleo frente a núcleo monolítico
https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiKzv_59--XAxVBgYQIHanDFSgQFnoECB8QAQ&url=https%3A%2F%2Ftranslate.google.com%2Ftranslate%3Fu%3Dhttps%3A%2F%2Fwww.geeksforgeeks.org%2Foperating-systems%2Fdifference-between-microkernel-and-monolithic-kernel%2F%26hl%3Des%26sl%3Den%26tl%3Des%26client%3Dsrp&usg=AOvVaw1Zs5iqOehWq0lzQaa_JK4B&opi=89978449