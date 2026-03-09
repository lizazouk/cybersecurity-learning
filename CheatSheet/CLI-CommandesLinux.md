![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

---- 

## 📂 Manipulation de fichiers spéciaux

### Commence par `-`
Sans rien devant, la commande le considère comme une option, ajouter `./` 

Ex:  `./-filename`

### Contient des espaces

Écrire le nom du fichier entre `""`



----

## 🔍 Recherche & Filtrage

### Trouver le seul fichier "lisible par un humain" : ASCII text

      file ./* | grep "ASCII text"
    
Traduction : Regarde le type de tous les fichiers ET montre-moi que les lignes où il y a écrit 'ASCII text'


### Trouver un fichier avec caractéristiques spéciales

      find -size 33c ...

**Rechercher partout sur la machine :** Rajouter / après la commande pour partir de la racine.

**Supprimer les messages d'erreur envahissants :** Quand on n'a pas les droits partout, le terminal affiche plein de "Permission denied". On peut les cacher en envoyant les erreurs dans le "trou noir" de Linux. 

Astuce : Rajouter `2>/dev/null` à la fin de ta commande. 

      find / -size 33c 2>/dev/null


### Trouver un mot dans un fichier précis

      grep "mot précis" fichier

##### Dans tous les fichiers dans lesquels il apparaît

      grep -irl "cesarbrut" *

-i pour insensible à la casse
-r pour récursif
-l pour que la commande te donne le nom du fichier
et * pour rechercher dans tous les fichiers à partir du répertoire courant

 
### Extraire une ligne / mot unique dans un fichier rempli de doublons non ordonnés. 

/!\ Toujours trier le fichier avant d'utiliser `uniq` grace à `sort`, sinon `uniq` ne compare que des lignes adjacentes (qui se touchent)

    cat data.txt | sort | uniq -u
`-u` permet de supprimer toutes les lignes / mots **ayant** dans doublons


----

## 📦 Encodage & Données

### Lire du texte lisible parmit du charabia

La ccommande `strings` ignore les caractères bizarres et n'affiche que les suites de caractères "imprimables" (le texte).

    strings "fichier"

**Note technique :** Si on utilise `cat` sur un fichier binaire, le terminal peut planter ou afficher des symboles étranges. `strings` est la méthode "propre" pour scanner l'intérieur d'un fichier exécutable ou d'une image à la recherche d'indices (comme des flags ou des commentaires).


### Identifier Base64

Indices visuels (Le "Check-list") :

    Le Padding `=` : l'indice ultime. Si la chaîne se termine par un ou deux `=`, c'est presque à coup sûr du Base64. (Note : le = sert à compléter la taille du bloc)

    L'Alphabet : Il n'utilise que :

        Des majuscules (A-Z)

        Des minuscules (a-z)

        Des chiffres (0-9)

        Les symboles + et /

**Exemple :** YWRtaW4= (Une fois décodé, cela donne admin).

**Pour le décoder** : commande `base64 -d`



----

## 🔑 Lecture & Droits 



----

## 🌐 Connexion & Réseau 


