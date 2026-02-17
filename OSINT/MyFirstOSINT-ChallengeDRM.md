15/02/2026

## Défi OSINT posté par la DRM (Direction du Renseignement Militaire) sur LinkedIn

### Objectif : Identifier le matériel et la localisation d'une image satellite

La DRM poste souvent des défis OSINT avec le tag #Yeuxdor sur LinkedIn tel que [celui-ci](https://www.linkedin.com/posts/drm-renseignement-militaire_yeuxdor-drm-renseignement-activity-7428709888928821248-tjif?utm_source=share&utm_medium=member_desktop&rcm=ACoAADUQEDEBXVVtMexFXLADOjBD5SySJItZ_Yw) 
, qui est celui d'aujourd'hui.

Je vais tenter d'y répondre. Cependant je n'ai aucune expérience dans ce domaine.
Vous pourrez voir mes recherches, mon avancé et peut être une hypothèse ?

## Ma Méthodologie :

- Analyse générale : Ce que jobserve sur cette image et premières hypothèses

- Metadata de l'image (même si venant de la DRM je ne pense pas avoir grand chose)

- Amélioration d'image : Tentative d'upscaling avec Upscayl et Waifu2x

- Analyse IMINT (Matériel) : Anlyse plus poussée avec des hypothèses sur les véhicules et matériel visible
  
- Analyse GEOINT (Terrain) : Étude du type de terrain, géocalisation possible


## Analyse Générale

- Un désert avec des nuances assez orangées, rouges
- Présence de merlons (murs de sable) : un grand pour délimiter la zone globale et des petits (encuvement) individuels, qui entourent les véhicules, chars
- De nombreuses traces de pneus, chenilles au sol indiquent une activité dynamique, ils entrent et sortes de la zone. De plus, certains emplacements pour chars sont vides
- On aperçoit une présence de piquets, ou grillage, ce qui suggère une zone militaire de défense ou un camps d'entraînement sécurisé
- L'observation de canons sur les véhicules confirme que ce sont des engins de combat / artillerie.  Ceux-ci sont bien rangés avec les canons en position route (droits dans l'axe)
- Les ombres sont franches et déportées vers la gauche.

Hypothèse géographique : Si le haut de l'image correspond au Nord (standard satellite), le soleil vient de l'Est/Sud-Est. Cela placerait la prise de vue en milieu de matinée.

L'alignement parfait des véhicules dans des écuvement délimitées, associé à une clôture, privilégie l'hypothèse d'un parc d'alerte ou d'une zone de stockage temporaire lors d'un exercice majeur, hors conflit.


## Metadata de l'image

Utilisation d'`exiftool` via un flux distant pour éviter la pollution locale :

       curl -s "URL_IMAGE" | exiftool -

Constat : Absence totale de données EXIF/GPS (nettoyage automatique par LinkedIn/OPSEC). C'était évident, au moins j'ai pris connaissance de la commande `exiftool`.


## 


---

SPURCES UTILES :

[youtube video : 4 Free Satellite Imagery Sources](https://youtu.be/OONjbRAR-TM?si=jTgfZjyu_CjshKbf)

[youtube video : find EXIF/metadata in a photo or video](https://youtu.be/d3NsT8lJRlE?si=1zk9UJbOHeyu0CTh)

Téléchargement de Exiftool pour l'utiliser directement depuis mon terminal

