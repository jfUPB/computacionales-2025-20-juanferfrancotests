# Unidad 3


## 🛠 Fase: Apply
## Actividad 06
### Hola Objeto: creación de un objeto en el stack

* Ejecuta el programa en C++ en modo depuración (F5) y coloca un breakpoint en la línea donde se declara Punto p(10, 20);.
  
* Paso a paso (F10), observa en la ventana de variables (Autos/Locals) los valores de x y y.
  
* En el menú Debug, selecciona Windows > Memory > Memory 1 y observa la dirección de memoria de p. Escribe en la entrada de texto de Memory 1 la dirección de memoria de p así &p y presiona Enter. Observa la dirección de memoria de p. Observa el contenido de la memoria, deberías ver algunos números en hexadecimal, tales como 0a 00 00 00 14 00 00 00.
Abre la calculadora de Windows y selecciona el modo de programador. Cambia a modo hexadecimal.

* Escribe 0a ¿Qué valor en decimal obtienes? Escribe 14 ¿Qué valor en decimal obtienes? ¿Qué observas?

* Nota el orden en el que están almacenados los bytes en la memoria. Observa que el byte de menor peso (menos significativo) está almacenado primero, es decir, en una dirección de memoria menor. A esto se le conocen como arquitecturas little-endian. Otro tipo de arquitectura es big-endian, donde el byte de mayor peso (más significativo) se almacena primero. La mayoría de las arquitecturas modernas son little-endian. Si la arquitectura de tu computador fuera big-endian, ¿Cómo quedarían almacenados los bytes en la memoria de p?
