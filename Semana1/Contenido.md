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

<details><summary>Haz CLICK aca</summary>

```assembly
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
</details>

      - Ejercicio MIPS. Crear un programa que muestre su nombre.

<details><summary>Haz CLICK aca</summary>

```assembly
.data
        nombre: .asciiz "\nMi nombre es: Luis Toledo!\n"
.text
        li $v0, 4
        la $a0, nombre
        syscall
```
</details>

## 3. Challenge de la Semana (Jueves)

      - Ejercicio. Escribir un programa que muestre los numeros pares del 1 al 100.

```JavaScript
for (let i = 0; i <=100; i++) {
    // Si la division no contiene residuo indica que es un numero PAR.
    
    if (i % 2 == 0)  {
        console.log(i);
    }
}
```

      - Ejercicio. Encontrar el error del desarrollador que creo el codigo y corrigalo. Explique.

```JavaScript
var cond = false;

//Se corrigio el simbolo = por == ya que el simbolo = es para asignar una variable y el simbolo == es para comparacion
// if ((cond = true)) {        Linea Anterior
if ((cond == true)) {       // Linea Corregida
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```

      - Ejercicio. Crear un codigo con la siguiente logica. Si el Numero es 100 mostrar "This is a special number", Si el numero es menor de 1000 y multiplo de 10 y es diferente a 100 mostrar "Its almost a special number" si no cumple con ninguna condicion mostrar "Just a regular number".

```JavaScript
var n = 100;
// var n = 800;
// var n = 2000;

if (n == 100) {
  console.log('This is a special number!');
} else {
    if ((n < 1000) && (n % 10 == 0)) {
        console.log('Its almost a Special number!'); 
    } else {
        console.log('Just a regular number');
    }
}
```

      - Realizar Curso de Git