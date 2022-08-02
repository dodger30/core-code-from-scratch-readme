# JavaScript - Parte 3

## 1. Challenges de la Semana (Lunes)

    - Mira el video y los ejemplos de "For Of"

    - Mira el Video "JavaScript Array Filter"

    - Mira el Video "JavaScript Array Reduce"

    - Mira el Video "JavaScript Array Map"

## 2. Challenges de la Semana (Martes)

    - Mira el Video de "Expresiones Regualares"

    - Lee la documentacion de "Expresiones Regulares"

    - Mira el Video acerca de "Replace"

    - Lee la documentacion acerca de "Replace"

    - Chequea "Regexr" Una herramienta para testear expresiones regulares

    - Mira el Video completo de "Expresiones Regualares"

## 3. Challenges de la Semana (Miercoles)

    - Ponte al dia o haz un trabajo extra

## 4. Challenges de la Semana (Jueves)

    - Completa el 2do Core Challenge

## 5. Extra

    - Validacion Simple de un usuario

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function validateUsr(username) {
  // Validando que sean letras minusculas, numeros o guion bajo. 
  // Minimo 4 Caracteres Maximo 16 Caracteres
  
  const ExpresionRegular = /^[a-z0-9_]{4,16}$/;
  return ExpresionRegular.test(username);

}

```

</details>

    - Obtener un numero desde un String

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function getNumberFromString(s) {
  //Se define la expresion regular elimine los caracteres que no son digitos del String
  return Number(s.replace(/\D/g, ''));
}

```

</details>

    - Limpiando un String

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function stringClean(s){
  // Regex Expression para eliminar los numeros de la cadena
  let pattern = /[^A-Za-z ~#$%()^&*@:;"'.,!?]/g;
  return result = (s.replace(pattern,''))
}

```

</details>

    - Validacion de Contraseña

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

const REGEXP = new RegExp("^(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9])(?=.*[!@#\$%\^&\*])(?=.{6,})")";

```

</deteails>
