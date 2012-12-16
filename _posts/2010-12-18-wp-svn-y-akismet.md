---
layout: post
title: WP, svn y akismet
tags : [wp,skismet]
--- 

Estaba actualizando el blog de la familia cuando me doy cuenta que en la consola de Wordpress se me indicaba que el plugin akismet tenía una nueva versión. Fui a la línea de comandos y actualicé:

    svn update

Pero no funcionó, el plugin seguía desactualizado, aún cuando forma parte de core WP. En ese momento me di cuenta que el plugin forma parte de [otro repositorio](<http://plugins.svn.wordpress.org/akismet/trunk/>), y que cuando se actualiza WP el mismo svn se encarga de ir al otro repositorio y actualizar akismet. Pero el problema es que akismet no apuntaba a su _trunk_ si no que a un _tags_ ([la 2.5.0](<http://plugins.svn.wordpress.org/akismet/tags/2.5.0/>)), por lo tanto había que reconfigurar el svn para que apuntara a la versión actual y oficial, es decir, al trunk.

Los pasos son:

1. Ir a directorio _plugins_
2. borrar el directorio akismet: `rm -rf akismet`
3. A modo de información, mostrar el repositorio externo: `svn propget svn:externals`
4. Eliminar la entrada: `svn propdel svn:externals`
5. Vincular la nueva (ojo el punto al final y las comillas simples)

     <code>svn propset svn:externals 'akismet http://plugins.svn.wordpress.org/akismet/trunk' .</code>

6. Vamos al raíz de WP y actualizamos:

    `svn update`
    
    `Fetching external item into 'wp-content/plugins/akismet'`
    
    `External at revision 324182.`

    `At revision 17048.`
    
7. Listo
