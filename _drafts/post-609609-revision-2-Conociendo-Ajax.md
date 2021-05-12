---
id: 2755
title: Conociendo Ajax
date: 2008-12-24T16:35:16+02:00
author: Chavalina
layout: revision
guid: http://www.chavalina.net/2008/12/24/609-revision-2/
permalink: /2008/12/24/609-revision-2/
---
<img class="imgizqda" src="/imagenes/fotos/ajax.png" alt="Logotipo de Ajax... pero de Ajax Pino" /> Nunca he sido una amante de la programación en cliente, no me gusta Flash, y tampoco Javascript. Es más, soy tan inútil que no distingo un **lenght** de un **length** (y así acabo luego…).

Sin embargo, por motivos de trabajo he tenido que programar un chat, y he elegido esta tecnología debido a que no disponíamos de un canal propio de IRC, ni entraba en nuestros planes, ni tampoco soy partidaria de los applets de Java. Para una clase de unos 20 alumnos y un profesor, tampoco merecía la pena usar sockets.

La idea de la aplicación es la siguiente: que la página pida los nuevos mensajes cada «x» segundos, haga ping para que se mantenga una lista de usuarios activa , que cuando envíe un mensaje el usuario, lo guarde y además recoja los nuevos mensajes que pueda haber, y, por supuesto, que sea accesible.

Para conseguir accesibilidad, en lugar de buscar la forma de refrescar la página de otra forma, simplemente opté por a&ntilde;adir un enlace a la propia página, y un formulario normal y corriente. Pocos son los usuarios que no utilizan Javascript, pero de esta forma, a los que no lo tienen les dejamos control total sobre cuándo quieren recibir mensajes nuevos.

Lo que me preocupa es la carga que pueda generar al servidor todo este tráfico, la fase de pruebas será crítica. Ya os contaré.