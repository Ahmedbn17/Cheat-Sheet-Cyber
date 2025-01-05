# Installation des Wordlists RockYou et SecLists

## Qu'est-ce qu'une Wordlist ?
Une wordlist est un fichier contenant une liste de mots utilisés principalement dans des attaques par force brute ou pour tester la robustesse des mots de passe.

---

## Installation de RockYou

### À propos de RockYou
La wordlist "RockYou" contient des millions de mots de passe compromis issus de fuites de données et est souvent utilisée pour des tests d'attaque par dictionnaire.

### Étapes d'installation :
1. **Accédez à la wordlist RockYou** :
   - Elle est présente par défaut sur Kali Linux dans le fichier compressé : `/usr/share/wordlists/rockyou.txt.gz`

2. **Décompressez le fichier** :
   ```bash
   gzip -d /usr/share/wordlists/rockyou.txt.gz
   ```

3. **Utilisez la wordlist** :
   - Le fichier décompressé est situé à : `/usr/share/wordlists/rockyou.txt`

---

## Installation de SecLists

### À propos de SecLists
SecLists est une collection complète de wordlists contenant des listes pour les tests de pénétration, y compris des utilisateurs, des mots de passe, des URL, etc.

### Étapes d'installation :
1. **Clonez le dépôt GitHub de SecLists** :
   ```bash
   git clone https://github.com/danielmiessler/SecLists.git
   ```

2. **Naviguez dans le répertoire cloné** :
   ```bash
   cd SecLists
   ```

3. **Accédez aux wordlists** :
   - Les fichiers sont organisés par catégorie (mots de passe, noms d'utilisateur, etc.) dans des sous-dossiers.
   - Exemple :
     ```bash
     ls Passwords/
     ```
