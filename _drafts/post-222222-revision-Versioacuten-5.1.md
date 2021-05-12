---
id: 1334
title: 'Versión 5.1'
date: 2004-09-18T06:19:16+02:00
author: Chavalina
layout: revision
guid: http://www.wp.chavalina.net/2004/09/18/222-revision/
permalink: /2004/09/18/222-revision/
---
He hecho un peque&ntilde;o cambio en el script que genera mi <acronym title="eXtensible Markup Language">XML</acronym> as&iacute; que ahora en mi lector de feeds puedo ver las imágenes y los enlaces que hay en mis post, como html normal. Estoy «estudiando» todav&iacute;a los diferentes formatos para sindicación que hay, y la verdad es que no sé si lo que he «apa&ntilde;ado» es muy correcto. En mi cuenta de <a href="http://bloglines.com/" target="_blank">Bloglines</a> y en mi <a href="http://www.mozilla.org/products/thunderbird/" target="_blank">Thunderbird</a> (ya es lector de feeds) se ve bien, pero si a alguien no le va bien, le agradecer&iacute;a much&iacute;simo que me lo dijera para volver a la versión anterior. Me parece una chapucilla, as&iacute; que no me f&iacute;o de que vaya bien. Tendré que estudiarlo un poco más y entonces volver a rehacerlo.

El cambio consiste en dejar la parte de <acronym title="HyperText Markup Language">HTML</acronym> tal y como está usando <a href="http://www.w3schools.com/xml/xml_cdata.asp" target="_blank">CDATA</a>, con lo que ese trozo de texto es ignorado por el parser y deja las etiquetas pasar sin problema.