---
id: 1498
title: 'Juan Piernas – DualFS'
date: 2004-05-24T15:42:56+02:00
author: Chavalina
layout: revision
guid: http://www.wp.chavalina.net/2004/05/24/124-revision/
permalink: /2004/05/24/124-revision/
---
Juan Piernas es un profesor de la Facultad de Informática de la Universidad de Murcia.

Y este profesor me impresionó un día resolviéndome una duda de mis prácticas de Redes. Y hoy vuelve a impresionarme un artículo de la <a href="http://www.revistaecho.com/" target="_blank">revista {echo}</a> (número 16) de la facultad de Informática de la Universidad, presentando un sistema de ficheros desarrollado por él. 

> ## DualFS en la práctica
> 
> La versión que tuve la oportunidad de probar es todavía experimental, por lo que hay  
> que considerar los resultados con cautela. Lo primero que hice fue compilarme un kernel 2.4.19,  
> parcheado para soportar DualFS, puesto que la versión de que dispongo esta preparada para este  
> kernel. Tras la compilación del módulo dualfs.o y la carga en memoria (insmod dualfs.o), ya puede  
> empezar a trabajar con este nuevo sistema de ficheros. He de resaltar que no es posible compilar  
> separadamente el kernel y el módulo sino que el kernel ha de compilarse para aceptar este módulo;  
> esto es así porque para la implementación de DualFS se ha retocado dos estructuras fundamentales  
> del kernel (en concreto el page-cache y buffer-cache unificados). El formateo de las particiones  
> de metadatos y datos es tan sencillo como el cualquier otro sistema de ficheros, la única  
> diferencia es que hay que indicar dos dispositivos en lugar de uno, simplemente escribir: mkdualfs  
> dispositivo\_metadatos dispositivo\_datos para formatear con todas las opciones por defecto. El  
> montaje también es igual salvo que se debe indicar el dispositivo de metadatos como dispositivo a  
> montar.
> 
> Probé a hacer algunas operaciones con DualFS para compararlas con los sistemas de  
> ficheros con journaling: xfs, reiserfs, jfs y ext3. Las pruebas las cronometré y pese a que realicé  
> las pruebas con las dos particiones adyacentes en el mismo disco duro, los resultados son positivos:  
> DualFS destacó en las operaciones con metadatos, en concreto en borrados y una prueba que  
> combinaba recorrido de directorios con lectura de algunos archivos. Todos los datos con estas  
> pruebas podéis encontrarlos en <a href="http://webs.ono.com/virginiogl_web" target="_blank">http://webs.ono.com/virginiogl_web</a>
> 
> <p class="cita">
>   Fuente: Virginio García López,<a href="http://www.revistaecho.com/" target="_blank"> número 16, revista {echo}</a> de la Facultad de Informática de la UM
> </p>

Aquí tenéis el artículo completo para quien no quiera bajar la revista… quería poner un emoticono pero no sé cuál poner.