---
layout: post
title: "ExpressionEngine: URLs cortas" 
tags : [ee,expressionengine,url,cortas]
--- 

Acabo de instalar un pequeño plugin llamado [Shortener](<http://expressionengine.com/forums/viewthread/111459/>) que acorta las direcciones (ú o URL's). Los pasos para la instalación son:

1. Bajar y dejar el plugin en el directorio _plugins_
2. Crear un nuevo grupo de plantillas, yo lo llamé «u»
3. Poner en la plantilla creada (_entry_ es la plantilla que maneja la entrada individual):<pre>
    &lt;?php {exp:shortener:redirect template="blog/entry" entry_id="{segment\_2}"} ?&gt;</pre>
4. Editar la plantilla que tiene el encabezado (<code>HEAD</code>) del sitio y poner:<pre>
    {exp:shortener:meta template="u" url_title="{segment\_3}"}</pre>
5. No olvidar poner el enlace corto en la plantilla de la entrada individual (acá aparece en la esquina inferior derecha), de nada sirve todo esto si no es visible ni clickeable.<pre>
{exp:shortener:link template="s" url_title="{segment\_3}"}
</pre>

## Comentarios

Hay que mencionar que el plugin fue desarrollado para sitios de la forma <code>blog/entry/titulo-de-la-entrada</code>, pero el mío tiene otra forma—<code>/log/año/mes/entrada</code>, por lo tanto debí _hackear_ un poco el plugin para adaptarlo a mis necesidades, en la función <code>Redirect()</code> simplemente traje la fecha de la entrada y le di el formato que tiene mi estructura, es decir, _año/mes_.

