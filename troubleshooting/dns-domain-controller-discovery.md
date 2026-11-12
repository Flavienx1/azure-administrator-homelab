# Diagnostic DNS du contrôleur de domaine

**État du suivi** · En attente jusqu’au module 08

## Objectif technique et environnement

Analyser un échec du diagnostic DNS sur le contrôleur de domaine Windows Server 2022 du lab Active Directory sous VirtualBox. Ce cas concerne la configuration du domaine au moment de la collecte des diagnostics.

## Procédure de diagnostic

Le diagnostic historique a utilisé l’outil Windows `dcdiag`. Sa sortie comprenait les tests de connectivité et de DNS. La [liste des vérifications](../00-On-Premises-Active-Directory/evidence-checklist.md) indique les commandes ciblées pour refaire ces tests sur le lab actuel.

## Diagnostic

Le contrôleur de domaine a réussi le test de connectivité. Le test DNS à l’échelle de l’annuaire a échoué. La sortie indiquait que le résolveur externe ne parvenait pas à résoudre un enregistrement de service LDAP d’AD. Le résolveur interne renvoyait des enregistrements AD dans l’extrait examiné. Les clients utilisent ces enregistrements pour localiser les contrôleurs de domaine. Le choix du résolveur compte donc même lorsque la connectivité réseau de base fonctionne.

## Correctif et validation

Une réussite ultérieure du test DNS du domaine a été signalée. La modification exacte du résolveur et la sortie complète du test réussi restent à confirmer. La [liste des vérifications](../00-On-Premises-Active-Directory/evidence-checklist.md) décrit comment retester la configuration actuelle.

## Preuves et compétences

La sortie historique documente l’échec initial et permet de distinguer la connectivité réseau de la résolution DNS des services AD. La réussite ultérieure repose sur un résultat rapporté. Il reste à collecter une capture ou un extrait anonymisé du nouveau test.

[Liste des incidents](README.md)
