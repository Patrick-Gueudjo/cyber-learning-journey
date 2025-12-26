# Commandes utiles pour Virtualisation

## Linux (VM + Labs)
- `ip a` → vérifier les interfaces réseaux
- `ping <ip>` → tester la connectivité
- `sudo apt update && sudo apt upgrade`
- `sudo systemctl status`
- `df -h` → vérifier le stockage
- `free -m` → vérifier la RAM
- qemu-img convert -O vdi source.qcow2 destination.vdi

-Action	                   →       Commande

-Voir interfaces	        →          ip link

-Voir IP	                →           ip addr

-Activer interface	     →    ip link set enp0s8 up

-Ajouter IP	       → ip addr add 192.168.100.10/24 dev enp0s8

-DHCP	                    →    dhclient enp0s8

-Ping                       →	ping 192.168.100.20


## VirtualBox
- Modifier une VM : `VBoxManage modifyvm <vm> --memory 4096`
- Lister les VM : `VBoxManage list vms`
- Démarrer une VM : `VBoxManage startvm <vm> --type headless`
