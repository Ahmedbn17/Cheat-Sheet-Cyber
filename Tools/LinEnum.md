# LinEnum - Installation et Utilisation

## Qu'est-ce que LinEnum ?
LinEnum est un script automatisé qui permet de collecter rapidement des informations sur un système Linux. Il est principalement utilisé en évaluation de la sécurité pour identifier des failles potentielles et des vecteurs d'escalade de privilèges.

---

## Installation de LinEnum
1. **Clonez le dépôt GitHub LinEnum** :
   ```bash
   git clone https://github.com/rebootuser/LinEnum.git
   ```

2. **Naviguez dans le répertoire cloné** :
   ```bash
   cd LinEnum
   ```

3. **Rendez le script exécutable** :
   ```bash
   chmod +x LinEnum.sh
   ```

---

## Utilisation de LinEnum
**Exécutez le script sur le système cible** :
   ```bash
   ./LinEnum.sh -r report.txt
   ```
   - L'option `-r` permet de sauvegarder les résultats dans un fichier texte (pas obligatoire on peut ecrire juste ./LinEnum.sh).
