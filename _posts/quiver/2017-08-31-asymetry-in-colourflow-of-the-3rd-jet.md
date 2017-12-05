---
title: Asymetry in ColourFlow of the 3rd jet
date: '2017-08-31'
tags:
- asymetry
- colorflow
---
# Context
* We observed an asymetry in reco samples with tracks (multiple events samples)
![IMAGE](/images/q/4D6B9A67271706B9C47AE52A70E87C4E.jpg)
# Major update
* Actually, this is not a complete asymetry : the mean is 0
* Example with ZnunuB Sherpa 221 MaxHTPtV 140-280 GeV
![IMAGE](/images/q/276C898B73454E8AEB731472EAA88B94.jpg)
# Truth Samples
)
## Single event
### Energy deposits and jets location
| Object         | DrawOption |
| -------------- | ---------- |
| TruthParticles | colz       |
| Jets           | "" (dots)  |
* Shows no asymetry
### Leading jet
![IMAGE](/images/q/6FE9307FF67512AAA494ED03B0413F64.jpg)
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
)
## PullAngle jet 3 distributions
)
### Calo interacting
* No asymetry observed
![IMAGE](/images/q/95AFF4E8581A956B3BC3079BBEF8F9AC.jpg)
### Pixels interacting
* No asymetry observed
* Possible bias with respect to CxAODReader_VHbb : mBB region ?
![IMAGE](/images/q/0E702622017C29D5A560DB013091050A.jpg)
## Distribution of dR Jet - constituent
![IMAGE](/images/q/9F2D9AC6104C6C61B12C73E3B0489B36.jpg)
# Reco Samples
)
Dependency highly correlated to the rapidity of the 3rd jet
![IMAGE](/images/q/B04459EBFC52DEA8684A90C0D376254F.jpg)
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

![IMAGE](/images/q/313D72C718D2C14D08939BAA4730459E.jpg)
{% highlight javascript %}
Nominal->Draw("etaJ3-etaB1:TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31","nJ==3&&abs(etaJ3)>2.5","glbox")
{% endhighlight %}

![IMAGE](/images/q/F5EF2F60144183D0A98C500868AF4C5F.jpg)
{% highlight javascript %}
 Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31","nJ==3&&etaJ3<-2.5","colz")
 new TCanvas
 Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31","nJ==3&&etaJ3>2.5","colz")
{% endhighlight %}

![IMAGE](/images/q/B56CA6CF36CAC810F0EA266C054ED43B.jpg)
![IMAGE](/images/q/A0E34FF9C15A646ED6B9760A6DF8B6C5.jpg)
![IMAGE](/images/q/AD455702B0C7505387B10823586ADFF5.jpg)
{% highlight javascript %}
Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31:etaJ3-etaB1","nJ==3&&etaJ3>3","glbox")
{% endhighlight %}

![IMAGE](/images/q/08B540F4385CCF251F8945C15C139191.jpg)
# Conclusion
It was due to a small bug which did not protect computing 3rd jet colourflow variable against no tracks matched ... should check for the other nJ
![IMAGE](/images/q/5C71485C248C7B7020520669F6550E24.jpg)
## Updated distributions
![2tag3jet_150ptv_SR_ColourFlowAngleJ12.png](/images/q/9CF2DD75D01400F5B21442A291D4A803.png)
