# SMB

## Emplacement du fichier de configuration
Le fichier de configuration de Samba se trouve ici :  
`/etc/samba/smb.conf`

## Les commandes de bases pour le SMB

Pour télécharger les fichiers du SMB : 

```bash
get [nom_du_fichier]
```

Pour lire le contenue du fichier (comme cat) : 

```bash
more [nom_du_fichier]
```

Pour avoir un résumer de la conf du smb (ip,version,...) : 

```bash
smbstatus
```

---

## Lister les partages disponibles

Utilisez la commande suivante pour afficher les partages disponibles :  

```bash
smbclient -N -L //10.129.14.128
```

## Lister les partages disponibles

Utilisez la commande suivante pour se connecter à un partage :  

```bash
smbclient //10.129.14.128/[nom_du_partage]
```