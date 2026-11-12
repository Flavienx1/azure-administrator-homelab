# Lab d’administration Azure

Je développe ce portfolio pour documenter ma pratique de l’administration système et cloud. Mon parcours va du support IT N1/N2 vers les fonctions d’administrateur Azure, de Cloud Engineer puis de DevOps Engineer. J’ai obtenu la certification Microsoft Azure Fundamentals (AZ-900). Ce dépôt rassemble les configurations du lab, les résultats de validation et les décisions prises lors des diagnostics.

## Environnement

- **Lab local** · VirtualBox, Windows Server 2022, Active Directory Domain Services (AD DS), DNS, DHCP, GPO, SMB et un client Windows 11.
- **Lab cloud** · Microsoft Entra ID est le premier module abordé. L’infrastructure Azure et l’intégration hybride sont prévues dans les modules suivants.

Le [schéma d’architecture](architecture/README.md) présente la topologie locale et les éléments à vérifier.

## Avancement des modules

| Module | État | Objectif |
| --- | --- | --- |
| [Active Directory local](00-On-Premises-Active-Directory/README.md) | En cours | Documenter le domaine Windows et vérifier sa configuration actuelle. |
| [Microsoft Entra ID](01-Microsoft-Entra-ID/README.md) | En cours | Gérer les identités, les accès et l’authentification dans un tenant cloud. |
| [Gouvernance Azure et RBAC](02-Azure-Governance-RBAC/README.md) | Prévu | Organiser les ressources et vérifier le principe du moindre privilège. |
| [Réseau Azure](03-Azure-Networking/README.md) | Prévu | Mettre en place une connectivité privée et diagnostiquer les flux réseau. |
| [Calcul Azure](04-Azure-Compute/README.md) | Prévu | Déployer et exploiter des VM en documentant les choix de disponibilité. |
| [Stockage Azure](05-Azure-Storage/README.md) | Prévu | Gérer les accès, la redondance et le cycle de vie des données. |
| [Supervision et sécurité](06-Monitoring-Security/README.md) | Prévu | Collecter la télémétrie, analyser les événements et examiner les recommandations de sécurité. |
| [Sauvegarde et reprise après sinistre](07-Backup-Disaster-Recovery/README.md) | Prévu | Vérifier la récupérabilité des données en chronométrant une restauration. |
| [Identité hybride](08-Hybrid-Identity/README.md) | Prévu | Relier un annuaire local vérifié à un tenant de test et valider la synchronisation. |

**Prévu** désigne un exercice planifié. **En cours** signifie que la pratique ou la documentation a commencé. **Validé** exige un résultat consigné et une preuve. Les exercices d’un même module peuvent avancer à des rythmes différents.

## Compétences techniques démontrées

- Interpréter les résultats historiques des tests de connectivité et de DNS d’un contrôleur de domaine.
- Distinguer la connectivité réseau de la découverte des services AD et identifier le résolveur incapable de répondre à la requête de localisation du domaine.

Le [cas de diagnostic DNS](troubleshooting/dns-domain-controller-discovery.md) détaille les observations et les vérifications restantes.

## Journal de progression

| Date | Étape |
| --- | --- |
| 2026-11-12 | Structure du portfolio, documentation initiale du lab local et du diagnostic DNS historique, début du travail sur Microsoft Entra ID. |

## Ressources du projet

[Architecture](architecture/README.md) · [Dépannage](troubleshooting/README.md) · [Captures d’écran](screenshots/README.md) · [Scripts](scripts/README.md) · [Modèle d’exercice](exercise-template.md)
