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
![IMAGE](/images/q/BFFEF2C9DE1A76B09B0E0B7B8BD4C118.jpg)
| Value   | Meaning                         |
| ------- | ------------------------------- |
| 1       | TruthTau Had.                   |
| 2       | TruthTau Lept.                  |
| - pdgID | parton pdgID if no match in 1-2 |
| 0       | No truthmatch  at all           |
)
![IMAGE](/images/q/CEC21A94AD8D72367910559EB868C931.jpg)
* TruthMatch)
![IMAGE](/images/q/1BF7C40A4CAD3DFACF61E92C7ECF6A7B.jpg)
## DeltaR(MET,Tau)
)
### ttbar
![IMAGE](/images/q/4AFF5E025A1157B513C80DA9D03C5DB9.jpg)
### WHbb
![IMAGE](/images/q/149AE312603E214A54166D1B3747067B.jpg)
### 2 tags
![IMAGE](/images/q/06B217A77909BC935483ED2DCBFC8C8D.jpg)
# Fixed tau origin
Conflicts Maker/PhPy8 with tau status for truthmatching
* re-run with PwPy6
![IMAGE](/images/q/354699282E819CB6CA95CA82D4606F68.jpg)
# DeltaPhi(MET, tau)
)
## ttbar
)
![IMAGE](/images/q/A1C3483DFF47DAA2D8E64AA5603B335B.jpg)
![IMAGE](/images/q/FC1DA6A8EF4F1F97F5B427E142983AC8.jpg)
### ttbar single leptonic
![IMAGE](/images/q/5C8EC5B110C4D7E6C551760C7BA7958F.jpg)
### ttbar dileptonic
![IMAGE](/images/q/DC2B114F60835062165A8FA86E79F35B.jpg)
## WH
)
![IMAGE](/images/q/BF69F9032618E1D122828813F0CFD678.jpg)
![IMAGE](/images/q/56F05E506CB5783759678C43E41464B5.jpg)
{% highlight sh %}
Nominal->Draw("TVector2::Phi_mpi_pi(tau1.Phi()-METp4.Phi())","EventWeight*(nJ<4)*(nTags==2)*(nTaus==1)*(nTruthLepW==1)","")
{% endhighlight %}

