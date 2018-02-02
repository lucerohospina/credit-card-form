# **Identificando funciones**

### Objetivo: Poner en práctica nuestra habilidad de poder identificar los tipos de funciones determinando así el alcance de estas dentro del ambiente lexical.

#### 1) Funciones Globales

> $(document).ready(function() {}

#### 2) Funciones Locales

> function activeButton() {} 

> function desactiveButton() {} 

> function longitud(input) {}

> function soloNumeros(input) {}

> function isValidCreditCard(numberCard) {}

#### 3) Funciones Statement

> function activeButton() {
    $buttonNext.attr('disabled', false);
  } 

> function desactiveButton() {  
    $buttonNext.attr('disabled', true);
  } 

> function longitud(input) {
    if (input.trim().length === 16) {
      return input;
    }
  }

> function soloNumeros(input) {
    var regex = /^[0-9]+$/;
    if (regex.test(input)) {
      return input;
    }
  }

> function isValidCreditCard(numberCard) {}

#### 4) Funciones Callback
> $(document).ready(function() {}

>  $inputCard.on('input', function() {
    isValidCreditCard($(this).val().trim());
  }); 

#### 5) Funciones Anónimas

> $inputCard.on('input', function() {
    isValidCreditCard($(this).val().trim());
  }); 

#### 6) Closure

> function isValidCreditCard(numberCard) {
    var creditCardNumber = soloNumeros(longitud(numberCard));
   ...
