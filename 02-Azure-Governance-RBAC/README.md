# Gouvernance Azure et RBAC

**État du module** · Prochain module

## Qui peut faire quoi, et à quel niveau ?

Dans Entra ID, j’ai attribué un rôle d’annuaire. Cette fois, je veux comprendre où attribuer un rôle Azure RBAC et jusqu’où les droits hérités s’appliquent. Je commencerai par dessiner la hiérarchie : tenant, groupes d’administration, abonnements, groupes de ressources et ressources.

Je testerai ensuite l’héritage d’un rôle. Avec une identité aux droits limités, je tenterai une action qui devrait être refusée. Ce test m’aidera à vérifier que j’ai accordé juste les droits nécessaires.

Je poserai des tags, puis j’utiliserai Azure Policy en mode audit pour voir ce qui remonte comme conforme ou non conforme. J’ajouterai un verrou pour vérifier son effet. Enfin, je configurerai une alerte budgétaire et je noterai les coûts prévisionnels.

Je consignerai mes réglages et mes résultats dans le [modèle d’exercice](../exercise-template.md).

[Accueil du portfolio](../README.md)
