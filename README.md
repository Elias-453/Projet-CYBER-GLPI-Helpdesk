# Projet-CYBER-GLPI-Helpdesk
PoC Helpdesk GLPI sur Windows Server 2022 virtualisé (VMware Workstation) — IIS, PHP 8.2, MariaDB, Active Directory, AD CS, DNS, HTTPS, GPO, FusionInventory, PowerShell


# Projet GLPI — Déploiement d'une solution Helpdesk

## Description
Preuve de Concept (PoC) du déploiement d'une solution helpdesk complète avec GLPI 
dans un environnement Windows Server 2022 virtualisé sous VMware Workstation.
Réalisé dans le cadre d'un projet scolaire en binôme.

## Infrastructure
| Composant | Rôle |
|-----------|------|
| Server1 (10.10.1.1) | AD DS, DNS, AD CS (Autorité de certification) |
| Server2 (10.10.1.2) | IIS, PHP 8.2, MariaDB, GLPI |
| Client Windows (10.10.1.3) | Poste utilisateur, Agent FusionInventory |

## Technologies utilisées
- Windows Server 2022 sous VMware Workstation
- GLPI (Gestionnaire Libre de Parc Informatique)
- IIS + PHP 8.2 + MariaDB
- Active Directory (AD DS / AD CS)
- PowerShell
- FusionInventory

## Ce qui a été réalisé
- Sécurisation HTTPS via certificat SSL généré par notre autorité de certification locale (leonidasCA)
- Accès via URL personnalisée www.leonidas.lan avec redirection automatique HTTP vers HTTPS
- Inventaire automatique des postes clients via FusionInventory
- Notifications email automatiques via SMTP
- Script PowerShell qui crée automatiquement un ticket GLPI quand un disque descend sous 5% d'espace libre
- Déploiement automatisé de l'agent via GPO
- Authentification des utilisateurs du domaine Active Directory dans GLPI (bonus)

## Documentation
La documentation complète est disponible dans le dossier /documentation.
