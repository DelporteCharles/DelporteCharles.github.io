---
title: FCNC normalisation des samples aux sections efficaces
date: '2018-04-11'
tags:
- fcnc
---
# Motivation
)
{% highlight sh %}
* avoir les poids d evenements corrects en tenant compte de :
  * MC Weight
  * XSection
  * Lumi = 36.1 fb-1
{% endhighlight %}

# Sections efficaces

* pour Br)
{% highlight sh %}
JB : Pour un coefficient d’operateur valant C = 1, les sections efficaces (avant BR de W et de H) 
pour les lots tphi,uphi sont 365.2 fb et pour les lots tcphi,ctphi 52.8 fb. 

 Pour un Br (t —> qH) = 0.1%, en supposant qu’un seul operateur contribue, cela
donne un coefficient C = 1.486 (papier de Maltoni et Zhang). Donc finalement tu 
devrais prendre les sections efficaces 806.3 fb et 116.6 fb pour les lots tH si tu 
normalises le lot ttbar a Br = 0.1%. 
{% endhighlight %}

{% highlight sh %}
* d apres mes calculs :
  * ttcHyyWmln 410804 : 0.617 fb
  * ttcHyyWpln 410805 : 0.617 fb
  * ttcHyyWmqq 410806 : 1.264 fb
  * ttcHyyWpqq 410807 : 1.264 fb
  * tphi(qqyy) 410753 : 1.227 fb
  * uphi(qqyy) 410757 : 1.227 fb
  * tcphi(qqyy) 410755  : 0.60 fb
  * ctphi(qqyy) 410759  : 0.60 fb
{% endhighlight %}

# Yields selection papier

* yields attendus dans le papier (pour Br(tqH))
![IMAGE](/images/q/842650B95AA443AD45DBD8B5073CF1C8.jpg)
{% highlight sh %}
Expected number of events tt pour Br = 0.1%

Categorie     SumW
had:M2tight : 3.67
had:M1loose : 5.45
lep:M2tight : 2.14
lep:M1loose : 0.31
{% endhighlight %}

### detail par sample (selection papier)
)
{% highlight sh %}
Processing root file FCNCttWmln_v1_4jets.root
Categorie     NEvt  SumW
had:M2tight : 617 	0.108168
had:M1loose : 1986 	0.415323
lep:M2tight : 4475 	1.05583
lep:M1loose : 621 	0.152549
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCttWpln_v1_4jets.root
Categorie     NEvt  SumW
had:M2tight : 612 	0.138154
had:M1loose : 2135 	0.444799
lep:M2tight : 4512 	1.08692
lep:M1loose : 570 	0.151948
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCttWmqq_v1_4jets.root
Categorie     NEvt  SumW
had:M2tight : 3276 	1.80115
had:M1loose : 5013 	2.27904
lep:M2tight : 5 	0.00305398
lep:M1loose : 0 	0
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCttWpqq_v1_4jets.root
Categorie     NEvt  SumW
had:M2tight : 3245 	1.62555
had:M1loose : 4883 	2.30968
lep:M2tight : 1 	-0.00105561
lep:M1loose : 1 	0.000778055
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCctphiQHgamgambWqq_v1_4jets.root
Categorie     NEvt  SumW
had:M2tight : 1070 	0.379653
had:M1loose : 1248 	0.469196
lep:M2tight : 0 	0
lep:M1loose : 1 	0.000193842
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCuphiQHgamgambWqq_v1_4jets.root
Categorie     NEvt  SumW
had:M2tight : 508 	0.400913
had:M1loose : 708 	0.562371
lep:M2tight : 0 	0
lep:M1loose : 0 	0
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCtcphiQHgamgambWqq_v1_4jets.root
Categorie     NEvt  SumW
had:M2tight : 1112 	0.41011
had:M1loose : 1295 	0.477442
lep:M2tight : 3 	0.00191544
lep:M1loose : 0 	0
{% endhighlight %}

{% highlight sh %}
Processing root file FCNCtphiQHgamgambWqq_v1_4jets.root
Categorie     NEvt  SumW
had:M2tight : 530 	0.402993
had:M1loose : 700 	0.563817
lep:M2tight : 0 	0
lep:M1loose : 0 	0
{% endhighlight %}


)
