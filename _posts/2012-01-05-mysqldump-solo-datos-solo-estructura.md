---
layout: post
title: "MySQLDump: sólo datos, sólo estructura"
tags : [mysql,dump]
--- 
Donde la base de datos se llama `acme`, el usuario `juanito` y la tabla `usuario`.

Exporta **sólo datos**, una fila, una inserción:

    mysqldump --no-create-info --extended-insert=false --compact -u juanito -p acme usuario

Exporta **sólo la estructura**:

    mysqldump -d --compact -u juanito -p acme usuario

