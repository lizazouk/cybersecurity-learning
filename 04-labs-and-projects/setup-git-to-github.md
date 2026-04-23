Lier Git à GitHub permet de travailler directement depuis le Terminal pour remplir des informations sur Github


# Configuration initiale (manipulation -> PC Fedora)

- `sudo yum install git` : installer le paquet Git 
	
- `git --version` : pour voir quelle version est téléchargée

Configuration :

- `git config --global user.name "TonPseudo"`
- `git config --global user.email "ton@email.com"`

# Créer un repo via le terminal -> PC to GitHub

- `mkdir "nom_du_dossier"` : créer dossier
- `cd "nom_du_dossier"` : entrer dedans
	
- `git init` : créer le dossier caché git
- `git branch -M main` : renommer la branche par défaut "M" en main (comme dans github)
	
- `git remote add origin https://github.com/votre-nom/votre-repo.git`

#  Si un repo est déjà créé -> copier sur PC :

- `git clone https://github.com/votre-nom/votre-repo.git` : permet de copier rapidement sur le PC tout ce qui a déjà été créé
	
- **`Git pull`** : si modifications faites sur le site pour tout copier sur PC
