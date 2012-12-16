---
layout: post
title: tar excluyente 
tags : [tar,excluyente]
--- 

Asumiendo que quieres comprimir un directorio completo, pero en el existe un sub-directorio (en cualquier nivel) con nombre «cache» que deseas excluir de la compresión, el comando sería:

     tar --exclude=cache -cvzf directorio.tar.gz directorio 

Listar el contenido y comprobar que todo ha ido bien:

     tar -ztvf directorio.tar.gz

