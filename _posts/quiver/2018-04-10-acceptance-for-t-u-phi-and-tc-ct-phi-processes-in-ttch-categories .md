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
* dans le fichier de configuration, j ai pris pour sections efficaces :
  * ttcHyyWmln 410804 : 0.617 fb
  * ttcHyyWpln 410805 : 0.617 fb
  * ttcHyyWmqq 410806 : 1.264 fb
  * ttcHyyWpqq 410807 : 1.264 fb
  * tphi(qqyy) 410753 : 1.227 fb
  * uphi(qqyy) 410757 : 1.227 fb
  * tcphi(qqyy) 410755  : 0.60 fb
  * ctphi(qqyy) 410759  : 0.60 fb
{% endhighlight %}

# Avec la normalisation MCWeight x XSection x lumi

* Selection hadronique 5 jets avec les nouvelles categories
)
{% highlight sh %}
Expected number of events tt pour Br = 0.1%

Categorie       SumW(tt)  tphi  uphi  ctphi tcphi tH/tt
had:M2tight:A : 2.00      0.06  0.06  0.07  0.09  0.14
had:M2tight:B : 3.54      0.45  0.40  0.39  0.40  0.46
had:M1loose:A : 1.35      0.06  0.07  0.07  0.06  0.19
had:M1loose:A : 2.77      0.40  0.37  0.30  0.30  0.49
{% endhighlight %}

{% highlight sh %}
- comme prevu, tres peu d evenements tH se trouvent en categorie A, du fait qu il n y a pas le jet c
- par contre, pas mal d evenements tH passentla selection pour les categories 1-B et 2-B, bien que l acceptance pour les evts tH soit ~ 2x moins grande que pour les evts tt (e.g. categorie 1.B dans les cutflows ci-dessous) par rapport a la preselection 4 jets
{% endhighlight %}

## comparaison de cutflow

* samples Wmqq et uphi
)
### Cutflow Wmqq
)
![IMAGE](/images/q/8E26CAC89EBBBB9E0F58F0559C1BB3F7.jpg)
### Cutflow tcphi
)
![IMAGE](/images/q/E65F1DB4255946203BA7D82C18A9E876.jpg)
## detail par sample
)
{% highlight sh %}
Processing root file FCNCttWpln_v1_5jets_tagging.root
Using 5 leading jets in combinatoric
had:M2tight:A : 332 	0.0787313
had:M2tight:B : 604 	0.123346
had:M1loose:A : 667 	0.134404
had:M1loose:A : 1255 	0.247878
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCttWmln_v1_5jets_tagging.root
Using 5 leading jets in combinatoric
had:M2tight:A : 355 	0.0570334
had:M2tight:B : 624 	0.0978305
had:M1loose:A : 600 	0.11878
had:M1loose:B : 1127 	0.25968
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCttWpqq_v1_5jets_tagging.root
Using 5 leading jets in combinatoric
had:M2tight:A : 1811 	0.904229
had:M2tight:B : 3316 	1.5587
had:M1loose:A : 1211 	0.579124
had:M1loose:B : 2453 	1.13612
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCttWmqq_v1_5jets_tagging.root
Using 5 leading jets in combinatoric
had:M2tight:A : 1829 	0.955565
had:M2tight:B : 3573 	1.75565
had:M1loose:A : 1185 	0.519523
had:M1loose:B : 2501 	1.12547
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCctphiQHgamgambWqq_v1_5jets_tagging.root
Using 5 leading jets in combinatoric
had:M2tight:A : 233 	0.0719167
had:M2tight:B : 1122 	0.388507
had:M1loose:A : 165 	0.0650322
had:M1loose:B : 793 	0.302794
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCuphiQHgamgambWqq_v1_5jets_tagging.root
Using 5 leading jets in combinatoric
had:M2tight:A : 72 	0.0578883
had:M2tight:B : 560 	0.397342
had:M1loose:A : 74 	0.0700264
had:M1loose:B : 489 	0.366217
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCtcphiQHgamgambWqq_v1_5jets_tagging.root
Using 5 leading jets in combinatoric
had:M2tight:A : 254 	0.0923442
had:M2tight:B : 1151 	0.402025
had:M1loose:A : 141 	0.0561969
had:M1loose:B : 852 	0.304061
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCtphiQHgamgambWqq_v1_5jets_tagging.root
Using 5 leading jets in combinatoric
had:M2tight:A : 81 	0.0613579
had:M2tight:B : 593 	0.445457
had:M1loose:A : 65 	0.0550036
had:M1loose:B : 507 	0.403232
{% endhighlight %}


)
# Version avec les poids MC seuls
)
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
