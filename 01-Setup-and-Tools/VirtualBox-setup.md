How to install a virtual machine - KaliLinux with Virtual Box

## Installer une machine virtuelle pour les CTF et projets offre des avantages :

	- accéder à linux même sur Windows ou Mac
	- outils Linux : certains préinstallés
	- en cas de problème (script malvaillant, erreur de configuration ...), seule la machine virtuelle est impacté, pas le PC
	- Snapshots : capturer l'état de la machine dans le temps, donc si problème, revenir sur un état passé de la machine.


# Installer sa Virtual Machine

Installation depuis le logiciel VirtualBox : https://www.virtualbox.org/


## KaliLinux

"Installer Images", puis télécharger Kali Linux : https://www.kali.org/get-kali/#kali-platforms


# Logiciels utiles Linux

- tor : accéder au darkweb
- nmap : exploration réseau, reconnaissance
- metasploit-framework : base de donnée qui répertorie différents exploid et qui permet de les lancer sur des cibles directement --- `msfconsole` pour lancer
- aircrack-ng : suite de sécurité pour tester la sécurité des réseaux wifi
- jonh (john the ripper) : craquage de mdp - tester la robustesse d'une mdp
- sqlmap : détection et exploitation de vulnérabilité injections SQL - app web
- maltego : reconnaissance , collecte infos
- hydra : bruit de force et crackage de mdp

### Usage app direct

- **wireshark** : analyse réseau - analyser connexion en court
- **burpsuite** : pour tester sécurité app web
- **zaproxy** : trouver vulnérabilité et scan auto pour app web

### ASTUCE : quand on ne connait pas le nom du paquet à télécharger : 
`apt -cash search aircrack`


# Vidéos intéréssantes pour comprendre comment installer et le paramêtrer :

- Installation : https://youtu.be/nvpkGJ-zYyU?si=q6VJIgQ6zn18uCeV
- Après installation - app utiles : https://youtu.be/ndeyY8w8OYA?si=wD9koMnBgpqiC4LZ


