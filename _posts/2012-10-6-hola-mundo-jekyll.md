---
layout: post
title: Hola mundo desde Jekyll 
tags : [intro, beginner, jekyll, tutorial]
--- 

Dicen que no poner un «hola mundo» como primer post/registro da mala suerte. Acá no desafiaremos a la _señora_ esta.

Este sitio ahora es gestionado por [Jekyll][1] — un generador de archivo estáticos basado en Ruby. Las [_pages_ de github][2] está gestionadas por Jekyll.

### Primer problema

La fecha de las entradas las quería en Español, para eso hice use de un plugin, los pasos para activarlo y usarlo son:

1. Crea dos carpeta: `_plugins` y `_locales`.
2. En `_plugins` [descarga este script][filtro] (no olvides setear la variable `LOCALE`).
3. En `_locales` [descarga tu _sabor_ de locale][sabor], en mi caso `es-CL`.
4. Listo, ahora podrás hacer `post.date | localize: "%e de %B, %Y"`.


### ¿Tutorial de Jekyll?

1. [Jekyll a static site generator](http://klepas.org/jekyll-a-static-site-generator/)
2. [Moving blog from wordpress com to jekyll](http://blog.rayapps.com/2010/08/09/moving-blog-from-wordpress-com-to-jekyll/)
3. [Sitios que usan jekyll](https://github.com/mojombo/jekyll/wiki/Sites) `#tip`: mira los _fuentes_.

[1]: https://github.com/mojombo/jekyll "Home del proyecto"
[2]: http://pages.github.com/ "github:pages"
[filtro]: https://github.com/gacha/gacha.id.lv/blob/master/_plugins/i18n_filter.rb
[sabor]: https://github.com/svenfuchs/rails-i18n/tree/master/rails/locale
