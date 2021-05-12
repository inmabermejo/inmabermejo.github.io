---
id: 2772
title: 'GTK &#8211; programación visual en Linux con C'
date: 2008-12-24T16:49:53+02:00
author: Chavalina
layout: revision
guid: http://www.chavalina.net/2008/12/24/105-revision-2/
permalink: /2008/12/24/105-revision-2/
---
Vaya temporadita que llevo, no me sale nada para el weblog excepto malas noticias y cancioncitas tontas… supongo que, como dice un amigo mío, uno hace cosas extrañas cuando pasa por momentos extraños. Pero me gustaría volver a hablar un poco de programación, esta vez C bajo linux.

Para todas las prácticas que he tenido que hacer en mi carrera (Ingeniería Técnica Informática) hemos programado "el meollo" dejando a la buena de dios la interfaz del usuario de todos los programas. Realmente es normal que ocurra esto ya que apenas tenemos tiempo para acabar estos ejercicios y siempre hay propuestas algunas "mejoras" que llevan casi el mismo tiempo que la práctica en sí. Pero esta vez hemos tenido suerte y hemos acabado pronto, así que mi compañero y yo decidimos hacer una interfaz gráfica para nuestro programa P2P (con su propio protocolo, olé) y para ello recurrimos al <a href="http://www.gtk.org/" target="_blank">GTK, Gimp Tool Kit</a>. Una serie de librerías que ponen a la disposición del programador de C lo necesario para construir ventanas.

Para poder usarlo hacen falta las librerías de glib, Pango y ATK, todas incluidas en Fedora, y en la mayoría de las distribuciones de linux, así que lo único que necesitamos para ponernos a trabajar es saber cómo<img src="/imagenes/emoticonos/asustado.gif" alt="asustado" width="16" height="16" /> pero no hay problema, porque aquí os dejo yo un enlace con <a href="http://libros.es.gnome.org/guias/gtk_tut_es/" target="_blank">el mejor tutorial</a> que he encontrado hasta ahora, y en español.

Si me va bien la práctica, os enseñaré los resultados.

  * <a href="http://www.gtk.org/" target="_blank">GTK, Gimp Tool Kit</a>
  * <a href="http://libros.es.gnome.org/guias/gtk_tut_es/" target="_blank">GTK Tutorial v1.2 Tony Gale <gale@gtk.org>, Ian Main <imain@gtk.org> </a>