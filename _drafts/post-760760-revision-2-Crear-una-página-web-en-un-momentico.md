---
id: 2751
title: Crear una página web en un momentico
date: 2008-12-24T16:33:40+02:00
author: Chavalina
layout: revision
guid: http://www.chavalina.net/2008/12/24/760-revision-2/
permalink: /2008/12/24/760-revision-2/
---
He dejado caer que estoy trabajando en un nuevo proyecto.  
Y algunos, sobre todo los que tengo en el messenger y en la vida real dirán «&iquest;No estabas tan ocupada?». Y yo me tendr&iacute;a que poner roja de verg&uuml;enza… &iquest;o no?

Me apetece contar un poco del proceso que he seguido para crear este sitio. No me he gastado ni un duro todav&iacute;a, y todo lo hice en ratos. Maravillas de los CMS actuales.

Vayamos por partes:

  1. **El dominio:**  
    Lo [consegu&iacute; gratis](http://www.com.es/00433/dominios-es-gratis/) gracias al blog [com](http://www.com.es/), y en el mismo sitio aprend&iacute; a [ponerlo bajo control](http://www.com.es/00438/gestionar-dominio-esnic/) para que el dominio _apuntara_ a mi página y más cosicas.</p> 
    Esto &uacute;ltimo, el cambio del registrador del dominio .es a ESNIC, me tard&oacute; un par de horas o tres, a otros les ha tardado más, pero tened paciencia, que pa eso es gratis.

  2. **El alojamiento:**  
    Aqu&iacute; casi todos sabéis que [yo tengo Dreamhost](http://chavalina.net/comentar.php?idpost=618), y con el espacio que tengo ah&iacute; no necesito contratar nada más para alojar más de un dominio (ya tengo 5 y 3 subdominios ah&iacute;), pero estaba un poco mosca por los [problemas de su uso de <acronym title="Hypertext PreProcessor">PHP</acronym> como GCI](http://mnm.uib.es/gallir/posts/2005/11/10/499/), que es lo que hace cuando eliges tener PHP5 en un dominio, pero volveremos sobre eso más tarde.</p> 
    Para alojar un dominio con [Dreamhost](http://www.dreamhost.com/r.cgi?chavalina) s&oacute;lo tienes que ir al «Manage Domains» del panel de control y decir el dominio que quieres alojar, elegir si quieres redirecci&oacute;n, mirror, alojamiento completo… yo eleg&iacute; esto &uacute;ltimo, y ellos me dieron los DNS para que los a&ntilde;adiera en ESNIC.
    
    Esto fue otro ratico de espera, pero en el mismo d&iacute;a yo ya ten&iacute;a mi dominio apuntando a donde yo quer&iacute;a, con todo el espacio de [Dreamhost](http://www.dreamhost.com/r.cgi?chavalina) y sin pagar nada todav&iacute;a.

  3. **El software:**  
    Yo siempre he abogado por el DO-IT-YOURSELF cuando se quiere algo medianamente complicado, pero los sistemas de gesti&oacute;n de contenido cada vez hacen más cositas, y esta vez _no ten&iacute;a tiempo_, as&iacute; que en el panel de goodies de Dreamhost hice una instalaci&oacute;n de [WordPress 2](http://www.wordpress.com), con un click y sin mirar una l&iacute;nea de <acronym title="Hypertext PreProcessor">PHP</acronym> &iexcl;qué feliz soy!</p> 
    **Plugins**  
    Esta instalaci&oacute;n que te hacen de WP te pone unos 50 temas para que elijas tu dise&ntilde;o y unos cuantos plugins. Yo activé [Akismet](http://akismet.com/), y [WP-Caché 2](http://mnm.uib.es/gallir/wp-cache-2/), cambié el que viene con la instalaci&oacute;n por la &uacute;ltima versi&oacute;n que aparec&iacute;a en la web. Aun as&iacute;, no fue soluci&oacute;n suficiente…
    
    Además, a&ntilde;ad&iacute; otros necesarios para el funcionamiento del sitio que ten&iacute;a en mente: 
    
    [Event Calendar](http://blog.firetree.net/2005/07/18/eventcalendar-30/) de Alex Tingle, que permite gestionar una categor&iacute;a de art&iacute;culos como eventos con su fecha de fin, crea un calendario para ellos solos y lo t&iacute;pico.
    
    [Simple Pie](http://simplepie.org/docs/installation/wordpress/), agregador de RSS.
    
    [Ultimate Tag Warrior](http://www.neato.co.nz/ultimate-tag-warrior/), al usar Event Calendar quer&iacute;a prescindir de las categor&iacute;as, as&iacute; que organizaré con etiquetas.
    
    **BB Press**  
    Mi página necesitaba un foro. Yo ya he probado muchos (PunBB, MiniBB, Simple Machines, phpBB, vBulletin…), pero teniendo WP instalado ser&iacute;a un crimen no probar su foro, además, sabiendo que se puede integrar… pues ale, a la aventura.
    
    Lo instalé bajo la carpeta de WP (esto es muy recomendable de cara a hacer la integraci&oacute;n), y con [un plugin y editar un archivo](http://bbpress.org/documentation/integration-with-wordpress/) ya ten&iacute;a el mismo usuario en ambos sistemas. 

  4. Lo malo es que todo no era tan bonito como lo he pintado… **los problemas:** 
    **Con el alojamiento:**  
    [Dreamhost](http://www.dreamhost.com/r.cgi?chavalina) y WordPress no son amigos. Todos lo sabemos y hay que aceptarlo![emo](/imagenes/emoticonos/confuso.gif) y poner soluciones, que las hay.
    
    Yo no iba a cambiar de alojamiento ni de sistema, as&iacute; que instalé [WP-Caché 2](http://mnm.uib.es/gallir/wp-cache-2/), más vale prevenir.
    
    Por supuesto, en el mismo d&iacute;a no pod&iacute;a consumir tanta CPU como para que me llamaran la atenci&oacute;n, pero no era necesario. Yo misma pod&iacute;a ver como la primera vez que intentaba accecer a la web tardaba entre 3 y 5 segundos en aparecer… si es que aparec&iacute;a, que normalmente se quedaba muerta.
    
    Algo mosca, ya que ten&iacute;a el WP-Caché, pregunté al servicio técnico de DH, que le echaron la culpa a WP, as&iacute; que la que me qued&oacute; fue ir al panel de control de DH, y, para este dominio, deshabilitar el uso de PHP5, dejar PHP4 y desaparecieron los problemas.
    
    Esto no dice mucho en favor de DH, pero a mi al menos no me molesta. Tengo soluci&oacute;n, usar PHP4, y también tengo que decir que tengo otros softwares instalados en el mismo hosting (mi CMS, foros PunBB, foros SMF, Drupal, ZenPhoto) y funcionando con PHP5 sin problemas de consumo de CPU ni nada…
    
    **Con los plugins:**  
    Event Calendar no funcionaba bien al principio, trataba los eventos como otro post más, joer que rabia me dio! pero lo que pasaba es que en WP2 hab&iacute;a un problema [fácil de arreglar](http://blog.firetree.net/2006/01/31/eventcalendar-303), por suerte.
    
    **Con los foros**  
    Ojo especialmente al fichero de configuraci&oacute;n de los foros (config.php). Para hacer la integraci&oacute;n hay que indicar en este fichero la ruta de la instalaci&oacute;n de WP… pero hay que hacerlo con todo, achetetepés, uvedobles y dominio completo.  
    Yo cre&iacute;a que lo hab&iacute;a puesto bien un par de veces pero tuve que darle algunas vueltas.</li> </ol> 
    
    Y creo que éste fue todo el <em lang="en">troubleshooting</em> para montar una página bastante completa. Ahora s&oacute;lo me queda lo más _entretenido_, que es crear la imagen corporativa (ya está casi) construir un tema personalizado que la implemente, empezar a crear contenido e idear un plan para darlo a conocer.
    
    [Miguel](http://www.processblack.com/weblog/), si lo lees, esto es lo que estaba preparando el otro d&iacute;a cuando te escrib&iacute;, a ver qué te parece c&oacute;mo lo he solventado![emo](/imagenes/emoticonos/guino.gif)