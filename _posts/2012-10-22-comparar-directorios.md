---
layout: post
title: Comparar directorios 
tags : [linux,diff,comparar,directorios,convert,fotos]
--- 

Suponga usted que tiene el directorio `aa` con estos archivos:

    $ tree aa
    aa
    ├── 99.txt
    ├── a.txt
    ├── b.txt
    ├── c.txt
    └── rrr.txt

    0 directories, 5 files

Suponga ahora que tiene otro directorio de nombre `bb` con estos otros archivos:

    $ tree bb
    bb
    ├── 99.txt
    ├── a.txt
    ├── aaa.txt
    ├── b.txt
    └── c.txt

    0 directories, 5 files

Problema: ¿Como comparar los archivos de ambos directorios?, es decir, **¿tiene
`aa` los mismos archivos que `bb` y viceversa?**.

## `diff` al rescate 

    $ diff <(ls -1a ./aa) <(ls -1a ./bb)
    4a5
    > aaa.txt
    7d7
    < rrr.txt

## Conclusión

El archivo `aaa.txt` no está en el directorio `aa` y el archivo `rrr.txt` no está en el
directorio `bb`. Fin del misterio.

## Problema del mundo real 

Estaba procesando 1500 fotos usando [convert][convert] (cambiando de tamaño,
como dicen por ahí: _escalando_), el proceso **se cortó a mitad de camino** por un
error en la conexión con el servidor, como ya me había tomado 20 minutos llegar
a 700 fotos no iba a comenzar todo de nuevo. Por eso busqué las fotos que no
habían sido procesadas y me ahorré un tiempo valioso. 

[convert]:http://www.imagemagick.org/script/convert.php
