Moteur de référence pour OSINT et reconnaissance passive.

Contrairement à Google qui indexe le contenu textuel des pages web, Shodan scanne en permanence l'ensemble du réseau IPv4/IPv6 mondial pour répertorier tous les équipements directement connectés à Internet (serveurs, routeurs, objets connectés IoT, caméras, bases de données, automates industriels SCADA).

## Comment ça fonctionne ?

Shodan envoie des requêtes en continu sur des milliers de ports réseau à travers le monde. Lorsqu'une machine répond, Shodan enregistre sa bannière (header HTTP, en-tête SSH/FTP, certificat SSL, version du système d'exploitation, etc.).


![image shodan](/home/lisa/Documents/Cybersécurité-GitHub/cybersecurity-learning/wiki-images/Shodan-exemple.png)


## Pourquoi c'est un outil puissant ?

- Reconnaissance 100 % passive : En phase d'audit (Red Team), Shodan te permet d'étudier la surface d'attaque d'une cible sans envoyer le moindre paquet depuis ton IP. Aucun risque de déclencher les alertes d'un IDS/IPS chez la cible.
- Chasse aux vulnérabilités (CVE) : Comme le montre la recherche apache 2.4.1 sur la capture d'écran, tu peux identifier instantanément tous les serveurs dans le monde qui font tourner une version obsolète ou vulnérable d'un logiciel.
- Détection de fuites de données : C'est l'outil n°1 pour repérer des bases de données de production (Elasticsearch, MongoDB) exposées sur Internet sans aucun mot de passe.
- Audit de sa propre infrastructure (Blue Team) : Les équipes de défense l'utilisent pour vérifier qu'un composant critique de leur réseau n'a pas été exposé par erreur sur Internet par un administrateur.


Filtre | Rôle | Exemple 
----
`country:` | Filtre par xode pays | `country:FR`
`org:` | Recherche par nom d'organisation/entreprise | `org:"DigitalOcean`
`product:` | Cible un logiciel précis | `product:"OpenSSH"
`version:` | Spécifie la version exacte du service | `product:"2.4.1"`
`port:` | Filtre par numéro de port | `port:3389`
`has_screenshot` | Affiche uniquement les cibles avec captures d'écran | `hasscreenshot:true` (utile pour RDP/VNC/Caméras)


C'est une ressource incontournable pour la reconnaissance réseau et l'OSINT.
