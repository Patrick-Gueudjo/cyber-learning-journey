📌Projet 3 : Snapshot + Test de sécurité
1. Objectif du projet
Dans ce troisième projet, nous allons tester l’utilisation d’un snapshot en créant volontairement une situation “à risque” dans une machine virtuelle.
L’objectif est de :

créer un snapshot de la VM dans son état initial

installer un logiciel inutile pour simuler une modification risquée

restaurer le snapshot

vérifier que la VM revient bien à son état d’origine

Ce test permet de comprendre l’utilité des snapshots pour sécuriser un environnement de travail.

2. Création du snapshot
Avant de modifier la machine virtuelle, nous créons un snapshot de son état actuel.

Étapes :

Ouvrir VirtualBox

Sélectionner la machine virtuelle

Aller dans l’onglet Snapshots

Cliquer sur Créer un instantané

Donner un nom clair (exemple : Instantané 1 – État initial)

Valider

Le snapshot enregistre l’état complet de la VM : disque, mémoire, configuration et système.

3. Installation d’un logiciel pour le test
Une fois le snapshot créé, nous allons installer un logiciel simple afin de simuler une modification du système.

Commande :

Code
sudo apt install cowsay
Après l’installation, nous testons le programme :

Code
cowsay bonjour
Si le message s’affiche correctement, cela confirme que le logiciel est bien installé.

4. Restauration du snapshot
Après le test, nous fermons la machine virtuelle.
VirtualBox peut afficher un message proposant de restaurer l’instantané enregistré.
Nous sélectionnons Oui pour restaurer le snapshot Instantané 1.

Sinon, la restauration peut se faire manuellement :

Ouvrir VirtualBox

Aller dans l’onglet Snapshots

Sélectionner Instantané 1

Cliquer sur Restaurer

Confirmer l’opération

La VM revient alors exactement dans l’état où elle se trouvait avant l’installation du logiciel.

5. Vérification après restauration
Une fois la VM restaurée, nous testons à nouveau la commande :

Code
cowsay bonjour
Le système répondra que la commande n’existe pas, ce qui prouve que :

le logiciel installé après le snapshot a disparu

la VM a bien été restaurée à son état initial

le snapshot a fonctionné correctement

6. Conclusion
Ce projet démontre l’importance des snapshots dans un environnement virtualisé.
Ils permettent :

de tester des logiciels

d’expérimenter des configurations

de revenir en arrière en cas d’erreur

de sécuriser un environnement de travail

Le snapshot est donc un outil essentiel pour éviter la perte de données ou la corruption d’un système lors de manipulations risquées.
