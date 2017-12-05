---
title: Asymetry in ColourFlow of the 3rd jet
date: '2017-08-31'
tags:
- asymetry
- colorflow
---
# Context
* We observed an asymetry in reco samples with tracks (multiple events samples)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

# Major update
* Actually, this is not a complete asymetry : the mean is 0
* Example with ZnunuB Sherpa 221 MaxHTPtV 140-280 GeV
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

# Truth Samples

## Single event
### Energy deposits and jets location
| Object         | DrawOption |
| -------------- | ---------- |
| TruthParticles | colz       |
| Jets           | "" (dots)  |
* Shows no asymetry
### Leading jet
![IMAGE](/images/q/IMAGE)
### SubLeading jet
![IMAGE](/images/q/IMAGE)
### 3rd jet
![IMAGE](/images/q/IMAGE)
Same picture but reverting the draw options : 3rd jet in colz
![IMAGE](/images/q/IMAGE)

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
![IMAGE](/images/q/IMAGE)

### Pixels interacting
* No asymetry observed
* Possible bias with respect to CxAODReader_VHbb : mBB region ?
![IMAGE](/images/q/IMAGE)

## Distribution of dR Jet - constituent
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

# Reco Samples

Dependency highly correlated to the rapidity of the 3rd jet
![IMAGE](/images/q/IMAGE)
These are most likely pile-up jets (from the etaJ3 distribution) which are not rejected beyond the pixels acceptance if abseta > 2.5.
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

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

![IMAGE](/images/q/IMAGE)

{% highlight javascript %}
Nominal->Draw("etaJ3-etaB1:TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31","nJ==3&&abs(etaJ3)>2.5","glbox")
{% endhighlight %}

![IMAGE](/images/q/IMAGE)

{% highlight javascript %}
 Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31","nJ==3&&etaJ3<-2.5","colz")
 new TCanvas
 Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31","nJ==3&&etaJ3>2.5","colz")
{% endhighlight %}

![IMAGE](/images/q/IMAGE)

![IMAGE](/images/q/IMAGE)

![IMAGE](/images/q/IMAGE)

{% highlight javascript %}
Nominal->Draw("TVector2::Phi_mpi_pi(phiJ3-phiB1):ColourFlowAngleJ31:etaJ3-etaB1","nJ==3&&etaJ3>3","glbox")
{% endhighlight %}

![IMAGE](/images/q/IMAGE)

# Conclusion
It was due to a small bug which did not protect computing 3rd jet colourflow variable against no tracks matched ... should check for the other nJ
![IMAGE](/images/q/IMAGE)

## Updated distributions
![2tag3jet_150ptv_SR_ColourFlowAngleJ12.png](/images/q/2tag3jet_150ptv_SR_ColourFlowAngleJ12.png)
![2tag3jet_150ptv_SR_ColourFlowAngleJ13.png](/images/q/2tag3jet_150ptv_SR_ColourFlowAngleJ13.png)
![2tag3jet_150ptv_SR_ColourFlowAngleJ21.png](/images/q/2tag3jet_150ptv_SR_ColourFlowAngleJ21.png)
![2tag3jet_150ptv_SR_ColourFlowAngleJ23.png](/images/q/2tag3jet_150ptv_SR_ColourFlowAngleJ23.png)
![2tag3jet_150ptv_SR_ColourFlowAngleJ31.png](/images/q/2tag3jet_150ptv_SR_ColourFlowAngleJ31.png)
![2tag3jet_150ptv_SR_ColourFlowAngleJ32.png](/images/q/2tag3jet_150ptv_SR_ColourFlowAngleJ32.png)

