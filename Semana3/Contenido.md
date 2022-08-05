# JavaScript - Parte 2

## 1. Challenges de la Semana (Lunes)

    - Ejercicio. Quien dio Like?

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function likes(names) {
  let personas = names.length;
  let respuesta = "";
  
  if (personas === 0) {
    respuesta = "no one likes this";
  }
  if (personas === 1) {
    respuesta = `${names[0]} likes this`;
  }
  if (personas === 2) {
    respuesta = `${names[0]} and ${names[1]} like this`;
  }
  if (personas === 3) {
    respuesta = `${names[0]}, ${names[1]} and ${names[2]} like this`;
  } 
  if (personas > 3) {
    respuesta = `${names[0]}, ${names[1]} and ${personas - 2} others like this`;
  }
  return respuesta;
}

```
</details>

    - Ejercicio. Contando Bits

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

var countBits = function(n) {
  let binario = Math.abs(n).toString(2);
  contador = 0;
  for(var i = 0; i < binario.length; i++) {
	  if (binario[i] === "1") {
      contador++;
    }
  }
  return contador ;
};

```

</details>

    - Ejercicio. Su orden, Por Favor!

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function order(words){
  // Inicializamos el Array
  if (words === "" ) {
    return "";
  } else {
    arreglo = words.split(' ');
    arreglo2 = [];
  
    for (let i=1; i < 10; i++) {
      for (let j=0; j < arreglo.length; j++) {
        if (arreglo[j].indexOf(i) != -1) {
          arreglo2.push(arreglo[j]);
        }
      }
    }
    return arreglo2.join(' '); 
  }
}

```

</details>

## 2. Challenges de la Semana (Martes)

    - Ejercicio. Simple Cerdo Latino

<details><summary><strong>Respuesta</strong></summary>    

```JavaScript

function pigIt(str){
  let vector = str.split(' ');
  let vector2 = [];
  
  for (let i=0; i < vector.length; i++) {
    // Verifico que no traiga signos de puntuacion
    final = (vector[i].substring(0,1) === "!" || vector[i].substring(0,1) === "?" ) 
      ? vector[i].substring(0,1)
      : vector[i].substring(0,1) + 'ay';
    
    vector2[i] = vector[i].substring(1,vector[i].length) + final;
  }
  let nueva = vector2.join(' ');
  return nueva;
}

```

</details>

    - Ejercicio. Contando Duplicados

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function duplicateCount(text){
  //Inicializamos las variables y ordenamos el arreglo
  text = text.toLowerCase();
  arreglo = text.split('').sort();
  let repetidos = [];
  let contador = 1;
  
  for ( let i=0; i < arreglo.length; i++ ) {
    if ( arreglo[i] === arreglo[i+1]) {
      contador++;
    } else {
      if (contador > 1) {
        repetidos.push(contador);
      }
      contador = 1;
    }
  }
  return repetidos.length;
}

```

</details>

    - Ejercicio. Decofificar el Codigo Morse

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

var decodeMorse = function(morseCode){
  var palabras = (morseCode).split('   ');
  var letras = palabras.map((w) => w.split(' '));
  var decoded = [];

  for(var i = 0; i < letras.length; i++){
    decoded[i] = [];
    for(var x = 0; x < letras[i].length; x++){
        if(MORSE_CODE[letras[i][x]]  && typeof MORSE_CODE[letras[i][x]] != 'undefined'){
            decoded[i].push( MORSE_CODE[letras[i][x]] );
        }
    }
  }

  return decoded.map(arr => arr.join('')).join(' ').replace(/  /g, ' ').trim();
}

```

</details>

## 3. Challenges de la Semana (Miercoles)

    - Ejercicio. Validar Parentesis

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function validParentheses(parens) {
  //Inicializamos variables
  let abiertos =0;
  let respuesta = false;
  
  for (let i = 0; i < parens.length; i++) {
    if (parens[i] === '(' ) {
      abiertos++;
    } 
    if (parens[i] === ')') {
      abiertos--;
    }
    if (abiertos < 0 ) {
      return respuesta;
    }
  }
  
  if (abiertos === 0 ) {
    respuesta = true;
  } 
  return respuesta;
}

```

</details>

    - Ejercicio. Convertir String a Camel Case

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function toCamelCase(str){
  let arreglo = str.split(/_|-/);
  let palabra = "";
  
  for (let i = 0; i < arreglo.length; i++) {
    if ( i != 0 ) {
     arreglo[i] = arreglo[i].charAt(0).toUpperCase() + arreglo[i].slice(1); 
    }
    palabra = palabra + arreglo[i];
  }
  return palabra;
}

```

</details>

    - Ejercicio. Unico en el Orden

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

var uniqueInOrder=function(iterable){
  //remember iterable can be string or an array
  let cadena = [];
   
  // Si es string lo convierto a Array
  let arreglo = (typeof(iterable) === 'string')   
    ? [...iterable]
    : iterable;
   
  for (let i=0; i< arreglo.length; i++) {
    if ( arreglo[i+1] != arreglo[i] ) {
      cadena.push(arreglo[i]);
    }
  }
  return cadena;
}

```

</details>

## 4. Challenges de la Semana (Jueves)

    - Ejercicio. Doblar un Vector

    - Ejercicio. Encripta esto!

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

var encryptThis = function(text) {
  let respuesta;
  let arreglo = text.split(" ");
  let cadena = [];
  
  for (let i=0; i<arreglo.length; i++) {
    respuesta = "";
    
    switch (arreglo[i].length) {
      case 1:
        respuesta = arreglo[i].charCodeAt(0);
        break;
      case 2:
        respuesta =  arreglo[i].charCodeAt(0) + arreglo[i].slice(arreglo[i].length-1,arreglo[i].length);
        break;
      case 3:
        respuesta =  arreglo[i].charCodeAt(0) + arreglo[i].slice(arreglo[i].length-1,arreglo[i].length) + arreglo[i].substring(1,2);
        break;
      default:
        respuesta =  arreglo[i].charCodeAt(0) +  
                     arreglo[i].slice(arreglo[i].length-1,arreglo[i].length) + 
                     arreglo[i].substring(2,arreglo[i].length - 1) +
                     arreglo[i].substring(1,2);
        break;
    }
    cadena.push(respuesta);
  }
  return cadena.join(' ');
}

```

</details>

    - Completa tu 1er Core Challenge