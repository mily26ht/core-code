## core-code
core code bootcamp
## Desafio de la Semana- Día Martes 11-01-22
### ¿El lenguaje Java está compilado o interpretado?
<p> ESCOBAR (2017) define que Java es un lenguaje particular porque es compilado, pero es compilado a un lenguaje intermedio llamado bytecode, que después es interpretado. <img src="https://cdn.worldvectorlogo.com/logos/java.svg" width="200" height="150" align="right" />
  Los creadores de Java querían crear un lenguaje compilado, pero que se pudiera ejecutar en cualquier sistema operativo y procesador sin necesidad de crear varios ejecutables.
                                                                               
Es por eso que si quieres ejecutar código Java debes instalar el JRE (Java Runtime Environment), que es el programa que se encarga de interpretar el bytecode al que son compilados los programas de Java.

Si deseas compilar código Java no es suficiente instalar el JRE, necesitas el JDK (Java Development Kit) que incluye el compilador, entre otras herramientas de desarrollo.</p>

### Algoritmo para conversion de cordobas a dolares
1-Saber el valor actual del dolar en cambio a tu moneda
2-Dividir tu moneda entre el valor del dolar

### ¿Por qué es útil el pseudocódigo?
El pseudocodigo es bastante util, una de las ventas de realizar pseudocodigos es que te permite ir agilizando tu cerebro para la programación de software,
mejoramiento del analisis para la resolución de problemas hasta volverse meticuloso.

### Pseudocódigo para calcular la edad aproximada de los usuarios
1. START
2. Definir variables Año Actual=2022, Año Nacimiento,Edad.
3. Para saber su edad, ingrese su Año de nacimiento:__ (Guarda valor en la variable Año Nacimiento)
4. Se realiza la operación aritmetica y se guarda en la variable edad; edad= Año actual - Año Nacimiento.
5. Se imprime el resultado (Su edad actual es: __ )
6. END

### ¿Por qué los diagramas de flujo son importantes para nosotros como desarrolladores?
Un diagrama de flujo es un diagrama que describe un proceso, sistema o algoritmo informático, y es de mucha importancia ya que facilita la manera de representar visualmente el flujo de datos

###  Lenguajes de programación
| Lenguaje de Alto Nivel  | Lenguaje de Bajo Nivel |
| ----------------------- | ---------------------- |
|tipo de lenguaje de programación que no expresa los algoritmos teniendo en cuenta la capacidad que tienen las máquinas para ejecutar órdenes, sino al que se utiliza teniendo en cuenta las capacidades cognitivas de los seres humanos.                         |  es aquel en el que sus instrucciones ejercen un control directo sobre el hardware y por lo tanto están condicionados por la estructura física de las computadoras que lo soportan                      |

## Desafio de la Semana- Día Miercoles 12-01-22
### Aprende sobre números binarios, decimales y hexadecimales
|  Binarios               |   El sistema binario es un sistema de numeración en el que se utiliza la base aritmética 2. Este sistema es el utilizado por los ordenadores y sistemas digitales.                      |
| :----:|  :---   |
|  Decimales              |  Es un sistema de numeración posicional en el que las cantidades son representadas mediante la base aritmética del número diez.                       |
|  Hexadecimales          |  el sistema de numeración decimal es un sistema de numeración posicional que tiene con base el número 16.                        |

### Traduce el año en que naciste a binario, decimal y hexadecimal
Para pasar un número en Binario Natural lo tenemos que dividir por 2 ir quedandonos con el resto.
1998 entre 2 sobra 0<br/>
999 entre 2 sobra 1<br/>
499 entre 2 sobra 1<br/>
249 entre 2 sobra 1<br/>
124 entre 2 sobra 0<br/>
62 entre 2 sobra 0<br/>
31 entre 2 sobra 1<br/>
15 entre 2 sobra 1<br/>
7 entre 2 sobra 1<br/>
3 entre 2 sobra 1<br/>
1 entre 2 sobra 1<br/>
El resultado de 1998 en Binario es: **01110011111**

Para pasar un número binario a decimal lo tenemos que multiplicar por 2 elevado a la potencia que corresponda.<br/>
1 por 2^0 igual a 1<br/>
1 por 2^1 igual a 2<br/>
1 por 2^2 igual a 4<br/>
1 por 2^3 igual a 8<br/>
1 por 2^4 igual a 16<br/>
0 por 2^5 igual a 0<br/>
0 por 2^6 igual a 0<br/>
1 por 2^7 igual a 128<br/>
1 por 2^8 igual a 256<br/>
1 por 2^9 igual a 512<br/>
0 por 2^10 igual a 0<br/>
El resultado de 1998 en Decimal es: **927**

Para pasar un numero decimal a hexadecimal lo que tenemos que hacer es dividir entre 16 y quedandonos el resto<br/>
927 entre 16 sobra 15<br/>
57 entre 16 sobra 9<br/>
y quedan 3<br/>
Esto lo  ordenamos y comparamos en la tabla de hexadecimales <br/>
El resultado de 1998 en Hexadecimal es: **39F**

### Traducir 51966 a hexadecimal y binario
El resultado en binario es:**1100101011111110**<br/>
El resultado en hexadecimal es:**CAFE**

### Crear un programa para sumar dos números dados por el usuario
Simulador de lenguaje emsanblador, Software que pide dos numero y los suma

```
.data
Se crean la variables y se colocan los mensajes para el usuario
Saludo: .asciiz "Bienvenidos\n"
number1: .asciiz "\nIngrese el primer numero a sumar: "
number2: .asciiz "\nIngrese el segundo numero a sumar: "
resultado: .asciiz " La suma es: "
despedida: .asciiz "\n Programa terminado"
.text

Imprime en la pantalla el saludo
li $v0, 4
la $a0, Saludo
syscall

imprimir en la pantalla solicitando el primer numero
	li $v0, 4
	la $a0, number1
	syscall
	
ingrese el 1er numero
	li $v0, 5
	syscall
	
se mueve el registro
	move $t0, $v0
	
imprimir en la pantalla solicitando el segundo numero
	li $v0, 4
	la $a0, number2
	syscall
	
ingrese el 2do numero
	li $v0, 5
	syscall
	
se mueve el registro
	move $t1, $v0
	
se hace la suma y se almacena en el registro $t2
	
	add $t2,$t0, $t1
	
imprimir en la pantalla el resultado
	li $v0, 4
	la $a0, resultado
	syscall
se imprime en pantalla el resultado
	li $v0,1
	move $a0, $t2
	syscall
	
despedida
	li $v0,4
	la $a0, despedida
	syscall
	
fin del programa
	
	li $v0, 10
syscall
 ``` 
  Crear un programa que muestre su nombre
  
  ```
  .data 
programa que pide e imprime tu nombre
pregunta: .asciiz "Cual es tu nombre?"
nombre: .space 20
 Saludo: .asciiz "\nHola nuevamente: "
 despedida: .asciiz"\nGracias por usar el programa, see you later"
 
 .text
 Imprime en la pantalla el pregunta
li $v0, 4
la $a0, pregunta
syscall

 main: 
para recibir el texto del usuario
    li $v0, 8
    la $a0, nombre
    li $a1, 20
    syscall
    
imprimir saludo
li $v0, 4
la $a0, Saludo
syscall
 
visualizar nombre
 li $v0,4
 la $a0, nombre
 syscall
 
despedida
	li $v0,4
	la $a0, despedida
	syscall

fin del programa
	
	li $v0, 10
	syscall
  ```
  
  ## Referencia
  -Escobar, G. (06 de Nov de 2017). make it real camp. Obtenido de https://blog.makeitreal.camp/lenguajes-compilados-e-interpretados/

