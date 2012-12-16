---
layout: post
title: "Safari: forzar abrir enlaces en nueva pestaña" 
tags : [safari,pestaña,navegador]
--- 

Safari por defecto abre los enlaces con atributos <code>target="_blank"</code> en una ventana nueva (de perogrullo), además todas aquellas llamadas al navegador —por ejemplo—desde un lector RSS también lo hace en una ventana nueva. Para algunos usuarios puede parecer muy cómodo, pero para otros no lo es tanto.

Para solucionar esto _comportamiento_ indeseado y dejar todas esas ventanas individuales en una sola tenemos dos alternativas:

1. En Safari ir a: <kbd>Ventana → Fusionar todas las ventanas</kbd> y listo. Lamentablemente no he encontrado todavía ningún atajo de teclado para esto.
2. Y la segunda alternativa es ir a Terminal.app, y cambiar la variable booleada que maneja este comportamiento: <kbd>defaults write com.apple.Safari TargetedClicksCreateTabs -bool true</kbd>. Luego debe reiniciar Safari para que el cambio surta efecto.

El punto 2 trae consigo un efecto colateral: Cuando realmente se necesita abrir una ventana nueva—como por ejemplo un popup—ya no lo hará, toda nueva ventana será una nueva **pestaña**. El usuario debe decidir cual camino tomará (fusionar o forzar por consola). 

Revertir el punto 2 es sencillo, solo cambie el valor <kbd>true</kbd> por <kbd>false</kbd> y todo volverá a su configuración inicial.
