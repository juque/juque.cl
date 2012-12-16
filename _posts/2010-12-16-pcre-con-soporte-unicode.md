---
layout: post
title: PCRE con soporte Unicode 
tags : [linux,pcre,unicode,utf8]
--- 

### Problema:

<pre>
PHP Notice:  Sorry, your PCRE extension does not support UTF8 
which is needed for the I18N core in 
/usr/share/php/Zend/Locale/Format.php on line 769
</pre>

### Verficación del problema:

<pre>
$ pcretest -C
PCRE version 6.6 06-Feb-2006
Compiled with
  UTF-8 support
  No Unicode properties support
  Newline character is LF
  Internal link size = 2
  POSIX malloc threshold = 10
  Default match limit = 10000000
  Default recursion depth limit = 10000000
  Match recursion uses stack
</pre>

### Solución:

Descargar: [pcre-6.6-2.7.x86_64.rpm](<http://dl.dropbox.com/u/66131/pcre-66-27x86_64.rpm>) &larr; PCRE 6.6 for CentOS 5.2 64-bit

### Instalar:

<pre>
# rpm -Uvh pcre-6.6-2.7.x86_64.rpm
</pre>

### Verificar solución:

<pre>
$ pcretest -C
PCRE version 6.6 06-Feb-2006
Compiled with
  UTF-8 support
  <strong>Unicode properties support</strong>
  Newline character is LF
  Internal link size = 2
  POSIX malloc threshold = 10
  Default match limit = 10000000
  Default recursion depth limit = 10000000
  Match recursion uses stack
</pre>

### Reiniciar Apache.
<pre>
# /etc/init.d/httpd restart
</pre>
Sacado de: [Unicode Support on CentOS 5.2 with PHP and PCRE](<http://chrisjean.com/2009/01/31/unicode-support-on-centos-52-with-php-and-pcre/>)

