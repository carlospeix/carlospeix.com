---
date:   2014-04-01 10:00:00 -0300
title:  "Mis motivaciones con TDD y ATDD"
categories: ["Comunidad", "Software"]
tags: ["TDD", "Software Craftmanship"]
---

Cuando pienso en (A)TDD me vienen a la cabeza dos cosas: **simplicidad y reducción del desperdicio**, dos cosas que son, en mi opinión, dos caras de la misma moneda.

El diseño de software, no importa como se lo mire, es un proceso complejo. El diseño, no importa de que cosa, es un proceso complejo. Nuestro cerebro no es capaz de evaluar todas las variables o grados de libertad en abstracto, como hacen los buenos jugadores de ajedrez tomando en cuenta muchas jugadas hacia adelante.

Es por esto que necesitamos concretar, eliminar grados de libertad, probar ideas.

## ¿Como reduce el desperdicio (A)TDD?

Evitando dedicar tiempo a construir (y probar, depurar, mantener, etc.) cosas que no necesitamos, utilizando el proceso:

1. analizo las necesidades
1. pienso como resolverlas
1. decido como probar lo que construiré, con ejemplos concretos
1. escribo una prueba que falle para el ejemplo mas simple
1. escribo el código mas simple posible que hace pasar la prueba
1. aprovecho oportunidades para mejorar mi código y pruebas

Veo este proceso como una suerte de embudo que me obliga a trabajar solo en lo que necesito, por ejemplo:

- en el paso 5 escribo solo el código necesario para pasar el test
- en el paso 4 escribo la prueba basada en el el ejemplo concreto mas simple sin resolver
- en el paso 3 pienso en ejemplos concretos de lo que quiero lograr (no en «posibles» necesidades abstractas)
- en el paso 2 dedico unos minutos a pensar como resolveré las funcionalidades (no comienzo a programar ciegamente)
- en el paso 1 dedico un tiempo a entender el contexto de lo que debo hacer

Este proceso respeta dos cuestiones transversales muy importantes: se repite en ciclos cortos y la calidad no es opcional (calidad es arquitectura, rendimiento, cumplir con estándares, documentación, etc.)

## ¿La simplicidad?

Encuentro la simplicidad en los mismos puntos anteriores pues no construyo nada que no sea necesario por un paso en el proceso que mencioné antes, sumando al combo al refactoring, esa simplificación de mis artefactos que me permita no solo sostener y mejorar el ritmo de trabajo a lo largo del proyecto.

¡Nos vemos!
