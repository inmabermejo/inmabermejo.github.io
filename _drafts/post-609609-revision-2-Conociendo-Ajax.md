---
id: 2755
title: Conociendo Ajax
date: 2008-12-24T16:35:16+02:00
author: Chavalina
layout: revision
guid: http://www.chavalina.net/2008/12/24/609-revision-2/
permalink: /2008/12/24/609-revision-2/
---
<img class="imgizqda" src="/imagenes/fotos/ajax.png" alt="Logotipo de Ajax... pero de Ajax Pino" /> Nunca he sido una amante de la programaci&oacute;n en cliente, no me gusta Flash, y tampoco Javascript. Es m&aacute;s, soy tan in&uacute;til que no distingo un **lenght** de un **length** (y as&iacute; acabo luego&#8230;).

Sin embargo, por motivos de trabajo he tenido que programar un chat, y he elegido esta tecnolog&iacute;a debido a que no dispon&iacute;amos de un canal propio de IRC, ni entraba en nuestros planes, ni tampoco soy partidaria de los applets de Java. Para una clase de unos 20 alumnos y un profesor, tampoco merec&iacute;a la pena usar sockets.

La idea de la aplicaci&oacute;n es la siguiente: que la p&aacute;gina pida los nuevos mensajes cada «x» segundos, haga ping para que se mantenga una lista de usuarios activa , que cuando env&iacute;e un mensaje el usuario, lo guarde y adem&aacute;s recoja los nuevos mensajes que pueda haber, y, por supuesto, que sea accesible.

Para conseguir accesibilidad, en lugar de buscar la forma de refrescar la p&aacute;gina de otra forma, simplemente opt&eacute; por a&ntilde;adir un enlace a la propia p&aacute;gina, y un formulario normal y corriente. Pocos son los usuarios que no utilizan Javascript, pero de esta forma, a los que no lo tienen les dejamos control total sobre cu&aacute;ndo quieren recibir mensajes nuevos.

Lo que me preocupa es la carga que pueda generar al servidor todo este tr&aacute;fico, la fase de pruebas ser&aacute; cr&iacute;tica. Ya os contar&eacute;.