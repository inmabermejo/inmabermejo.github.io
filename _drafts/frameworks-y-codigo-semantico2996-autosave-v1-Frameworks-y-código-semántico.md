---
id: 3002
title: Frameworks y código semántico
date: 2013-12-04T07:23:00+02:00
author: Chavalina
layout: revision
guid: http://www.chavalina.net/2013/12/04/2996-autosave-v1/
permalink: /2013/12/04/2996-autosave-v1/
---
Esta semana me llegó por Twitter el artículo [Bootstrap without all the debt](https://coderwall.com/p/wixovg). En él se habla de cómo se utiliza [Bootstrap](http://getbootstrap.com/), un framework para programación front-end muy popular, de forma que el HTML queda sometido a las clases CSS y propone una forma alternativa para evitar un HTML caótico, lleno de clases sin significado.

Y lo primero que pensé fue **¿es que esto no es lo usual?**.

Nunca he sido muy amiga de los frameworks para mi desgracia, tienen muchas ventajas pero me parecen _moles_, grandes monstruos generalistas, así que intento coger partes y **quedarme sólo con lo que me interesa** para la producción real.

Y una de las razones es la que mencionan en este artículo: la **deuda** que asumes en el HTML si lo construyes directamente sobre un framework. Por bueno que sea, puedes acabar con código poco semántico, con cosas como `class="span-8"`, que, meses después, cuando alguien tenga que volver a trabajar sobre ese código, no será fácil de comprender de un vistazo. Además de estar vendido si el framework deja de ser actualizado&#8230;

Tras años dando la lata con la importancia del **HTML semántico**, la independencia del contenido y aspecto, CSS Zen garden y demás, no es cuestión de olvidarse de ello tan rápidamente. Porque el HTML semántico son los elementos, pero también las clases, los id, y hasta los comentarios. Y también es importante el **estilo del código**, que sea sencillo, breve y elegante o código que ni tú mismo quieres leer.

Es igual de feo `class="span-2"` que `<bold>`, hace llorar a _[inserte aquí su gurú favorito]_.

Hace un tiempo era complicado, pero ahora con los preprocesadores de CSS (ej. LESS, SAAS) no hay excusa que valga.

Un ejemplo sencillo es una implementación que estoy preparando de iconos con webfonts, manteniendo la independencia de estilos y HTML. Con **una capa adicional de LESS**, en este caso, se puede hacer fácil (y seguro que mejor que yo lo he hecho). No solamente ganas en que el código queda semántico y legible, sino en que luego tienes un sistema de iconos independiente y reutilizable para cualquier elemento.

Primero vemos cómo nos ofrece los iconos de forma genérica un framework, por ejemplo [icomoon](http://icomoon.io/):

<pre class="prettyprint lang-css">@font-face {
     font-family: 'icomoon';
     src:url('fonts/icomoon.eot');
     src:url('fonts/icomoon.eot?#iefix') format('embedded-opentype'),
          url('fonts/icomoon.woff') format('woff'),
          url('fonts/icomoon.ttf') format('truetype'),
          url('fonts/icomoon.svg#icomoon') format('svg');
     font-weight: normal;
     font-style: normal;
}

.icon-tag, .icon-comment {
     speak: none;
     font-style: normal;
     font-weight: normal;
     font-variant: normal;
     text-transform: none;
     line-height: 1;
     -webkit-font-smoothing: antialiased;
}

.icon-tag:before {
     content: "\e00a";
     font-family: 'icomoon';
}

.icon-comment:before {
     content: "\e00b";
     font-family: 'icomoon';
}</pre>

Modificando un poco, con LESS en esta ocasión, podemos hacer que esto sea «extendible» fácilmente. Creamos una clase «tipo icono» `.icon-webfont`, que será extendida por todos los iconos, y éstos serán los que utilizaremos después:

<pre class="prettyprint lang-css">.icon-webfont {
     speak: none;
     font-style: normal;
     font-weight: normal;
     font-variant: normal;
     text-transform: none;
     line-height: 1;
     -webkit-font-smoothing: antialiased;
}
.icon-tag {
.icon-webfont;

     &:before {
     content: "\e00a";
     font-family: 'icomoon';
     }
}
.icon-comment {
.icon-webfont;

     &:before {
     content: "\e00b";
     font-family: 'icomoon';
     }
}
</pre>

Si no hacemos esta modificación, LESS no sería capaz de mostrar correctamente el icono, pues no podría extender lo declarado para `:before`. Pero así podemos usar la misma clase `.icon-comment` previamente declarada, extendida, y modificar o añadir otras propiedades que los diferencien. Por ejemplo, un icono de comentario cuando queramos usar para un ancla a la zona de éstos, y para un botón de acción, para publicarlos:

<pre class="prettyprint lang-css">.comment-shortcut {
.icon-comment;
color:#0ff;
}

button {
.icon-comment;
background:#090;
color:#fff;
padding:5px 10px;
border-radius:4px;
}
</pre>

Aparte de no tener que aparecer clases como `"icon-comment"` directamente en nuestro HTML, tenemos la ventaja de poder reutilizar, centralización para cambios posteriores&#8230; qué os voy a contar que no sepáis.

Igual que con estos iconos, con el resto de cosas. Por ejemplo, clases «tipo» para definir los estilos de la tipografía y luego extenderlos en todo el sitio. Y lo mismo para cualquier otro elemento del diseño.

Os recomiendo el artículo original [Bootstrap without all the debt](https://coderwall.com/p/wixovg), que pone susy, aunque cueste un pequeño esfuerzo, que mantengáis vuestro HTML semántico e independiente.

**Vosotros mismos dentro de un año lo agradeceréis**.