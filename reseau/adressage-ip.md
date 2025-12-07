# 📘 Adressage IP – Notes du cours TCP/IP (OpenClassrooms)

L’adressage IP permet d’identifier les machines dans un réseau et d’organiser la communication entre elles.  
Cette section explique les bases essentielles que tout administrateur réseau ou analyste cybersécurité doit comprendre.

---

## 1️⃣ Structure d’une adresse IPv4

Une adresse IPv4 est composée de **32 bits**, séparés en 4 octets :

Exemple :192.168.10.25


Chaque nombre (0 à 255) représente un octet.

---

## 2️⃣ Adresse réseau vs Adresse hôte

Dans un réseau IP, une adresse se divise en deux parties :

- **Partie réseau** → identifie le réseau  
- **Partie hôte** → identifie une machine dans ce réseau  

Cette séparation dépend du **masque de sous-réseau**.

---

## 3️⃣ Le masque de sous-réseau (Subnet Mask)

Le masque détermine quelles parties de l’adresse sont réservées au réseau ou aux hôtes.

Exemple masques :

| Masque | Notation | Nombre d'hôtes |
|--------|----------|----------------|
| 255.255.255.0 | /24 | 254 hôtes |
| 255.255.0.0 | /16 | 65 534 hôtes |
| 255.0.0.0 | /8 | 16 777 214 hôtes |

---

## 4️⃣ Les classes d’adresses (A, B, C)

| Classe | Exemple | Usage |
|--------|---------|-------|
| A | 10.0.0.0 – 10.255.255.255 | Très grands réseaux |
| B | 172.16.0.0 – 172.31.255.255 | réseaux moyens |
| C | 192.168.x.x | Petits réseaux (LAN) |

Les réseaux domestiques et petites entreprises utilisent presque toujours **Classe C : 192.168.x.x**

---

## 5️⃣ Adresse réseau & adresse de broadcast

Exemple :  
Réseau **192.168.10.0/24**

| Type | Adresse |
|------|---------|
| Adresse réseau | 192.168.10.0 |
| Première adresse hôte | 192.168.10.1 |
| Dernière adresse hôte | 192.168.10.254 |
| Broadcast | 192.168.10.255 |

---

## 6️⃣ Calcul simple d’un sous-réseau

Si tu prends un bloc /24 (254 hôtes) :


Et que tu veux 2 sous-réseaux → tu divises en /25 :

- 192.168.1.0/25 → hôtes de .1 à .126  
- 192.168.1.128/25 → hôtes de .129 à .254  

---

## 7️⃣ Exemple d’adressage d’une petite entreprise

| Réseau | Masque | Passerelle | Usage |
|--------|--------|------------|--------|
| 192.168.10.0/24 | /24 | 192.168.10.1 | Utilisateurs |
| 192.168.20.0/24 | /24 | 192.168.20.1 | Administration |
| 192.168.30.0/24 | /24 | 192.168.30.1 | Serveurs |

---

## 8️⃣ Importance en cybersécurité

- Séparer les réseaux limite la propagation d’attaques  
- Le bon adressage permet le filtrage par pare-feu  
- Chaque VLAN doit avoir un adressage propre  
- Les erreurs d’adressage créent des pannes réseau

---

✍️ *Notes personnelles (complète ici ce que tu veux retenir du cours)* :

- Toujours verifier son travail et etre minitieux afin déviter les erreurs
- 
- 

