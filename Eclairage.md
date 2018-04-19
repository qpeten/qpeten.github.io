---
title: Éclairage automatisé
onFrontPage: true
---

Il y a pour le moment 3 éclairages automatisés automatisés dans la maison. Dans l’ordre, du plus simple au plus compliqué : l’éclairage extérieur, l’éclairage du garage et l’éclairage dans ma chambre.

#### Lumière parking
Le seul contrôle sur l’éclairage extérieur consiste à l’éteindre complètement ou à activer le capteur de mouvement. Comme le capteur de mouvement avait tendance à allumer un peu trop souvent la lumière, nous le désactivons lorsque nous sommes certains de ne pas être présents, ainsi qu’en journée et il suit aussi certains évènements (la présence d’invités).

#### Lumière garage
La lumière du garage était complètement manuelle. Avant de mettre en place mon système, il était donc impossible de rentrer ou de sortir du garage (en voiture) lorsque la lumière était allumée, vu que le conducteur était dans la voiture et n’avait donc pas accès à l’interrupteur !
J’ai ajouté un capteur (de courant sur le fusible lié) aux portes du garage afin de pouvoir savoir lorsqu’elles sont en mouvement. Lorsqu’elles sont en mouvement, la lumière du garage s’allume automatiquement (et s’éteindra après quelques minutes). L’interrupteur original est resté à sa place et fonctionne toujours comme avant mais avec l’ajout d’une minuterie d’une heure pour le cas ou nous l’avons oublié.

#### Barre de led
Pour le fun, j’ai ajouté dans ma chambre une barre de led (blanche) le long d’un mur. Il y a moyen de la dimmer. Je l’ai installée moi-même à partir d’une barre de LED, d’une alimentation de PC, et d’une arduino nano. Cette lampe me sert également de réveil, en s’allumant progressivement pendant 30 minutes. Mon but était de ne jamais devoir toucher l’interrupteur. J’y suis pour le moment presque : 1,2 fois par jour.
Pour arriver à cela, j’utilise beaucoup d’inputs. Il y a tout d’abord deux capteurs de mouvements (un pour la porte, un pour le reste de la chambre), une information si oui ou non j’écoute de la musique sur ma chaîne HiFi, et finalement un signal lorsque je mets mon gsm à charger (je le branche toujours juste avant d’aller dans mon lit.)

<!--more-->
## Preuves
D’après les chiffres, cela fonctionne assez bien. Voir graphique @@@.
Je n'ai pas de chiffres pour l'éclairage extérieur.
Voici une photo de la Raspberry Pi (en F1) et des relais (en bas, en vert. 2 pour les lumières garage & parking, et deux autres pour contrôler les balons d'eau chaude. Ne pas tenir compte de l'inscription manuscrite, nous avons retiré un des boilers.)
![RPi garage]({{ "assets/ecl-garage.JPG" | absolute_path }})

Pour la lumière du garage, je peux affirmer que cela fonctionne assez bien. Voici un graphique en date du 1er avril 2018, qui couvre les 90 derniers jours. On peut clairement voir qu'il n'y a eu aucun faux positif durant les 8 jours pendant lesquels nous sommes partis en vacances. Sur les 30 derniers jours, la lumière a été allumée en tout 3% du temps. Elle a été allumée 167 fois, soit 5,6 fois par jour en moyenne.
![Lumière garage sur 90 jours]({{ "/assets/garage-90j.png" | absolute_path }})

Voici une photo de l'arduino et de l'alimentation de PC qui contrôle la barre de led dans ma chambre. Ce montage a été fait en sachant qu'il serait temporaire (quelques mois avant que je ne quitte la maison). Merci de ne pas juger la propreté du câblage !
![Alim et arduino]({{ "assets/ecl-alim.JPG" | absolute_path }})

Et voici deux photos montrant la barre de led ainsi que le résultat final. Les barres plus foncées horizontales et verticales sont dues au fait que les LEDs sont dimmés par PWM. C'est totatlement invisible à l'oeuil nu.
![Barre de led]({{ "assets/ecl-barreled.JPG" | absolute_path }})
![Résultat]({{ "assets/ecl-final.JPG" | absolute_path }})
