# Protocoles Réseau Importants (TCP/IP)

Ce document résume les principaux protocoles utilisés dans les réseaux modernes.  
Ils sont essentiels pour comprendre le fonctionnement du modèle TCP/IP et pour réaliser un diagnostic réseau.

---

## 🔹 1. ICMP (Internet Control Message Protocol)
- **Port :** Aucun (protocole)
- **Rôle :** Messages d’erreur et de diagnostic
- **Exemples :** `ping`, `traceroute`

---

## 🔹 2. ARP (Address Resolution Protocol)
- **Rôle :** Associe une adresse IP à une adresse MAC
- **Utilité :** Communication dans un réseau local (LAN)
- **Commandes :**
  - `arp -a` (Windows)
  - `show ip arp` (Cisco)

---

## 🔹 3. DHCP (Dynamic Host Configuration Protocol)
- **Ports :** UDP 67/68
- **Rôle :**
  - Attribution automatique : IP, masque, passerelle, DNS
- **Fonctions importantes :**
  - Discover
  - Offer
  - Request
  - Acknowledge (DORA)

---

## 🔹 4. DNS (Domain Name System)
- **Port :** UDP/TCP 53
- **Rôle :** Convertit un nom domaine en adresse IP
- **Exemple :** `google.com → 142.250.x.x`

---

## 🔹 5. HTTP / HTTPS
- **Ports :** 80 / 443
- **Rôle :** Communication web
- **HTTPS :** version sécurisée (TLS/SSL)

---

## 🔹 6. FTP / SFTP
- **FTP Ports :** 20, 21
- **Rôle :** Transfert de fichiers
- **SFTP :** version sécurisée via SSH

---

## 🔹 7. SSH (Secure Shell)
- **Port :** 22
- **Rôle :** Connexion sécurisée à distance (Linux, routeur, serveur)

---

## 🔹 8. SMTP / POP3 / IMAP (Emails)
- **SMTP Port :** 25 (envoi)
- **POP3 Port :** 110 (réception)
- **IMAP Port :** 143 (réception)

---

## 🔹 9. TCP vs UDP
| Caractéristique |    TCP    |     UDP     |
|-----------------|-----------|-------------|
| Fiabilité       | Oui       | Non         |
| Vitesse         | Plus lent | Plus rapide |
| Applications   | Web, mails | VoIP, gaming, streaming |

---

## 🔹 10. Port Well-Known (0–1023)
Quelques ports essentiels :
| Port | Protocole | Usage |
|------|-----------|--------|
| 22   | SSH       | Admin à distance |
| 23   | Telnet    | Admin non sécurisée |
| 25   | SMTP      | Email |
| 53   | DNS       | Résolution noms |
| 67/68 | DHCP     | Attribution IP |
| 80    | HTTP     | Web |
| 443   | HTTPS    | Web sécurisé |

---

## ✔️ Ce que j'ai appris
- Le rôle de chaque protocole dans la communication réseau.
- Les ports logiques associés aux applications.
- L’importance des protocoles pour le diagnostic réseau.
- Chaque protocole a un rôle précis
- TCP = fiable, UDP = rapide
- ARP, ICMP, DHCP sont essentiels pour diagnostiquer un réseau
- Comprendre ces protocoles = base solide pour la cybersécurité et l’administration réseau

