---
layout: post
title: "Micro-HowTo: SSH sin contraseña"
tags : [ssh,howto,rsa]
--- 

    # localhost
    scp .ssh/id_rsa.pub juanito@servidor:/home/juanito/
    echo "alias servidor='ssh juanito@servidor'" >> .bashrc
    source .bashrc 

    # servidor
    mkdir .ssh
    mv id_rsa.pub .ssh/authorized_keys
    chmod 700 .ssh
    chmod 600 .ssh/authorized_keys

