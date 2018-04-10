---
title: Acceptance for t-u-phi and tc-ct-phi processes in ttcH categories 
date: '2018-04-10'
tags:
- fcnc
---
# Motivation

* mesure de l'acceptance des processus t/u-phi et tc/ct-phi dans les categories actuelles (1-A/B et 2-A/B)
* design de categories dediees dans une autre note
)
# Samples

* ttWmqq 410806
* ttWpqq 410807
* tphi 410753  h019 reprocessé avec le tag officiel
* uphi 410757  h019 reprocessé avec le tag officiel
* tcphi 410755 h019 reprocessé avec le tag officiel
* ctphi 410759 h019 reprocessé avec le tag officiel
)
{% highlight sh %}
/sps/atlas/d/devivie/FCNC/ANA/ANAR21OFF/run/MxAODrun410806e5483_e5984_a875_r9364_r9315_p3472v0
/sps/atlas/d/devivie/FCNC/ANA/ANAR21OFF/run/MxAODrun410807e5483_e5984_a875_r9364_r9315_p3472v0
/sps/atlas/d/delporte/FCNC/run/prodMxAOD/tphiQHgamgambWqq_410753__v1
/sps/atlas/d/delporte/FCNC/run/prodMxAOD/tcphiQHgamgambWqq_410755_v1
/sps/atlas/d/delporte/FCNC/run/prodMxAOD/uphiQHgamgambWqq_410757_v1
/sps/atlas/d/delporte/FCNC/run/prodMxAOD/ctphiQHgamgambWqq_410759__v1
{% endhighlight %}

# Observations principales

* Contributions au signal W+-qq (avec rescaling C*C pour Br(tqH)=0.1%)
  * 1A : 7.5e-4
  * 1B : 2.7e-3
  * 2A : 1.2e-3
  * 2B : 3.3e-3
  
* pour la suite : essais de coupures/cutflows pour construire une categorie dediee
)
# Mes yields (avec et sans la correction pour le coefficient C à Br(tqH))
{% highlight sh %}
JB : Pour un coefficient d’operateur valant C = 1, les sections efficaces (avant BR de W et de H) 
pour les lots tphi,uphi sont 365.2 fb et pour les lots tcphi,ctphi 52.8 fb. 

 Pour un Br (t —> qH) = 0.1%, en supposant qu’un seul operateur contribue, cela
donne un coefficient C = 1.486 (papier de Maltoni et Zhang). Donc finalement tu 
devrais prendre les sections efficaces 806.3 fb et 116.6 fb pour les lots tH si tu 
normalises le lot ttbar a Br = 0.1%. 
{% endhighlight %}

* dans le fichier de configuration, j'avais pour sections efficaces :
   * tphi 410753  : 246.46  --> XSection *= 365.2/246.46)
{% highlight sh %}
Processing root file FCNCttWmqq_v0_5jets_tagging.root
Categorie       NEvt  SumW
had:M2tight:A : 1829 	55628.8   
had:M2tight:B : 3573 	102304
had:M1loose:A : 1185 	29248.5
had:M1loose:B : 2501 	65911.6
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCttWpqq_v0_5jets_tagging.root
Categorie       NEvt  SumW
had:M2tight:A : 1811 	52375.4
had:M2tight:B : 3316 	90351.3
had:M1loose:A : 1211 	31921.7
had:M1loose:B : 2453 	65202.8
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCtphiQHgamgambWqq_v0_5jets_tagging.root
Categorie       NEvt  SumW      SumW*C*C  Fraction de SumW par rapport à Wmqq+Wpqq
had:M2tight:A : 81    21.7551   32.24     3e-4
had:M2tight:B : 593   141.22    209.28    1.1e-3
had:M1loose:A : 65 	  18.0704   26.78     4.4e-4
had:M1loose:B : 507   126.477   187.43    1.4e-3
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCuphiQHgamgambWqq_v0_5jets_tagging.root
Categorie       NEvt  SumW      SumW*C*C  Fraction par rapport à Wmqq+Wpqq
had:M2tight:A : 72 	  17.7015   26.13     2.4e-4
had:M2tight:B : 560   130.567   192.71    1e-3
had:M1loose:A : 74    21.393    31.58     5.16e-4
had:M1loose:B : 489   116.162   171.46    1.3e-3
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCtcphiQHgamgambWqq_v0_5jets_tagging.root
Categorie       NEvt  SumW      SumW*C*C  Fraction par rapport à Wmqq+Wpqq
had:M2tight:A : 254 	8.76254   13.00     1.2e-4
had:M2tight:B : 1151 	37.2123   55.19     2.9e-4
had:M1loose:A : 141 	5.22598   7.75      1.3e-4
had:M1loose:B : 852 	28.8234   42.75     3.3e-4
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCctphiQHgamgambWqq_v0_5jets_tagging.root
Categorie       NEvt  SumW      SumW*C*C  Fraction par rapport à Wmqq+Wpqq
had:M2tight:A : 233 	7.02204   10.38     9.6e-5
had:M2tight:B : 1122 	36.2246   53.54     2.8e-4
had:M1loose:A : 165 	6.17848   9.13      1.5e-4
had:M1loose:B : 793 	28.0391   41.44     3.16e-4
{% endhighlight %}

# Nombres de Daniel

* la difference est comprise
  * Daniel etait resté sur les essais de selection sur les jets : pT > 30 GeV et |eta| < 2.5
)
![IMAGE](/images/q/3583BE7543F8A8680CE0FFD9BBC7F857.jpg)
