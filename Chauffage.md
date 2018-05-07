---
title: Chauffage
onFrontPage: false
---

Nous nous sommes installés dans une nouvelle maison il y 2 ans. Il y avait un système de chauffage par le sol contrôlé par un seul thermostat. Certaines pièces étaient toujours trop froides, d’autres toujours trop chaudes. La consommation de mazout était élevée.

J’ai mis en place une régulation pièce par pièce du chauffage, en contrôlant les électrovannes sur chaque circuit de chauffage, les différentes pompes de circulation, ainsi que la température de l’eau de chauffage (via une vanne 3 voies et le contrôle de la chaudière).

Les résultats sont encourageants… nous économisons 20% de mazout sur l'année avec ma solution. En outre, le confort s'est amélioré : aucune pièce n’est trop froide ou trop chaude, les pièces non utilisées (enfants en kot) peuvent ne pas être chauffées.

J’ai beaucoup appris sur la domotique en général pendant ce projet. Ça a aussi été intéressant de voir comment interfacer des anciens systèmes : pour contrôler la température de la chaudière, j’ai du simuler une sonde de tempérture à l’aide de plusieurs résistances de valeur différentes.

<!--more-->
## Preuves
![État des actuateurs]({{ "/assets/chauffage-OH-advanced.png" | absolute_path }})
L'interface avancée (Openhab) pour voir l'état des différents actuateurs et senseurs.

![Grafana]({{ "/assets/chauffage-grafana.png" | absolute_path }})
L'interface de Grafana avec les données historique. Ici 48h typiques de fin mars, avec une après-midi ensoleillée. En pointillées, la consigne; en continu, la température réelle. Les barres en bas du graphe représentent les temps de chauffe pièce par pièce.

![RPi chaudiere]({{ "/assets/chauffage-chaudiere.JPG" | absolute_path }})
La raspberry et les relais qui contrôlent la chaudière (température de sortie eau chaude), la vanne 3 voies (température circuit sol), les pompes des 2 circuits, ainsi que le repassage à l'ancien thermostat en cas de dysfonctionnement de mon système.

![RPi collecteur]({{ "assets/chauffage-collecteur.JPG" | absolute_path }})
Un des trois collecteurs. Les electrovannes sont en rouge. J'ai un peu honte du câblage en le voyant maintenant…
