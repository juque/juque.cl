---
layout: post
title: "MySQL: Comparando fechas que no son fechas"
tags : [mysql,date,fecha,strtodate]
--- 

Este es un problema más frecuente que lo que se pueda pensar, ¿cómo hago una consulta MySQL que debe comparar fechas usando campos que no son del tipo `DATE` si no más bien `VARCHAR`?.

El otro día me pidieron listar todos los usuarios de un sistema—dicho sea de paso: ¡sistema que **no** es de mi autoría!—que están de cumpleaños en Enero. Pan comido, dije, pero buseando en la base de datos me di cuenta que el campo fecha de nacimiento no era del tipo `DATE` «pan no tan comido».

Pero gracias al creador del iPhone que en MySQL existe una función que pasa cadenas a fechas:[STR\_TO\_DATE](<http://dev.mysql.com/doc/refman/5.1/en/date-and-time-functions.html#function_str-to-date>), ¡aleluya!.

Así y todo, finalmente la consulta quedó:

    SELECT * 
      FROM 
         usuarios 
      WHERE 
         MONTH(CURDATE()) = MONTH(STR_TO_DATE(fnacimiento,'%d-%m-%Y'));


