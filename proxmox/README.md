Role Name
=========

Hacer tunning de proxmox

Requirements
------------

1.- Copiar las claves SSH a los servidores de proxmox:

oscar@PRT-OMAS:~/ilba/proxmox_tunning$ for x in host{1..3}.ilba.cat; do ssh-copy-id -i .ssh/id_rsa.pub root@$x; done

oscar@PRT-OMAS:~/ilba/proxmox_tunning$ for x in host{1..3}.ilba.cat; do ssh root@$x -C "hostname"; done

2.- Launch

oscar@PRT-OMAS:~/ilba/proxmox_tunning$ ansible-playbook tunning.yml

3.- Acuerdate de subirlo al git

COMMIT="Primer commit"

git add . && git commit -m "$COMMIT" && git push -u origin master

