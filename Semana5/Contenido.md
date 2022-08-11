# Fin del Mes y TypeScript

## 1. Challenges de la semana (Lunes)

    - Tiempo para Ponerte al dia

## 2. Challenges de la semana (Martes)

    - Tiempo para Ponerte al dia

## 3. Challenges de la semana (Miercoles)

    - Aprende acerca de FP vs OOP

    - Aprende conceptos basicos de OOP

    - Lee acerca de OOP

## 4. Challenges de la semana (Jueves)

    - Realiza el Ejercicio guiado de TypeScript

    - Completa el 3er Core Challenge

## 5. Extra

    - Ejercicio. Encuentra la Letra Faltante

<details><summary><strong>Respuesta</strong></summary>

```JavaScript

function findMissingLetter(array)
{
  const alphabet = ["A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z"];
  const alfabeto = ["a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z"];
  
  
  if (alphabet.includes(array[0])) {
    let pos = alphabet.indexOf(array[0]);
    
    for (let i=0; i<array.length; i++) {
      if (!(alphabet[i+pos] === array[i])) {
        return alphabet[i+pos];
      }
    }
  } else {
    let pos = alfabeto.indexOf(array[0]);
    
    for (let i=0; i<array.length; i++) {
      if (!(alfabeto[i+pos] === array[i])) {
        return alfabeto[i+pos];
      } 
    }
  }
}

```

</details>

    - Ejercicio. Reversa o Rotacion?

    - Ejercicio. Cual es tu Veneno?

    - Ejercicio. Diferencia en Vector