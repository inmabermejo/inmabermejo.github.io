---
id: 1422
title: Transparencias con CSS
date: 2005-01-30T14:27:03+02:00
author: Chavalina
layout: revision
guid: http://www.wp.chavalina.net/2005/01/30/343-revision/
permalink: /2005/01/30/343-revision/
---
<img class="imgizqda" src="http://www.chavalina.net/imagenes/fotos/fondopng.jpg" alt="Ejemplo del uso de png para el fondo de una capa" />Entre ayer y hoy hemos tenido una <acronym title="por llamarlo de alguna manera">discusi&oacute;n</acronym> en la lista de distribuci&oacute;n sobre <acronym title="Cascade Style Sheets">CSS</acronym> <a href="http://ovillo.org/" target="_blank">ovillo</a> que me ha resultado muy productiva para una web que estaba dise&ntilde;ando.

Hasta entonces yo hab&iacute;a usado la t&eacute;cnica que encontr&eacute; en <a href="http://www.simple-d.net/200411/transparencies/" target="_blank">simple-d</a>, se trata simplemente de definir un color de fondo para la capa y luego especificar su opacidad:

<div class="codigo">
  -moz-opacity:0.75;<br /> opacity:0.75;<br /> filter:alpha(opacity=&prime;75&prime;);
</div>

Sin embargo, con esta t&eacute;cnica he observado que los elementos que est&aacute;n dentro del contenedor al que se le aplique autom&aacute;ticamente adoptan tambi&eacute;n esa opacidad (texto, fotos&#8230;), y adem&aacute;s, como dec&iacute;a stripTM en la lista, esto no se ver&aacute; bien en todos los navegadores pues no pertenece a CSS1 o CSS2, proponiendo como alternativa las transparencias PNG.

<a href="http://es.wikipedia.org/wiki/PNG" target="_blank">PNG</a> es un formato para im&aacute;genes que pretende convertirse en est&aacute;ndar para gr&aacute;ficos y sustituir al GIF, y tiene bastantes ventajas, como la que nos interesa, que permite varios niveles de transparencia.

El inconveniente es que el jod&iacute;o <acronym title="Internet Explorer">IE</acronym> (en Windows, seg&uacute;n parece) <a href="http://msdn.microsoft.com/library/default.asp?url=/workshop/author/filter/reference/filters/AlphaImageLoader.asp" target="_blank">no interpreta las transparencias de PNG</a> y cuando quieres usar una imagen de este tipo para conseguir que el fondo de una zona sea semitransparente, lo que consigues es un cuadro opaco y poco est&eacute;tico.

Hay <a href="http://webfx.eae.net/dhtml/pngbehavior/pngbehavior.html" target="_blank">muchos (WebFX)</a> <a href="http://www.alistapart.com/articles/pngopacity/" target="_blank">muchos (A list Apart)</a> <a href="http://redvip.homelinux.net/varios/explorer-png.html" target="_blank">muchos</a> hacks y tutoriales para hacer que <acronym title="Internet Explorer">IE</acronym> _se lo trague_ (vaya, creo que esa frase me reportar&aacute; sendas visitas desde Google&#8230;).

Para el dise&ntilde;o que estoy construyendo ahora mismo el que mejor me ha venido ha sido el que encontr&eacute; en <a href="http://www.daltonlp.com/daltonlp.cgi?item_type=1&#038;item_id=217" target="_blank">daltonlp</a> porque tambi&eacute;n indica c&oacute;mo hacerlo para im&aacute;genes de fondo especificadas en archivos CSS, y la que dan es una soluci&oacute;n muy elegante, porque permite ponerlo todo sin tener que a&ntilde;adir nada al HTML.

Para hacer que el fondo de una capa sea semitransparente creamos una imagen PNG tal y como queramos, en este ejemplo se llama grey.png, y creamos una clase <acronym title="Cascade Style Sheets">CSS</acronym> para estos objetos:

<div class="codigo">
  .transp {<br /> /* Mozilla ignores crazy MS image filters, so it will skip the following */<br /> filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(enabled=true, sizingMethod=scale src=&prime;grey.png&prime;);<br /> }<br /> /* <acronym title="Internet Explorer">IE</acronym> ignores styles with [attributes], so it will skip the following. */<br /> .transp [class] {<br /> background-image:url(&prime;grey.png&prime;);<br /> }
</div>

Y para usarlo simplemente tendremos que hacer una capa y darle esta clase.

Hay que tener en cuenta varias cosas al usar esta t&eacute;cnica:

  * La capa o elemento tiene que tener el atributo «class» para que esto funcione, ya que es el hack que empleamos.
  * La anchura del elemento al que lo vamos a aplicar debe estar definida (ya sea en esa misma clase de otra forma)
  * La imagen a usar cuanto m&aacute;s peque&ntilde;a mejor.

Esto &uacute;ltimo se debe al principal problema de este m&eacute;todo, y es que al usarlo, si la imagen de fondo es grande los enlaces contenidos en el elemento no funcionar&aacute;n.

En <a href="http://www.daltonlp.com/daltonlp.cgi?item_type=1&#038;item_id=217" target="_blank">el art&iacute;culo</a> hay una tabla donde se pueden consultar los tama&ntilde;os de im&aacute;genes de fondo que s&iacute; van bien, y en los comentarios mismos hay otros hacks para este problema, como a&ntilde;adir en la capa el estilo del cursor del rat&oacute;n, o poner a los enlaces posici&oacute;n relativa, pero vamos, yo creo que mejor poner una imagen peque&ntilde;a, nada m&aacute;s que por estilo, porque hacer un fondo semitransparente para que se vea el de la parte de atr&aacute;s, y luego poner otro fondo encima quiz&aacute; resulte algo agresivo.

Aunque esta soluci&oacute;n me gusta porque no es intrusiva, no usa javascript, ni <acronym title="Hypertext PreProcessor">PHP</acronym> ni nada raro, pero **no es una soluci&oacute;n definitiva** porque cuando <acronym title="Internet Explorer">IE</acronym> se decida a solucionar su problema con PNG habr&aacute; que retocar las webs que hayan usado este truco&#8230; ahora vosotros ver&eacute;is si lo us&aacute;is.