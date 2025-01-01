
# SMB

## Emplacement du fichier de configuration
Le fichier de configuration de Samba se trouve ici :  
`/etc/samba/smb.conf`

## Les commandes de bases pour le SMB

### Télécharger un fichier depuis le partage SMB

Pour télécharger les fichiers du SMB : 

```bash
get [nom_du_fichier]
```

### Lire le contenu d'un fichier (comme `cat`)

Pour lire le contenu d'un fichier sur le partage, utilisez la commande suivante : 

```bash
more [nom_du_fichier]
```

### Résumé de la configuration SMB

Pour obtenir un résumé de la configuration du serveur SMB (IP, version, etc.) : 

```bash
smbstatus
```

---

## Lister les partages disponibles

Utilisez la commande suivante pour afficher les partages disponibles :  

```bash
smbclient -N -L //10.129.14.128
```

## Se connecter à un partage spécifique

Utilisez la commande suivante pour se connecter à un partage spécifique :  

```bash
smbclient //10.129.14.128/[nom_du_partage]
```

