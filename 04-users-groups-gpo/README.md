LAB WINDOWS SERVER : Gestion des Users, Groups et GPO (Active Directory)

Objectif du laboratoire
Ce laboratoire a pour objectif de montrer comment administrer un environnement Active Directory sous Windows Server en :
- Créant des utilisateurs et des groupes
- Organisant les ressources via les OU
- Gérant les permissions avec les groupes de sécurité
- Appliquant des stratégies de groupe (GPO)
- Restreignant l’accès au Panneau de configuration


 Prérequis
- Windows Server installé
- Active Directory Domain Services (AD DS) configuré
- Domaine fonctionnel (ex: `lab.local`)
- Poste client joint au domaine
- Droits administrateur


 Partie 1 : Création des utilisateurs

Étapes :
1. Ouvrir Active Directory Users and Computers
2. Créer une OU : `Utilisateurs`
3. Créer un utilisateur (ex: ali)
4. Définir un mot de passe


Partie 2 : Création des groupes

Étapes :
1. Créer un groupe de sécurité (ex: Informatique)
2. Type : Security
3. Scope : Global
4. Ajouter l’utilisateur au groupe


 Partie 3 : Liaison utilisateur / groupe

- Ouvrir le groupe
- Ajouter les utilisateurs dans l’onglet Members
- Valider les changements


 Partie 4 : GPO – Bloquer le Panneau de configuration

Objectif :
Empêcher l’accès au Panneau de configuration

Étapes :
1. Ouvrir Group Policy Management
2. Créer une GPO et la lier à l’OU
3. Modifier la GPO :
