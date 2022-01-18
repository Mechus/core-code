# core-code
Core Code bootcamp

### Tuesday 11/01/2022
- Java language is compiled or interpreted?  
**Java es lenguaje compilado e interpretado.**

- Create an algorithm to calculate the equivalent of your local currencty to USD  
**Ingresar monto de moneda local  
Validar si monto es valido  
Si no es valido mostrar error y terminar  
Si monto es valido consultar equivalencia de moneda local a 1 dolar  
Dividir monto de moneda local dentro de equivalencia a 1 dolar 
Mostrar monto total en dolares**

- Why is pseudocode helpful?  
**Es importante para tener un boceto de la idea o algoritmo que queremos transformar en el lenguaje que deseamos implementar, asi poder identificar mejor la idea para optimizar y tener un codigo mas limpio.**

- Create a pseudocode to calculate the aproximated age of a user base on the year they born  
**INICIO PROGRAMA  
DECLARAR listadoUsuarios, anioActual  
LEER listado  
GUARDAR (listadoUsuarios,listado);  
LEER añoActual  
GUARDAR (anioActual,añoActual);  
RECORRER listadoUsuarios  
  CALCULAR anioActual - anioNacimiento  
  MOSTRAR CALCULO  
FIN RECORRER  
FIN PROGRAMA**

- Why are flowcharts important to us as developers?  
**Son importantes para documentar y planificar la construccion de funciones que se implementan dentro de nuestro codigo. Tambien para plasmar de forma grafica la idea del algoritmo que deseamos implementar.**




### Tuesday 12/01/2022
- Translate the year you where born to binary, decimal and hexadecimal
**1994 -> 11111001010**
1994 / 2 = 997 + 0
997 / 2 = 498 + 1
498 / 2 = 249 + 0
249 / 2 = 124 + 1
124 / 2 = 112 + 0
62 / 2 = 31 + 0
31 / 2 = 15 + 1
15 / 2 = 7 + 1
7 / 2 = 3 + 1
3 / 2 = 1 + 1
1 / 2 = 0 + 1
 
**1994 -> 7CA**
1994 / 16 = 124 , 10 -> A
124 / 16 = 7 , 12 -> C
7 / 16 = 0 , 7 -> 7

- Translate 51966 into hexadecimal and binary
**51966 -> 1100101011111110** 
51966 / 2 = 25983 + 0
25983 / 2 = 12991 + 1
12991 / 2 = 6495 + 1
6495 / 2 = 3247 + 1
3247 / 2 = 1623 + 1
1623 / 2 = 811 + 1
811 / 2 = 405 + 1
405 / 2 = 202 + 1
202 / 2 = 101 + 0
101 / 2 = 50 + 1
50 / 2 = 25 + 0
25 / 2 = 12 + 1
12 / 2 = 6 + 0
6 / 2 = 3 + 0
3 / 2 = 1 + 1
1 / 2 = 0 + 1

**51966 -> CAFE** 
51966 / 16 = 3247 , 14 -> E
3247 / 16 = 202 , 15 -> F
202 / 16 = 12 , 10 -> A
12 / 16 = 0 , 12 -> C


- Create a program to add two numbers given by the user
`.data
	title: .asciiz "\nPrograma para realizar sumas de 2 numeros\n"
	result: .asciiz "\nEl resultado de la suma es: "
	number1: .asciiz "\nIngrese el primer numero: "
	number2: .asciiz "\nIngrese el segundo numero: "
.text
	main:
      		li $v0, 4
      		la $a0, title
      		syscall
      		
		li $v0, 4
		la $a0, number1
		syscall

		li $v0, 5
		syscall

		move $t0, $v0

		li $v0, 4
		la $a0, number2
		syscall

		li $v0, 5
		syscall

		move $t1, $v0

		add $t2, $t0, $t1
		
      		li $v0, 4
      		la $a0, result
      		syscall
		
		li $v0, 1
		move $a0, $t2
		syscall`

- Create a program that display your name
`.data
	title: .asciiz "\nPrograma para mostrar mi nombre\n"
	result: .asciiz "\nMi nombre es: Edgar Nemecio Ortiz Barrientos"
.text
	main:
      		li $v0, 4
      		la $a0, title
      		syscall
      				
      		li $v0, 4
      		la $a0, result
      		syscall
		
		li $v0, 1
		move $a0, $t3
		syscall`

