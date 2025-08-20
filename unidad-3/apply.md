# Unidad 3


## 🛠 Fase: Apply
## Actividad 06
### Hola Objeto: creación de un objeto en el stack

* Ejecuta el programa en C++ en modo depuración (F5) y coloca un breakpoint en la línea donde se declara Punto p(10, 20);.
  
* Paso a paso (F10), observa en la ventana de variables (Autos/Locals) los valores de x y y.
  
* En el menú Debug, selecciona Windows > Memory > Memory 1 y observa la dirección de memoria de p. Escribe en la entrada de texto de Memory 1 la dirección de memoria de p así &p y presiona Enter. Observa la dirección de memoria de p. Observa el contenido de la memoria, deberías ver algunos números en hexadecimal, tales como 0a 00 00 00 14 00 00 00.
Abre la calculadora de Windows y selecciona el modo de programador. Cambia a modo hexadecimal.

* Escribe 0a ¿Qué valor en decimal obtienes? Escribe 14 ¿Qué valor en decimal obtienes? ¿Qué observas?

con 0a me da igual a 10 y con 14 me da igual a 20 en HEX

* Nota el orden en el que están almacenados los bytes en la memoria. Observa que el byte de menor peso (menos significativo) está almacenado primero, es decir, en una dirección de memoria menor. A esto se le conocen como arquitecturas little-endian. Otro tipo de arquitectura es big-endian, donde el byte de mayor peso (más significativo) se almacena primero. La mayoría de las arquitecturas modernas son little-endian. Si la arquitectura de tu computador fuera big-endian, ¿Cómo quedarían almacenados los bytes en la memoria de p?

Muy enrredado, no entiendo.

Reflexiona sobre las siguientes cuestiones:

*¿Cuál es la diferencia entre un constructor y un destructor en C++? el constructor es una funcion que construye algo apartir de unos insumos que el requiere y retorna lo construido en una parte de la memoria, el destructor lo que hace es que se ejecuta automaticamente para borrar lo construido cuando ya cuando salga de la funcion del constructor. esto ayuda para que la memoria no se llene y cause problemas a largo plazo.

*¿Cuál es la diferencia entre un objeto y una clase en C++?

una clase es un molde que defininen como debe ser el objeto, el objeto posee caracteristicas definidas (los metodos de la clase se ejecutan en los objetos)

*¿Qué diferencia notas entre el objeto Punto en C++ y C#?
que en c++ es una copia y en C# es un referencia que apunta a la misma posicion de memoria del valor original

*¿Qué es p en C++ y qué es p en C#? (en uno de ellos p es un objeto y en el otro es una referencia a un objeto).

*¿En qué parte de memoria se almacena p en C++ y en C#?

*¿Qué observaste con el depurador acerca de p? Según lo que observaste ¿Qué es un objeto en C++?
Actividad 07


