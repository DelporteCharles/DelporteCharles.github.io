---
title: UEPS systematic in the qqZH125 signal sample of SM VH(bb)
date: '2017-11-03'
tags: []
---
https://cds.cern.ch/record/2235887/files/ATL-COM-PHYS-2016-1747.pdf
)
50k events in
* mc15_13TeV.345056.PowhegPythia8EvtGen_NNPDF3_AZNLO_ZH125J_MINLO_vvbb_VpT.evgen.EVNT.e5706
* mc15_13TeV.345573.PowhegHerwig7EvtGen_NNPDF3_AZNLO_ZH125J_MINLO_vvbb_VpT.evgen.EVNT.e5971

Pythia8 in red
Herwig7 in blue
)
![IMAGE](/images/q/98EB549EFF476B5608830BB2B808D056.jpg)
{% highlight sh %}
TFile *_file0 = TFile::Open("PowhegPythia8EvtGen_345056/nominal.root")
TFile *_file1 = TFile::Open("PowhegHerwig7EvtGen_345573/central.root")
.ls
TH1F *py8=(TH1F*)_file0->Get("MC_VH2BB_2015_Official/Cuts3j")
 TH1F *he7=(TH1F*)_file1->Get("MC_VH2BB_2015_Official/Cuts3j")
py8->GetBinContent(0)
py8->GetBinContent(1)
he7->GetBinContent(1)
py8->Scale(he7->GetBinContent(1)/py8->GetBinContent(1))
py8->SetLineColor(kRed)
py8->Draw("text")
he7->Draw("same text")
{% endhighlight %}

# All events
* https://bigpanda.cern.ch/task/12764998/
* https://bigpanda.cern.ch/task/12769510/

Ordre des coupures :

0) All
1) 0-lepton
2) 2 or 3 jets
3) MET > 150 GeV
4) dPhiMETMPT < pi/2
5) mindPhiMETJets > 20 degrees
6) SumpT > 120 (150) GeV
7) pTB1 > 45 GeV
8) dPhiBB < 140 degrees
9) dPhiMETBB > 120 degrees
)
* Cutflows ratio py8/he7 in 2jets
![IMAGE](/images/q/EB03516D528D8B31F259DCC3ECBBF6FC.jpg)
* Cutflows ratio py8/he7 in 3jets
![IMAGE](/images/q/7ABC944E69F5EBB6AE768DB99FFC0FC2.jpg)
{% highlight sh %}
root -l user.cdelport.mc15_13TeV.345056.PowhegPythia8EvtGen_NNPDF3_AZNLO_ZH125J_MINLO_vvbb_VpT.evgen.EVNT.e5706.VH_PwPy8_v0_EXT0/Rivet.root user.cdelport.mc15_13TeV.345573.PowhegHerwig7EvtGen_NNPDF3_AZNLO_ZH125J_MINLO_vvbb_VpT.evgen.EVNT.e5971.VH_PwHe7_v0_EXT0/Rivet.root

py8 = (TH1F*)_file0->Get("MC_VH2BB_2015_Official/Cuts2j")
he7 = (TH1F*)_file1->Get("MC_VH2BB_2015_Official/Cuts2j")
py8->Scale(1./py8->GetBinContent(1))
he7->Scale(1./he7->GetBinContent(1))
py8->Divide(he7)
py8->Draw("text")
{% endhighlight %}

### METADATA
* small difference in sumOfWeights from inner cross section ? (should not, job was normalized )
  * ratio)
