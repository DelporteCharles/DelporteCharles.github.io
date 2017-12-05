---
title: Tau studies in ttbar samples
date: '2017-11-14'
tags: []
---
# Purpose

Interest in extending the SM VH(bb) analyis to events with taus in an additionnal category

![IMAGE](/images/q/A69FC298ED256E92D0DA48E92F87CAEA.jpg)
## Tau origin

* Truth matching with truth tau or partons with a dR association with R=0.2

![IMAGE](/images/q/E350848D2D9AA6237AA8587AF5F8C1F3.jpg)
## DeltaR(MET,Tau)
* ttbar :
![IMAGE](/images/q/4AFF5E025A1157B513C80DA9D03C5DB9.jpg)
# Fixed tau origin
Conflicts Maker/PhPy8 with tau status for truthmatching
* re-run with PwPy6
![IMAGE](/images/q/354699282E819CB6CA95CA82D4606F68.jpg)
# DeltaPhi(MET, tau)
* ttbar
![IMAGE](/images/q/A1C3483DFF47DAA2D8E64AA5603B335B.jpg)
{% highlight sh %}
Nominal->Draw("TVector2::Phi_mpi_pi(tau1.Phi()-METp4.Phi())","EventWeight*(nJ<4)*(nTags==2)*(nTaus==1)*(nTruthLepW==1)","")
{% endhighlight %}

