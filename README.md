# Producto Final
## Tarjeta de Crédito Válida:

En este producto final se requiere crear una función **(isValidCard)** para validar los números de una tarjeta de crédito.

Pasos:
1. La web solicita al cliente que ingrese los números de su tarjeta de crédito por medio de un prompt ().
2. La web devuelve una respuesta en la pantalla por medio de un documet.write ().

### Pseudocódigo

~~~
//Solicitando al usuario su número de tarjeta de crédito
var inputCodeCard = prompt ("Ingrese su número de una tarjeta de crédito")

  //Llamando a la función
  isValidCard (inputCodeCard)

  //Creando función para validar tarjeta
    function isValidCard (codeCard){

    var arrReverse = []; //Creando un array donde se almacenarán los números de la tarjeta en orden inverso

    for (var i = 0; i < codeCard.length; i++){
          arrReverse.unshift(parseInt(codeCard[i]))
    }

    //Obteniendo números en posición par
    for (var j = 1; j <arrReverse.length; j = j+2){

        if (arrReverse[j]*2 >= 10){
            var numberForTwo = arrReverse[j]*2
            //Si el valor de la multiplicación es de dos dígitos: sumar digitos y luego reemplzar en arrReverse
            arrReverse[j] = parseInt(numberForTwo.toString(10)[0]) + parseInt(numberForTwo.toString(10)[1])

        }else{
            //Si el valor de la multiplicación es de un dígito, se reemplaza en arrReverse
            arrReverse[j] = arrReverse[j]*2
        }

    //Sumando los digitos de la tarjeta
    var sum = 0
    for (var k = 0; k < arrReverse.length; k++){
        sum = sum + arrReverse[k]
    }

    }

    //Validando tarjeta
    if (sum % 10 === 0) {
        return document.write ('Tu número de tarjeta es VÁLIDA')
    }else{
        return documet.wirte ('Tu número de tarjeta es INVÁLIDA')
    }

   }

~~~

### Diagrama de flujo

A continuación se detalla en un diagrama de flujo:

[Diagrama Tarjeta Crédito](https://drive.google.com/open?id=0B8fqMV-mBqZgZ3VJSWdhSE1SbHc)
