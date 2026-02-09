4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

---- 

## 📂 Manipulation de fichiers spéciaux

### Commence par `-`
Sans rien devant, la commande le considère comme une option, ajouter `./` 

Ex:  `./-filename`

### Contient des espaces

Écrire le nom du fichier entre `""`



----

## 🔍 Recherche & Filtrage (Chercher un mot dans 100 fichiers, trouver un fichier par sa taille)

### Trouver le seul fichier "lisible par un humain" : ASCII text

Utiliser la commande `file` sur tous les fichiers du dossier

    file ./* (pour analyser tous les fichiers du dossier actuel)
    l'étoile permet de remplacer "tout ce qui suit"

Si on sait quel type de fichier est recherché :

    file ./* | grep "ASCII text"
    Traduction : "Regarde le type de tous les fichiers ET ne montre-moi que les lignes où il y a écrit 'ASCII text'".

----

## 🔑 Lecture & Droits (Lire un fichier que tu n'as pas le droit d'ouvrir, comprendre les permissions)



----

## 🌐 Connexion & Réseau (Se connecter en SSH, envoyer un fichier à distance)


