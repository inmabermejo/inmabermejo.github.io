---
id: 1428
title: 'GTK &#8211; programaci&oacute;n visual en Linux con C'
date: 2004-05-02T08:44:19+02:00
author: Chavalina
layout: revision
guid: http://www.wp.chavalina.net/2004/05/02/105-revision/
permalink: /2004/05/02/105-revision/
---
Vaya temporadita que llevo, no me sale nada para el weblog excepto malas noticias y cancioncitas tontas&#8230; supongo que, como dice un amigo m&iacute;o, uno hace cosas extra&ntilde;as cuando pasa por momentos extra&ntilde;os. Pero me gustar&iacute;a volver a hablar un poco de programaci&oacute;n, esta vez C bajo linux.

Para todas las pr&aacute;cticas que he tenido que hacer en mi carrera (Ingenier&iacute;a T&eacute;cnica Inform&aacute;tica) hemos programado "el meollo" dejando a la buena de dios la interfaz del usuario de todos los programas. Realmente es normal que ocurra esto ya que apenas tenemos tiempo para acabar estos ejercicios y siempre hay propuestas algunas "mejoras" que llevan casi el mismo tiempo que la pr&aacute;ctica en s&iacute;. Pero esta vez hemos tenido suerte y hemos acabado pronto, as&iacute; que mi compa&ntilde;ero y yo decidimos hacer una interfaz gr&aacute;fica para nuestro programa P2P (con su propio protocolo, ol&eacute;) y para ello recurrimos al <a href="http://www.gtk.org/" target="_blank">GTK, Gimp Tool Kit</a>. Una serie de librer&iacute;as que ponen a la disposici&oacute;n del programador de C lo necesario para construir ventanas.

Para poder usarlo hacen falta las librer&iacute;as de glib, Pango y ATK, todas incluidas en Fedora, y en la mayor&iacute;a de las distribuciones de linux, as&iacute; que lo &uacute;nico que necesitamos para ponernos a trabajar es saber c&oacute;mo<img src="/imagenes/emoticonos/asustado.gif" alt="asustado" width="16" height="16" /> pero no hay problema, porque aqu&iacute; os dejo yo un enlace con <a href="http://libros.es.gnome.org/guias/gtk_tut_es/" target="_blank">el mejor tutorial</a> que he encontrado hasta ahora, y en espa&ntilde;ol.

Si me va bien la pr&aacute;ctica, os ense&ntilde;ar&eacute; los resultados.

  * <a href="http://www.gtk.org/" target="_blank">GTK, Gimp Tool Kit</a>
  * <a href="http://libros.es.gnome.org/guias/gtk_tut_es/" target="_blank">GTK Tutorial v1.2 Tony Gale <gale@gtk.org>, Ian Main <imain@gtk.org> </a>