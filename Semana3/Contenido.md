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

## 2. Challenges de la Semana (Martes)

    - Ejercicio. Simple Cerdo Latino

<details><summary><strong>Respuesta</strong></summary>    

```JavaScript

function pigIt(str){
  let vector = str.split(' ');
  let vector2 = [];
  
  for (let i=0; i < vector.length; i++) {
    // Verifico que no traiga signos de puntuacion
    if (vector[i].substring(0,1) === "!" || vector[i].substring(0,1) === "?" ) {
      final = vector[i].substring(0,1);
    } else {
      final = vector[i].substring(0,1) + 'ay';
    }
    vector2[i] = vector[i].substring(1,vector[i].length) + final;
  }
  let nueva = vector2.join(' ');
  return nueva;
}

```

</details>

    - Ejercicio. Contando Duplicados

    - Ejercicio. Decofificar el Codigo Morse

## 3. Challenges de la Semana (Miercoles)

    - Ejercicio. Validar Parentesis

    - Ejercicio. Convertir String a Camel Case

    - Ejercicio. Unico en el Orden

## 4. Challenges de la Semana (Jueves)

    - Ejercicio. Doblar un Vector

    - Ejercicio. Encripta esto!

    - Completa tu 1er Core Challenge