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

