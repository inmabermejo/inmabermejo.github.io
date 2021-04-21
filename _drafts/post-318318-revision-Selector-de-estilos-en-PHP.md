---
id: 1425
title: Selector de estilos en PHP
date: 2005-01-09T06:19:43+02:00
author: Chavalina
layout: revision
guid: http://www.wp.chavalina.net/2005/01/09/318-revision/
permalink: /2005/01/09/318-revision/
---
Desde que puse varias hojas de estilo para elegir en el blog not&eacute; que iba m&aacute;s lento, bueno, con mi conexi&oacute;n se nota especialmente![emo](/imagenes/emoticonos/triste.gif) sin embargo, no hab&iacute;a mucha m&aacute;s carga gr&aacute;fica que en otras ocasiones.

El problema es que se tienen que cargar las cuatro hojas de estilo al recibir la p&aacute;gina. Y esto adem&aacute;s hace que al elegir otro estilo con el selector a veces haya que recargar la p&aacute;gina para que se vean todas las im&aacute;genes. Para evitar esto y hacer que la p&aacute;gina sea menos pesada, he cambiado el <a href="http://www.alistapart.com/articles/alternate/" target="_blank">selector de estilos</a> de A List Apart, basado en JavaScript, por uno similar pero en PHP.

Veamos c&oacute;mo funciona.  
En los elementos del men&uacute; de la izquierda que seleccionan el estilo antes ten&iacute;amos una llamada a una funci&oacute;n de javascript como se describe en <a href="http://www.alistapart.com/articles/alternate/" target="_blank">el art&iacute;culo</a>, ahora simplemente hay un enlace a un script, que ser&aacute; el encargado de hacer el cambio, pas&aacute;ndole un par&aacute;metro (mediante el m&eacute;todo GET) que indica la hoja de estilo elegida: 

<div class="codigo">
  <a href="styleswitcher.php?estilo=4-7" title="estilo 4.7">
</div>

Hay que tener cuidado con los nombres que se ponen a estos par&aacute;metros, mejor no usar caracteres «raros».

Este script, llamado styleswitcher.php, simplemente recoge ese par&aacute;metro y la p&aacute;gina desde la que se ha llegado, para luego volver a ella y que el usuario no se desconcierte, env&iacute;a una cookie para recordar el estilo elegido, y vuelve a la p&aacute;gina desde la que se lleg&oacute;:

<div class="codigo">
  <?<br /> $referencia = getenv(«HTTP_REFERER»);<br /> $estilo=$HTTP_GET_VARS[&prime;estilo&prime;];<br /> setcookie(«chnet_estilo»,$estilo);<br /> ?><br /> <html><br /> <head><br /> <title>modificando estilo</title> <br /> </head><br /> <body onLoad = "parent.location = &prime;<? echo $referencia; ?>&prime;"><br /> </body><br /> </html>
</div>

Ahora hemos vuelto a la p&aacute;gina en la que est&aacute;bamos, y s&oacute;lo queda cambiar el estilo por el nuevo.  
Para ello, lo primero recogemos la cookie reci&eacute;n establecida, y tenemos cuidado de seleccionar un estilo predeterminado por si no hubiera cookie:

<div class="codigo">
  <?<br /> $estilo=$HTTP_COOKIE_VARS[«chnet_estilo»];<br /> if(!isset($estilo)){<br /> $estilo=»7&#8243;;<br /> }<br /> ?>
</div>

A diferencia del m&eacute;todo mencionado en A List Apart, en este caso s&oacute;lo nos har&aacute; falta definir una hoja de estilo, que se elegir&aacute; con la variable $estilo que acabamos de crear:

<div class="codigo">
  <link rel="stylesheet" href="<? echo $estilo; ?>.css" type="text/css" />
</div>

y de esta manera, ahorraremos que se carguen el resto de las hojas, que en mi caso eran cuatro, a 4 &oacute; 5kb cada una, pues casi 20kb menos de p&aacute;gina.

Otra ventaja de esto es que tambi&eacute;n funciona en navegadores que no permitan el uso de JavaScript, y tambi&eacute;n que, en teor&iacute;a, al hacer la petici&oacute;n con el nuevo estilo al servidor, las im&aacute;genes cargar&aacute;n desde el principio, a diferencia de antes, que a veces (yo) ten&iacute;a que recargar la p&aacute;gina para que bajaran todas.

El inconveniente de esto es que se hace de lado del servidor, con lo que hay que hacer dos peticiones m&aacute;s, una a styleswitcher.php y otra a la misma p&aacute;gina que est&aacute;bamos viendo, con lo que se genera tr&aacute;fico «innecesario». Sin embargo, como uno no est&aacute; cambiando de estilo cada vez (seguramente nadie lo usar&aacute;![emo](/imagenes/emoticonos/triste.gif) ) y en cada p&aacute;gina me ahorro 20kb, creo que merece la pena, as&iacute; podr&eacute; incluir todos los dise&ntilde;os que me apetezca sin hacer que la p&aacute;gina acabe siendo m&aacute;s pesada que yo jejeje.

Adem&aacute;s si est&aacute;bamos en alguna zona concreta del documento (#referencias, #comentarios en mi caso) no vuelve ah&iacute;. Esto tengo que buscarme alguna ma&ntilde;a para conseguirlo.

Me gustar&iacute;a que si veis otra forma m&aacute;s sencilla de hacer esto me lo dig&aacute;is, que nunca est&aacute; de m&aacute;s![emo](/imagenes/emoticonos/guino.gif) 

Sin embargo, mi index.php sigue siendo demasiado pesado.  
Pens&eacute; en «cortar» los art&iacute;culos menos actuales (por ejemplo, los cinco m&aacute;s antiguos) de la portada dejando solo unas l&iacute;neas a modo de resumen, pero no s&eacute; si es c&oacute;modo tener que hacer otro click para leer el art&iacute;culo, a mi no me gusta mucho pero&#8230; &iquest;vosotros qu&eacute; pens&aacute;is?