#Dig

`dig` (Domain Information Groper) est un outil de ligne de commande utilisé pour interroger les serveurs DNS et effectuer des diagnostics. Voici les principales commandes et leur usage.

---

## Commandes de base

### 1. Requête de base pour un enregistrement A
```bash
dig A <nom_de_domaine>
```
- **Utilité** : Retourne l'adresse IPv4 associée au domaine.
- **Exemple** : 
  ```bash
  dig A www.google.com
  ```

### 2. Requête pour un enregistrement spécifique
```bash
dig <type_d_enregistrement> <nom_de_domaine>
```
- **Utilité** : Permet de rechercher des informations précises.
- **Types courants** :
  - `A` : Adresse IPv4 du domaine.
  - `AAAA` : Adresse IPv6 du domaine.
  - `MX` : Serveurs de messagerie.
  - `NS` : Serveurs de noms.
  - `TXT` : Informations textuelles, souvent pour des vérifications de sécurité ou d'authentification.
  - `CNAME` : Alias d'un domaine.
  
### 3. Requête inverse (PTR)
```bash
dig -x <adresse_ip>
```
- **Utilité** : Effectue une recherche inversée pour obtenir le nom de domaine associé à une adresse IP.

### 4. Requête avec un serveur DNS spécifique
```bash
dig @<serveur_dns> <nom_de_domaine>
```
- **Utilité** : Utilise un serveur DNS particulier pour effectuer la requête.
- **Exemple** : 
  ```bash
  dig @8.8.8.8 www.google.com
  ```

### 5. Affichage détaillé des résultats
```bash
dig +short <nom_de_domaine>
```
- **Utilité** : Affiche des résultats simplifiés, avec uniquement les informations essentielles (adresse IP, etc.).

### 6. Afficher des détails complets (y compris les sections supplémentaires)
```bash
dig +all <nom_de_domaine>
```
- **Utilité** : Affiche une sortie détaillée incluant les enregistrements supplémentaires et d'autres informations liées.

### 7. Recherche des serveurs de noms
```bash
dig NS <nom_de_domaine>
```
- **Utilité** : Affiche les serveurs de noms (DNS) associés à un domaine.
  
### 8. Obtenir les enregistrements MX
```bash
dig MX <nom_de_domaine>
```
- **Utilité** : Affiche les serveurs de messagerie associés à un domaine.

---

## Options avancées

### 1. Délai d'attente personnalisé
```bash
dig +time=<délai> <nom_de_domaine>
```
- **Utilité** : Permet de définir un délai d'attente en secondes avant que la commande échoue.

### 2. Vérifier l'utilisation du DNS pour un domaine spécifique
```bash
dig +trace <nom_de_domaine>
```
- **Utilité** : Affiche l'ensemble du processus de résolution DNS, en montrant les serveurs DNS utilisés et le chemin emprunté jusqu'à l'adresse IP.

### 3. Requête pour un enregistrement DNS spécifique avec un type de query
```bash
dig <type_d_enregistrement> <nom_de_domaine> +noall +answer
```
- **Utilité** : Affiche uniquement les informations de la section réponse, excluant les sections supplémentaires ou d'autorité.

---
