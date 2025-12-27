# Projet 3 – Interconnexion de 2 sites avec 2 routeurs

## 🎯 Objectif

Interconnecter deux réseaux locaux (Site A et Site B) à l'aide de deux routeurs reliés par un lien WAN, en utilisant du **routage statique**.

- Site A : Réseau Utilisateurs
- Site B : Réseau Utilisateurs
- Lien WAN : point-à-point entre les deux routeurs

---

## 🧱 Topologie logique

Site A (LAN A)  ── RouterA ── Lien WAN ── RouterB ──  Site B (LAN B)

- Le réseau LAN A doit pouvoir joindre le réseau LAN B.
- Le ping doit fonctionner dans les deux sens.

---

## 🗺️ Plan d’adressage IP

### 🌐 Réseaux utilisés

| Rôle          | Réseau           | Masque           |
|---------------|------------------|------------------|
| LAN Site A    | 192.168.10.0     | 255.255.255.0 (/24) |
| LAN Site B    | 192.168.30.0     | 255.255.255.0 (/24) |
| Lien WAN      | 10.10.10.0         | 255.255.255.252 (/30) |

---

### 🧩 Détails par équipement

#### 🏢 Site A

- **PC-A**
  - IP : 192.168.10.2 
  - Masque : 255.255.255.0  
  - Passerelle (gateway) : 192.168.10.1  

- **RouterA**
  - Interface LAN : `GigabitEthernet0/0`  
    - IP : 192.168.10.1  
    - Masque : 255.255.255.0  
  - Interface WAN : `Serial0/0/0`  
    - IP : 10.10.10.1  
    - Masque : 255.255.255.252  

---

#### 🏢 Site B

- **PC-B**
  - IP : 192.168.30.2
  - Masque : 255.255.255.0  
  - Passerelle : 192.168.30.1  

- **RouterB**
  - Interface LAN : `GigabitEthernet0/0`  
    - IP : 192.168.30.1  
    - Masque : 255.255.255.0  
  - Interface WAN : `Serial0/0/0`  
    - IP : 10.10.10.2  
    - Masque : 255.255.255.252  

---

## 🚏 Routage statique

Sur **RouterA** :

- Route vers LAN B :  
  - Réseau : `192.168.30.0`  
  - Masque : `255.255.255.0`  
  - Next-hop : `10.10.10.2`  

Sur **RouterB** :

- Route vers LAN A :  
  - Réseau : `192.168.10.0`  
  - Masque : `255.255.255.0`  
  - Next-hop : `10.0.0.1`  

---

## ✅ Objectifs de validation

- PC-A doit pouvoir **ping** :
  - 192.168.10.1 (gateway locale)
  - 10.10.10.1 (WAN côté RouterA)
  - 10.10.10.2 (WAN côté RouterB)
  - 192.168.30.1 (gateway du Site B)
  - 192.168.30.2 (PC-B)

- PC-B doit pouvoir **ping** l’inverse.

Tous ces tests seront détaillés dans `tests.md`.
