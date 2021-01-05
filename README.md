## Credit Card Checker

Ejercicio de codecademy.com donde dan 15 arrays con números de tarjetas de crédito y se pide qque se compruebe si son números válidos o no.

### Requisitos

1. Crear una función `validateCred()` que tiene como parámetro un array. La función **no debe mutar el array** y tiene que:

    * Empezando por el último dígito e iterando de derecha a izquierda, los números alternos se multiplicarán por dos. Es decir, el primero no se multiplica,   el segundo sí, el tercero se multiplica, y así sucesivamente. Si el número resultante de la multiplicación es >9 hay que restarle 9.
    * Sumar todos los dígitos de la tarjeta de crédito.
    * Si el número restante se divide por 10 y el resto de la división es 0 la tarjeta **es válida**. En caso contrario es inválida.

2. Crear la función `findInvalidCards()` a la que se le pase un array con los todos números de tarjeta y devuelva un array con las tarjetas de números inválidos.

3. Crear una función `idInvalidCardCompanies()` a la que se pase el array con los números de tarjeta inválidos y devuelva una array con compañías de tarjetas según el siguiente cuadro:


| First Digit | Company |
| ------- | ------- |
| 3  | Amex  |
| 4  | Visa  |
| 5  | Mastercard  |
| 6  | Discover  |



Si el número no comienza con ninguno de los números enumerados, imprimir el mensaje: "Compañía no encontrada".

`idInvalidCardCompanies()` debe devolver una array de empresas de las tarjetas con números no válidos. Este array NO debe contener duplicados, es decir, incluso si hay dos tarjetas Visa no válidas, "Visa" solo debe aparecer una vez en la matriz.


### Project Requirements

1. Look over the starter code. There are 15 arrays that each contain the digits of separate credit card numbers. They all have prefixes to reflect their status, i.e. variables that start with `valid` contain a valid number, whereas `invalid` do not, and `mystery` variables can be either. There is also a `batch` array that stores all of the provided credit cards in a single array.
You’ll use these arrays later to check if your functions are working properly.

2. Create a function, `validateCred()` that has a parameter of an array. The purpose of `validateCred()` is to return `true` when an array contains digits of a valid credit card number and `false` when it is invalid. This function **should NOT mutate** the values of the original array.
To find out if a credit card number is valid or not, use the Luhn algorithm. 
The calculations in the Luhn algorithm can be broken down as the following steps:

    * Starting from the farthest digit to the right, AKA the check digit, iterate to the left.
    * As you iterate to the left, every other digit is doubled (the check digit is not doubled). If the number is greater than 9 after doubling, subtract 9 from its value.
    * Sum up all the digits in the credit card number.
    * If the sum modulo 10 is 0 (if the sum divided by 10 has a remainder of 0) then the number is valid, otherwise, it’s invalid.
Here’s a visual that outlines the steps. Check your function using both the provided valid and invalid numbers.

3. Create another function, `findInvalidCards()` that has one parameter for a nested array of credit card numbers. The role of `findInvalidCards()` is to check through the nested array for which numbers are invalid, and return another nested array of invalid cards.

5. After finding all the invalid credit card numbers, it’s also necessary to identify the credit card companies that have possibly issued these faulty numbers. Create a function, `idInvalidCardCompanies()` that has one parameter for a nested array of invalid numbers and returns an array of companies.

Currently, there 4 accepted companies which each have unique first digits. The following table shows which digit is unique to which company:


| First Digit | Company |
| ------- | ------- |
| 3  | Amex  |
| 4  | Visa  |
| 5  | Mastercard  |
| 6  | Discover  |


If the number doesn’t start with any of the numbers listed, print out a message like: “Company not found”.

`idInvalidCardCompanies()` should return an array of companies that have mailed out cards with invalid numbers. This array should NOT contain duplicates, i.e. even if there are two invalid Visa cards, `"Visa"` should only appear once in the array.

