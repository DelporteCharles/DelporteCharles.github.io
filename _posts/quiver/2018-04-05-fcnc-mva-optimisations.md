---
title: FCNC MVA Optimisations
date: '2018-04-05'
tags:
- fcnc
---
# Purpose

* Trouver le meilleur set de variables

* Je separe les variables en 3 categories pour que ce soir plus clair :
  * pT/eta
  * dR/dEta/DPhi
  * Meff/Ht
*Dans chacune de ces cateégories, je garderai les 3-4 meilleures variables, et je ferai une nouvelles selection de variables parmi celles ci
)
# Procedure

* BDT entraines avec le setup VHbb
* Poids negatifs pris en compte

* Procedure iterative :
  1. je demarre avec toutes les variables
  2. pour chaque variable (restante), j'entraine un nouveau BDT sans la variable en question
  3. le BDT qui donne la meilleure significance indique la variable la moins utile : elle ne sera pas utilisee dans les prochaines iterations
  4. je reprends au point b. et à chaque iteration j'enleve une nouvelle variable
)
* la significance est evaluee sur les distributions de BDT (rebinnees comme dans VHbb, de facon a reduire l'erreur stat dans chaque bin a une valeur raisonnable) en calculant :
)
{% highlight sh %}
  Float_t sensitivity = 0.;
  Float_t uncertainty = 0.;
  
  Int_t nBins = m_mvaHistSig->GetNbinsX();
  for(Int_t i=0; i<nBins; i++)
    {
      double iS = m_mvaHistSig->GetBinContent(i+1);
      double iB = m_mvaHistBkg->GetBinContent(i+1);
      
      double idS = m_mvaHistSig->GetBinError(i+1);
      double idB = m_mvaHistBkg->GetBinError(i+1);

      if(iS<=0 or iB<=0)
        continue;
      
      double iLSB = log(1+iS/iB);
      double s = 2*((iS+iB)*iLSB-iS);
      double u = iLSB * iLSB * idS * idS + (iLSB - iS/iB) * (iLSB - iS/iB) * idB * idB;
      
      sensitivity += s;
      uncertainty += u;
    }

  m_sensitivity = sqrt(sensitivity);
{% endhighlight %}

# Samples

* h019
  * FCNC W +- qq
  * Sherpa yy + jets
)
# Selection

* Selection 5 jets
* Categories de tagging A et B uniquement
* Si plusieurs combinaisons sont possibles, je prends celle qui donne mTop2 le plus proche de 173 
)
# Plots de ranking

* chaque bin en x correspond à un BDT entrainé, où on a retiré des variables d'entrainement la variable indiquee en label du bin. Dans chaque bloc, la premiere variable retiree correspond au BDT qui donne la meilleure significance, ce qui montre que cette variable est la moins importante de toutes celles testees. Pour l'iteration suivante, elle est donc definitivement supprimee, et on cherche a retirer une variable de plus du BDT a chaque iteration.
* je pense que l'on sait que l'on atteint un seuil critique dans les variables enlevees lorsque, quelle que soit variable retiree, la significance diminue significativement par rapports aux BDT du bloc d'avant ...
)
# pT / eta / m
)
* Ordre d'importance des variables (importance decroissante)

1. pTyy
2. mW
3. mtt
4. pTj1
5. pTb
6. etayy
7. etab
8. pTtt
9. etaj0
10. pTratiobjj0j1
11. etaj1
12. pTratioj0j1
13. ytt
14. pTj0

6% de difference en significance entre le meilleure entrainement avec 13 variables et le moins bon à 2 variables
)
* Proposition de variables a conserver :

1. pTyy
2. mW
3. mtt
4. pTj1
5. pTb

![IMAGE](/images/q/E99C96AB7336869E39E7544981F3797B.jpg)
{% highlight sh %}
variablesOptimizationLocal rootFiles/h019/ BDTTree_FCNCttWpqq_v0_5jets_tagging:BDTTree_FCNCttWmqq_v0_5jets_tagging BDTTree_FCNCttShergg_allVariables_v1_5jets_tagging pTj0:etaj0:pTj1:etaj1:pTb:etab:mW:pTratiobjj0j1:pTratioj0j1:pTtt:ytt:mtt:pTyy:etayy kinematic_v0
{% endhighlight %}

# dR / dPhi / dEta
)
* Ordre d'importance des variables (importance decroissante)

1. maxdRcy
2. mindRbj
3. dEtacH
4. mindRcy
5. dRbW
6. maxdPhicy
7. dPhibW
8. mindPhicy
9. mindPhibj
10. dRcH
11. dEtabW
12. dPhicH
13. costhetastary

3% de difference en significance entre le meilleure entrainement avec 12 variables et le moins bon à variables
)
* Proposition de variables a conserver :

1. maxdRcy
2. mindRbj
3. dEtacH
4. mindRcy

![IMAGE](/images/q/E509F703A03DD58CB9A31E254544D270.jpg)
{% highlight sh %}
variablesOptimizationLocal rootFiles/h019/ BDTTree_FCNCttWpqq_v0_5jets_tagging:BDTTree_FCNCttWmqq_v0_5jets_tagging BDTTree_FCNCttShergg_allVariables_v1_5jets_tagging dRbW:dPhibW:dEtabW:mindRbj:mindPhibj:dRcH:dPhicH:dEtacH:maxdRcy:mindRcy:maxdPhicy:mindPhicy:costhetastary distances_v0
{% endhighlight %}

# Meff / HT
)
* Ordre d'importance des variables (importance decroissante)

1. HTcjy0y1bjj0j1
2. HT4jets
3. MefftopSM
4. MefftopEx
5. HTjets

2.5% de difference en significance entre le meilleure entrainement avec 12 variables et le moins bon à 2 variables
)
* Proposition de variables a conserver :

1. HTcjy0y1bjj0j1

--> retirer les autres variables n'impact quasiment pas, et dans la mesure où toutes ces variables sont tres correlees entre elles, pas la peine d'en donner plusieurs au BDT, il s'agissait surtout de trouver la meilleure d'entre elles

![IMAGE](/images/q/46C59B0779D07B13D95476B916F4FD8B.jpg)
{% highlight sh %}
variablesOptimizationLocal rootFiles/h019/ BDTTree_FCNCttWpqq_v0_5jets_tagging:BDTTree_FCNCttWmqq_v0_5jets_tagging BDTTree_FCNCttShergg_allVariables_v1_5jets_tagging MefftopSM:HTcjy0y1bjj0j1:HT4jets:HTjets:MefftopEx meffht_v0
{% endhighlight %}

# Optimisation finale
)
* je rajoute costhetastary pour verifier la significance avec toutes les variables selectionnees precedemment (BDT temoins disons ... je re-coderai ce BDT temoins plus proprement une autre fois) ... costhetastary devrait etre eliminee assez rapidement, et permettra peut-etre de supprimer certaines variables qui rankent bien grace a des fluctuations statistiques
)
* Ordre d'importance des variables (importance decroissante)

1. HTcjy0y1bjj0j1
2. mindRbj
3. maxdRcy
4. mtt
5. pTb
6. mW
7. pTyy
8. pTj1
9. costhetastary
10. mindRcy
11. dEtacH

4.9% de difference en significance entre le meilleure entrainement avec 12 variables et le moins bon à 2 variables
)
* Proposition finale de variables a conserver (TRAIN__Thu_Apr__5_14_28_01_2018_) :

1. HTcjy0y1bjj0j1
2. mindRbj
3. maxdRcy
4. mtt
5. pTb
6. mW
7. pTyy

--> significance de 1821.26 (voire 1er bin du bloc precedent la suppression de pTyy) avec seulement 7 variables
--> significance de 1852.59 dans un BDT avec toutes les variables testees dans cette note (32 variables)
==> 1.7% de perte en significance en passant de 32 variables aux 7 meilleures

![IMAGE](/images/q/556BF85876FD5D6614822CEDA2F2F017.jpg)
![IMAGE](/images/q/D9967B6AC96215730D70DE9BBF4E1921.jpg)
![IMAGE](/images/q/99A167FC0DBBBE52B47EA867FDC3D4EE.jpg)
![IMAGE](/images/q/A21B35015024A831C542E0F74F8EB9BE.jpg)
* correlation de ce BDT a myy : profile BDT:myy pour le bruit de fond

![IMAGE](/images/q/4C764DDC74FCBD62CACB71BCE3DE9E1C.jpg)
{% highlight sh %}
variablesOptimizationLocal rootFiles/h019/ BDTTree_FCNCttWpqq_v0_5jets_tagging:BDTTree_FCNCttWmqq_v0_5jets_tagging BDTTree_FCNCttShergg_allVariables_v1_5jets_tagging pTyy:mW:mtt:pTj1:pTb:maxdRcy:mindRbj:dEtacH:mindRcy:HTcjy0y1bjj0j1:costhetastary final_v0
{% endhighlight %}

### for record : all variables
)
{% highlight sh %}
variablesOptimizationLocal rootFiles/h019/ BDTTree_FCNCttWpqq_v0_5jets_tagging:BDTTree_FCNCttWmqq_v0_5jets_tagging BDTTree_FCNCttShergg_allVariables_v1_5jets_tagging pTj0:etaj0:pTj1:etaj1:pTb:etab:dRbW:dPhibW:dEtabW:mW:mindRbj:mindPhibj:MefftopSM:pTratiobjj0j1:pTratioj0j1:pTtt:ytt:mtt:HTcjy0y1bjj0j1:HT4jets:HTjets:dRcH:dPhicH:dEtacH:mTopEx:MefftopEx:maxdRcy:mindRcy:maxdPhicy:mindPhicy:costhetastary:ptyy:etayy allVars
{% endhighlight %}

