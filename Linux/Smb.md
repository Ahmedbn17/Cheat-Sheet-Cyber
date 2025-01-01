# SMB

## Emplacement du fichier de configuration
Le fichier de configuration de Samba se trouve ici :  
`/etc/samba/smb.conf`

---

## Lister les partages disponibles

Utilisez la commande suivante pour afficher les partages disponibles :  

```bash
smbclient -N -L //10.129.14.128
