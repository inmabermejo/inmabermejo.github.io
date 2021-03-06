---
id: 1425
title: Selector de estilos en PHP
date: 2005-01-09T06:19:43+02:00
author: Chavalina
layout: revision
guid: http://www.wp.chavalina.net/2005/01/09/318-revision/
permalink: /2005/01/09/318-revision/
---
Desde que puse varias hojas de estilo para elegir en el blog noté que iba más lento, bueno, con mi conexión se nota especialmente![emo](/imagenes/emoticonos/triste.gif) sin embargo, no había mucha más carga gráfica que en otras ocasiones.

El problema es que se tienen que cargar las cuatro hojas de estilo al recibir la página. Y esto además hace que al elegir otro estilo con el selector a veces haya que recargar la página para que se vean todas las imágenes. Para evitar esto y hacer que la página sea menos pesada, he cambiado el <a href="http://www.alistapart.com/articles/alternate/" target="_blank">selector de estilos</a> de A List Apart, basado en JavaScript, por uno similar pero en PHP.

Veamos cómo funciona.  
En los elementos del menú de la izquierda que seleccionan el estilo antes teníamos una llamada a una función de javascript como se describe en <a href="http://www.alistapart.com/articles/alternate/" target="_blank">el artículo</a>, ahora simplemente hay un enlace a un script, que será el encargado de hacer el cambio, pasándole un parámetro (mediante el método GET) que indica la hoja de estilo elegida: 

<div class="codigo">
  <a href="styleswitcher.php?estilo=4-7" title="estilo 4.7">
</div>

Hay que tener cuidado con los nombres que se ponen a estos parámetros, mejor no usar caracteres «raros».

Este script, llamado styleswitcher.php, simplemente recoge ese parámetro y la página desde la que se ha llegado, para luego volver a ella y que el usuario no se desconcierte, envía una cookie para recordar el estilo elegido, y vuelve a la página desde la que se llegó:

<div class="codigo">
  <?<br /> $referencia = getenv(«HTTP_REFERER»);<br /> $estilo=$HTTP_GET_VARS[′estilo′];<br /> setcookie(«chnet_estilo»,$estilo);<br /> ?><br /> <html><br /> <head><br /> <title>modificando estilo</title> <br /> </head><br /> <body onLoad = "parent.location = ′<? echo $referencia; ?>′"><br /> </body><br /> </html>
</div>

Ahora hemos vuelto a la página en la que estábamos, y sólo queda cambiar el estilo por el nuevo.  
Para ello, lo primero recogemos la cookie recién establecida, y tenemos cuidado de seleccionar un estilo predeterminado por si no hubiera cookie:

<div class="codigo">
  <?<br /> $estilo=$HTTP_COOKIE_VARS[«chnet_estilo»];<br /> if(!isset($estilo)){<br /> $estilo=»7″;<br /> }<br /> ?>
</div>

A diferencia del método mencionado en A List Apart, en este caso sólo nos hará falta definir una hoja de estilo, que se elegirá con la variable $estilo que acabamos de crear:

<div class="codigo">
  <link rel="stylesheet" href="<? echo $estilo; ?>.css" type="text/css" />
</div>

y de esta manera, ahorraremos que se carguen el resto de las hojas, que en mi caso eran cuatro, a 4 ó 5kb cada una, pues casi 20kb menos de página.

Otra ventaja de esto es que también funciona en navegadores que no permitan el uso de JavaScript, y también que, en teoría, al hacer la petición con el nuevo estilo al servidor, las imágenes cargarán desde el principio, a diferencia de antes, que a veces (yo) tenía que recargar la página para que bajaran todas.

El inconveniente de esto es que se hace de lado del servidor, con lo que hay que hacer dos peticiones más, una a styleswitcher.php y otra a la misma página que estábamos viendo, con lo que se genera tráfico «innecesario». Sin embargo, como uno no está cambiando de estilo cada vez (seguramente nadie lo usará![emo](/imagenes/emoticonos/triste.gif) ) y en cada página me ahorro 20kb, creo que merece la pena, así podré incluir todos los diseños que me apetezca sin hacer que la página acabe siendo más pesada que yo jejeje.

Además si estábamos en alguna zona concreta del documento (#referencias, #comentarios en mi caso) no vuelve ahí. Esto tengo que buscarme alguna maña para conseguirlo.

Me gustaría que si veis otra forma más sencilla de hacer esto me lo digáis, que nunca está de más![emo](/imagenes/emoticonos/guino.gif) 

Sin embargo, mi index.php sigue siendo demasiado pesado.  
Pensé en «cortar» los artículos menos actuales (por ejemplo, los cinco más antiguos) de la portada dejando solo unas líneas a modo de resumen, pero no sé si es cómodo tener que hacer otro click para leer el artículo, a mi no me gusta mucho pero… ¿vosotros qué pensáis?