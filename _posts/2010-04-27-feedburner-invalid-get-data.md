---
layout: post
title: "ExpressionEngine y Feedburner: Invalid GET Data" 
tags : [ee,expressionengine,feedburner]
--- 

He detectado un problema con el feed—gestionado por [Feedburner](<http://www.feedburner.com/> "Visitar feedburner")—generado por el sitio (que corre en [ExpressionEngine](<http://www.expressionengine.com> "visitar ExpressionEngine")). Estando en mi lector RSS hago clic en la entrada para ir al sitio y éste me arrojar un mensaje:

<pre>Invalid GET Data</pre>

Googleando el problema al parecer la solución está en **quitar un paréntesis** en el panel de control de Feedburner.com, específicamente en: <kbd>Analize &rarr; Configure Stats &rarr;  Customize...</kbd> y en <kbd>Campaign</kbd> cambiar:

<kbd>Feed: ${feedUri} (${feedName})</kbd> 

a

<kbd>Feed: ${feedUri} ${feedName}</kbd> 

Al menos ahora funcionar adecuadamente y el mensaje desapareció.
