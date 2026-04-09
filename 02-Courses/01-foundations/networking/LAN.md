# LAN - Réseau Local

**LAN** : Local Area Network

Un réseau est un ensemble d'entités interconnectés. Il en existe plusieur (réseau de transport, téléphonique, neurones ...), et celui qui nous intéresse est le **Réseau Informatique**, cad, des ordinateurs reliés entre eux grâce à des lignes physiques échangeant des informations sous forme de données numériques (communications, ressources ...)

Il peut se présenter sous plusieurs formes : **Topologies**

### Topologies

- **Star Topology** (en étoile) : Tous les ordinateurs sont reliés à un *concentrateur*
- **Bus Topology** (en bus) : Tous les ordinateurs sont reliés à une même ligne de transmission
- **Ring Topology** (en anneau) : Les ordinateurs sont situés sur une boucle
- **Tree Topology** (en maille) : Chaque machine est reliée à toutes les autres par un câble

![SchémasTopologies](https://github.com/lizazouk/cybersecurity-learning/blob/main/wiki-images/LANtopology.gif?raw=true)


TOPOLOGY |AVANTAGES | INCONVÉNIENTS 
---------|----------|----------------
STAR (Le plus couramment utilisé)  |  Fiable, Extensible  |  Coûteux, + de machines = + de maintenance, sujet aux défaillances et depannage pouvant devenir compliqué : si la centrale tombe en panne, les appareils connectés ne pourront plus transmettre ou recevoir les données
BUS  |  Facile, installation peu cher  |  Lent si plusieurs machines demandent des données simultanément, embouteillages. Difficile d'identifier quelle machine est défectueuse. Si le câcle principal lâche, les données ne peuvent plus du tout circuler.
RING | Peu de câcle nécessaire, pas de matériel central coûteux. Peu cher. Une seule direction, localisation de fail simplifiée. Moins d'embouteillages, données circulents de manière ordonnée. |   Lent, l'information doit traverser toute les machines inutilement avant d'arriver à destination. Un câcle ou machine défecteuse, la boucle est rompue. Les machines envoies leurs propres données avant de faire passer celles des autres, créant du retard.


### Switch - commutateur

Boitier central ; connecter plusieurs appareils entre eux à l'aide de câbles ethernets. Dirige les données précisément vers le bon destinataire = réseau fluide et rapide

Plus intelligent qu'un Hub (répartiteur):
HUB  |  Switch
-----|---------
Message reçu = transmit à tout le monde sur le réseau. Trafic inutile et ralentit tout  | Liste interne pour savoir quelle machine est connectée à quel port, donc envoie direct.

![SwitchSystem](https://github.com/lizazouk/cybersecurity-learning/blob/main/wiki-images/THM_PreSecurityPath/2504bf9d718556c764c28843f43febe0.png?raw=true)

Le fait de connecter les switchs à des routeurs, créait une redondance. Si un chemin tombre, un autre est possible.
Réseau continuellement actif mais chemin de secours peut parfois être plus long ou lent.

### Router

Pont entre les réseaux. Connecter le réseau LAN au reste du monde WAN (internet).

Le Routage (routing) est le processus qui consiste à choisir le meilleur chemin pour les donées :

- chercher le chemin le plus court
- observer l'état du trafic (saturé, en panne)
- trouver un chemin avec la meilleure connexion

![routersystem](https://github.com/lizazouk/cybersecurity-learning/blob/main/wiki-images/THM_PreSecurityPath/router.png?raw=true)

