# Introduccion a la Programacion y JavaScript

## - Challenge de la Semana (Martes)

      - Crear una explicacion acerca de Lenguages de Programacion Interpretados y Compilados.

Podria decirce que primordialmente la diferencia entre un lenguaje de programacion interpretado y un lenguaje de programacion compilado es que el compilado requiere un paso adicional antes de ser ejecutado, la compilacion que convierte el codigo fuente a lenguaje de maquina. Por otro lado, el lenguaje interpretado es convertido a lenguaje de maquina a medida que es ejecutado.

      - Es Java compilado o interpretado o ambos? 

El Lenguaje de Programacion Java es compilado en un archivo .java y a la misma vez este archivo es interpretado por la maquina virtual de Java (JVM).

      - Ejercicio. Pseudocodigo conversion de Moneda de Dolares a Bitcoins

1. Inicio
2. ValorEnDolares <-- Obtiene
3. TasaDeCambioDiaria <-- Obtiene
4. ValorBitcoins <-- ValorEnDolares * TasaDeCambioDiaria
5. Mostrar ValorBitcoins
6. Fin
---
      
      - Lenguajes de Bajo y Alto Nivel

El ordenador sólo entiende un lenguaje conocido como código binario o código máquina, consistente en ceros y unos. Es decir, sólo utiliza 0 y 1 para codificar cualquier acción.
Los lenguajes más próximos a la arquitectura hardware se denominan lenguajes de bajo nivel y los que se encuentran más cercanos a los programadores y usuarios se denominan lenguajes de alto nivel.


## 2. Challenge de la Semana (Miercoles)

      - Ejercicio. Ingresar la Fecha de Cumpleaños en una Matriz (Convertir decimal a Binario)

Fecha de Cumpleaños = 10 de Marzo de 1971. Conversion de Decimal a Binario a traves de divisiones:

1971 / 2 = 985 numero Restante = 1

985 / 2  = 492 numero Restante = 1

492 / 2  = 246 numero Restante = 0

246 / 2  = 123 numero Restante = 0

123 / 2  = 61  numero Restante = 1

61  / 2  = 30  numero Restante = 1

30  / 2  = 15  numero Restante = 0

15  / 2  = 7   numero Restante = 1

7   / 2  = 3   numero Restante = 1

3   / 2  = 1   numero Restante = 1

1   / 2  = 0   numero Restante = 1    ==>  numero binario 11110110011 

      - Ejercicio MIPS. Crear un programa que sume 2 numeros ingresados por el usuario.

```MIPS
.data
	#Se crean las etiquetas de los mensajes
	saludo: .asciiz "Bienvenido\n"
	numero1: .asciiz "Ingresa el Primer Numero:\n" 
	numero2: .asciiz "Ingresa el Segundo Numero:\n"
	suma: .asciiz "El Resultado de la Suma es = "	
.text
	#Muestra mensaje de saludo
	li $v0,4
	la $a0, saludo
	syscall 
	
	#Imprime mensaje del Primer Numero
	li $v0,4
	la $a0, numero1
	syscall 
	
	#Pedimos el Primer Numero
	li $v0,5
	syscall 
	
	#Movemos el primer numero a una variable temporal ($t0)
	move $t0, $v0
	
	#Imprime mensaje del Segundo Numero
	li $v0,4
	la $a0, numero2
	syscall
	
	#Pedimos el Segundo Numero
	li $v0,5
	syscall
	
	#Movemos el segundo numero a una variable temporal ($t1)
	move $t1, $v0
	
	#Se hace la suma y se guarda el resultado en la variable ($t2)
	add $t2, $t0, $t1
	
	#Se muestra en pantalla el mensaje del resultado
	li $v0, 4
	la $a0, suma
	syscall
	
	#Se muestra el resultado de la suma
	li $v0, 1
	move $a0, $t2
	syscall

	#Fin del Programa
	li $v0, 10
	syscall 
```
      - Ejercicio MIPS. Crear un programa que muestre su nombre.

```MIPS
.data
        nombre: .asciiz "\nMi nombre es: Luis Toledo!\n"
.text
        li $v0, 4
        la $a0, nombre
        syscall
```

## 3. Challenge de la Semana (Jueves)

      - Ejercicio. Escribir Numeros Especiales

      - Ejercicio. Mal Codigo

      - Ejercicio. Mal Codigo 2

      - Realizar Curso de Git