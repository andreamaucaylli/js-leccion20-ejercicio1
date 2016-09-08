# EJERCICIO 1: Usando Closures

Modificar el siguiente script para que muestre el resultado correcto:

```
var num2 = 0;

function suma(num1) {
	return function() {
		return num1 + num2;
	}
} 

var suma2 = suma(2);
console.log(suma2(5)); // Debería mostrar 7 de resultado

var suma12 = suma(12);
console.log(suma12(76)) // Debería mostrar 88 de resultado.
```


-En la primera imagen se observa que se declara una variable num2 inicializada en 0 así tenemos: num2 = 0; y que tenemos una función aninadada anónima que no presenta ningún parámetro. Al ejecutarse la función el interprte irá en busca de la variable para ejecutar el return que es otra función que tiene 2 variables: num1 y num2, por lo qu irá e busca de dichas variables, siendo num1 un parámetro ya dado pero num2 no aparece en el contexto local de la función por lo que el intérprete tomará la variable global num2 con el valor asinado de 0.
Al ejercutarse entonces el resultado será 2, ya que 2 más 0 igual 2, lo mismo en el segundo console.log: 12 más 0 igual 12.

![codigo sin editar](http://i63.tinypic.com/2qv741w.jpg)

-En la segunda imagen partiendo del análisis anterior lo primero qu debemos hacer es eliminar la variable global num2 asignada con el valor 0 y escribir la variable num2 como parámetro en la función anónima, así al ejecutar obtendremos el resultado deseado.

![codigo editdo](http://i64.tinypic.com/ncij46.jpg)
