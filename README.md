# Lab d’administration Azure

Je développe ce portfolio pour documenter ma pratique de l’administration système et cloud. Mon parcours va du support IT N1/N2 vers les fonctions d’administrateur Azure, de Cloud Engineer puis de DevOps Engineer. J’ai obtenu la certification Microsoft Azure Fundamentals (AZ-900). Ce dépôt rassemble les configurations du lab, les résultats de validation et les décisions prises lors des diagnostics.

## Priorité actuelle

Les exercices pratiques du [module 01 — Microsoft Entra ID](01-Microsoft-Entra-ID/README.md) sont terminés. Le prochain module est la [gouvernance Azure et le RBAC](02-Azure-Governance-RBAC/README.md).

La [documentation Active Directory locale](00-On-Premises-Active-Directory/README.md) est conservée en attente. Le lab SRV01 sera repris au [module 08 — Identité hybride](08-Hybrid-Identity/README.md) pour travailler sur l’intégration entre AD DS et Microsoft Entra ID.

## Avancement des modules

| Module | État | Objectif |
| --- | --- | --- |
| [Active Directory local](00-On-Premises-Active-Directory/README.md) | En attente | Reprendre la validation du lab local au module 08. |
| [Microsoft Entra ID](01-Microsoft-Entra-ID/README.md) | Exercices pratiques terminés | Gérer les identités, les accès et l’authentification dans un tenant cloud. |
| [Gouvernance Azure et RBAC](02-Azure-Governance-RBAC/README.md) | Prochain module | Organiser les ressources et vérifier le principe du moindre privilège. |
| [Réseau Azure](03-Azure-Networking/README.md) | Prévu | Mettre en place une connectivité privée et diagnostiquer les flux réseau. |
| [Calcul Azure](04-Azure-Compute/README.md) | Prévu | Déployer et exploiter des VM en documentant les choix de disponibilité. |
| [Stockage Azure](05-Azure-Storage/README.md) | Prévu | Gérer les accès, la redondance et le cycle de vie des données. |
| [Supervision et sécurité](06-Monitoring-Security/README.md) | Prévu | Collecter la télémétrie, analyser les événements et examiner les recommandations de sécurité. |
| [Sauvegarde et reprise après sinistre](07-Backup-Disaster-Recovery/README.md) | Prévu | Vérifier la récupérabilité des données en chronométrant une restauration. |
| [Identité hybride](08-Hybrid-Identity/README.md) | En attente | Relier un annuaire local vérifié à un tenant de test et valider la synchronisation. |

**Prévu** désigne un exercice planifié. **Prochain module** indique la prochaine étape du parcours. **En attente** désigne un travail reporté à la phase d’identité hybride. Les preuves et limites de chaque exercice figurent dans sa documentation. Les exercices d’un même module peuvent avancer à des rythmes différents.

## Compétences documentées dans le lab local

- Interpréter les résultats historiques des tests de connectivité et de DNS d’un contrôleur de domaine.
- Distinguer la connectivité réseau de la découverte des services AD et identifier le résolveur incapable de répondre à la requête de localisation du domaine.

Le [cas de diagnostic DNS](troubleshooting/dns-domain-controller-discovery.md) détaille les observations et les vérifications restantes.

## Journal de progression

| Date | Étape |
| --- | --- |
| 2026-11-12 | Structure du portfolio, documentation initiale du lab local et du diagnostic DNS historique, début du travail sur Microsoft Entra ID. |
| 2026-11-12 | Priorité aux modules Azure 01 à 07. Microsoft Entra ID devient le module actif et le lab local est reporté au module 08. |
| 2026-11-18 | Exercices pratiques Microsoft Entra ID terminés. Documentation des résultats et des captures du lab. Gouvernance Azure et RBAC désigné comme prochain module. |

## Ressources du projet

[Architecture](architecture/README.md) · [Dépannage](troubleshooting/README.md) · [Captures d’écran](screenshots/README.md) · [Scripts](scripts/README.md) · [Modèle d’exercice](exercise-template.md)
