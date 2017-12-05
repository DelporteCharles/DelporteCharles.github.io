---
title: Tau studies in ttbar samples
date: '2017-11-14'
tags: []
---
# Purpose

Interest in extending the SM VH(bb) analyis to events with taus in an additionnal category

![IMAGE](/images/q/IMAGE)

## Tau origin

* Truth matching with truth tau or partons with a dR association with R=0.2

![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

| Value   | Meaning                         |
| ------- | ------------------------------- |
| 1       | TruthTau Had.                   |
| 2       | TruthTau Lept.                  |
| - pdgID | parton pdgID if no match in 1-2 |
| 0       | No truthmatch  at all           |



![IMAGE](/images/q/IMAGE)
* TruthMatch = 0 in red
* TruthMatch != 0 in blue

![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

## DeltaR(MET,Tau)
* ttbar :
![IMAGE](/images/q/IMAGE)
* WHbb
![IMAGE](/images/q/IMAGE)
* in 2 tags
* ![IMAGE](/images/q/IMAGE)

# Fixed tau origin
Conflicts Maker/PhPy8 with tau status for truthmatching
* re-run with PwPy6
![IMAGE](/images/q/IMAGE)

# DeltaPhi(MET, tau)
* ttbar
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
  * ttbar single leptonic
  ![IMAGE](/images/q/IMAGE)
  * ttbar dileptonic
  ![IMAGE](/images/q/IMAGE)
* WH
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

{% highlight sh %}
Nominal->Draw("TVector2::Phi_mpi_pi(tau1.Phi()-METp4.Phi())","EventWeight*(nJ<4)*(nTags==2)*(nTaus==1)*(nTruthLepW==1)","")
{% endhighlight %}

