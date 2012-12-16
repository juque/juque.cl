---
layout: post
title: "Insertar cierto rango de archivo"
tags : [vim,util,insert,texto,rango]
--- 
Trabajando con algunos archivo CSS se me presentó el siguiente problema: ¿Cómo puedo insertar ciertas líneas del archivo A en el archivo B (que era en el cual estaba trabajando)?. Googleando un poco la solución finalmente llegué a esta—usando [Vim](<http://www.vim.org/>) por supuesto.

<pre><code>:r !sed -n '49,51p' /tmp/header.css.tpl</code></pre>

Lo que hace es llamar a `sed` para insertar el rango 49,51 del archivo `/tmp/header.css.tpl`, el resultado es leído por el buffer. Bello.

Perfeccionando un poco la inserción puedo incluso decirle a Vim en qué parte del archivo B puedo insertar el trozo de código, en el ejemplo a partir de la línea 33:

<pre><code>:33r !sed -n '49,51p' /tmp/header.css.tpl</code></pre>

Nuevamente [vim](<http://www.vim.org/>) salvándome el día.

