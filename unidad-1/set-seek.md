# Unidad 1

## 🔎 Fase: Set + Seek

### Actividad 01

Deduciendo el codigo de la actividad 1 puedo hallar los siguientes apuntes;

-  @(numero) :es A no explicita un numero en un espacio de la rom
- D=A: A aquiere y asigna el valor a D el numero del la rom anterior
- D=D+A :una suma de sus valores actuales
- M=D : se usa para guardar la informacion de D en una parte de la ram
- 0,JMP : si el valor de A es igual a 0 salta a la pocision #0 de la ROM pero el valor que posea D se mantiene
#### Experimento 1

*  ¿Qué sucede? se observa como los valores (PC,A y D) vancambiando a lo largo de la interaccion 
* ¿Qué valor se almacena en la dirección de memoria 16? Se guardo el valor de D 
* ¿Por qué crees que es ese valor? creo que porque en el anterior paso se le indico el numero 16 a A y M lo tomo como una orde de posicion 
* ¿Qué instrucciones se ejecutan en cada ciclo Fetch-Decode-Execute? se asigna un numero en de -> se suman numeros -> se obtiene un resultado-> se asina el resultado a un apocision de memoria
* ¿Qué cambios observas en el contenido de la memoria y los registros? que la RAM # 16 tiene un valor de 5

#### Experimento 1
 Escribe un programa en lenguaje ensablador que sume los números 5 y 10, y almacene el resultado en la dirección de memoria 20. Utiliza el simulador de la CPU Hack para ejecutar tu programa y verifica que el resultado es correcto.

#### Programa
@5

D=A

@10

D=D+A

@20

M=D
