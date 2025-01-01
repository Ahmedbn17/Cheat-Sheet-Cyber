#Samrdump.py récupere des infos sur smb

Ce script permet de lister les utilisateurs locaux et de récupérer des informations sur les comptes d'utilisateurs d'un serveur Windows via SMB, y compris :

Les utilisateurs du domaine : Il peut afficher les utilisateurs locaux sur la machine cible.

Les groupes d’utilisateurs : Le script peut récupérer des informations sur les groupes et les membres associés.

Les informations sur les mots de passe : Bien que le script ne récupère pas directement les mots de passe en clair, il peut récupérer des hachages ou des informations associées aux comptes d’utilisateurs, qui peuvent ensuite être utilisées pour des attaques comme le pass-the-hash.

```bash
samrdump.py 10.129.14.128
```