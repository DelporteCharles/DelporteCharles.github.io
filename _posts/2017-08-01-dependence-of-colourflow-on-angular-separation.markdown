---
layout: post
title: Dependence of colourflow on angular separation
tags: 
    - colorflow
---

Plots with reco tracks but no selection at all (cuts in reader desactiviated)

Colour reconnection effects may be the cause of Zbb not being discriminating :
* Zbb would typically have back-to-back gluon and Z, i.e. close-by b-jets from the gluon splitting --> reconnected in colour (MCNet)

![IMAGE](quiver-image-url/86C9694EAC85A0C48C9ADB94BF99C2AA.jpg =1425x520)

* Even more, the leading jet is likely to "steal" jets truht-constituents from the sub-leading jet, see for dR<0.8, but this effect is invisible on ColourFlow21 in inclusive dR and will tend to make ColourFlow12 to peak at 0 !
![IMAGE](quiver-image-url/0D10FC88E6FBF123402D4721F491EC4E.jpg =1193x764)

* Inversely, typical ttbar events would have back-to-back top quarks, i.e. at first order back-to-back b-quarks --> not reconnected in colour
![colourflow_ttbar_dR.png](quiver-image-url/43E979CB35C65324123174940F7CCC6E.png =1426x524)

* Same jet stealing in ttbar, but less stat at low dR

![IMAGE](quiver-image-url/6B50B75EF695EF4F8AF2FDC0A3D084E0.jpg =1196x767)

Implemented in Sherpa (?)
https://arxiv.org/pdf/hep-ph/0311085.pdf
https://sherpa.hepforge.org/trac/wiki/SherpaPublications

Hypothesis :
* The leading jet steal constituents from the sub-leading jet

Verification :
* Plot the distribution Sum(pT) over jets constituents from the B-hadron / B-hadron pT
* Sum(pT) over jets constituents from the B-hadron / B-jet pT is a bad idea, if the jet's pt is actually falsified : leading will have enhanced pT so lower ratio, which is not intuitive
* No obvious evidence from the appropriate b quark / b jet constituents : maybe crossing the b quarks would show it better 
* ![IMAGE](quiver-image-url/26DB0CE74FA4A25A8D68620BD283EC00.jpg =1194x767)
* From a more direct approach, couting the number of constituents in the jet, it looks like close-by jets are exchanging constituents : these are probably not the largest pT contributions to the jet (as unseen from energy fractions) but if they are far from the jet's center, they would have an important weight in colourflow computation
* ![IMAGE](quiver-image-url/F1227430A16F9E934A515D027AE08BD9.jpg =1428x520)
  * looks like something is happening at dR > 3 --> related to the pseudo-rapidity maybe ?
* ![IMAGE](quiver-image-url/E15288369F70FFCEF8E98E2BB3C6BF96.jpg =1430x521)
* Moreover, large correlation between the number of constituents and the pulVector magnitude
* ![IMAGE](quiver-image-url/EE85DEC3B5D9A987CDAAA928E015FC6D.jpg =1358x487)
* ![IMAGE](quiver-image-url/F8AF5B39E1560A43009130654462963E.jpg =688x471)
* red is the leading jet, blue is subleading
* ![IMAGE](quiver-image-url/2AD7BFEED6C0C5576BDA71A07D75B4B6.jpg =1193x768)

2nd Hypothesis :
* Without necessarily stealing constituents to the other jet, the distribution of constituents within the jet may vary, with some non-intuitive dependence on dRbb --> previous hypothesis show that the subleading jet has less constituents, but is it due to the number of interacting daughters which is lower, or is there really some stealing ?
* Following plot shows at least that the magnitude of the pull angle is different according to dRbb, and is correlated with dTheta
![IMAGE](quiver-image-url/FB6B747B913692838DD0008A79D078AA.jpg =1202x774)

## A priori final answer :
* New implementation of the code

### Stealing number of constituents depency
![IMAGE](quiver-image-url/872162E03A6C87138A367025C14A47ED.jpg =1192x767)
![IMAGE](quiver-image-url/1898257FD6B58C928C6A71E50AAEA1F0.jpg =1196x770)

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
