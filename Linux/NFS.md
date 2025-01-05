# NFS (Système de fichiers en réseau) - Guide Récapitulatif

## Afficher les Partages NFS Disponibles
Pour lister tous les partages NFS disponibles sur un serveur distant :
```bash
showmount -e [ip]
```

---

## Monter un Partage NFS
1. Créez un répertoire qui servira de point de montage :
   ```bash
   mkdir target-NFS
   ```

2. Montez le partage NFS dans le répertoire cible :
   ```bash
   sudo mount -t nfs [ip]:/ ./target-NFS/ -o nolock
   ```

3. Accédez au répertoire monté :
   ```bash
   cd target-NFS
   ```

4. Explorez la structure du répertoire :
   ```bash
   tree .
   ```

---

## Démonter le Partage NFS
Pour démonter le partage NFS en toute sécurité :
```bash
sudo umount ./target-NFS
```
