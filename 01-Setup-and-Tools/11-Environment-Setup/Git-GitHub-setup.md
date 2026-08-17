Comment lier son PC à GitHub + commandes souvent utilisés dans le terminal

# Configuration initiale (manipulation unique sur PC Fedora)

- **`sudo yum install git`** : installer le paquet Git 
	
- **`git --version`** : pour voir quelle version est téléchargée

Configuration :

- `git config --global user.name "TonPseudo"`
- `git config --global user.email "ton@email.com"`

# Obstacle du MDP : Le Token (PAT)

Pour se connecter via le lien direct, GitHub va demander un password particulier, le token.

**Comment créer ton Token :**

Sur GitHub.com : Settings > Developer Settings

Personal Access Tokens > Tokens (classic).

Generate new token (classic).

Donner un nom (ex: "Mon PC") et cocher la case repo (pour avoir tous les droits sur les projets).

COPIER IMMÉDIATEMENT (il commence par ghp_...). Visible qu'un seule fois.

[!IMPORTANT]
Quand le terminal demande le "Password", il faut coller le token.


# Créer un repo via le terminal -> PC to GitHub

- **`mkdir "nom_du_dossier"`** : créer
- **`cd "nom_du_dossier"`** : entrer
	
- **`git init`** : créer le dossier caché git
- **`git branch -M main`** : conseil, renommer la branche par défaut "M" en main (comme dans github)
	
- `git remote add origin https://github.com/votre-nom/votre-repo.git`

#  Si un repo est déjà créé -> copier sur PC :

- **`git clone https://github.com/votre-nom/votre-repo.git`** : permet de copier rapidement sur le PC tout ce qui a déjà été créé


# A chaque fin de modification dans le terminal :

- **`git add .`** : Tu mets toutes tes nouvelles pages dans la chemise cartonnée.
    
- **`git commit -m "..."`** : Tu fermes la chemise et tu colles une étiquette dessus avec la date et le sujet. À ce stade, c'est archivé **sur ton PC**.
    
- **`git push -u origin main`** : Tu envoies la chemise par la poste à GitHub. Maintenant, c'est archivé **sur le serveur**. -u sert à retenir ce qui est derière, donc le chemin. Utile la première fois pour seulement écrire `git push` les prochaines fois

### Si modification sur GitHub, enregistrer les actions sur le PC

- **`git pull origin main`**


---


# Naviguer et s'orienter

Avant de créer, il faut savoir où l'on se trouve.

- **`pwd`** : (_Print Working Directory_) Affiche le chemin du dossier où tu es.
    
- **`ls`** : Liste les fichiers du dossier.
    
- **`ls -la`** : Liste **tous** les fichiers, même les cachés (comme `.git` ou `.gitignore`) avec les détails (droits, taille).
    
- **`cd nom_du_dossier`** : Entre dans un dossier.
    
- **`cd ..`** : Remonte d'un niveau (sort du dossier actuel).


# Créer et Organiser

- **`mkdir nom_du_dossier`** : Crée un nouveau dossier.
    
- **`touch nom_du_fichier.md`** : Crée un fichier vide (pratique pour initialiser un Write-up).
    
- **`cp source.md destination.md`** : Copie un fichier.
    
- **`mv ancien_nom.md nouveau_nom.md`** : Renomme un fichier ou un dossier.
    
- **`mv fichier.md dossier/`** : Déplace un fichier dans un dossier.
    
- **`rm fichier.md`** : Supprime un fichier (**Attention :** c'est définitif, il n'y a pas de corbeille dans le terminal).
    
- **`rm -rf dossier/`** : Supprime un dossier et tout son contenu (à manipuler avec une prudence extrême).
    


# Ajouter du contenu et Modifier

- **`echo "Mon texte" > fichier.md`** : Écrase le contenu du fichier par "Mon texte".
    
- **`echo "Autre ligne" >> fichier.md`** : Ajoute "Autre ligne" à la fin du fichier sans rien effacer.
    
- **`cat fichier.md`** : Affiche tout le contenu du fichier dans le terminal.
    
- **`head -n 5 fichier.md`** : Affiche seulement les 5 premières lignes.
    
- **`nano fichier.md`** : Ouvre l'éditeur de texte simple intégré au terminal pour écrire tes notes.
