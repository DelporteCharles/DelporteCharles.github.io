---
title: FCNC data yields
date: '2018-02-15'
tags:
- data
- fcnc
---
# Purpose

* comparison with Daniel and Jean-Baptiste
)
# Sample

* data 15-16
)
# Selection

* paper selection
* paper selection + b-Tagging
* paper selection + b-Tagging + try 5 leading jets

)
# paper selection

* nombres identiques a ceux de Jean-Baptiste (c'est bien 105 je crois, tu avais copie 115 dans ton cahier)
* nombres differents a ceux de Daniel
)
{% highlight sh %}
Hadron-Tight 105
Hadron-Loose 365

Lepton-Tight 2
Lepton-Loose 6
{% endhighlight %}

# paper selection + b-Tagging
)
{% highlight sh %}
Hadron-Tight A 20
Hadron-Tight B 66
Hadron-Tight C 38

Hadron-Loose A 47
Hadron-Loose B 252
Hadron-Loose C 132

Lepton-Tight A 1
Lepton-Tight B 0
Lepton-Tight C 3

Lepton-Loose A 1
Lepton-Loose B 1
Lepton-Loose C 4
{% endhighlight %}

# paper selection + b-Tagging + try 5 leading jets
)
{% highlight sh %}
Hadron-Tight A 29
Hadron-Tight B 113
Hadron-Tight C 62

Hadron-Loose A 45
Hadron-Loose B 265
Hadron-Loose C 119

Lepton-Tight A 2
Lepton-Tight B 3
Lepton-Tight C 5

Lepton-Loose A 0
Lepton-Loose B 3
Lepton-Loose C 4
{% endhighlight %}

# Changements a mes anciens nombres

* j'ai recopie les fichiers config de JB pour la deuxieme iteration, ce qui explique surement que je retrouve ses nombres), je liste en-dessous les changements que je vois entre les fichiers log de mes deux iterations
)
{% highlight sh %}
asetup AnalysisBase,21.2.16 --> asetup AnalysisBase,21.2.17
{% endhighlight %}

{% highlight sh %}
EventHandler.PRW.ConfigFilesMC16a: FCNCAna/ntpurwmc16a.root -->  HGamAnalysisFramework/ntpurwmc16afastim.root    
{% endhighlight %}

{% highlight sh %}
IsAFII.410804: YES                                                                                                          
IsAFII.410805: YES
IsAFII.410806: YES
IsAFII.410807: YES 
{% endhighlight %}


)
