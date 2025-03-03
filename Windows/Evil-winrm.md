# Evil-WinRM

## 📌 Présentation
Evil-WinRM est un outil permettant d'obtenir un accès interactif sur des machines Windows via le protocole WinRM (Windows Remote Management), souvent utilisé dans les environnements Active Directory.

## 🛠️ Installation
Sur Kali Linux, Evil-WinRM peut être installé avec :
```bash
sudo apt install evil-winrm -y
```
Ou via Ruby :
```bash
gem install evil-winrm
```

## 🚀 Utilisation de base

### 🔗 1. Se connecter à une machine Windows avec des identifiants valides
```bash
evil-winrm -i <IP_TARGET> -u <USER> -p <PASSWORD>
```
Exemple :
```bash
evil-winrm -i 192.168.1.100 -u Administrateur -p P@ssw0rd
```

### 🔑 2. Se connecter avec un fichier de clé privée
```bash
evil-winrm -i 192.168.1.100 -u Administrateur -k key.pem
```

### 📦 3. Télécharger et exécuter un script PowerShell
```bash
evil-winrm -i 192.168.1.100 -u Admin -p password -s /chemin/script.ps1
```

