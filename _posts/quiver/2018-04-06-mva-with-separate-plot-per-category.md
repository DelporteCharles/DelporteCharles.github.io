---
title: MVA with separate plot per category
date: '2018-04-06'
tags:
- fcnc
---
# Purpose

* verifier la forme du BDT separement pour chaque categorie
* et aussi celle des variables du top SM, pour lequel on a de bons matchings en categorie 1, mais pas en categorie 2
  * comment se comportent les variables du top SM lorsqu'on a des mauvais jets dans la combinaison ? 
    * mindRbj
    * mW
    * mtt
  * question sous-jacente : utiliser la combinaison la plus proche de mTop2=173 pour la categorie 2 ?
)
# BDT à l'étude

* BDT proposé comme baseline, a partir des optimisations sur MG:Sherpa h019

* Liste des variables :

1. HTcjy0y1bjj0j1
2. mindRbj
3. maxdRcy
4. mtt
5. pTb
6. mW
7. pTyy
)
# Observations principales

- faible stat dans les categories 1-A et 2-A ce qui ne permet un tres bon accord training/testing ...
- bon accord training/testing en 1-B et 2-B
- comme Jean-Baptiste l'avais intuité, certaines variables (mW et mtt) ont moins de sens dans la catégorie 2 dans la mesure ou l'un des 2 jets non-b-tagged vient surement d'un ISR/FSR/PW et n'apporte donc pas d'information pour discriminer le signal du bruit de fond : peut-etre faut-il en effet prendre un jeu de variables different pour les categories 1 et 2 ...
- par contre pour mindRbj, la discrimination est presque plus importante en categorie 2 que categorie 1 (pas discriminante du tout en 1-B)
)
# Plot de comparaison des BDT par categorie (plus de plots en dessous)
)
Categories sur le screenshot avec 4 plots :
)
{% highlight sh %}
1-A      |      1-B
2-A      |      2-B
{% endhighlight %}

![IMAGE](/images/q/61EFAE6D42BC81AF429CC1B78F9A84DD.jpg)
# Categorie 1-A
)
![IMAGE](/images/q/58A641622733F7743417593E5CC43659.jpg)
![IMAGE](/images/q/F3FF2FAC83DF8EDAE60191A0D1F62BFD.jpg)
![IMAGE](/images/q/8FC0473EB7BC40673CEFD0B9A139193A.jpg)
![IMAGE](/images/q/F1110CD2760D064885357B570B22B898.jpg)
# Categorie 1-B
)
![IMAGE](/images/q/234C83DBBE074BF53D307739195C2662.jpg)
![IMAGE](/images/q/D7524232FECE11C31E9D8B1E043FCEB4.jpg)
![IMAGE](/images/q/73DC9036A09A86725F70442BE4BCDA36.jpg)
![IMAGE](/images/q/DD9F424B996802F3B19BFD4ADF9F2031.jpg)
# Categorie 2-A
)
![IMAGE](/images/q/C20C9B3C6D26E1DB05DB85E088CB1214.jpg)
![IMAGE](/images/q/4E769A6317A9A5D862972FC8B4D8F248.jpg)
![IMAGE](/images/q/04F54AC9FC94B6EA5E838B49B5199B77.jpg)
![IMAGE](/images/q/8D75BFD7D669527BA3C4482A27400865.jpg)
# Categorie 2-B
)
![IMAGE](/images/q/9172142E3B42812F177EA5D95D77806D.jpg)
![IMAGE](/images/q/59EE94353D4C9C420495BD12A06EC773.jpg)
![IMAGE](/images/q/030DC6E326B30250B6B1061D51FD47BD.jpg)
![IMAGE](/images/q/79041CBA776AD07CCDCB243B12258C80.jpg)
## Correspondance de categories dans le fichier root et l'analyse

- cat1A fold1o2)
{% highlight sh %}
<SubMethod Index="0" Method="BDT::BDTCat_1o2_tagcat_1_sel_1" Cut="(((EventNumberMod2%2&gt;-0.5)&amp;&amp;(EventNumberMod2%2&lt;0.5))&amp;&amp;(tagcat==1))&amp;&amp;(mTopSM&gt;=120&amp;&amp;mTopSM&lt;=220)" Variables="pTyy:mW:mtt:pTb:maxdRcy:mindRbj:HTcjy0y1bjj0j1">
<SubMethod Index="1" Method="BDT::BDTCat_1o2_tagcat_1_sel_2" Cut="(((EventNumberMod2%2&gt;-0.5)&amp;&amp;(EventNumberMod2%2&lt;0.5))&amp;&amp;(tagcat==1))&amp;&amp;(mTopSM&lt;120||mTopSM&gt;220)" Variables="pTyy:mW:mtt:pTb:maxdRcy:mindRbj:HTcjy0y1bjj0j1">
<SubMethod Index="2" Method="BDT::BDTCat_2o2_tagcat_1_sel_1" Cut="(((EventNumberMod2%2&gt;0.5)&amp;&amp;(EventNumberMod2%2&lt;1.5))&amp;&amp;(tagcat==1))&amp;&amp;(mTopSM&gt;=120&amp;&amp;mTopSM&lt;=220)" Variables="pTyy:mW:mtt:pTb:maxdRcy:mindRbj:HTcjy0y1bjj0j1">
<SubMethod Index="3" Method="BDT::BDTCat_2o2_tagcat_1_sel_2" Cut="(((EventNumberMod2%2&gt;0.5)&amp;&amp;(EventNumberMod2%2&lt;1.5))&amp;&amp;(tagcat==1))&amp;&amp;(mTopSM&lt;120||mTopSM&gt;220)" Variables="pTyy:mW:mtt:pTb:maxdRcy:mindRbj:HTcjy0y1bjj0j1">
<SubMethod Index="4" Method="BDT::BDTCat_1o2_tagcat_2_sel_1" Cut="(((EventNumberMod2%2&gt;-0.5)&amp;&amp;(EventNumberMod2%2&lt;0.5))&amp;&amp;(tagcat==2))&amp;&amp;(mTopSM&gt;=120&amp;&amp;mTopSM&lt;=220)" Variables="pTyy:mW:mtt:pTb:maxdRcy:mindRbj:HTcjy0y1bjj0j1">
<SubMethod Index="5" Method="BDT::BDTCat_1o2_tagcat_2_sel_2" Cut="(((EventNumberMod2%2&gt;-0.5)&amp;&amp;(EventNumberMod2%2&lt;0.5))&amp;&amp;(tagcat==2))&amp;&amp;(mTopSM&lt;120||mTopSM&gt;220)" Variables="pTyy:mW:mtt:pTb:maxdRcy:mindRbj:HTcjy0y1bjj0j1">
<SubMethod Index="6" Method="BDT::BDTCat_2o2_tagcat_2_sel_1" Cut="(((EventNumberMod2%2&gt;0.5)&amp;&amp;(EventNumberMod2%2&lt;1.5))&amp;&amp;(tagcat==2))&amp;&amp;(mTopSM&gt;=120&amp;&amp;mTopSM&lt;=220)" Variables="pTyy:mW:mtt:pTb:maxdRcy:mindRbj:HTcjy0y1bjj0j1">
<SubMethod Index="7" Method="BDT::BDTCat_2o2_tagcat_2_sel_2" Cut="(((EventNumberMod2%2&gt;0.5)&amp;&amp;(EventNumberMod2%2&lt;1.5))&amp;&amp;(tagcat==2))&amp;&amp;(mTopSM&lt;120||mTopSM&gt;220)" Variables="pTyy:mW:mtt:pTb:maxdRcy:mindRbj:HTcjy0y1bjj0j1">
{% endhighlight %}

