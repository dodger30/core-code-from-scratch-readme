# JavaScript

## 1. Challenge de la Semana (Lunes)

        - Continuar con el Curso de Git

        - Crear una cuenta de Codewars

<details><summary><strong>Respuesta</strong></summary>

![Usuario en CodeWars](CuentaCodewars.jpg)

</details>

        - Comando If - Else

        - Comando for

        - Comando While

        - Funciones

## 2. Challenge de la Semana (Martes)

        - Iniciar el Curso de HTML

<details><summary><strong>Respuesta</strong></summary>

![Inicio del Curso HTML](CursoHTMLIntro.jpg)

</details>

        - Ejercicio. Multiplicacion

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function multiply(a, b){
  //Se modifico la funcion para que regresara el resultado de la multiplicacion.
  return (a * b);
}

```

</details>

        - Ejercicio. ASCII Total

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function uniTotal (string) {
// Convirtiendo de String a Codigo ASCII
  let Cadena = 0;
  
  if (string != "")
    for (let i=0; i<string.length; i++) {
      Cadena = Cadena + string.charCodeAt(i);
    }
    
  return Cadena;
}

```

</details>

## 3. Challenge de la Semana (Miercoles)

        - Continuar con el curso de HTML

<details><summary><strong>Respuesta</strong></summary>

![Continuacion Curso HTML](CursoHTMLVSCode.jpg)

</details>

        - Ejercicio. Char a Valor ASCII

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function getChar(c){
  // Funcion para convertir un valor entero a Codigo ASCII
  
  caracter = String.fromCharCode(c);
  return caracter;
}

```

</details>

        - Ejercicio. Suma Binaria

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function addBinary(a,b) {
  var resultado = (a + b);
  var cadena = '';
  var cadena2 = '';
  
  do {
     residuo = (resultado % 2);
     cadena = cadena + residuo;
     resultado = Math.trunc(resultado/2);
  } while (resultado !== 0);
  
  for (var i=cadena.length - 1; i >= 0; i--) {
    cadena2 = cadena2 + cadena[i];
  }
  return cadena2;
}

```
</details>

        - Ejercicio. Nota Final del Estudiante

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function finalGrade (exam, projects) {
  let nota_final = 0
  
  if ((exam >90) || (projects >10)) {
    nota_final = 100
  } else if ((exam >75) && (projects >=5)) {
    nota_final = 90
  } else if ((exam >50) && (projects >=2)) {
    nota_final = 75
  }   
  return nota_final     // final grade
}

```
</details>

## 4. Challenge de la Semana (Jueves)

        - Continuar con el curso de HTML

<details><summary><strong>Respuesta</strong></summary>

![Continuacion Curso HTML](CursoHTMWebSite.jpg)

</details>

        - Ejercicio. Remover puntos de exclamacion.

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function remove (string) {  
  string2 = '';
  
  // Verificamos si al menos contiene el simbolo '!' al final de la cadena
  if (string.lastIndexOf("!") == string.length -1 ) {
    ultimo = string.length;
    var i = string.length -1;
    while (i >= 0) {
       if (string[i] == "!") {
         ultimo = i; 
       } else {
           break;
       }
      i--;
    }
    string2 = string.substring(0,ultimo);
  } else {
    string2 = string;
  }
  return string2;
}

```

</details>

        - Ejercicio. Remover Vowel

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function shortcut(string){
  return string.replace(/[aeiou]/g,'')
}

```

</details>

        - Ejercicio. Piedra, Papel o Tijera

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

const rps = (p1, p2) => {
  var winner = "";
  if (p1 === p2) {
    winner = "Draw!";
  } else if (p1 === "rock") {
      if (p2 === "paper") {
        winner = "Player 2 won!";
      } else {
        winner = "Player 1 won!";
      }
    } else if (p1 === "paper") {
      if (p2 === "rock") {
        winner = "Player 1 won!";
      } else {
        winner = "Player 2 won!";
      }
    } else {
      if (p2 === "paper") {
        winner = "Player 1 won!";
      } else { 
        winner = "Player 2 won!";
      }
    }
    return winner;
  }

```

</details>

        - Ejercicio. Bugger Persistente

## 5. Ejercicios Extra 

        - Ejercicio. Holiday VIII - Duty Free

        - Ejercicio. Twice as Old

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function twiceAsOld(dadYearsOld, sonYearsOld) {
  // Calcular hace cuantos años el padre tuvo el doble de la edad del hijo o en cuantos años lo tendra.
  var fecha = (dadYearsOld - sonYearsOld * 2);
  if (fecha < 0) {
    fecha = fecha * -1;
  }
  return fecha;
}

```

</details>

        - Ejercicio. Valid Spacing

        - Ejercicio. Fake Binary