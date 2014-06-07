---
layout: post
title: sqlplus con historial de comandos
tags: [sqlplus]
---
Si te gusta usar [`sqlplus`][1] y odias que **no tenga** historial de comandos lo siguiente te puede hacer la vida más fácil.

Existe una utilidad que permite tener un historial de tus comandos, se llama `rlwrap`. 

> rlwrap is a wrapper that uses the GNU readline library to allow the editing of
> keyboard input for any other command. Input history is kept between
> invocations, separately for each command; history completion and search work
> as in bash and completion word lists can be specified on the command line.

Los pasos para instalarla y correrla son:

1. [Descargar `rlwrap`](http://utopia.knoware.nl/~hlub/uck/rlwrap/#rlwrap).
2. Es requisito tener Readline - [instalar Readline](http://cnswww.cns.cwru.edu/php/chet/readline/rltop.html).
3. Descomprime `rlwrap` e instala:
	
		$ ./configure
		$ make
		$ make install
	
5. Correr 

    	$ rlwrap sqlplus USUARIO/PASS@tns
    	
Boom!, ahora tienes `sqlplus` con historial de comandos (`Ctrl+r` es ahora tu copiloto).

[1]:http://en.wikipedia.org/wiki/SQL*Plus
