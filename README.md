# Producto Final
## Tarjeta de Crédito Válida:

En este producto final se requiere crear una función **(isValidCard)** para validar los números de una tarjeta de crédito.

Pasos:
1. La web solicita al usuario que ingrese los números de su tarjeta de crédito por medio de un prompt ().
2. La web devuelve una respuesta en la pantalla por medio de un documet.write ().

### Pseudocódigo

~~~
//Solicitando al usuario su número de tarjeta de crédito
Hacer {    
    Obtener número de tarjeta de crédito;
}Mientras (No se obtenga un número);

//Llamando a la función
isValidCard (número de tarjeta de crédito)

//Creando función para validar tarjeta
funcion isValidCard (cuerda){

    Arreglo = []; //Creando un arreglo donde se almacenarán los números de la tarjeta en orden inverso
    Para i = 0 Hasta 'longitud de cuerda'-1 Con Paso i+1 Hacer
          Agregar en el arreglo los números de la cuerda en orden inverso
    Fin Para

    //Obteniendo números en posición par
    Para j = 0 Hasta 'longitud de arreglo'-1 Con Paso j+2 Hacer

      Si NumeroDePosicionPar*2 >= 10 Entonces
        Crear variable que almacena la multiplicación
        //Si el valor de la multiplicación es de dos dígitos: sumar digitos y luego reemplazar en el Arreglo
        Reemplazar en el Arreglo el valor de la suma de los digitos
      Si no Entonces
        //Si el valor de la multiplicación es de un dígito, se reemplaza directamente en el Arreglo
        Reemplazar en el Arreglo el valor de la multiplicación
      Fin Si

      //Sumando los digitos de la tarjeta
      Variable suma = 0
      Para k = 0 Hasta 'longitud de arreglo'-1 Con Paso k+1 Hacer
        suma = suma + 'NumeroDelArreglo en posicion i'
        Fin Para
    Fin Para

    //Validando tarjeta
    Si suma mod 10 = 0 Entonces
      Retorna mensaje: 'Tu número de tarjeta es VÁLIDA'
    Si no Entonces
      Retorna mensaje: "Ingrese su número de tarjeta de crédito"
    Fin Si

Fin Funcion
~~~

### Diagrama de flujo

A continuación se detalla en un diagrama de flujo:

[Diagrama Tarjeta de Crédito](https://drive.google.com/file/d/0B8fqMV-mBqZgWWxzU08zd0tOMXM/view?usp=sharing)
