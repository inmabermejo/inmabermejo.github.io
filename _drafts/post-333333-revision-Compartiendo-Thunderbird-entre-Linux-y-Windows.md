---
id: 1512
title: Compartiendo Thunderbird entre Linux y Windows
date: 2005-01-20T11:34:34+02:00
author: Chavalina
layout: revision
guid: http://www.wp.chavalina.net/2005/01/20/333-revision/
permalink: /2005/01/20/333-revision/
---
Quiz&aacute; lo que voy a contar lo conoc&eacute;is y os parece una obviedad (mira que no cont&aacute;rmelo, malosos) pero yo acabo de probarlo y me va a ser muy &uacute;til ahora que **tengo** que estar en Linux.

No me gustaba tener un gestor de correo en Windows y otro en Linux por si aparecen inconsistencias (no tener los mismos correos en los dos sitios), y porque es un desperdicio de espacio, as&iacute; que pens&eacute; si Thunderbird usara el mismo modus-operandi para los dos sistemas operativos podr&iacute;a compartirlo.

Efectivamente.  
Se puede usar el mismo profile, compartiendo los archivos, que funciona todo perfectamente. Est&aacute;n las cuentas, las direcciones, los filtros&#8230; He hecho las pruebas de enviar y recibir correo, filtros incluidos, y todo perfecto.

Ya lo ten&iacute;a instalado en Windows, e hice que en Linux (<a href="http://www.chavalina.net/comentar.php?idpost=230&#038;q=" target="_blank">uso Suse</a>) la partici&oacute;n de Windows se montara en /mnt/windows al arrancar, editando el fichero /etc/fstab y a&ntilde;adiendo esta l&iacute;nea:

<div class="codigo">
  /dev/hda2 /windows/C vfat user,rw,auto,umask=000
</div>

Con esto se consigue que monte el dispositivo hda2 (segunda partici&oacute;n de mi ordenador, donde tengo el Windows) en la carpeta /windows/c, y entonces podremos acceder a ella como si de otro directorio se tratase.  
**Ojo!** si us&aacute;is NTFS esto no es tan sencillo, dependiendo de la distribuci&oacute;n, posiblemente teng&aacute;is que a&ntilde;adir algo a vuestro n&uacute;cleo, por ejemplo en Red Hat, pero &eacute;se no es el tema ahora.

Ahora hay que instalar el Thunderbird en Linux. Esto no es muy dif&iacute;cil, hay varias formas y depende de cada distribuci&oacute;n as&iacute; que no profundizo. Y una vez instalado, indicarle que use el mismo directorio que Thunderbird de Windows.

Para ello tenemos que ir al directorio de nuestro usuario en Linux, en mi caso /home/inma, y buscar un directorio (oculto) llamado .thunderbird. Ah&iacute; hay un archivo llamado profiles .ini que tendr&aacute; el siguiente aspecto cuando lo abrimos:

<div class="codigo">
  [General]<br /> StartWithLastProfile=1</p> 
  
  <p>
    [Profile0]<br /> Name=default<br /> IsRelative=1<br /> Path=hrxhxybe.default</div> 
    
    <p>
      Pues ah&iacute; tenemos que indicar la ruta de nuestro directorio de Windows.
    </p>
    
    <p>
      Para saber cu&aacute;l y d&oacute;nde est&aacute; podemos ir <br /> <a href="http://www.mozilla.org/support/thunderbird/profile#locate" target="_blank">al soporte de Mozilla</a> y enterarnos, por ejemplo en mi caso se encuentra en la ruta c:/Documents and Settings/Inma.NOTEBOOK/Datos de programa/Thunderbird/profiles.ini y ah&iacute; encontraremos un fichero similar al anterior, pr&aacute;cticamente igual, con la ruta de nuestro perfil de Thunderbird en Windows:
    </p>
    
    <div class="codigo">
      [General]<br /> StartWithLastProfile=1</p> 
      
      <p>
        [Profile0]<br /> Name=inma<br /> IsRelative=0<br /> Path=C: hunderbirdinmahrxhxybe.slt<br /> Default=1</div> 
        
        <p>
          Bien.<br /> Como nuestra ruta es el valor de Path, una vez que la partici&oacute;n de Windows est&eacute; montada en Linux, la ruta de este mismo profile ser&aacute; <strong>/windows/c/thunderbird/inma/hrxhxybe.slt</strong>, que ser&aacute; lo que tenemos que poner en el fichero profiles.ini de Linux, que finalmente quedar&aacute; as&iacute;:
        </p>
        
        <div class="codigo">
          [General]<br /> StartWithLastProfile=1</p> 
          
          <p>
            [Profile0]<br /> Name=default<br /> IsRelative=0<br /> Path=/windows/c/thunderbird/inma/hrxhxybe.slt</div> 
            
            <p>
              He cambiado el 1 por un 0 en IsRelative porque la ruta que he indicado para el profile es absoluta.
            </p>
            
            <p>
              Y ya est&aacute;, arrancar el Thunderbird y a correr.<br /> Por cierto, si vais a intentarlo, haced una copia de seguridad antes, basta con una copia en zip del directorio del Thunderbird, porque <strong>no me hago responsable de las consecuencias que pueda tener ponerlo en pr&aacute;ctica</strong> <img src="/imagenes/emoticonos/guino.gif" alt="emo" />
            </p>