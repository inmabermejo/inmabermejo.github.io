---
id: 1412
title: Conociendo Ajax
date: 2006-01-12T15:40:02+02:00
author: Chavalina
layout: revision
guid: http://www.wp.chavalina.net/2006/01/12/609-revision/
permalink: /2006/01/12/609-revision/
---
<img class="imgizqda" src="/imagenes/fotos/ajax.png" alt="Logotipo de Ajax... pero de Ajax Pino" /> Nunca he sido una amante de la programación en cliente, no me gusta Flash, y tampoco Javascript. Es más, soy tan inútil que no distingo un **lenght** de un **length** (y así acabo luego…).

Sin embargo, por motivos de trabajo he tenido que programar un chat, y he elegido esta tecnología debido a que no disponíamos de un canal propio de IRC, ni entraba en nuestros planes, ni tampoco soy partidaria de los applets de Java. Para una clase de unos 20 alumnos y un profesor, tampoco merecía la pena usar sockets.

La idea de la aplicación es la siguiente: que la página pida los nuevos mensajes cada «x» segundos, haga ping para que se mantenga una lista de usuarios activa , que cuando envíe un mensaje el usuario, lo guarde y además recoja los nuevos mensajes que pueda haber, y, por supuesto, que sea accesible.

Para conseguir accesibilidad, en lugar de buscar la forma de refrescar la página de otra forma, simplemente opté por añadir un enlace a la propia página, y un formulario normal y corriente. Pocos son los usuarios que no utilizan Javascript, pero de esta forma, a los que no lo tienen les dejamos control total sobre cuándo quieren recibir mensajes nuevos.

Lo que me preocupa es la carga que pueda generar al servidor todo este tráfico, la fase de pruebas será crítica. Ya os contaré.