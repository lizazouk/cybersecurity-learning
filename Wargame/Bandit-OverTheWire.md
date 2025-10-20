# Bandit - wargame Overthewire
https://overthewire.org/wargames/bandit/

Voici ce que j'ai pu apprendre niveaux par niveaux, ainsi que les difficultés que j'ai pu rencontrer


Niveau | Apprentissage | Commandes | Dificultés rencontrées et astuces
------|----------------|----------|-----
0-1 | Se connecter au serveur en utilisant le SSH depuis un terminal | ls, cat
1-2 | Lire un fichier avec caractère spécial "-" | cat ./-file
2-3 | Ouvrir un fichier comportant des espaces | cat "file with spaces" | Dans ce niveau, le dossier à ouvrir comporte "--" au début, ce qui fait que celui-ci est considéré comme une option par le terminal. <br> **Astuce**: Ajouter "--" avant d'écrire le nom du fichier. Ce qui donne : $ cat -- "--file with spaces"
3-4 | Se diriger dans un dossier et voir tous les fichiers, ceux cachés aussi | cd, ls -al | cd : change directory
4-5 | Découvrir le type de fichier pour ouvrir le seule lisible par l'humain | file ./-file* | Ici, les fichiers commences tous par un "-", donc on utilise la technique de "./-file". <br> **Astuce**: l'étoile de permet de dire "tout ce qui suit". Donc ici, la commande nous permet de voir l'origine de tous les fichiers comportant "-file" et tout ce qui suit. Le seul fichier lisible par les humains est un ASCII text dans ce context.
5-6 | Trouver un fichier avec plusieurs propriétés connues ; taille, human-readable, not executable | find -size 1033c | Cette technique permet d'aller plus rapidement car il n'y a qu'un fichier de cette taile. <br> **Pour compléter** : Recherche avec tous les critères; **$ find -type f ! -readable -executable -size 1033c** <br> <br> **Ce qui signifie** : <br> -type f — seulement les fichiers ordinaires <br> -size 1033c — taille exacte 1033 octets (c = bytes) <br> ! -executable — "!" représente la négation
6-7 | Trouver un fichier avec propriétés connues; propriétaire, groupe, taille | find / -user bandit7 -group bandit6 -size 33c 2>/dev/null | **Problème 1** : la commande :$ find -user bandit7 -group bandit6 -size 33c n'affiche absolument rien. <br> **Astuce** : J'ai rajouté "/" avant les propriétés, ce qui permet de rechercher partout sur la machine. <br> <br> **Problème 2** : Beaucoup de fichiers "permission denied". <br> **Astuce**: Supprimer les messages d'erreur avec l'option "2>/dev/null"
7-8 | Rechercher un mot spécifique dans un fichier | grep | ici, $ grep millionth data.txt
8-9 | Rechercher un mot ou une phrase unique dans un fichier | uniq | $ cat data.txt \| uniq -u
9-10 | Rechercher des chaînes de caractères dans un fichier qui ne contient pas uniquement des caractères ASCII | strings, grep : $ strings data.txt \| grep "==" | La commande strings permet de retrouver uniquement les caractères lisibles par l'humain. La commande grep ajoute l'information que je dois trouver un caractère particulier.
10-11 | Décoder base64 | base64 | La commande $ base 64 : permet d'encoder <br> $ base64 -d : permet de décoder <br> **Ici** : base64 -d data.txt
11-12 |
12-13 |
