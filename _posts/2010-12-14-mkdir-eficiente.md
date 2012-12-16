---
layout: post
title: mkdir eficiente 
tags : [linux,unix,comando,mkdir]
--- 
<pre>
$ mkdir -p project/{lib/ext,bin,src,doc/{html,info,pdf},demo/stat/a}
$ tree project
project/
|-- bin
|-- demo
|   `-- stat
|       `-- a
|-- doc
|   |-- html
|   |-- info
|   `-- pdf
|-- lib
|   `-- ext
`-- src
</pre>

(Un código... vale más que mil palabras)
