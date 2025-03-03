# John The Ripper

## 📌 Présentation
John The Ripper (JTR) est un outil de cassage de mots de passe open-source utilisé pour tester la robustesse des mots de passe en les comparant à des dictionnaires ou en utilisant des attaques de force brute.

## 🛠️ Installation
Sur Kali Linux, JTR est préinstallé. Pour vérifier :
```bash
john --help
```
Si ce n'est pas le cas :
```bash
sudo apt update && sudo apt install john -y
```

## 📂 Formats supportés
JTR supporte de nombreux formats comme :
- **/etc/shadow** (Linux)
- **NTLM, LM** (Windows)
- **ZIP, RAR, PDF, SSH** (fichiers protégés par mot de passe)
- **NTLMv2** (capturé avec Responder)

## 🚀 Utilisation de base

### 🔍 1. Cracker un hash simple
```bash
john --format=<FORMAT> --wordlist=<liste_de_mots> <fichier_hash>
```
Exemple pour NTLM :
```bash
john --format=NT --wordlist=/usr/share/wordlists/rockyou.txt hashes.txt
```

### ⚡ 2. Casser un mot de passe avec attaque par force brute
```bash
john --incremental <fichier_hash>
```

### 💜 3. Afficher les mots de passe déjà cassés
```bash
john --show <fichier_hash>
```

### 🔄 4. Générer un hash pour tester
Exemple pour SHA-512 :
```bash
echo -n "password" | sha512sum
```

## 🎯 Exemples avancés

### 🏴‍☠️ Casser des hashes Windows récupérés avec Responder
```bash
john --format=netntlmv2 --wordlist=/usr/share/wordlists/rockyou.txt hashes.txt
```

### 🛆 Casser un fichier ZIP protégé par mot de passe
1. Extraire le hash avec `zip2john`
```bash
zip2john archive.zip > hash.txt
```
2. Casser le mot de passe
```bash
john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
```