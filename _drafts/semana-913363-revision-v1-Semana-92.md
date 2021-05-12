---
id: 3369
title: 'Semana #92'
date: 2015-09-02T22:33:08+02:00
author: Chavalina
layout: revision
guid: http://www.chavalina.net/2015/09/02/3363-revision-v1/
permalink: /2015/09/02/3363-revision-v1/
---
Hace noche para sacar la hamaca a la terraza y quedarse durmiendo al fresco. Hay que aprovechar.

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="4" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);">
  <div style="padding:8px;">
    <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;">
      <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAAGFBMVEUiIiI9PT0eHh4gIB4hIBkcHBwcHBwcHBydr+JQAAAACHRSTlMABA4YHyQsM5jtaMwAAADfSURBVDjL7ZVBEgMhCAQBAf//42xcNbpAqakcM0ftUmFAAIBE81IqBJdS3lS6zs3bIpB9WED3YYXFPmHRfT8sgyrCP1x8uEUxLMzNWElFOYCV6mHWWwMzdPEKHlhLw7NWJqkHc4uIZphavDzA2JPzUDsBZziNae2S6owH8xPmX8G7zzgKEOPUoYHvGz1TBCxMkd3kwNVbU0gKHkx+iZILf77IofhrY1nYFnB/lQPb79drWOyJVa/DAvg9B/rLB4cC+Nqgdz/TvBbBnr6GBReqn/nRmDgaQEej7WhonozjF+Y2I/fZou/qAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;">
      </div>
    </div>
    
    <p style=" margin:8px 0 0 0; padding:0 4px;">
      <a href="https://instagram.com/p/68WaPrtsjG/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_top">??</a>
    </p>
    
    <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">
      A photo posted by Inma Bermejo (@inmabermejosalar) on <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2015-08-28T21:58:08+00:00">Aug 28, 2015 at 2:58pm PDT</time>
    </p>
  </div>
</blockquote>



Y también los días que se pueda **ir a la playa**, que ya son contados. Aunque me he propuesto secretamente ir todos los fines de semana mientras sea verano, sin poder conducir, lo tengo crudo. Ayer tuve suerte y de nuevo acabamos en La Manga con mi madre y mi hermana, uno de nuestros _viajes con las Salar_.

Algunas medusas y muchísimo oleaje, que no impidieron que apenas saliéramos del agua -salvo para el aperitivo y la merienda-, pero que me dejaron K.O. incluso hasta hoy. ¿Tener resaca de nadar? ¿Será esto la edad?

Mi **proyecto personal analógico** está parado pero tengo claros los siguientes pasos, y también que necesitaré ayuda, porque de contactos en esos temas estoy a cero.

Y de mi **proyecto personal digital** he dado un pasito más, y y tengo ya a mi _socia_ de motivación hasta arriba para empezar a crear contenidos.

Tras terminar _Viaje al centro de la tierra_, y recuperar el gusanillo por ir a [Islandia](https://www.google.com/maps/place/Sn%C3%A6fellsj%C3%B6kull,+Islandia/@64.7999732,-23.783333,99217m/data=!3m1!1e3!4m2!3m1!1s0x492a8685179e96c3:0x178e44c84748be97), ahora retomo _Matar a un ruiseñor_. Ya lo empecé en marzo y no lo acabé, pero ahora que he encontrado momentos para la lectura tendré más adherencia. Y también porque me han prestado [el nuevo libro de Harper Lee](http://www.amazon.es/gp/product/B00UFA8N40/ref=as_li_ss_tl?ie=UTF8&camp=3626&creative=24822&creativeASIN=B00UFA8N40&linkCode=as2&tag=chavadiari-21) y quiero acabar el otro antes.

En el trabajo, sigo repartiendo mi tiempo entre el **front-end de nuestra nueva versión responsive**, y el proyecto W. Esta semana, mucho arreglo de bugs y crear plantillas para el tipo de post [_slideshow_](http://www.trendencias.com/tendencias/el-ante-planea-su-invasion-y-estos-11-looks-te-ayudaran-a-saber-como-lucirlo) y para los [espacios de contenidos](http://www.decoesfera.com/planesdeverano) que las marcas tienen en nuestros sitios.

En esto, tengo la problemática de automatizar la elección del color de texto para que sea «legible» sobre los colores que se personalizan para algunos elementos, como las cabeceras, _disclaimers_… pues no quiero añadir complejidad al código que usan mis compañeros para preparar estas personalizaciones.

Así que empiezo a investigar, sin mucha fé, pues no esperaba encontrar algo para LESS, y me encuentro algo para [calcular automáticamente un color con contraste adecuado con SASS](http://thesassway.com/intermediate/dynamically-change-text-color-based-on-its-background-with-sass). Por suerte sigo buscando, y veo que alguien ha encontrado [algo similar para LESS](http://stackoverflow.com/questions/8036580/using-less-jquery-to-switch-body-text-color-dependent-on-background-color) usando «ifs», o _guardas_. esto nos va a solucionar bastantes casos.

Y en esa búsqueda, doy con un interesante artículo sobre [qué función de contraste de color es más conveniente](https://24ways.org/2010/calculating-color-contrast/) usar para buscar el color del texto según un fondo dado. Y, casualmente, de Brian Suda, de Analog.is. Qué pequeño es el _internet_.

Para el **proyecto W** tuve varias sesiones de chat con los compañeros de desarrollo para ver cuáles eran las dificultades con las que se habían encontrado hasta ahora (yo me acabo de incorporar) y cómo podía ayudar.

Y con mi jefe convocamos una reunión para el viernes discutirlo todo. Yo tan tranquila… no pensé que esa reunión incluiría a nuestro equipo de desarrollo de India y que sería una videoconferencia **en inglés**. Lo que me acordé entonces de mi amiga Carmen y la oportunidad que dejé pasar de practicar la conversación en clases con ella.

<q>Es que no me va a servir de nada practicar la conversación una temporada si luego no lo utilizo, pues voy a acabar igual que estoy</q> <cite>Yo misma, siempre tan clarividente</cite>

Mi problema es la pronunciación y la soltura en la conversación. Todos los días me comunico por escrito en inglés sin mayor problema. Tampoco es muy difícil, pues casi todo es lenguaje técnico. Pero a la hora de hablar, si se unen mi falta de práctica, los nervios por lo mismo, y mi acento murciano -cerradísimo-, **tenía todas las papeletas para que nadie me entendiera**.

Bueno, no sé aún cómo, conseguí hacerme entender y seguir la conversación sin mayor problema, aunque con más vergüenza que miedo, que ya es decir, pero ahora hay que tomar cartas en el asunto para mejorar, y rápido.