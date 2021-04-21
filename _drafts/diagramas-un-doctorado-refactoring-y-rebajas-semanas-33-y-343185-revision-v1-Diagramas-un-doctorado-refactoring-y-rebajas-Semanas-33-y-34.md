---
id: 3190
title: 'Diagramas, un doctorado, refactoring y rebajas! Semanas #33 y #34'
date: 2014-07-12T09:57:46+02:00
author: Chavalina
layout: revision
guid: http://www.chavalina.net/2014/07/12/3185-revision-v1/
permalink: /2014/07/12/3185-revision-v1/
---
De nuevo voy a contar dos semanas en una, mi disculpa: _estaba de shopping_ 🙂



Mi debilidad, **las rebajas**, compras por internet a horas intempestivas, pero también una **actividad familiar** que ya es tradición ir con mi hermana y mi madre. Tan buena para nosotras como ir al cine o de cañas, o incluso mejor, me atrevo a decir. Lo malo es que sufrimos _bulimia de compras_, término acuñado por Suso Lahuerta para describir la forma de comprar típica de mi madre.

Pero no toda la actividad familiar fue tan superficial, ya que este jueves acompañamos a mi hermana en la **lectura de su tesis doctoral** en Filosofía: _El problema de la interpretación en el arte: intención y significado_. 

Una presentación impecable, un saber estar en la tarima y la forma de responder a las preguntas, con naturalidad pero contundencia, un dominio del inglés hablado que para mi quisiera la mitad, y, sobre todo, valentía al elegir un tema actual, desarrollado por filósofos contemporáneos y generando contenido original. Enhorabuena Ali!



En el trabajo, han sido dos semanas muy diferentes. La primera, dedicada a cerrar frentes, como el **proyecto largamente retrasado**, revisión, ayudar a la implementación de los **snippets** de código en el panel de edición, hacer algunos prototipos para implementar la votación de comentarios en nuestras versiones móviles, y dar soporte a algunos compañeros de servicios a empresas, que han tenido mucho trabajo estos días y necesitaban un poco de ayuda.

También empecé una tarea que llevaba tiempo pendiente: **refactorizar** el CSS de nuestra capa de visualización. Decir que el código no estaba optimizado es ser muy amable: tras tres versiones de diseño y dos del backend completamente diferentes que tuvieron que convivir durante un tiempo, con las versiones para tablet y móvil que desarrollamos en base a un framework genérico (Twitter Bootstrap), y haber introducido LESS en medio de todo este proceso, la cosa está de _mírame y no me toques_.

Así que, como la arquitectura está muy definida en este momento, he empezado a **hacer limpieza y a crear módulos reutilizables** pero extensibles, para, por ejemplo, tener una definición base de botones, y luego sólo tener que ajustar las mínimas propiedades necesarias para adaptarlo a móviles o tablets (ej. tamaño del área pulsable, o del texto), todo a través de LESS. Así tendremos un código más sencillo, modular, con menos sitio para errores, y más fácil de mantener.

Botones, iconos, formularios, colores&#8230; es lo básico que he abordado esta emana, pero aun queda la mayor parte, que seguiré haciendo poco a poco. Después además quiero construir una **guía del estilo** de la de [Mapbox](https://www.mapbox.com/base/styling/components/) o [Heroku](http://sfdc-styleguide.herokuapp.com/) que permita a front-ends y desarrolladores usar los componentes fácilmente, y respetando el estilo.

También he empezado a preparar una escala tipográfica nueva, que no será tan sencilla de incorporar en esta refactorización como el resto de componentes. Necesita mucho más trabajo de diseño previo, pero es necesario también.

<blockquote class="twitter-tweet" lang="en">
  <p>
    <a href="https://twitter.com/hashtag/lecturadeverano?src=hash">#lecturadeverano</a> Qué potra, pillé el Design for the real world por 11€ y ahora cuesta el doble <a href="http://t.co/3rR7ih2KyU">http://t.co/3rR7ih2KyU</a> <a href="http://t.co/C8mnLWSgcY">pic.twitter.com/C8mnLWSgcY</a>
  </p>
  
  <p>
    &mdash; chavalina (@chavalina) <a href="https://twitter.com/chavalina/statuses/485361824750374912">July 5, 2014</a>
  </p>
</blockquote>



Y la siguiente semana ha venido marcada por una nueva tarea que me han pedido para el panel de edición, relacionada con la **visualización de datos**. 

En este tema estoy bastante verde, así que lo primero que hice fue dejar [mi lectura de verano](http://www.amazon.es/gp/product/0500273588/ref=as_li_ss_tl?ie=UTF8&camp=3626&creative=24822&creativeASIN=0500273588&linkCode=as2&tag=chavadiari-21) y coger un libro que tenía pendiente desde hace tiempo, [Digital Diagrams](http://www.amazon.es/gp/product/0823015726/ref=as_li_ss_tl?ie=UTF8&camp=3626&creative=24822&creativeASIN=0823015726&linkCode=as2&tag=chavadiari-21) (uno de los [recomendados por el profesor Cañada](http://www.vostokstudio.com/blog/2011/01/the-26-books-that-made-me-an-interaction-designer/)), que por ahora me parece bastante básico, y con muchísimos ejemplos, lo que me viene de perlas, y buscando un poco más, di con [Now You See It: Simple Visualization Techniques for Quantitative Analysis](http://www.amazon.es/gp/product/0970601980/ref=as_li_ss_tl?ie=UTF8&camp=3626&creative=24822&creativeASIN=0970601980&linkCode=as2&tag=chavadiari-21), que [Yusef Hassan ha recomendado alguna vez en su blog](http://www.human-computer.net/blog/), que _me he pasado_ esta semana. Tengo que buscar alguna referencia más de este libro, a ver si voy a por él o no.

Con todo esto, y repasando los [principios de la Gestalt](http://es.wikipedia.org/wiki/Psicolog%C3%ADa_de_la_Gestalt) y la teoría de diseño de información que aprendí el año pasado, espero poder hacer un buen trabajo. Estoy un poco nerviosilla con esto.

Por último, acabamos la semana con una **reunión de departamento**. Normalmente las hacíamos entre dos compañeros, sin periodicidad, y dábamos reporte de actividad al resto del equipo, pero ahora hemos cambiado el método y vamos a mantener un documento con el estado de los proyectos, de forma que quien quiera pueda consultarlo en cualquier momento y tener una visión global de los avances. Y cada dos semanas, reunión _de departamento_ para contarnos entre nosotros. 

A ver si esta manera, sencilla pero **más metódica** que lo anterior, nos permite mejorar nuestra comunicación y visibilidad, ya que tenemos un problema grave con esto: los otros departamentos no tienen conocimiento de la mitad de o que hacemos.

Y ahora, **a darme un remojón!**