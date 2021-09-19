---
date:   2015-07-28 10:00:00 -0300
title:  "Las dos estimaciones"
categories: ["Agilidad organizacional"]
tags: [Estimación]
---

En las últimas semanas tuve la oportunidad de colaborar con un cliente en la adopción de metodologías ágiles en un proyecto corporativo de reemplazo de las aplicaciones centrales del negocio (core).

El equipo del proyecto (unas 60 personas entre desarrolladores, responsables de producto y representantes del negocio) estará trabajando los próximos tres años en la construcción y puesta en producción escalonada (afortunadamente no optaron por un big bang).

Quiero compartirles en esta entrada un aprendizaje respecto de la estimaciones necesarias en este tipo de proyectos.
<!--more-->

> ¿Que pasó desde que escribí esta entrada?  (en el orden en que me llegaron estas noticias)
> 
> - Jason Gorman escribió una entrada  el 1 de Agosto que creo explora ideas similares.
> - El genio de Martín Salías me cuestionó en privado algunas cosillas, luego debatimos un poco y llegamos a la conclusión de que estábamos más o menos de acuerdo y clarificaría algunos puntos.
> - El otro genio de Steve McConnell, que de estimaciones escribió bastante, publica un video el 30 de Julio.
> - Ron Jeffries lo responde al día siguiente, el 31 de Julio con una entrada.
> - Steve McConnell escribe una entrada en su blog, el mismo día.
> - Ron Jeffries responde, a su vez, con otra entrada.

## Primera estimación: la factibilidad

Todo proyecto corporativo del rango de varios millones de dólares está sujeto a muchas decisiones estratégicas de mediano y largo plazo. El dinero no crece en los árboles y el comité ejecutivo debe tomar riesgos, debe decidir donde invierte entre muchas otras opciones igualmente importantes.

Los equipos de tecnología deben comprender y empatizar con estos riesgos si queremos una industria sana, no se trata de dos bandos, de un campo de batalla donde abunda la desconfianza mutua y, por ende, triunfa la baja productividad y el desperdicio de dinero, tiempo y motivación.

En esta etapa, **la estimación** de esfuerzo tiene técnicas y fines específicos, que son los de determinar la factibilidad del proyecto con base en la estimación de plazos y costos. No es extraño en estos casos encontrar fechas de finalización que, a primera vista, parecen arbitrarias.

En uno de los debates en este cliente, intentando acercar la visión del comité ejecutivo a la de los equipos de desarrollo, utilicé dos metáforas.

La primera fue la de la entrega para la temporada de ventas, por ejemplo, Navidad. Hay factores más importante que la estimación de esfuerzo en este caso, el proyecto debe estar terminado para el 15 de Diciembre, dos o tres días mas lo harían inviable.

Otra de las metáforas fue la de construcción de un edificio (¡cuando no este paralelismo!), imaginemos que estamos construyendo un edificio de 20 pisos que tiene fecha límite de inspección, luego de la cual ¡nunca podrá ser aprobado! En este caso, no hay nada más importante que esa fecha, si no termina a tiempo, de nada sirve todo el esfuerzo.

**Resumen:** El objetivo de la estimación en esta etapa es determinar la factibilidad del proyecto. Debemos tomar en cuenta aspectos técnicos, de arquitectura, tiempos de interacción, etc. Dentro de los parámetros de factibilidad es normal llegar a fechas de entrega y a presupuestos exactos e inamovibles, al menos en el comienzo del proyecto.

> ### ¿Son fijos los plazos y presupuestos?
> No debemos olvidar que los proyectos de desarrollo de tecnología en organizaciones que se basan fuertemente en ella son inversión. Lo que puede ser fijo e inamovible ahora, cuando el proyecto comienza (con todos los riesgos) puede ser mas flexible si el proyecto demuestra que los riesgos fueron controlados y el proyecto marcha bien, está en manos del equipo de desarrollo.

## Resto de las estimaciones: el mejor producto posible

Finalmente el proyecto comienza y el equipo tiene tres años por delante para reemplazar un core de negocio, frente a un mar de incertezas y con fecha fija de entrega. Pocas situaciones me parecen más aterrorizantes en el mundo del trabajo, incluso como consultor o coach, donde podría decirse que «lo vemos desde afuera».

En esta etapa las estimaciones tienen otro fin completamente distinto. En esta etapa el foco debe estar en llegar al plazo indicado con el mejor producto posible. Para llegar a ese objetivo el responsable de producto debe priorizar, debe decidir que funcionalidades incluye y cuales no incluye. También debe decidir como se implementan las funcionalidades incluidas.

Para todo esto, el responsable del producto necesita visibilidad del avance del proyecto (para entender que es lo que ya está terminado) y visibilidad de las posibilidades desarrollo futuro. El equipo es responsable de brindar esta información con claridad y transparencia.

Con respecto a las funcionalidades terminadas, no deben requerir ningún tipo de trabajo adicional (ya fue desarrollado, el representante del usuario final lo aprobó, ya tiene el proceso de despliegue automatizado y probado en entornos similares a producción e, idealmente, ya esta en uso en producción). Lo que se dice, terminado-terminado.

Con respecto a las posibilidades de desarrollo futuro, el equipo debe garantizar las prácticas técnicas y de equipo para que la productividad sea sostenible (prueba automatizada, código simple, etc).

Por último, el equipo debe mantener actualizadas las estimaciones de todo lo que resta desarrollar (con nivel de detalle acorde a la posición en el backlog, lo de la cima con detalle, lo de abajo, con poco detalle) de manera que el responsable de producto tenga visibilidad sobre el avance del proyecto según el plan.

En el ejemplo de la construcción del edificio de 20 pisos que mencioné en el apartado anterior, puede implicar que el responsable de proyecto decida que prefiere no terminar uno de los pisos para llegar al plazo, es mejor un edificio con 19 pisos aprobados que uno con 20 pisos que nunca podrán ser habitados (creo que es por este motivo que muchos edificios no tiene piso 13).

**Resumen:** El objetivo de la estimación en esta etapa es brindar información confiable al responsable de producto para priorizar las funcionalidades a incluir (y cuales excluir, sobre todo) en el proyecto, para finalizar con el mejor producto posible.
