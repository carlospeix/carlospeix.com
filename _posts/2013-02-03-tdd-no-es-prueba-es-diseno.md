---
date:   2013-02-03 10:00:00 -0300
title:  "TDD no es prueba, es diseño"
categories: ["Comunidad", "Software"]
tags: ["TDD", "Software Craftmanship"]
---

En una de las últimas sesiones de coaching en la cual ayudé a un equipo a experimentar TDD, escuché una de las reacciones mas usuales ante el primer paso.

Para definir el contexto, imaginen que van a escribir la famosa [kata tenis](http://codingdojo.org/cgi-bin/wiki.pl?KataTennis) y que aun no han escrito absolutamente nada de código. Una de las posibilidades es escribir esta prueba:
<!--more-->

~~~ csharp
[Test]
public void ShouldProvideTheScorerTitle() {
    var scorer = new Scorer("Federer", "Nadal");
    Assert.AreEqual("Federer vs. Nadal", scorer.Title());
}
~~~

Y una de las posibilidades para el código mas simple posible que hace pasar ese test, es:

~~~ csharp
public class Scorer {
    public Scorer(string jugador1, string jugador2) {
    }

    public string Title() {
        return "Federer vs. Nadal";
    }
}
~~~

La reacciones suelen ser:
- ¿Por qué debemos escribir ese código tan tonto ahora?
- ¿Por qué no creamos directamente las variables de instancia para los nombres de los dos jugadores?
- ¿Qué sentido tiene devolver ese texto fijo?
- ¡Esa prueba no tiene sentido!

Mi respuesta usual es:

> No tiene sentido porque **no es una prueba**, es una actividad, un paso, una canal por donde fluye el diseño.

¿Qué tenemos antes de empezar?

Nada concreto, solo una idea de lo que tenemos que hacer y alguna estrategia de diseño que debemos aún desarrollar, **entender**.

Luego del primer paso tenemos:

- el nombre de la clase, 
- decidimos que pasaremos los nombres de los jugadores en el constructor,
- que basta con pasar los nombres como string,
- que usaremos un método para devolver en título
-  y que ese método retornará un string.

> Lo mas importante es que tenemos todas estas decisiones antes de escribir el código de producción, solo habiendo escrito la prueba.

¿No les parece que hemos diseñado mucho en un solo paso como para preocuparnos por detalles de implementación?

Por ejemplo, ¿es razonable que un músico se obligue a escribir música de manera que cada paso tenga sentido en la versión final? Por supuesto que no, empieza a jugar con notas y melodías (a partir de alguna idea) y luego va desarrollando, en forma iterativa la versión final.

A medida que va avanzando entiende mejor como se ajustan todos los bloques, la idea va tomando forma, **va entendiendo que es lo que quiere** la pieza musical.

> Hay otros motivos importantes por los cuales debemos escribir el código mas sencillo posible, pero hay mucho material sobre esos motivos en la red y, en todo caso, puede ser materia de una futura entrada.

Creo un requisito importante para lograr una buena práctica de TDD es entender e incorporar la idea de que no es una técnica de prueba sino una manera de diseñar software.

Nos vemos.
