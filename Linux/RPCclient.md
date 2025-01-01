
# RPCclient

**Accès aux ressources partagées** comme **SMB**, etc.

## Commandes de base pour le RPC

### 1. **Informations sur le serveur**

#### `srvinfo`
Affiche des informations sur le serveur distant, telles que son nom, sa version, et d'autres paramètres de configuration.

```bash
srvinfo
```

### 2. **Lister les domaines**

#### `enumdomains`
Cette commande permet d'énumérer tous les domaines présents dans le réseau.

```bash
enumdomains
```

### 3. **Obtenir des informations sur un domaine**

#### `querydominfo`
Fournit des informations détaillées sur le domaine, le serveur et l'utilisateur du domaine déployé.

```bash
querydominfo
```

### 4. **Lister les partages**

#### `netshareenumall`
Cette commande énumère tous les partages disponibles sur le serveur distant.

```bash
netshareenumall
```

### 5. **Obtenir des informations sur un partage spécifique**

#### `netsharegetinfo <share>`
Fournit des informations détaillées sur un partage spécifique. Remplacez `<share>` par le nom du partage pour obtenir des informations comme la taille, les permissions, etc.

```bash
netsharegetinfo <share>
```

### 6. **Lister les utilisateurs du domaine**

#### `enumdomusers`
Énumère tous les utilisateurs d'un domaine donné. Utile pour récupérer les informations d'authentification possibles.

```bash
enumdomusers
```

### 7. **Obtenir des informations sur un utilisateur spécifique**

#### `queryuser <RID>`
Fournit des informations détaillées sur un utilisateur spécifique, en remplaçant `<RID>` par l'identifiant d'utilisateur (Relative Identifier).

```bash
queryuser <RID>
```

### 8. **Lire le contenu d'un fichier (comme `cat`)**

#### `enumdomains`
Cette commande permet de lire le contenu d'un fichier, similaire à la commande `cat` sous Linux.

```bash
enumdomains
```

### 9. **Obtenir un résumé de la configuration SMB**

#### `smbstatus`
Fournit un résumé de l'état actuel des connexions SMB, y compris les IP, la version SMB, les utilisateurs connectés, et plus encore.

```bash
smbstatus
```
---

