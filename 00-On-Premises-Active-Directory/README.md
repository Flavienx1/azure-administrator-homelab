# Lab Active Directory local

**État** · En attente

La documentation et les diagnostics historiques sont conservés. Les vérifications du lab SRV01 reprendront au [module 08 — Identité hybride](../08-Hybrid-Identity/README.md), en préparation de l’intégration avec Microsoft Entra ID.

## Objectif technique

Construire et valider un domaine Windows permettant la découverte du contrôleur de domaine, la jonction d’un client, l’accès par groupe et l’application de stratégies. Établir une base vérifiée pour les futurs exercices d’identité hybride.

## Architecture et prérequis

L’environnement décrit utilise VirtualBox, une VM Windows Server 2022 et une VM cliente Windows 11. Le serveur a tenu le rôle de contrôleur de domaine AD DS et de serveur DNS. DHCP, les GPO et les groupes de sécurité font partie du périmètre déclaré.

Le [schéma d’architecture](../architecture/README.md) présente les composants. La vérification du nom de domaine, du mode réseau, de la configuration DHCP et de la jonction du client reste à effectuer.

Le client a besoin d’une édition de Windows prenant en charge la jonction à un domaine AD, d’une connexion réseau au contrôleur et d’un résolveur capable d’interroger la zone DNS AD.

## Concepts

AD DS gère les identités du domaine et leur authentification. Les enregistrements DNS SRV permettent au client de localiser un contrôleur de domaine. DHCP fournit les paramètres IP et, selon la configuration, l’adresse du résolveur DNS. Les groupes de sécurité permettent d’attribuer les accès selon les rôles. Les GPO appliquent des paramètres selon leur portée et leur filtrage.

## Configuration réalisée

Les sorties de diagnostic historiques identifient le contrôleur de domaine et montrent des enregistrements AD renvoyés par le DNS interne. Les étapes et paramètres exacts de la promotion restent à confirmer. Une VM Windows 11 a été mise en place et une mise à jour de la configuration du domaine a été signalée après ces diagnostics. Le nom actuel du domaine et l’appartenance du client restent à vérifier.

Le [cas de dépannage DNS](../troubleshooting/dns-domain-controller-discovery.md) présente l’échec observé et le suivi. La [liste des vérifications](evidence-checklist.md) donne les commandes à exécuter sur la configuration actuelle.

## Captures d’écran et preuves

Les extraits des diagnostics historiques ont été examinés. La liste des vérifications précise quelles captures et sorties de commandes collecter sur le lab actuel.

## Validation et résultats

| Vérification | Résultat observé | Preuve |
| --- | --- | --- |
| Connectivité du contrôleur de domaine lors du diagnostic historique | Réussite | Extrait du test `Connectivity` |
| Test DNS historique | Échec initial, puis réussite signalée | Sortie historique et résultat rapporté |
| Domaine actuel et jonction du client | À vérifier | Identité du serveur, appartenance au domaine et canal sécurisé |
| DHCP, GPO et accès par groupe sur le lab actuel | À vérifier | Bail, stratégie appliquée et tests d’accès |

## Incidents et résolution

Voir le [diagnostic DNS du contrôleur de domaine](../troubleshooting/dns-domain-controller-discovery.md).

## Compétences démontrées

Les sorties historiques permettent de documenter la lecture des diagnostics d’un contrôleur de domaine et l’identification d’un résolveur incapable de répondre aux requêtes sur les enregistrements de service AD.

## Vérifications reportées au module 08

- Vérifier AD DS et le DNS côté serveur et côté client.
- Confirmer la jonction de Windows 11, le canal sécurisé et la connexion d’un utilisateur du domaine.
- Valider un bail DHCP, l’application d’une GPO et les accès SMB attribués par groupe.
- Consigner les résultats des exercices de diagnostic DNS, DHCP, SMB et RDP déjà pratiqués lorsque les preuves sont disponibles.

[Accueil du portfolio](../README.md)
