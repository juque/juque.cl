---
layout: post
title: Como saber el theme configurado en WP vía MySQL
tags : [wp,wordpress,mysql]
--- 

Típico: ¿Cómo saber que theme está configurado por defecto a una instalación Wordpress sin entrar al admin - es decir, vía MySQL:

    SELECT * FROM wp_options WHERE 
       option_name = 'template' OR 
       option_name = 'stylesheet' OR 
       option_name = 'current_theme'; 

¿Y cómo puedo setear el theme por defecto por si algo anda mal?

    UPDATE wp_options SET option_value = 'Twenty Eleven' WHERE option_name = 'template';
    UPDATE wp_options SET option_value = 'twentyeleven' WHERE option_name = 'stylesheet';
    UPDATE wp_options SET option_value = 'twentyeleven' WHERE option_name = 'current_theme';


