---
title: FCNC Combinatoric TruthMatching (v2)
date: '2018-04-13'
tags:
- combinatoric
- fcnc
- truthmatching
---
# Purpose

* optimiser la selection des jets parmis les differents combinaisons qui passent les coupures
)
# Sample

* Signal h019 Wpqq+Wmqq
)
# Procedure

* Analyse nominale sur les 5 leading pT jets avec categories en bTagging
* Les evenements sont classes selon les categories habituelles (selon les priorites 1 puis 2 pour mTop SM, A puis B)
  * si un evenement vit dans sa categorie avec une seule combinaison, je regarde s'il est 'matched' :
    * dR(c quark, jet de mTop1) < 0.4
    * dR(b quark, jet bTagged de mTop2) < 0.4
    * dR(leading pT light quark, jet light le plus proche de mTop2) < 0.4
    * dR(light quark restant, jet light restant de mTop2) < 0.4
  * si plusieurs combinaisons passent la selection pour la même categorie (mais aucune ne passe une 'meilleure' categorie), j'essaie 3 strategies pour trouver la strategie qui donnera des 'matched' le plus souvent :
    * firstCombLeadingPt (le default actuel) : la premiere combinaison qui passe les coupures avec les jets ordonnes en pT
    * mTop1Matched : la combinaison selectionnee est celle qui donne abs(mTop1-173) le plus proche de 0
    * mTop2Matched : la combinaison selectionnee est celle qui donne abs(mTop2-173) le plus proche de 0
    * mTop12Matched : la combinaison selectionnee est celle qui donne abs(mTop1-173)+abs(mTop2-173) le plus proche de 0
  * puis je regarder si la combinaison selectionnee est 'matched' selon le meme critere que precedement (dR < 0.4 pour chaque association quark-jet)
  * pour mesure a quel point on pourrait encore faire mieux, je regarder aussi la combinaison qui minimise la somme des dR cites au-dessus (deltaRMatched) : ca utilise la truth mais c'est juste pour se faire une idee des pertes potentielles (meme si certains de ces matchings en dR sont surement fortuits avec des jets de pile-up)
)
# Plots presentes

- categories de matching (plots a 5 bins)
  - on regarde surtout le bin entre 4-5 (tous les jets sont matches a un quark)
  - et aussi le bin 3-4 (les jets b et c sont matches aux quarks b et c respectivement)
- nombre de jets legers matches aux quarks du W (plots a 3 bins)
)
# Categorie 1A
)
* en general on a la bonne paire bc grace au b-c-tagging
* quand il y a plusieurs possibilites pour le c, on a de meilleurs matching en considerant la combinaison avec le meilleur mTop2
)
![IMAGE](/images/q/9FDFF9994054CD258ED733234E8D0379.jpg)
  * quand il n'y a qu'une possibilite pour le c, la plus grande valeur du min(pT jet) et mTop2 (un peu moins) donnent les 2 bons quarks dans 30% des cas et 1 dans 50% (35%) des cas
)
![IMAGE](/images/q/AF22487090EAE5A441933D7F20B104F4.jpg)
# Categorie 1B
)
* quand il y a plusieurs possibilites pour le c, on a de meilleurs matching en considerant la combinaison avec le meilleur mTop1
)
![IMAGE](/images/q/53A92B0D3EEB29C6206DBCCFE1EEBB7B.jpg)
* quand il n'y a qu'une possibilite pour le c, la plus grande valeur du min(pT jet) et mTop2 (un peu moins) donnent les 2 bons jets du W dans 35% des cas et 1 dans 30% des cas
)
![IMAGE](/images/q/ECB3BD92766EA8DB25731CEE4741F74B.jpg)
# Categorie 2A
)
* quand il y a plusieurs possibilites pour le c, on a de meilleurs matching de la paire bc en considerant la combinaison avec le meilleur mTop1
)
![IMAGE](/images/q/3D55BC95A84C0F1E8C50DC336CFCCBB1.jpg)
* on a presque toujours un quark qui est perdu, mais prendre la combinaison avec la plus petite valeur de max(dR(b,j)) ou mTop2 permettent d'avoir un bon jet du W dans 70% et 65% des evts
)
![IMAGE](/images/q/668EDE488EFF36E0FCFB81024308D928.jpg)
# Categorie 2B
)
* quand il y a plusieurs possibilites pour le c, on a de meilleurs matching en considerant la combinaison avec le meilleur mTop1
)
![IMAGE](/images/q/5493A4F091EDBE222FFC9C936F4B68AB.jpg)
* on a presque toujours un quark qui est perdu, mais prendre la combinaison avec la plus petite valeur de max(dR(b,j)) ou mTop2 permettent d'avoir un bon jet du W dans 65% et 60% des evts
)
![IMAGE](/images/q/AC7FBDEA4ADAB938936733DFD06B7902.jpg)
# Proposition pour la combinatoire

* si plusieurs possibilites pour le jet c, on prends celle qui donne le meilleur mTop1
* une fois le c-jet fixe :
  * en categorie 1, on prends la combinaison de jets qui donne le meilleur mTop2
  * en categorie 2, on prends la combinaison avec la plus petite valeur de max(dR(b,j))
)
