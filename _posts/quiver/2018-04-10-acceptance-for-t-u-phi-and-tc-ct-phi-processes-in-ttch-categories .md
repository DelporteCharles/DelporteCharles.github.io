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

# Mes yields (avec et sans la correction pour le coefficient C à Br(tqH))
{% highlight sh %}
JB : Pour un coefficient d’operateur valant C = 1, les sections efficaces (avant BR de W et de H) 
pour les lots tphi,uphi sont 365.2 fb et pour les lots tcphi,ctphi 52.8 fb. 

 Pour un Br (t —> qH) = 0.1%, en supposant qu’un seul operateur contribue, cela
donne un coefficient C = 1.486 (papier de Maltoni et Zhang). Donc finalement tu 
devrais prendre les sections efficaces 806.3 fb et 116.6 fb pour les lots tH si tu 
normalises le lot ttbar a Br = 0.1%. 
{% endhighlight %}

{% highlight sh %}
* dans le fichier de configuration, j avais pour sections efficaces :
   * tphi 410753  : 246.46  --> XSection *= 806.3/246.46 = 3.27
   * uphi 410757  : 247.49  --> XSection *= 806.3/247.49 = 3.26
   * tcphi 410755 : 35.6    --> XSection *= 116.6/35.6   = 3.28
   * ctphi 410759 : 35.7    --> XSection *= 116.6/35.7   = 3.27
{% endhighlight %}

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
had:M2tight:A : 81    21.7551   71.1
had:M2tight:B : 593   141.22    460.4
had:M1loose:A : 65 	  18.0704   59.3
had:M1loose:B : 507   126.477   413.6
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCuphiQHgamgambWqq_v0_5jets_tagging.root
Categorie       NEvt  SumW      SumW*C*C  Fraction par rapport à Wmqq+Wpqq
had:M2tight:A : 72 	  17.7015   57.9
had:M2tight:B : 560   130.567   425.6
had:M1loose:A : 74    21.393    70.2
had:M1loose:B : 489   116.162   379.8
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCtcphiQHgamgambWqq_v0_5jets_tagging.root
Categorie       NEvt  SumW      SumW*C*C  Fraction par rapport à Wmqq+Wpqq
had:M2tight:A : 254 	8.76254   28.7
had:M2tight:B : 1151 	37.2123   121.3
had:M1loose:A : 141 	5.22598   17.1
had:M1loose:B : 852 	28.8234   94.3
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCctphiQHgamgambWqq_v0_5jets_tagging.root
Categorie       NEvt  SumW      SumW*C*C  Fraction par rapport à Wmqq+Wpqq
had:M2tight:A : 233 	7.02204   23.0
had:M2tight:B : 1122 	36.2246   118.1
had:M1loose:A : 165 	6.17848   20.3
had:M1loose:B : 793 	28.0391   91.7
{% endhighlight %}

# Nombres de Daniel

* la difference est comprise
  * Daniel etait resté sur les essais de selection sur les jets : pT > 30 GeV et |eta| < 2.5
)
![IMAGE](/images/q/3583BE7543F8A8680CE0FFD9BBC7F857.jpg)
