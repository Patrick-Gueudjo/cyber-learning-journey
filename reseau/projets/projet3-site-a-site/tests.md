# Tests de connectivité – Projet 3

## 🔍 Objectif

Vérifier que les deux réseaux locaux (LAN A et LAN B) peuvent communiquer à travers les deux routeurs.

---

## 🧪 1. Tests depuis PC-A (192.168.10.10)

1️⃣ Ping la gateway locale :

- `ping 192.168.10.1`  
  ✅ Résultat attendu : réponses OK

2️⃣ Ping l’interface WAN de RouterA :

- `ping 10.10.10.1`  
  ✅ Résultat attendu : OK

3️⃣ Ping l’interface WAN de RouterB :

- `ping 10.10.10.2`  
  ✅ Résultat attendu : OK

4️⃣ Ping la gateway du LAN B :

- `ping 192.168.30.1`  
  ✅ Résultat attendu : OK

5️⃣ Ping PC-B :

- `ping 192.168.30.2`  
  ✅ Résultat attendu : OK

---

## 🧪 2. Tests depuis PC-B (192.168.20.10)

1️⃣ Ping la gateway locale :

- `ping 192.168.30.1`  
  ✅ Résultat attendu : OK

2️⃣ Ping l’interface WAN de RouterB :

- `ping 10.10.10.2`  
  ✅ Résultat attendu : OK

3️⃣ Ping l’interface WAN de RouterA :

- `ping 10.10.10.1`  
  ✅ Résultat attendu : OK

4️⃣ Ping la gateway du LAN A :

- `ping 192.168.10.1`  
  ✅ Résultat attendu : OK

5️⃣ Ping PC-A :

- `ping 192.168.10.10`  
  ✅ Résultat attendu : OK

---

## ❌ Si un test échoue

- Vérifier que les interfaces sont `up` sur les deux routeurs :  
  - `show ip interface brief`
- Vérifier le routage statique :  
  - sur RouterA : `show ip route`  
  - sur RouterB : `show ip route`
- Vérifier la passerelle par défaut des PCs :
  - PC-A → 192.168.10.1
  - PC-B → 192.168.20.1
