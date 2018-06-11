---
layout: post
published: true
title: Descarga archivo con URLs
---

Supongamos que tienes un archivo txt que contiene muchas URLs de imágenes:

```
$ cat urls.txt

https://c2.staticflickr.com/8/7214/7377987498_9b9a9fa852_c.jpg
https://c2.staticflickr.com/8/7303/11624120355_703921f4d2_c.jpg
https://c2.staticflickr.com/8/7468/16056448100_8633ae0a0b_c.jpg
```

Ahora quieres descargar esas fotos pero generando una secuencia, por ejm: `auto_1.jpg`, `auto_2.jpg`, etc.

En solo una línea de comandos puedes hacer lo siguiente:

```
$ cat -b urls.txt | while read N U; do $(curl -o auto_$N.jpg $U); done
```

## Bonus

¿Quieres fotos aleatorias para tu maqueta?, servido:

```
for i in {1..10}; do curl -L -o "foto_$i.jpg" https://source.unsplash.com/random/500x500;sleep 3; done
```
