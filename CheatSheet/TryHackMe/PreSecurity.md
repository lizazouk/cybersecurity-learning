![TryHackMe](https://img.shields.io/badge/TryHackMe-990000?style=for-the-badge&logo=tryhackme&logoColor=white)

# "Pre Security" - début 01/04/2026

*Cours THM pour apprendre les basics de l'informatique et de la cybersécurté*

---

# LAN - Réseau Local

**LAN** : Local Area Network

Dans un premier temps, comprenons ce que c'est : ensemble d'entités interconnectés. Il en existe plusieur (réseau de transport, téléphonique, neurones ...), et celui qui nous intéresse est le **Réseau Informatique**, cad, des ordinateurs reliés entre eux grâce à des lignes physiques échangeant des informations sous forme de données numériques (communications, ressources ...)

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


### Switch




### Router
