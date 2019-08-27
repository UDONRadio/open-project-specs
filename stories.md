# DISCLAIMER
Ces stories ne sont pas figees dans le marbre et peuvent evoluer selon les
futures orientations de la direction artistique d'UDONRadio.

# Types d'utilisateurs

- Anonyme: n'importe quel visiteur qui n'est pas connecte a son compte.
- Membre: n'importe quel visiteur qui est connecte a son compte.
- Adherent: Membre qui a adhere a l'association.
- Moderateur: Adherent qui s'est porte volontaire pour la moderation
  du chat.
- Documentaliste: Adherent responsable d'un genre.
- Animateur: Membre qui diffuse une emission en live ou en differe.
- Admin: Nous.

# Features

## Calendrier
La radio diffuse 24/7. Ce temps d'antenne est divisible en des plages horaires
de differents types. Les plages d'un meme planning ne peuvent pas se chevaucher.
On fait une distinction entre le planning "automatique" et le planning
"spontane":

- Planning automatique (ou _par defaut_): il est en permanence rempli de plages
  horaires contigues. C'est-a-dire qu'a tout moment de la semaine, il doit y
  avoir une plage horaire correspondant sur ce planning.
- Planning spontane (ou _manuel_): il prend le dessus sur le planning
  automatique dans le cas ou la plage horaire prevue est diffusable. Il peut y
  avoir des vides temporels entre les differentes plages. Dans ce cas, les
  plages du planning automatique seront diffusees.

### Types de plages horaires
Planning automatique:
- [Genres](#genres)
- [Like Pool](#like pool)
Planning spontane:
- [Genres](#genres)
- [Like Pool](#like pool)
- [Emissions](#emissions)
- [Playlists](#playlists)
- [Grande Tambouille](#grande tambouille)

### TODO Generation du planning automatique
- definir l'API et les datas a propos d'un type de plage qui peut etre query par
  l'algorithme.
En debut de semaine, le programme de la semaine a venir est fractionne
automatiquement en plages horaires. Chaque type de plage horaire peut influer
sur l'algorithme qui determine la duree d'une plage, l'heure a laquelle une
plage est difusee (l'algorithme calcule un poids pour chaque type de plage) etc.

### Plannification
Depuis le site, un Admin doit pouvoir:
- changer le type de plage
- regler la configuration du type de plage en question. Par exemple pour un
  genre, regler quel genre est diffuse.
- ajuster l'heure de debut et de fin d'une plage si celle-ci est de duree
  variable. Dans le cas d'une plage sur le planning auto, les plages adjacentes
  sont redimensionees en consequence. Dans le cas du planning spontane, le
  chevauchement de plages horaires est interdit et entraine l'affichage d'un
  message d'erreur.
- supprimer une plage horaire. Dans le cas du planning auto, la plage precedente
  s'etend alors a la fin de la plage supprimee.
- ajouter une plage horaire. Dans le cas du planning auto, une plage horaire
  peut etre cree uniquement en divisant une plage horaire en deux.
Il n'est pas question de pouvoir deleguer une partie du planning a un DJ par
exemple, qui souhaiterait diffuser une playlist a la suite de son emission.
Dans ce cas la, le DJ demande a l'admin de mettre lui meme sa playlist ensuite.

### Consultation
- On doit pouvoir voir la plage courante et la plage a suivre sur la landing
  page.
- On doit pouvoir voir le calendrier de la semaine.
- On doit aussi pouvoir l'exporter facilement pour le partager sur les reseaux
  sociaux.
- On doit pouvoir savoir ce qui a ete diffuse a une heure donnee en tant
  qu'admin (avec eventuellement les logs du playout engine).
- L'admin peut voir si une plage spontanee est diffusable (via un warning ?).

### Services externes
Le calendrier doit pouvoir etre requetable pour permettre l'integration de
robots.


## TODO Genres
Les _genres_ sont des plages horaires similaires a une playlist classique, mais
dont la playlist est generee automatiquement a partir des chansons qu'il
contient. Chaque _genre_ est modere par un ou plusieurs _documentalistes_
specifiques. Lorsqu'un _adherent_ lambda upload une chanson, il peut choisir a
quel genre envoyer sa chanson. Les _documentalistes_ sont alors charges de
tagger proprement la chanson si ils l'acceptent dans leur _genre_. Ils ont acces
a la liste des chansons qui font partie de leur _genre_.

### TODO Creation de genres
### TODO LIQUIDSOAP
### TODO Rejet d'une chanson
### TODO Consultation de la discographie




















### Services externes
Mise en place d’un Slackbot pour prévenir les documentalistes qu’il y a une ou
plusieurs nouveautés dans leur groupe

## Emissions
## Playlists
## Grande Tambouille
## Like Pool
(la fifo avec des like)
## Upload
Application  technique 
:  liste  de  sous-genres  à  remplir  /  menu  déroulant  proposé  au 
moment du référencement de la chanson
## Replays
## Utilisateurs
## Statistiques
## Chat
## Player
## Jingles

## TODO Misc
Un Admin doit pouvoir exporter la liste de toutes les chansons jouees entre deux
dates, dans un format compatible avec les attentes de la SACEM.


# Deploiement
# Tests
