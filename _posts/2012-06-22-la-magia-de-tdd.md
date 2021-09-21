---
date:   2012-06-22 10:00:00 -0300
title:  "La magia de TDD"
categories: ["Comunidad", "Software"]
tags: ["TDD", "Software Craftmanship"]
---

Nos encontrábamos ayer en las oficinas de [Kleer](http://www.kleer.la/), en un Yoseki Codig Dojo, exclusivo para un equipo de un cliente, trabajando con la [Kata CheckOut](http://codekata.pragprog.com/2007/01/kata_nine_back_.html).

Quiero contarles solo 3 minutos donde se notan las ventajas de diseñar nuestro código a partir del ejemplo.
<!--more-->

Trabajamos en Java con Eclipse pues este es el entorno de desarrollo en el cual el equipo trabaja. Les presento el código al comienzo de los 3 minutos mágicos:

~~~ java
int cantA = 0, cantB = 0, cantC = 0, cantD = 0;
for(String producto: productos.split(","))
{
    if (producto.equals("A"))
        cantA++;
    else if (producto.equals("B"))
        cantB++;
    else if (producto.equals("C"))
        cantC++;
    else if (producto.equals("D"))
        cantD++;
}
return cantA*50 + cantB*30 + cantC*20 + cantD*15;
~~~

Decidimos, en ese momento, eliminar la duplicación de lógica (en la declaración de variables y en la cadena de ifs). Entonces, quien estaba al teclado dijo:

> “Podemos hacer una método para encapsular la lógica…” a lo cual yo respondí: “¡Adelante!”. Entonces esta persona escribió:

~~~ java
private ...
~~~

... y sobrevino una larga pausa, luego un debate.

El problema es que hay mucho que decidir si vamos por ese camino: ¿Cuál es el tipo que retorna ese método? ¿Cuál debería ser su nombre? ¿Qué parámetros debe recibir? y, sobre todo, ¿Qué debe hacer?.

Luego de dar tiempo al debate, sugerí eliminar esa línea de código y escribir lo siguiente:

~~~ java
return getCantA(productos)*50 + cantB*30 + cantC*20 + cantC*15;
~~~

Noten que reemplace la variable cantA por el llamado al método getCantA(…), aun inexistente.

En ese momento quedaron muy claras las respuestas a las preguntas: el método debe devolver un entero, su nombre ya esta definido y debe sumar la cantidad de productos de tipo A. En 15 segundos quedo escrito lo siguiente:

~~~ java
private int getCantA(String productos)
{
    int cant = 0;
    for(String producto: productos.split(","))
    {
        if (producto.equals("A"))
            cant++;
    }
    return cant;
}
~~~

Y las pruebas unitarias pasaron y el pequeño paso en el refactoring fue exitoso.

A esto me refiero con la magia de TDD. Es muy difícil diseñar el método “desde adentro”. Es mucho mas fácil y efectivo diseñarlo “desde afuera”, es decir, desde el lugar donde lo necesitamos.

Para aquellos que estén preocupados por el final de la historia (o de este refactoring), les cuento que el último paso dejó el código en estas condiciones:

~~~ java
private int price(String productos)
{
    return getCant(productos, "A")*50 + 
           getCant(productos, "B")*30 + 
           getCant(productos, "C")*20 + 
           getCant(productos, "D")*15;
}
private int getCant(String productos, String codProducto)
{
    int cant=0;
    for(String letra : productos.split(","))
    {
        if(letra.equals(codProducto))
            cant++;
    }
    return cant;
}
~~~

Luego siguieron otros refactorings, por supuesto, pero eso fue luego de los 3 minutos mágicos, así que termino esta entrada aquí.

Si alguno de ustedes quiere experimentar algo parecido, no dejen de organizar coding dojos en sus lugares de trabajo, un lunes por la mañana, un viernes por la tarde, cuando sea.

Si no se sienten seguros para comenzar, participen de un Yoseki Codig Dojo en Kleer, los organizamos mensualmente en Buenos Aires, en Lima, y en otras ciudades. Y son gratuitos.
