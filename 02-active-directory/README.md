ctive Directory Domain Services (AD DS)

 Objectif
Installer et configurer un contrôleur de domaine (Domain Controller) afin de gérer un domaine Windows et centraliser les utilisateurs et ressources.


 Environnement utilisé
  Windows Server 
  Serveur configuré (voir dossier 01-installation)
  IP statique configurée
  DNS installé automatiquement avec AD DS


Nom du domaine
Domaine créé : `lab.local`

 Étapes réalisées

 1. Installation du rôle AD DS
 Ouverture de Server Manager
 Ajout du rôle Active Directory Domain Services
 Installation des fonctionnalités nécessaires


 2. Promotion du serveur en contrôleur de domaine
 Choix : "Ajouter une nouvelle forêt"
 Nom du domaine : `lab.local`
 Configuration du niveau fonctionnel (Windows Server 2016/2019)
 Définition du mot de passe DSRM

 3. Redémarrage du serveur
 Le serveur devient automatiquement un Domain Controller

voir dossier 02-active-diectory

 Auteur

Abbas Senoussi ALHAFIZ  
Ingénieur Réseaux et Télécommunications
