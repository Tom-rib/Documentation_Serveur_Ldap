# Documentation Serveur LDAP et Gestion Accès

## Introduction

Bienvenue à la documentation du projet de mise en place d'un serveur LDAP chez DataTrust. Ce projet vise à centraliser l'authentification et la gestion des accès des employés aux différentes applications et services de l'entreprise. L'implémentation d'un serveur LDAP permettra une gestion efficace et sécurisée des utilisateurs et de leurs droits d'accès.
Objectifs


Mettre en place un serveur LDAP pour centraliser la gestion des utilisateurs.

Créer et organiser des groupes d'utilisateurs en fonction de leurs rôles.

Configurer des options de sécurité de base pour le serveur LDAP.


# Comprendre et Préparer LDAP

## Présentation

LDAP (Lightweight Directory Access Protocol) est un protocole destiné à interroger et modifier les services de répertoire. 
C'est un outil majeur pour les entreprises car il permet de centraliser la gestion des utilisateurs, simplifiant ainsi l'administration. Voici quelques-uns de ses avantages :

Centralisation : Gestion unique des utilisateurs et des droits d'accès.

Sécurité : Accès contrôlés de manière granulée.

Scalabilité : Capable de gérer un grand nombre d'utilisateurs et de ressources.


### Définir les Groupes d’Utilisateurs

Organisation des utilisateurs en trois groupes :

Utilisateurs Basiques : Accès aux fichiers partagés.

Développeurs : Accès limité aux applications de développement.

Administrateurs : Accès complet, y compris la modification des paramètres de sécurité.


## Mise en Place Technique

### Installation du Serveur LDAP

Pour installer un serveur LDAP sur un système Linux :

Installez les packages nécessaires via le gestionnaire de paquets (ex: sudo apt-get install slapd ldap-utils).

Configurez le serveur initialement (sudo dpkg-reconfigure slapd).

Notez chaque étape pour faciliter le dépannage et la compréhension.


### Création des Utilisateurs

Créez des utilisateurs et attribuez-les à leurs groupes respectifs :

Alice : Utilisateur basique

Bob : Développeur

Claire : Administratrice


### Test des Accès

Pour chaque utilisateur, assurez-vous que les permissions sont correctement appliquées :

Connectez-vous en tant qu'utilisateur.

Vérifiez l'accès aux ressources autorisées.

Confirmez que les restrictions sont respectées.


## Options de Sécurité de Base

### Gestion des Mots de Passe

Configurez le serveur LDAP pour exiger des mots de passe d'au moins 8 caractères. Documentez :

Utilisation de modules de politique de mot de passe.

Configuration des règles via des outils comme ldappasswd.


### Déconnexion Automatique

Implémentez une déconnexion automatique en cas d'inactivité :

Recherchez des solutions scriptées ou des modules complémentaires pour gérer l'expiration de session.

Documentez la mise en œuvre pour garantir la sécurité des sessions utilisateur.


## Conclusion

Ce document offre un guide clair pour la mise en place et la gestion d'un serveur LDAP chez DataTrust, assurant une gestion centralisée, sécurisée et efficace des utilisateurs et de leurs droits d'accès. Avec une configuration soignée et une documentation précise, l'infrastructure LDAP soutiendra les besoins croissants de l'entreprise en matière de gestion des identités.