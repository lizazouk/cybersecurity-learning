![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

## Commande de lancement

Il peut être intéressant, au lancement du terminal, de mettre à jour les logiciels :

`apt update` : permet de rechercher s'il y a des mises à jour
`apt update && full-upgrade` : ajoute la fonction "si il y a du nouveau, alors mettre à jour"


## Navigation et Gestion de base

- **pwd** : Affiche le répertoire courant (Print Working Directory).
    
- **ls** : Liste le contenu du répertoire.
    
    - **ls -l** : Format détaillé (droits, taille, date).
        
    - **ls -a** : Affiche les fichiers cachés (commençant par un point).
        
    - **ls -R** : Liste récursive (inclut les sous-dossiers).
        
- **cd [dossier]** : Se déplacer dans un dossier.
    
    - **cd ..** : Remonter d'un niveau.
        
    - **cd ~** : Retourner au répertoire personnel.
        
- **mkdir [nom]** : Créer un dossier.
    
    - **mkdir -p A/B/C** : Crée toute l'arborescence parente si nécessaire.
        
    - **mkdir {D1,D2}** : Crée plusieurs dossiers d'un coup (expansion d'accolades).
        
- **cp [source] [destination]** : Copier un fichier.
    
- **mv [source] [destination]** : Déplacer ou renommer un fichier/dossier.
    
- **rm [fichier]** : Supprimer un fichier.
    
    - **rm -r [dossier]** : Supprimer un dossier et son contenu.
        

## Manipulation de fichiers spéciaux

### Fichiers commençant par un tiret (-)

Utiliser le chemin relatif pour éviter la confusion avec une option de commande.

- Exemple : `cat ./-filename`
    

### Noms contenant des espaces

Encadrer le nom par des guillemets doubles.

- Exemple : `cat "nom avec espaces.txt"`
    

## Recherche et Filtrage

### Identification du type de fichier

- **file [fichier]** : Analyse la signature (magic bytes) pour donner le type réel.
    
- __file ./_ | grep "ASCII text"_* : Trouve les fichiers lisibles par l'humain dans le répertoire.
    

### Commande find

- **find [chemin] -size [taille]** : Recherche par taille (ex: 33c pour 33 octets).
    
- **find / -name "nom" 2>/dev/null** : Recherche sur toute la racine en masquant les erreurs de permission.
    

### Commande grep (Recherche de texte)

- **grep "motif" [fichier]** : Cherche un mot précis.
    
- **grep -irl "motif" *** : Recherche récursive, insensible à la casse, affiche uniquement les noms de fichiers.
    

### Tri et Unicité

- **sort** : Trie les lignes par ordre alphabétique.
    
- **uniq -u** : Affiche uniquement les lignes qui n'apparaissent qu'une seule fois (nécessite un fichier trié au préalable).
    
    - Exemple : `cat data.txt | sort | uniq -u`
        

## Encodage et Données

### Analyse de binaires

- **strings [fichier]** : Extrait les chaînes de caractères imprimables d'un fichier binaire. Utile pour trouver des indices cachés dans des images ou exécutables.
    

### Base64

- **Indices** : Alphabet (A-Z, a-z, 0-9, +, /) et présence possible de "=" ou "==" en fin de chaîne (padding).
    
- **base64 -d** : Décode une chaîne.
    
    - Exemple : `echo "YWRtaW4=" | base64 -d`
        

## Workflow Git et GitHub

### Configuration initiale

- **git init** : Initialise un nouveau dépôt local.
    
- **git remote add origin [url]** : Lie le dépôt local au dépôt distant (GitHub).
    
- **git remote set-url origin [url]** : Change l'URL (ex: passer de HTTPS à SSH).
    

### Cycle de modification

1. **git pull origin main** : Récupère les modifications distantes (à faire avant de travailler).
    
2. **git add .** : Ajoute tous les fichiers modifiés à l'index (zone de préparation).
    
3. **git commit -m "message"** : Enregistre les modifications localement avec un commentaire.
    
4. **git push origin main** : Envoie les modifications sur GitHub.
    

### Diagnostic

- **git status** : Affiche l'état des fichiers (modifiés, non suivis).
    
- **git remote -v** : Vérifie l'URL distante et le protocole utilisé (HTTPS ou SSH).
    

## Connexion et Réseau

- **ssh [user]@[ip]** : Connexion sécurisée à une machine distante.
    
- **ssh -T git@github.com** : Teste la validité de la clé SSH avec GitHub.
    
- **script [nom_fichier.log]** : Enregistre l'intégralité de la session terminal dans un fichier.
    
    - Taper `exit` pour arrêter l'enregistrement.
