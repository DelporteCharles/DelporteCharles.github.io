---
title: Dependence of colourflow on angular separation
date: '2017-08-25'
tags:
- colorflow
---
Plots with reco tracks but no selection at all (cuts in reader desactiviated)

Colour reconnection effects may be the cause of Zbb not being discriminating :
* Zbb would typically have back-to-back gluon and Z, i.e. close-by b-jets from the gluon splitting --> reconnected in colour (MCNet)

![IMAGE](/images/q/86C9694EAC85A0C48C9ADB94BF99C2AA.jpg)
Hypothesis :
* The leading jet steal constituents from the sub-leading jet

Verification :
* Plot the distribution Sum(pT) over jets constituents from the B-hadron / B-hadron pT
* Sum(pT) over jets constituents from the B-hadron / B-jet pT is a bad idea, if the jet's pt is actually falsified : leading will have enhanced pT so lower ratio, which is not intuitive
* No obvious evidence from the appropriate b quark / b jet constituents : maybe crossing the b quarks would show it better 
* ![IMAGE](/images/q/26DB0CE74FA4A25A8D68620BD283EC00.jpg)
2nd Hypothesis :
* Without necessarily stealing constituents to the other jet, the distribution of constituents within the jet may vary, with some non-intuitive dependence on dRbb --> previous hypothesis show that the subleading jet has less constituents, but is it due to the number of interacting daughters which is lower, or is there really some stealing ?
* Following plot shows at least that the magnitude of the pull angle is different according to dRbb, and is correlated with dTheta
![IMAGE](/images/q/FB6B747B913692838DD0008A79D078AA.jpg)
## A priori final answer :
* New implementation of the code
)
### Stealing number of constituents depency
![IMAGE](/images/q/872162E03A6C87138A367025C14A47ED.jpg)
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

