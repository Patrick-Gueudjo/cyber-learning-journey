📘 Projet 1 — Réseau d’une petite entreprise (3 LAN)
🎯 Objectif

Mettre en place un réseau simple composé de :

*1 LAN Utilisateurs

*1 LAN Serveurs

*1 LAN Administration

*1 routeur avec 3 interfaces

Routage statique entre les réseaux

🧱 Architecture
        Admin LAN
            │
        +---┴---+
        │Router │
        +---┬---+
            │
   ┌────────┴─────────┐
   │                  │
Client LAN        Serveur LAN



📡 Plan d’adressage

Réseau	Adresse	Masque	Passerelle
Admin LAN	192.168.63.0	/24	192.168.63.254
Client LAN	192.168.191.0	/24	192.168.191.254
Serveur LAN	192.168.127.0	/24	192.168.127.254

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

Tests réalisés

✔️ Ping Client → Serveur
✔️ Ping Admin → Client
✔️ Ping Serveur → Admin
✔️ Ping routeur depuis chaque LAN


