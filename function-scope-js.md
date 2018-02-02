# LECTURA DE CÓDIGO JAVASCRIPT "CREDIT-CARD-FORM" (app.js)

## Funciones globales: Son funciones que no están dentro de una función

   El archivo app.js tiene solo una función global y es anónima.

```js
      $(document).ready(function(){...

      });
 ```

## Variables Globales cuando se cargue en el DOM

 ```js
  var $inputCard = $('#card-number');
  var $inputMonth = $('.input-month');
  var $inputYear = $('.input-year');
  var $buttonNext = $('#next');
  var regexOnlyNumbers = /^[0-9]+$/;
  var labelErrorOrSuccessMessages = $('label[for="card-number"]');
 ```

## Funciones locales: Son funciones que están dentro de una función

* Identificar el evento que nos permite capturar el input del usuario

    ```js
        $inputCard.on('input', function() {...});
    ```

* Funciones que habilita el boton del formulario

    ```js
        function activeButton() {...} 
    ```

* Función que desabilita el boton del formulario

    ```js
        function desactiveButton() {...} 
    ```

* Función que valida la longitud del input ingresado por el usuario

    ```js
        function longitud(input) {...}
    ```

* Función que valida la longitud del input ingresado por el usuario

    ```js
        function soloNumeros(input) {...}
    ```

* Función que valida que sea una un numero de tarjeta valido

    ```js
        function isValidCreditCard(numberCard) {...}

    ```

## Variables locales

    ```js
        var regex = /^[0-9]+$/;
        ...
        var creditCardNumber = soloNumeros(longitud(numberCard));
        ...
        var arr = [];
        var sumaTotal = 0;
        ...
        var index
    ```

## Funciomes de Callback: Son funciones dentro de otras funciones

    

## Funciones expresions: Se declara una función en una variable y en este tipo de funciones no pasa el hoisting.

No trabajan con funciones expresions.

## Funciones statement: Lee la función por el hoisting que lo eleva a la memoria las variables y funciones

   ```js
        function(){}
        function activeButton() {} 
        function desactiveButton() {} 
        function longitud(input) {}
        function soloNumeros(input) {}
        function isValidCreditCard(numberCard) {}
   ``` 

* Anónima

    ```js
        $inputCard.on('input', function() {});
        
    ```
## Funciones de clousure
recuerda sus variables externas y puede acceder a ellas

## Funciones de scope: Solo se puede acceder estando dentro de la función

    ```js
    global scope: 

    $(document).ready(function() {
    var $inputCard = $('#card-number'); var $inputMonth = $('.input-month'); var $inputYear = $('.input-year'); var $buttonNext = $('#next'); var regexOnlyNumbers = /^[0-9]+$/; var labelErrorOrSuccessMessages = $('label[for="card-number"]'); };
    ```
Scope local: las variables en el scope local solo se les puede acceder estando dentro de dicha función.

## Contextos de ejecución

Esta conformada por las siguientes fases: 
* Fase de creación
 ```js
  var $inputCard = $('#card-number');
  var $inputMonth = $('.input-month');
  var $inputYear = $('.input-year');
  var $buttonNext = $('#next');
  var regexOnlyNumbers = /^[0-9]+$/;
  var labelErrorOrSuccessMessages = $('label[for="card-number"]');
  ``` 
  ```js
        function activeButton() {} 
        function desactiveButton() {} 
        function longitud(input) {}
        function soloNumeros(input) {}
        function isValidCreditCard(numberCard) {}
   ``` 
* Fase de ejecución

    ```js
    $(document).ready(function() {
    });
    ```

## Funciones que forman parte de la pila de ejecución (stack execution) 

    ```js
        function isValidCreditCard(numberCard) {}
        function soloNumeros(input) {}
        function longitud(input) {}
        function desactiveButton() {} 
        function activeButton() {} 
        function(){}
        contexto de ejecución global(document)
    ``` 

## Funciones que forman parte de la cola de eventos (event queue) 

   ```js
     $inputCard.on('input', function() {
    isValidCreditCard($(this).val().trim());
  });
   ``` 
## Leido por:

Eleyne Karina Ramírez De la Cruz

