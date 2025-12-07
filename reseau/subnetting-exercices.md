# 🧮 Exercices de Subnetting – Niveau Débutant → Avancé

Ces exercices viennent du cours **“Concevez votre réseau TCP/IP”** (OpenClassrooms), complétés avec des méthodes professionnelles utilisées en CCNA et cybersécurité.

---

# 🟦 1️⃣ Rappel : Méthode rapide (4 étapes)

1. Identifier le nombre d’hôtes nécessaires  
2. Choisir le masque adapté  
3. Déterminer l’incrément  
4. Calculer réseau, plage d’hôtes et broadcast  

Exemple :  
Créer 4 sous-réseaux dans un /24 → passer en /26 (car 2 bits empruntés → 4 réseaux).

---

# 🟩 2️⃣ Exercices niveau débutant

## 🔹 Exercice 1
Découper le réseau **192.168.1.0/24** en **2 sous-réseaux égaux**.

**Solution :**
- /25  
- Incrément = 128  
- Sous-réseaux :

| Réseau | Hôtes | Broadcast |
|--------|--------|-----------|
| 192.168.1.0/25 | 1–126 | 192.168.1.127 |
| 192.168.1.128/25 | 129–254 | 192.168.1.255 |

---

## 🔹 Exercice 2
Donner l’adresse de broadcast du réseau **10.0.4.0/22**

**Solution :**
- /22 → masque 255.255.252.0  
- Incrément = 4 sur le 3ᵉ octet  
- Réseau courant : 10.0.4.0  
- Prochain réseau : 10.0.8.0  

➡️ **Broadcast = 10.0.7.255**

---

# 🟧 3️⃣ Exercices niveau intermédiaire

## 🔹 Exercice 3
Une entreprise a besoin de **6 sous-réseaux** dans 192.168.10.0/24.

**Solution :**
- 6 réseaux → il faut 8 → emprunter 3 bits  
- Nouveau masque : /27  
- Incrément : 32  

Sous-réseaux :

- 192.168.10.0/27  
- 192.168.10.32/27  
- 192.168.10.64/27  
- 192.168.10.96/27  
- 192.168.10.128/27  
- 192.168.10.160/27  

---

## 🔹 Exercice 4
Trouver l’adresse réseau pour : **172.16.5.200/20**

**Solution :**
- /20 → masque = 255.255.240.0  
- Incrément = 16 sur le 3ᵉ octet  
- 5 ∈ [0–15] → réseau = 172.16.0.0  
- Broadcast = 172.16.15.255

---

# 🟥 4️⃣ Exercices avancés (type CCNA)

## 🔹 Exercice 5
Un réseau **10.0.0.0/16** doit être divisé en **100 sous-réseaux**.

**Solution :**
- 2⁷ = 128 → il faut 7 bits  
- Nouveau masque : /23  
- Hôtes par réseau = 510

---

## 🔹 Exercice 6
Identifier le sous-réseau auquel appartient :  
**192.168.45.78/26**

**Solution :**
- /26 → incrément = 64  
- Plages :

  - 192.168.45.0  
  - 192.168.45.64  
  - 192.168.45.128  
  - 192.168.45.192

78 ∈ [64–127] → **réseau = 192.168.45.64/26**

Broadcast = **192.168.45.127**

---

# 🏁 Conclusion

Ce fichier regroupe :
- les exercices du cours TCP/IP  
- des exercices supplémentaires niveau CCNA  
- les méthodes rapides utilisées en entreprise  

Ces calculs sont essentiels pour :
- concevoir des réseaux d’entreprise  
- configurer des VLAN  
- écrire des plans d’adressage  
- passer des entretiens cybersécurité / réseau

