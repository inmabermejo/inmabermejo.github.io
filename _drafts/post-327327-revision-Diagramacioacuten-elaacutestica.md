---
id: 1424
title: 'Diagramación elástica'
date: 2005-01-13T04:41:10+02:00
author: Chavalina
layout: revision
guid: http://www.wp.chavalina.net/2005/01/13/327-revision/
permalink: /2005/01/13/327-revision/
---
Bajo ese nombre tan raro hay en la web de <a href="http://www.100px.com/" target="_blank">Nicolás Fantino</a> un muy muy buen <a href="http://www.100px.com/articulos/ni_fijo_ni_liquido_elastico/" target="_blank">artículo sobre maquetación</a> con <acronym title="Cascade Style Sheets">CSS</acronym> y <acronym title="eXtended HyperText Markup Language">XHTML</acronym> donde los anchos de los bloques o divisiones se fijan en _em_ en lugar de los píxeles o porcentajes acostumbrados, haciendo así que, además del texto, sus contenedores también se van a redimensionar cuando el usuario aumente el tamaño de letra.

Es muy interesante sobre todo para temas de accesibilidad, porque, como comenta Nicolás, cuando una persona necesita aumentar el tamaño de la letra en una web, si los contenedores tienen tamaño fijo la longitud de las líneas se hará demasiado corta como para leerlo cómodamente. Un ejemplo de esto lo tenéis en esta misma web.

El problema que presenta esto son las imágenes que usamos como fondo, curiosa <a href="http://www.100px.com/100logs/2005/01/#post-61" target="_blank">una solución</a> que propone con <a href="http://w3.org/Graphics/SVG/" target="_blank">imágenes vectoriales</a>, o también definiendo sus dimensiones de la misma forma que el texto y los bloques, ilustrado con un bonito <a href="http://www.csszengarden.com/?cssfile=063%2F063%2Ecss" target="_blank">ejemplo</a> del <a href="http://www.csszengarden.com/" target="_blank">CSS Zen Garden</a>.

**Actualización:** he hecho mi primera prueba con esta técnica sólo, sin más florituras, en <a href="http://www.chavalina.net/cv/" target="_blank">mi currículum</a> y no ha resultado nada difícil maquetar, igual igual que con píxeles.