Projet 2 : Réseau interne entre deux machines virtuelles
1. Présentation du projet
Dans le premier projet, nous avons créé une machine virtuelle Ubuntu.
Dans ce second projet, nous allons créer une seconde machine virtuelle Debian afin de mettre en place un réseau interne entre deux VM et tester la communication entre elles.

L’image Debian utilisée provient du site suivant :
https://www.linuxvmimages.com/

L’objectif final est de configurer les deux VM en réseau interne (Host‑Only) et de vérifier la connectivité via un test de ping entre VM1 et VM2.

2. Création de la VM Debian (VirtualBox)
L’environnement de virtualisation utilisé reste VirtualBox.

Paramètres de la VM :
Nom : Debian (ou selon votre choix)

Type : Linux

Version : Debian (64-bit)

Configuration matérielle :
Mémoire RAM : 2048 MB

Processeurs : 2 CPU

Mémoire vidéo : 128 MB

Contrôleur graphique : VMSVGA
(Ce contrôleur est recommandé car il offre une excellente compatibilité avec les distributions Linux.)

Disque dur virtuel :
Type : VDI

Taille : 15 Go

Mode d’allocation : Dynamique (allocation à la demande)

3. Configuration réseau
Pour permettre la communication directe entre les deux machines virtuelles, nous utilisons le mode réseau suivant :

Mode réseau : Réseau interne (Host‑Only)

Ce mode permet aux VM de communiquer entre elles et avec l’hôte, mais sans accès Internet.
Il est idéal pour les tests réseau en environnement isolé.

4. Installation du système d’exploitation
Monter l’image ISO Debian téléchargée.

Démarrer la VM.

Suivre les étapes d’installation proposées par l’installateur Debian.

Redémarrer la VM une fois l’installation terminée.

5. Configuration réseau interne
Les deux VM (Ubuntu et Debian) doivent être configurées sur le même réseau Host‑Only.

Exemple d’adresses IP :
VM1 (Ubuntu) : 192.168.100.2

VM2 (Debian) : 192.168.100.3

Masque : 255.255.255.0

Les adresses peuvent être configurées manuellement ou obtenues via DHCP si celui-ci est activé sur l’interface Host‑Only de VirtualBox.

6. Test de connectivité (Ping)
Une fois les deux VM configurées sur le même réseau interne, nous effectuons un test de communication.

Depuis VM1 vers VM2 :
Code
ping 192.168.100.2
Depuis VM2 vers VM1 :
Code
ping 192.168.100.3
Si les deux machines répondent, cela confirme que le réseau interne est fonctionnel.

7. Résultat attendu
À la fin de ce projet, les deux machines virtuelles doivent :

être installées et configurées correctement

être connectées au même réseau interne Host‑Only

pouvoir communiquer entre elles via un ping

Ce réseau interne servira de base pour les projets suivants impliquant des services réseau ou des tests multi‑VM.
