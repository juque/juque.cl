--- 
layout: post
title: "Mercurial: custom log"
tags: [mercurial,log,custom]
---

Estaba buscando un trozo de código que puse y luego borre en un proyecto
versionado con mercurial - no recordaba la revisión, lo único que tenía en mente
fue que puse un texto de _sumario_ bastante descriptivo. Pero hacer un `hg log` en 
un proyecto con más de 900 revisiones **no es útil**. 

Aplicar `grep` a la salida del log tampoco me servía de mucho porque no muestra
el número de revisión. 

Luego recordé que mercurial tiene la posibilidad de personaliza el log:

    hg log --template "{rev} - {desc}\n" | grep TEXTO_BUSCADO

¡Asunto resuelto! — [más información](http://hgbook.red-bean.com/read/customizing-the-output-of-mercurial.html).

