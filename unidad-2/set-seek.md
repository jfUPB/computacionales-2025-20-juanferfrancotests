# Unidad 2

## 🔎 Fase: Set + Seek

###Actividad 1

**Dibujando un punto en la pantalla**

Vamos a resolver juntos este problema:

La pantalla del computador Hack se controla a través de un mapa de memoria que comienza en la dirección 16384 (SCREEN). Cada bit en este mapa de memoria representa un pixel en la pantalla (1 = negro, 0 = blanco). Escribe un programa que dibuje un punto negro en la esquina superior izquierda de la pantalla. (Recuerda que la esquina superior izquierda corresponde al primer bit del primer word en la dirección SCREEN).

Traduce este programa a lenguaje C++ para que relaciones cómo los conceptos de alto nivel se traducen a bajo nivel.

``` cpp
screen= 1; // suponiendo que sscreen representa la posicion 16384

```

### Actividad 02


Dibujando una línea horizontal
Vamos a resolver juntos este problema:

Modifica el programa anterior para que dibuje una línea horizontal negra de 16 pixeles de largo en la esquina superior izquierda de la pantalla. (Recuerda que cada word en la memoria representa 16 pixeles).

``` asm
screen= -1; // forzar al compilador para que asigne la variables screen a  la direccion  1684

```

Traduce este programa a lenguaje C++ para que relaciones cómo los conceptos de alto nivel se traducen a bajo nivel.

``` cpp
screen= -1; // forzar al compilador para que asigne la variables screen a  la direccion  1684

```
Otra forma de hacerlo.
``` cpp
screen= 0xFFFF; // forzar al compilador para que asigne la variables screen a  la direccion  1684

```

Actividad 03


Entrada salida interactiva
Modifica el programa de la actividad anterior de tal manera que puedas mover la línea horizontal de derecha a izquierda usando las teclas d y i respectivamente. Tu programa no tiene que verificar si la línea se sale de la pantalla.

``` asm
@SCREEN
M=-1
@contador
M=0

M=-1

(LEER)
@kBD
D=M
@100
D=D-A
@DERECHA
D;JEQ

@kBD
D=M
@105
D=D-A
@IZQUIERDA
D;JEQ

@LEER
D;JMP

(DERECHA)
@contador
D=M
@SCREEN
A=D+A
M=0
//
@contador
M=M+1
D=M
@SCREEN
A=D+A
M=-1

@LEER
D;JMP

(IZQUIERDA)
@contador
D=M
@SCREEN
A=D+A
M=0

@contador
M=M+1
D=M
@SCREEN
A=D+A
M=-1

@LEER
D;JMP

```

Traduce este programa a lenguaje C++ para que relaciones cómo los conceptos de alto nivel se traducen a bajo nivel.

Modifica el programa de la actividad anterior de tal manera que puedas mover la línea horizontal de derecha a izquierda usando las teclas d y i respectivamente. Tu programa no tiene que verificar si la línea se sale de la pantalla.


``` c

// intaciamos pantalla con una variable
//se crea una variable de la posicion inicial

int pantalla = kBD;
int contador = 0;

// se crea una funcion donde  se oprima d; pinta de negro; suma 1 a la variable pantalla; vuelve al inicio.



// se crea una funcion donde  se oprima i; pinta de blanco; resta 1 a la variable pantalla; vuelve al inicio.

 
```

Convierte un ciclo while en un ciclo for


### Actividad 04

Enunciado: considera el siguiente programa:

``` c

//Adds 1+...+100.
 int i=1;
 int sum=0;

 while(i <=100){
    sum+= i;
    i++;
 }
 
```


``` c
//Adds 1+...+100.
int sum=0;
for(int i = 1; i <=100; i++){
   sum+= i;
}
```


* Analiza los programas con while y for asegúrate de entender por qué son equivalentes.

Son equivalentes porque los dos estan contando lo mismo, solo que el contdor en While lo refleja en todo el codigo y el for permanece solo en el ciclo for y desaparece luego de haber terminado.

* Convierte la versión del for a ensamblador.

``` asm

@INICIO
// incializamos los valores
A=0
D=A
@i
M=D
// funcion for queremos que M(i) sume hasta 100 y luego se borre
@FOR
// creamos un contador que va alimitar a i
@i
D=M
D = D + 1
@i
M=D
// queremos restarlo con 100
A=100
D=A
@i
A=M
D=D-A
// si no es igual a 0 salta a @FOR
@FOR
D;JMP
@INICIO
D;JMP



```

* No olvides comprobar el funcionamiento de los programas en ensamblador en el simulador.

* Compara las versiones en ensamblador del while y del for. ¿Qué puedes concluir?

