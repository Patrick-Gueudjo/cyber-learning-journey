Projet 1 : Installation d’une VM Linux
1. Téléchargement de l’image ISO
L’image d’installation d’Ubuntu peut être téléchargée depuis différentes plateformes.
Dans ce projet, l’image utilisée provient du site officiel d’Ubuntu :

https://www.ubuntu.com/download/desktop

Une fois le fichier ISO téléchargé, nous pouvons procéder à la création de la machine virtuelle.

2. Création de la machine virtuelle (VirtualBox)
L’environnement de virtualisation utilisé pour ce projet est VirtualBox.

Paramètres de la VM :
Nom : Ubuntu (ou selon votre choix)

Type : Linux

Version : Ubuntu (64-bit)

Configuration matérielle :
Mémoire RAM : 2048 MB

Nombre de processeurs : 2 CPU

Disque dur virtuel :

Type : VDI

Taille : 15 Go

Mode d’allocation : Dynamique (allocation à la demande)

Configuration réseau :
Mode réseau : NAT
Le mode NAT est utilisé car il permet à la machine virtuelle d’accéder facilement à Internet sans configuration réseau avancée.

3. Installation du système d’exploitation
Après la création de la VM :

Monter l’image ISO d’Ubuntu dans le lecteur virtuel.

Démarrer la machine virtuelle.

Suivre les étapes d’installation proposées par l’installateur Ubuntu.

Une fois l’installation terminée, redémarrer la VM et retirer l’ISO.

4. Résultat attendu
À la fin de ce projet, vous devez obtenir une machine virtuelle Ubuntu fonctionnelle, connectée à Internet via NAT, et prête à être utilisée pour les projets suivants.
