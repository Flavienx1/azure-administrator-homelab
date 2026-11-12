# Vérifications et preuves du lab Active Directory

Pour chaque test, noter la date, la machine et le résultat observé. Dans les exemples publiés, utiliser un nom de domaine anonymisé et masquer les noms de comptes, les détails réseau de l’hôte et les informations sans rapport avec le test.

| Périmètre | Vérification à effectuer | Preuve à collecter |
| --- | --- | --- |
| Contrôleur de domaine | Sur le serveur, exécuter `hostname`, `Get-ADDomain \| Select-Object DNSRoot,NetBIOSName` et `Get-WindowsFeature AD-Domain-Services,DNS,DHCP`. | Identité anonymisée du domaine et liste des rôles installés. |
| DNS AD et connectivité | Sur le serveur, exécuter `dcdiag /test:dns`. Sur le client, vérifier `ipconfig /all` et lancer `Resolve-DnsName -Type SRV "_ldap._tcp.dc._msdcs.<current-ad-domain>"` en remplaçant le paramètre par le domaine actuel. | Résumé du test serveur et réponse SRV du client. Vérifier également le mode réseau dans VirtualBox. |
| DHCP | Si le serveur du lab fournit le service DHCP, comparer les options d’étendue et le bail avec la sortie de `ipconfig /all` sur Windows 11. | Étendue, option DNS et bail client anonymisés. |
| Jonction de Windows 11 | Sur le client, exécuter `Get-CimInstance Win32_ComputerSystem \| Select-Object Domain,PartOfDomain`. Après la jonction, lancer `Test-ComputerSecureChannel` dans une session PowerShell élevée et tester la connexion d’un utilisateur du domaine. | Appartenance au domaine, résultat du canal sécurisé et preuve de connexion anonymisée. |
| GPO | Identifier un paramètre de stratégie et l’OU à laquelle la GPO est liée. Exécuter `gpresult /r` dans la session de l’utilisateur concerné et vérifier l’effet du paramètre. | Lien de la GPO, stratégie appliquée et effet constaté. |
| Groupes de sécurité | Choisir un groupe de test et une ressource protégée. Comparer les accès d’un compte membre et d’un compte hors du groupe après réouverture des sessions. | Appartenance anonymisée, attribution des droits et résultats d’accès autorisé et refusé. |
| Incident DNS historique | Confirmer le changement de résolveur effectué à l’époque si une trace existe. | Sorties anonymisées avant et après, si disponibles. |
| Historique de configuration | Confirmer les étapes d’installation et de configuration des rôles serveur, du domaine, du DHCP, des GPO, des groupes et de la VM cliente. | Notes ou captures d’origine, avec les dates connues. |

## Captures à collecter

1. Paramètres réseau VirtualBox des deux VM, avec les détails de l’interface hôte masqués.
2. Rôles serveur et identité anonymisée du domaine, puis zone DNS AD ou résultat de la requête SRV sur le client.
3. Étendue et bail DHCP si le service est hébergé sur le serveur du lab.
4. Appartenance de Windows 11 au domaine et résultat du test du canal sécurisé.
5. Lien d’une GPO et effet constaté sur le client.
6. Partage SMB, permissions NTFS et résultats des tests d’accès autorisé et refusé.

Consulter les [consignes de publication](../screenshots/README.md) avant d’ajouter des captures.

[Lab Active Directory](README.md)
