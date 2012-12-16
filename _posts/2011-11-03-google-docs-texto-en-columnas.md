---
layout: post
title: "Google Docs: texto en columnas"
tags : [googledocs,google,python]
--- 

Estaba compartiendo un documento CSV con un colega cuando traté de transformarlo en texto en columnas usando Numbers pero—por lo que investigué—no es posible.

Pero luego recordé Google Docs Hojas de Cálculo (o Spreadsheet) y acá sí funciona, pero muy al estilo google: `=SPLIT(array, delimiter)`, es decir, `=split(A1,",")`
