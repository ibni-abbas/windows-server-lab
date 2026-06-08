DHCP & DNS Server Configuration

Objectif
Ce projet a pour objectif de configurer un serveur DHCP et DNS sous Windows Server afin d’automatiser l’attribution des adresses IP et assurer la résolution de noms dans un réseau local.

Environnement utilisé:
- Active Directory déjà installé (lab.local)
- Machine virtuelle client Windows 10/11
- Réseau privé VMware

  PARTIE 1 : DHCP SERVER

 Objectif DHCP
 Attribuer automatiquement les adresses IP aux machines clientes.

  Étapes réalisées

 1. Installation du rôle DHCP
- Ouverture de Server Manager
- Ajout du rôle DHCP Server
- Installation des fonctionnalités associées

  2. Configuration du scope DHCP
Création d’une plage IP :

- Nom du scope : `LAN-POOL`
- Plage IP :
  - Start IP : 192.168.1.100  
  - End IP : 192.168.1.200  
- Masque : 255.255.255.0
- Passerelle : 192.168.1.1
- DNS : 192.168.1.10 (serveur AD)

   3. Activation du scope
- Activation de la plage DHCP
- Autorisation du serveur DHCP dans Active Directory


 4. Test client DHCP
- Sur un PC client :
bash
ipconfig /release
ipconfig /renew


PARTIE 2 : DNS SERVER

Objectif DNS

Permettre la résolution des noms de machines dans le domaine lab.local.

 Étapes réalisées
1. Installation du rôle DNS
Installation automatique avec Active Directory
Vérification via Server Manager
2. Création de zone DNS
Zone : lab.local
Type : Primary Zone
Intégrée à Active Directory
3. Ajout d’enregistrements DNS

Exemples :

srv-dc01.lab.local → 192.168.1.10
client1.lab.local → 192.168.1.100

4. Test de résolution DNS

Sur client :

nslookup lab.local
ping srv-dc01.lab.local
