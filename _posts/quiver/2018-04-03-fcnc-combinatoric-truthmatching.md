---
title: FCNC Combinatoric TruthMatching
date: '2018-04-03'
tags:
- combinatoric
- fcnc
- truthmatching
---
# Purpose

* optimiser la selection des jets parmis les differents combinaisons qui passent les coupures
)
# Sample

* Signal h017 Wmqq
)
# Procedure

* Analyse nominale sur les 5 leading pT jets avec categories en bTagging
* Les evenements sont classes selon les categories habituelles (selon les priorites 1 puis 2 pour mTop SM, A puis B puis C pour le tagging)
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
# Observations principales

* en categorie 1 (tight) : peu de differences entre les differentes strategies reco, mais matcher avec mTop2 (ou par extension mTop1+mTop2) semble faire gagner le plus, et ca fait plus de sens que la strategie actuelle (firstCombLeadingPt).
  * le truth-matching en dR semble montrer qu'on prend la meilleure combinaison a peine une fois sur 2, et les strategies que j'ai essayees (mTop1, mTop2, mTop12) ameliorent a peine : vu que firstCombLeadingPt donne moins de 50% de bons matchings parmis ceux possibles (si on considere que le max serait la valeur pour deltaRMatched) peut-etre qu'il faudrait prendre la combinaison avec HT plus faible ou quelque chose comme ca ? le plus petit jet de pt ?
* en categorie 2 (loose) : il n'y a que tres peu (1%) de bon matching possible, mais une nouvelle fois mTop2 semble donner le meilleur gain, surtout en 2-A et 2-B
)
# Nombres pour les evenements ayant plusieurs combinaisons possibles
)
{% highlight sh %}
* hadM2tightA
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |         108 |      484 |     22.3 %
        mTop1Matched |         112 |      484 |     23.1 %
        mTop2Matched |         128 |      484 |     26.4 %
       mTop12Matched |         129 |      484 |     26.7 %
       deltaRMatched |         225 |      484 |     46.5 %
---------------------------------------------------------

* hadM2tightB
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |         252 |     1446 |     17.4 %
        mTop1Matched |         262 |     1446 |     18.1 %
        mTop2Matched |         260 |     1446 |       18 %
       mTop12Matched |         276 |     1446 |     19.1 %
       deltaRMatched |         493 |     1446 |     34.1 %
---------------------------------------------------------


* hadM2tightC
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |          10 |      240 |     4.17 %
        mTop1Matched |          11 |      240 |     4.58 %
        mTop2Matched |          11 |      240 |     4.58 %
       mTop12Matched |          11 |      240 |     4.58 %
       deltaRMatched |          22 |      240 |     9.17 %
---------------------------------------------------------

* hadM1looseA
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |           1 |      565 |    0.177 %
        mTop1Matched |           1 |      565 |    0.177 %
        mTop2Matched |           8 |      565 |     1.42 %
       mTop12Matched |           8 |      565 |     1.42 %
       deltaRMatched |           9 |      565 |     1.59 %
---------------------------------------------------------

* hadM1looseB
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |           8 |     1363 |    0.587 %
        mTop1Matched |           8 |     1363 |    0.587 %
        mTop2Matched |          24 |     1363 |     1.76 %
       mTop12Matched |          25 |     1363 |     1.83 %
       deltaRMatched |          29 |     1363 |     2.13 %
---------------------------------------------------------

* hadM1looseC
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |           3 |      443 |    0.677 %
        mTop1Matched |           3 |      443 |    0.677 %
        mTop2Matched |           3 |      443 |    0.677 %
       mTop12Matched |           3 |      443 |    0.677 %
       deltaRMatched |           4 |      443 |    0.903 %
---------------------------------------------------------
{% endhighlight %}

# Nombres inclusifs (une combinaison + plusieurs combinaisons possibles)
)
{% highlight sh %}
* hadM2tightA
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |         633 |     1807 |       35 %
        mTop1Matched |         637 |     1807 |     35.3 %
        mTop2Matched |         653 |     1807 |     36.1 %
       mTop12Matched |         654 |     1807 |     36.2 %
       deltaRMatched |         750 |     1807 |     41.5 %
---------------------------------------------------------

* hadM2tightB
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |         881 |     3551 |     24.8 %
        mTop1Matched |         891 |     3551 |     25.1 %
        mTop2Matched |         889 |     3551 |       25 %
       mTop12Matched |         905 |     3551 |     25.5 %
       deltaRMatched |    1.12e+03 |     3551 |     31.6 %
---------------------------------------------------------

* hadM2tightC
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |          77 |      877 |     8.78 %
        mTop1Matched |          78 |      877 |     8.89 %
        mTop2Matched |          78 |      877 |     8.89 %
       mTop12Matched |          78 |      877 |     8.89 %
       deltaRMatched |          89 |      877 |     10.1 %
---------------------------------------------------------

* hadM1looseA
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |          13 |     1182 |      1.1 %
        mTop1Matched |          13 |     1182 |      1.1 %
        mTop2Matched |          20 |     1182 |     1.69 %
       mTop12Matched |          20 |     1182 |     1.69 %
       deltaRMatched |          21 |     1182 |     1.78 %
---------------------------------------------------------

* hadM1looseB
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |          17 |     2506 |    0.678 %
        mTop1Matched |          17 |     2506 |    0.678 %
        mTop2Matched |          33 |     2506 |     1.32 %
       mTop12Matched |          34 |     2506 |     1.36 %
       deltaRMatched |          38 |     2506 |     1.52 %
---------------------------------------------------------

* hadM1looseC
Matching strategy    | Matched     | Total     | Fraction
-------------------- | ----------- | --------- | --------
  firstCombLeadingPt |           4 |      985 |    0.406 %
        mTop1Matched |           4 |      985 |    0.406 %
        mTop2Matched |           4 |      985 |    0.406 %
       mTop12Matched |           4 |      985 |    0.406 %
       deltaRMatched |           5 |      985 |    0.508 %
---------------------------------------------------------
{% endhighlight %}

