# Lab d’administration Azure

## Du support IT à l’administration Azure

J’ai commencé par le support IT N1/N2, puis j’ai obtenu la certification Microsoft Azure Fundamentals (AZ-900). J’ai lancé ce lab pour mettre les notions Azure en pratique. En entreprise, je veux savoir donner les bons accès, vérifier qu’une configuration fait ce que j’attends et remonter à la cause d’un incident avec les journaux. Je vise d’abord un poste d’administrateur Azure, puis je veux évoluer vers le cloud engineering et le DevOps.

J’ai commencé par [Microsoft Entra ID](01-Microsoft-Entra-ID/README.md). J’y ai terminé les exercices pratiques sur les comptes, les groupes et l’authentification. J’ai aussi suivi une connexion refusée jusqu’à sa cause : un compte désactivé. Je passerai ensuite à la [gouvernance Azure et au RBAC](02-Azure-Governance-RBAC/README.md) pour apprendre à organiser les ressources et à attribuer les droits au bon niveau.

J’ai mis en pause mon [lab Active Directory local](00-On-Premises-Active-Directory/README.md). Je reprendrai SRV01 dans le [module 08 — Identité hybride](08-Hybrid-Identity/README.md) pour travailler sur l’intégration entre AD DS et Microsoft Entra ID.

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

## Un premier diagnostic dans mon lab local

Dans mes essais sur le contrôleur de domaine, j’ai distingué la connectivité réseau de la découverte des services AD. J’ai identifié le résolveur qui ne répondait pas à la requête de localisation du domaine. J’ai gardé mes observations et les vérifications à reprendre dans le [cas de diagnostic DNS](troubleshooting/dns-domain-controller-discovery.md).

## Journal de progression

| Date | Étape |
| --- | --- |
| 2026-11-12 | J’ai structuré le portfolio, documenté le lab local et le diagnostic DNS, puis commencé Microsoft Entra ID. |
| 2026-11-12 | J’ai donné la priorité aux modules Azure 01 à 07 et mis le lab local de côté jusqu’au module 08. |
| 2026-11-18 | J’ai terminé les exercices Entra ID et documenté mes résultats avec les captures du lab. J’ai choisi la gouvernance Azure et le RBAC comme prochaine étape. |

## Ressources du projet

[Architecture](architecture/README.md) · [Dépannage](troubleshooting/README.md) · [Captures d’écran](screenshots/README.md) · [Scripts](scripts/README.md) · [Modèle d’exercice](exercise-template.md)
