---
title: FCNC Matching with MTop
date: '2018-04-20'
tags: []
---
# Purpose

- definir a partir de quelle valeur de mTop1 on doit chercher les combinaisons les plus proches dans tous les categories, et mTop2 pour la categorie 1
)
# Procedure
)
- selection sur la combinatoire comme definit precedemment
- je remplit de facon independante les histogrammes de :
  - mTop1 si dR(c-jet, c-quark) < 0.4
  - mTop2 si dR(b-jet, b-quark) < 0.4 et dR(jet0, quark0) < 0.4 et dR(jet1, quark1)
  
- Jean-Baptiste suggerait de prendre la combinaison matchée en dR, mais est-ce que ca n'introduirait pas un biais par rapport a notre strategie dans son ensemble ?
)
# Valeurs moyennes de mTop mesurees avec le matching
)
{% highlight sh %}
1A :
  mTop1 = 171.9 GeV
  mTop2 = 170 GeV
1B :
  mTop1 = 172.4 GeV
  mTop2 = 171.7 GeV
2A :
  mTop1 = 172.2 GeV
2B :
  mTop1 = 172.4 GeV
  
Proposition commune a toutes les categories :
  mTop1 : 172 GeV
  mTop2 : 171 GeV
{% endhighlight %}


)
# Categorie 1A
)
![IMAGE](/images/q/73F30EC980942B557783A0BDA6B11998.jpg)
![IMAGE](/images/q/EDCC371E626358103B48DC419E3C99BD.jpg)
# Categorie 1B
)
![IMAGE](/images/q/490E2619C270C419BFA74FB284EAAEEE.jpg)
![IMAGE](/images/q/03A8630950AABEC017F8868D8F9D6757.jpg)
# Categorie 2A
)
![IMAGE](/images/q/65DC188C0DEC1C2B6616952ACD98AB8B.jpg)
# Categorie 2B
)
![IMAGE](/images/q/6888111F1C3ECACEBF0EA7CFC13FFC9B.jpg)

)
