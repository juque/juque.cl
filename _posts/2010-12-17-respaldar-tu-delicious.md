---
layout: post
title: "Respaldar tus enlaces del.icio.us"
tags : [delicious,backup]
--- 

Hoy [se supo](<http://mashable.com/2010/12/16/leaked-slide-shows-yahoo-is-killing-delicious-other-web-apps/>) (producto de un accidente) que posiblemente Yahoo! borraría a [Del.icio.us](<http://www.delicious.com/>) de su «parrilla» de servicios webs. Este fue mi primer servicio social, por eso le guardo especial cariño, sería una pena sepultarlo.

¿Cómo respaldar todos tus enlaces del.icio.us?, desde la línea de comandos y usando curl ([Doc API](<http://www.delicious.com/help/api>)).

<pre>
<code>curl https://[mi_usuario]:[mi_contraseña]@api.del.icio.us/v1/posts/all > bookmarks.xml</code>
</pre>

Hice mi respaldo, ¡2265 enlaces! desde diciembre del 2004. Trivia: mi primer enlace fue [un tutorial de DOM](<http://www.kusor.net/traducciones/brainjar.es/introdom1.es.html>).

Mañana seguramente aparecerán *n+1* alternativas importables desde nuestro —posible—desahuciado del.icio.us.

