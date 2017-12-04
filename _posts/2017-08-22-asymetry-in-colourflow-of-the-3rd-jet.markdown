---
layout: post
title: Asymetry in ColourFlow of the 3rd jet
tags: 
    - asymetry
    - colorflow
---

# Context
* We observed an asymetry in reco samples with tracks (multiple events samples)
![IMAGE](quiver-image-url/4D6B9A67271706B9C47AE52A70E87C4E.jpg =382x260)
![IMAGE](quiver-image-url/DB317717BC6A7C941688906D489E4C1A.jpg =382x259)

# Major update
* Actually, this is not a complete asymetry : the mean is 0
* Example with ZnunuB Sherpa 221 MaxHTPtV 140-280 GeV
![IMAGE](quiver-image-url/276C898B73454E8AEB731472EAA88B94.jpg =647x449)
![IMAGE](quiver-image-url/B1C2043DA1B834E3580020AD44C60DD8.jpg =664x451)

# Truth Samples

## Single event
### Energy deposits and jets location
| Object         | DrawOption |
| -------------- | ---------- |
| TruthParticles | colz       |
| Jets           | "" (dots)  |
* Shows no asymetry
### Leading jet
![IMAGE](quiver-image-url/6FE9307FF67512AAA494ED03B0413F64.jpg =1341x820)
### SubLeading jet
![IMAGE](quiver-image-url/2E97108D4D911733B206D07CEE0B5C3D.jpg =1343x827)
### 3rd jet
![IMAGE](quiver-image-url/FD84A25A0B69441A27D5DE1CDB874AE0.jpg =1338x829)
Same picture but reverting the draw options : 3rd jet in colz
![IMAGE](quiver-image-url/A18F89EE1533C6BD4436CDEDA512525D.jpg =1402x830)

{% highlight javascript %}
root -l /sps/atlas/d/delporte/COLORFLOW/framework/submitDir_ppzhvvbb/hist-DAOD.root
energyDeposits_4->Draw("colz")
tree->Draw("Jet3_4->Phi():Jet3_4->Rapidity()","passLoose_4","same")
new TCanvas
energyDeposits_4->Draw("colz")
tree->Draw("bJet1_4->Phi():bJet1_4->Rapidity()","passLoose_4","same")
new TCanvas
tree->Draw("bJet2_4->Phi():bJet2_4->Rapidity()","passLoose_4","same")
energyDeposits_4->Draw("colz")
tree->Draw("bJet2_4->Phi():bJet2_4->Rapidity()","passLoose_4","same")
new TCanvas
tree->Draw("Jet3_4->Phi():Jet3_4->Rapidity()","passLoose_4","colz")
energyDeposits_4->Draw("same")
{% endhighlight %}

## Multiple events
* Looking in Zbb which presented the effect and has a large statistics
* Looking both loose and tight selections, but effect initially observed in tight selection (mBB cut to be removed ?)

## PullAngle jet 3 distributions

### Calo interacting
* No asymetry observed
![IMAGE](quiver-image-url/95AFF4E8581A956B3BC3079BBEF8F9AC.jpg =1193x767)

### Pixels interacting
* No asymetry observed
* Possible bias with respect to CxAODReader_VHbb : mBB region ?
![IMAGE](quiver-image-url/0E702622017C29D5A560DB013091050A.jpg =1192x769)

## Distribution of dR Jet - constituent
![IMAGE](quiver-image-url/9F2D9AC6104C6C61B12C73E3B0489B36.jpg =1331x780)
![IMAGE](quiver-image-url/6D170B6C7F70DB9FFECEACD04B32F1DD.jpg =1350x784)

# Reco Samples

Dependency highly correlated to the rapidity of the 3rd jet
![IMAGE](quiver-image-url/B04459EBFC52DEA8684A90C0D376254F.jpg =1193x767)
These are most likely pile-up jets (from the etaJ3 distribution) which are not rejected beyond the pixels acceptance if abseta > 2.5.
![IMAGE](quiver-image-url/3DED881E991E641F0018F07F657827D0.jpg =673x463)
![IMAGE](quiver-image-url/B453E3E3EBE9557B820EAB87E8FE63DD.jpg =1195x770)

{% highlight javascript %}
Nominal->Draw("ColourFlowAngleJ31:MindPhiMETJet","nJ==3&&abs(etaJ3)>2.5","colz")
{% endhighlight %}

{% highlight javascript %}
Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31","nJ==3&&abs(etaJ3)>2.5","colz")
new TCanvas
Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):etaJ3-etaB1","nJ==3&&abs(etaJ3)>2.5","colz")
new TCanvas
Nominal->Draw("ColourFlowAngleJ31","nJ==3&&abs(etaJ3)>2.5&&TVector2::Phi_mpi_pi(phiJ3-phiB1)<0.4&&etaJ3-etaB1<0.4")
new TCanvas
Nominal->Draw("ColourFlowAngleJ31","nJ==3&&abs(etaJ3)>2.5&&TVector2::Phi_mpi_pi(phiJ3-phiB1)<0.4&&etaB1-etaJ3<0.4")
{% endhighlight %}

![IMAGE](quiver-image-url/313D72C718D2C14D08939BAA4730459E.jpg =1360x499)

{% highlight javascript %}
Nominal->Draw("etaJ3-etaB1:TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31","nJ==3&&abs(etaJ3)>2.5","glbox")
{% endhighlight %}

![IMAGE](quiver-image-url/F5EF2F60144183D0A98C500868AF4C5F.jpg =1353x397)

{% highlight javascript %}
 Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31","nJ==3&&etaJ3<-2.5","colz")
 new TCanvas
 Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31","nJ==3&&etaJ3>2.5","colz")
{% endhighlight %}

![IMAGE](quiver-image-url/B56CA6CF36CAC810F0EA266C054ED43B.jpg =700x517)

![IMAGE](quiver-image-url/A0E34FF9C15A646ED6B9760A6DF8B6C5.jpg =1388x800)

![IMAGE](quiver-image-url/AD455702B0C7505387B10823586ADFF5.jpg =1250x773)

{% highlight javascript %}
Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31:etaJ3-etaB1","nJ==3&&etaJ3>3","glbox")
{% endhighlight %}

![IMAGE](quiver-image-url/08B540F4385CCF251F8945C15C139191.jpg =1368x799)

# Conclusion
It was due to a small bug which did not protect computing 3rd jet colourflow variable against no tracks matched ... should check for the other nJ
![IMAGE](quiver-image-url/5C71485C248C7B7020520669F6550E24.jpg =1193x769)

## Updated distributions
![2tag3jet_150ptv_SR_ColourFlowAngleJ12.png](quiver-image-url/9CF2DD75D01400F5B21442A291D4A803.png =696x472)
![2tag3jet_150ptv_SR_ColourFlowAngleJ13.png](quiver-image-url/E9C5355523EE623D7A0B6861ED9FB2A9.png =696x472)
![2tag3jet_150ptv_SR_ColourFlowAngleJ21.png](quiver-image-url/937A3D238363CAC60A2823383D973838.png =696x472)
![2tag3jet_150ptv_SR_ColourFlowAngleJ23.png](quiver-image-url/1C7A5B647B2F86B193B059EA05FF913D.png =696x472)
![2tag3jet_150ptv_SR_ColourFlowAngleJ31.png](quiver-image-url/E4A2A209C362D08D4E2A7B79D6E3181F.png =696x472)
![2tag3jet_150ptv_SR_ColourFlowAngleJ32.png](quiver-image-url/10CB3FE5A1ADDEC045595A56A8FC882C.png =696x472)
