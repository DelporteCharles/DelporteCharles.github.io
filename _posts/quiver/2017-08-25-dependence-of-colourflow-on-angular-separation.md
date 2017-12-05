---
title: Dependence of colourflow on angular separation
date: '2017-08-25'
tags:
- colorflow
---
Plots with reco tracks but no selection at all (cuts in reader desactiviated)

Colour reconnection effects may be the cause of Zbb not being discriminating :
* Zbb would typically have back-to-back gluon and Z, i.e. close-by b-jets from the gluon splitting --> reconnected in colour (MCNet)

![IMAGE](/images/q/IMAGE)

* Even more, the leading jet is likely to "steal" jets truht-constituents from the sub-leading jet, see for dR<0.8, but this effect is invisible on ColourFlow21 in inclusive dR and will tend to make ColourFlow12 to peak at 0 !
![IMAGE](/images/q/IMAGE)

* Inversely, typical ttbar events would have back-to-back top quarks, i.e. at first order back-to-back b-quarks --> not reconnected in colour
![colourflow_ttbar_dR.png](/images/q/colourflow_ttbar_dR.png)

* Same jet stealing in ttbar, but less stat at low dR

![IMAGE](/images/q/IMAGE)

Implemented in Sherpa (?)
https://arxiv.org/pdf/hep-ph/0311085.pdf
https://sherpa.hepforge.org/trac/wiki/SherpaPublications

Hypothesis :
* The leading jet steal constituents from the sub-leading jet

Verification :
* Plot the distribution Sum(pT) over jets constituents from the B-hadron / B-hadron pT
* Sum(pT) over jets constituents from the B-hadron / B-jet pT is a bad idea, if the jet's pt is actually falsified : leading will have enhanced pT so lower ratio, which is not intuitive
* No obvious evidence from the appropriate b quark / b jet constituents : maybe crossing the b quarks would show it better 
* ![IMAGE](/images/q/IMAGE)
* From a more direct approach, couting the number of constituents in the jet, it looks like close-by jets are exchanging constituents : these are probably not the largest pT contributions to the jet (as unseen from energy fractions) but if they are far from the jet's center, they would have an important weight in colourflow computation
* ![IMAGE](/images/q/IMAGE)
  * looks like something is happening at dR > 3 --> related to the pseudo-rapidity maybe ?
* ![IMAGE](/images/q/IMAGE)
* Moreover, large correlation between the number of constituents and the pulVector magnitude
* ![IMAGE](/images/q/IMAGE)
* ![IMAGE](/images/q/IMAGE)
* red is the leading jet, blue is subleading
* ![IMAGE](/images/q/IMAGE)

2nd Hypothesis :
* Without necessarily stealing constituents to the other jet, the distribution of constituents within the jet may vary, with some non-intuitive dependence on dRbb --> previous hypothesis show that the subleading jet has less constituents, but is it due to the number of interacting daughters which is lower, or is there really some stealing ?
* Following plot shows at least that the magnitude of the pull angle is different according to dRbb, and is correlated with dTheta
![IMAGE](/images/q/IMAGE)

## A priori final answer :
* New implementation of the code

### Stealing number of constituents depency
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

{% highlight javascript %}
root -l submitDir_ZnunuB_Pt140_280_Sherpa_Test/hist-user.cdelport.r363420e4772_Truth1_v2_EXT0.root 
tree->Draw("abs(dTheta2_4):nConstituentsIntLost2_4>>h","passLoose_4==1&&dR_4<0.8","colz")
h->ProfileX("hh")
hh->Draw()
new TCanvas
tree->Draw("abs(dTheta2_4):nConstituentsIntLost2_4>>h2","passLoose_4==1&&dR_4>1","colz")
h2->ProfileX("hh2")
hh2->Draw()
new TCanvas
tree->Draw("abs(dTheta2_4)","passLoose_4==1&&dR_4<0.8","colz")
new TCanvas
tree->Draw("abs(dTheta2_4)","passLoose_4==1&&dR_4>1","colz")
{% endhighlight %}

