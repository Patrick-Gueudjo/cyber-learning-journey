Créer 3 VLANs sur un switch + un routeur avec sous-interfaces :

VLAN 10 : Utilisateurs

VLAN 20 : Admin

VLAN 30 : Serveurs 

🧩 Architecture
                          PCs → Switch → (Trunk) → Routeur g0/0

Plan d’adressage
  

        | VLAN            | Réseau          | Passerelle   |
| --------------- | --------------- | ------------ |
| 10 Utilisateurs | 192.168.10.0/24 | 192.168.10.1 |
| 20 Admin        | 192.168.20.0/24 | 192.168.20.1 |
| 30 Serveurs     | 192.168.30.0/24 | 192.168.30.1 |


Routeur — Configuration des sous-interfaces

  interface g0/0
 no shutdown

interface g0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0

interface g0/0.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0

interface g0/0.30
 encapsulation dot1Q 30
 ip address 192.168.30.1 255.255.255.0   

Switch — Configuration VLAN + Trunk

 vlan 10
vlan 20
vlan 30

interface fa0/1
 switchport mode access
 switchport access vlan 10

interface fa0/2
 switchport mode access
 switchport access vlan 20

interface fa0/3
 switchport mode access
 switchport access vlan 30

interface g0/1
 switchport mode trunk
 switchport trunk allowed vlan 10,20,30

 Tests réalisés

✔️ Ping VLAN10 → VLAN20
✔️ Ping VLAN10 → VLAN30
✔️ Ping VLAN30 → routeur
✔️ Ping inter-VLAN réussi 

Résultat

Le routage inter-VLAN fonctionne parfaitement.
