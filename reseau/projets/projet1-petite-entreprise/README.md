# 🧪 Projet 1 — Réseau d’entreprise (3 LAN + routage statique)

## 🎯 Objectif
Concevoir un réseau simple composé de :
- 1 LAN Utilisateurs
- 1 LAN Serveurs
- 1 LAN Administration
- 1 routeur avec 3 interfaces
- Du routage statique

## 🧱 Plan d’adressage
| LAN          | Réseau           | Passerelle      |
|--------------|------------------|-----------------|
| Utilisateurs | 192.168.128.0/18 | 192.168.191.254 |
| Serveurs     | 192.168.64.0/18  | 192.168.127.254 |
| Admin        | 192.168.0.0/18   | 192.168.63.254  |

## 🔧 Configuration Router
interface g0/0
 ip address 192.168.63.254 255.255.255.0
 no shutdown	

interface g0/1
 ip address 192.168.191.254 255.255.255.0
 no shutdown

interface g0/2
 ip address 192.168.127.254 255.255.255.0
 no shutdown

ip route 192.168.63.0 255.255.255.0 g0/0
ip route 192.168.191.0 255.255.255.0 g0/1
ip route 192.168.127.0 255.255.255.0 g0/2


## 🧪 Tests
- Ping Client → Serveur  
- Ping Admin → Client  
- Ping Client → Routeur  

Statut : ✔️ Fonctionnel

