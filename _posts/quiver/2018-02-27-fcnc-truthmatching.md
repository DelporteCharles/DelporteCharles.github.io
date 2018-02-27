---
title: FCNC TruthMatching
date: '2018-02-27'
tags:
- fcnc
---
# Purpose

* Voir quelle proportion des objets reco utilises dans l'analyse nous viennent des TruthParticles visées
)
# Sample

* Wmqq
)
# Selection

* habituelle avec les categories de tagging
  * avec les coupures de C-Tagging calibrées
  * avec la coupure FJVT
  * 1) avec jets pt > 30 et tout eta 
  * 2) avec jets pt > 25 et abseta < 2.5
)
# Matching

* un objet est matched si dans son utilisation dans le calcul des mTops et vis a vis du b/c-tagging, il presente dR < 0.4 avec l'objet truth correspondant
* pour les deux quarks dans W->qq du top SM, je match d'abord le leading quark avec le jet le plus proche (parmi les deux jets non b-tagged utilise dans le top SM), et le subleading quark est alors associe a l'autre jet
* s'il n'y a pas de jet b-tagged ou qu'il y en a plusieurs, ils sont ordonnés en pT pour savoir lequel doit matcher à quel quark
)
# Bins

* 4 : b, c, q0 et q1 matched (q0 et q1 dans W->qq)
* 3 : b et c matched, mais pas q0 et/ou q1
* 2 : c matched mais pas b
* 1 : b matched mais pas c
* 0 : ni b ni c matched
)
# Principales observations

* en Tight A : bon matching bcqq et bc (4eme et 5eme bins), entre 30% et 40% chacun
* en Tight B : on match plus souvent le b mais pas le c (2eme bin) : normal, c'est la categorie un bTag mais pas de cTag
  * mais dans 1/5 des evenements, on a quand meme tous les bons objets (5eme bin)
  * dans encore 1/5 des evenements, on a quand meme la bonne paire bc (4eme bin)
* en Tight C : on match plus souvent le c mais pas le b (normal, c'est la categorie un cTag mais pas de bTag)

* dans ces categories tight, on a plutot interet a garder les coupures actuelles sur les jets (30 GeV tout eta) plutot que 25 GeV abseta < 2.5

* en Loose A : c'est le matching bc mais il manque au moins un des quarks de Wqq qui domine (3eme bin), autour de 60%-70%, donc rien de choquant : on a un mauvais jet dans le top2, c'est normal qu'il y aie besoin d'une fenetre en masse plus large
* en Loose B : idem, mais contribution plus importante de b matched sans le c (2eme bin), et un peu de ni b ni c matchés (1er bin)
* en Loose C : on match tres souvent le c mais pas le b, dans des proportions similaires a la categorie tight :
)
# Tight A

![IMAGE](/images/q/71D52E9B93C88B487B4E16C74E3F205C.jpg)
# Tight B

![IMAGE](/images/q/7C0605F7491CCDFF6D06DD85D49CCD4E.jpg)
# Tight C

![IMAGE](/images/q/0218856917E265983A4E56E83A60DCA1.jpg)
# Loose A

![IMAGE](/images/q/BA627220AE2634E1AE2EF3753884B613.jpg)
# Loose B

![IMAGE](/images/q/7C7CC1A741FD9E90C875E45DA6569291.jpg)
# Loose C

![IMAGE](/images/q/E5630FE54118508908B2795546F25637.jpg)
