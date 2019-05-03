# Introduction

Une premiere version de l'infrastructure UDONRadio a ete realisee par @theof.
L'interaction des utilisateurs se fait via un site internet. Celui-ci,
rudimentaire, a un nombre de fonctionnalites plutot limite.

*Pour l'auditeur:*

- ecoute de la webradio (avec controles: play/pause/volume slider/mute)
- apercu de la chanson en cours de lecture
- apercu des dernieres chanson jouees precedemment
- comptes utilisateurs (creation/connexion/deconnexion)
- chat
- compteur d'auditeurs
- page "a propos" tres basique

*Pour l'animateur et l'administrateur:*

- upload depuis un fichier audio
- upload depuis un lien youtube
- edition des tags (artiste/album/titre)
- prise en main du stream et diffusion en live, avec des autorisations
  differentes configurables par animateur
- suppression et edition des chansons par l'interface admin de django

*Dans les coulisses:*

- generation de la webradio a partir d'une pool de chansons de facon aleatoire
- lecture d'une chanson tout juste uploadee a la suite de la chanson actuelle
- telechargement asynchrone depuis youtube, avec un systeme de queue, qui ne
  bloque pas les requetes utilisateur, et qui leur permet de revenir editer les
  metadonnees des chansons plus tard, eventuellement en rechargant le site
  entre-temps.
- transcodage et normalisation du volume des fichiers audio


Ces features constituent le MVP d'UDONRadio. L'infrastructure sous-jacente n'est
pas triviale pour autant:

![Infrastructure block diagram](https://raw.githubusercontent.com/UDONRadio/UDONRadio/master/docs/block_diagram.svg)


# Stack logicielle
TODO

## Web frontend
TODO

## Web backend
TODO

## Playout
TODO

## Containers
TODO


# Limitations techniques et bugs

## afra

## Tests / CI / CD
