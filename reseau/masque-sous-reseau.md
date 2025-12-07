# 🎯 Masques de sous-réseau et Subnetting

Le masque de sous-réseau permet de déterminer :
- La partie réseau d’une adresse IP
- La partie hôte
- Le nombre de réseaux possibles
- Le nombre d’hôtes par réseau

---

## 🧩 1. Rappel : masque par défaut

| Classe | Exemple réseau | Masque par défaut |
|--------|----------------|-------------------|
| A | 10.0.0.0 | 255.0.0.0 |
| B | 172.16.0.0 | 255.255.0.0 |
| C | 192.168.0.0 | 255.255.255.0 |

---

## 🔢 2. Masques CIDR

| CIDR | Masque | Hôtes possibles |
|------|--------|----------------|
| /24 | 255.255.255.0 | 254 |
| /25 | 255.255.255.128 | 126 |
| /26 | 255.255.255.192 | 62 |
| /27 | 255.255.255.224 | 30 |
| /28 | 255.255.255.240 | 14 |
| /29 | 255.255.255.248 | 6 |
| /30 | 255.255.255.252 | 2 |

---

## 🧠 3. Méthode rapide de calcul (subnetting)

1. Choisir le nombre d’hôtes nécessaires  
2. Choisir le masque adapté  
3. Calculer les **incréments**  
4. Déterminer les plages IP

Exemple :  
Créer 4 sous-réseaux dans : **192.168.1.0/24**

→ /24 → /26 (car il faut 4 réseaux)  
→ Incrément = 64  
→ Résultat :

| Sous-réseau | Plage | Diffusion |
|-------------|--------|-----------|
| 192.168.1.0/26 | 192.168.1.1 – 62 | 192.168.1.63 |
| 192.168.1.64/26 | 65 – 126 | 127 |
| 192.168.1.128/26 | 129 – 190 | 191 |
| 192.168.1.192/26 | 193 – 254 | 255 |

---

## 🛠️ 4. Exemple pratique (OpenClassrooms)

Réseau : **10.0.0.0/24**  
Besoin : 3 sous-réseaux

→ Choisir /26  
→ Incrément = 64

Résultat :

- 10.0.0.0/26  
- 10.0.0.64/26  
- 10.0.0.128/26  

---

## 📌 5. Ce qu'un recruteur veut voir

- Capacité à créer plusieurs sous-réseaux  
- Comprendre CIDR et les masques  
- Savoir choisir le bon masque selon le besoin  
- Savoir expliquer clairement le subnetting

---

## ✔️ Ce chapitre du cours TCP/IP inclut :
- Découpage de réseau  
- Masques CIDR  
- Calcul du nombre d’hôtes  
- Plan d’adressage  
- Subnetting hiérarchique

Tu maîtrises maintenant la base du subnetting utilisé dans les entreprises et dans les examens techniques.
