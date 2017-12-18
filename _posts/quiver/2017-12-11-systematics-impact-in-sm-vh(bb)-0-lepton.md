---
title: Systematics impact in SM VH(bb) 0-lepton
date: '2017-12-11'
tags: []
---
# Purpose
* Reduce the impact of systematics in the cut-based analysis prioritarily
* Dominant systematics are b-Tagging and modelling ones
  * consist of a different weighting strategy to cover shape variations of relevant variables : pTV, mBB

Ranking of systematics in the SM VH(bb) 0-lepton only fit MVA (prefit and post-fit unconditional, p.179 of supporting note)
![IMAGE](/images/q/ECDDF009C81122E936C23BED91A73A2D.jpg)
## Zjets pTV
* reweight events as a function of TruthMET computed from leptons/neutrinos
  * https://gitlab.cern.ch/CxAODFramework/CxAODReader_VHbb/blob/master/Root/AnalysisReader_VHbb.cxx#L393
  * https://gitlab.cern.ch/CxAODFramework/CorrsAndSysts/blob/master/Root/CorrsAndSysts.cxx#L1444
* **Do these plots as a function of TruthMET or MET ?**
)
* Up variation, reweighting SF vs MET
![IMAGE](/images/q/DA1AE92762CBE86C0F3D53D2AC647B96.jpg)
* Down variation, reweighting SF vs MET
![IMAGE](/images/q/9282B86588A50CF28751CBFD48B629DC.jpg)
* Up/Down variations, reweighting SF vs MVA
![IMAGE](/images/q/7773CD3F4B21AC5DC4212E8A153005F4.jpg)
* Profiles
![IMAGE](/images/q/2EDED551C4F4D8D052D8578F76FDD212.jpg)
* MVA vs MET
![IMAGE](/images/q/6573E20A8A1AAA077A5E9DC1FFDE2A45.jpg)
## Zjets mBB shape
* reweight events as a function of the reco mBB
  * https://gitlab.cern.ch/CxAODFramework/CxAODReader_VHbb/blob/master/Root/AnalysisReader_VHbb0Lep.cxx#L607
  * https://gitlab.cern.ch/CxAODFramework/CorrsAndSysts/blob/master/Root/CorrsAndSysts.cxx#L1459
)
* Up/down variation, reweighting SF vs mBB
![IMAGE](/images/q/63EA67695E343272CA2DEA3A7035F429.jpg)
* Up/down variation, reweighting SF vs mBB
  * SF is close to one, so it has a small impact in the prefit ranking
  * this NP is largely pulled (almost 1 sigma up), so the impact of the down variation makes it highly ranked in the unconditionnal fit ?
![IMAGE](/images/q/18AE93AEDA29C4A631FA2D82167E7298.jpg)
* X-Profile
![IMAGE](/images/q/41E1F3C5CDD1DC11B4B056EC32B3E429.jpg)
* Y-Profile
![IMAGE](/images/q/29F19AAA2109D031A4F80DB8F3A21AB5.jpg)
* Variation with respect to nominal in 2jets
![IMAGE](/images/q/C350E53809079A984D6FB9AAA5267844.jpg)
{% highlight sh %}
TH1F *hNo = new TH1F("hNo", "Nominal", 20, 0, 500);
TH1F *hDo = new TH1F("hDo", "Down", 20, 0, 500);
TH1F *hUp = new TH1F("hUp", "Up", 20, 0, 500);

Nominal->Draw("mBB>>hNo","EventWeight*(nTags==2)*(nJ==2)*(mBB<500)");
Nominal->Draw("mBB>>hDo","EventWeight*(nTags==2)*(nJ==2)*(mBB<500)*ZMbb__1down");
Nominal->Draw("mBB>>hUp","EventWeight*(nTags==2)*(nJ==2)*(mBB<500)*ZMbb__1up");

hDo->SetLineColor(kRed);
hUp->SetLineColor(kGreen);

TLegend *leg = new TLegend(0.7,0.7,0.9,0.9);
leg->AddEntry(hNo, "Nominal", "l");
leg->AddEntry(hDo, "Down", "l");
leg->AddEntry(hUp, "Up", "l");

hNo->DrawNormalized();
hDo->DrawNormalized("same");
hUp->DrawNormalized("same");

leg->Draw("same");
{% endhighlight %}

![IMAGE](/images/q/48F94AB63FF897CEF87F22F4EF2BB5D3.jpg)
{% highlight sh %}
gStyle->SetOptStat(0);

TH1F *hNo = new TH1F("hNo", "Nominal", 20, 0, 500);
TH1F *hDo = new TH1F("hDo", "Down", 20, 0, 500);
TH1F *hUp = new TH1F("hUp", "Up", 20, 0, 500);

TH2F *wDo = new TH2F("wDo", "SF Down", 20, 0, 500, 50, 0.5, 1.5);
TH2F *wUp = new TH2F("wUp", "SF Up", 20, 0, 500, 50, 0.5, 1.5);

Nominal->Draw("mBB>>hNo","EventWeight*(nTags==2)*(nJ==2)*(mBB<500)");
Nominal->Draw("mBB>>hDo","EventWeight*(nTags==2)*(nJ==2)*(mBB<500)*ZMbb__1down");
Nominal->Draw("mBB>>hUp","EventWeight*(nTags==2)*(nJ==2)*(mBB<500)*ZMbb__1up");

Nominal->Draw("ZMbb__1down:mBB>>wDo","EventWeight*(nTags==2)*(nJ==2)*(mBB<500)");
Nominal->Draw("ZMbb__1up:mBB>>wUp","EventWeight*(nTags==2)*(nJ==2)*(mBB<500)");

hDo->Divide(hNo);
hUp->Divide(hNo);

hDo->Scale(19./hDo->Integral());
hUp->Scale(19./hUp->Integral());

wDo->ProfileX("wDox");
wUp->ProfileX("wUpx");

hDo->SetLineColor(kRed);
hUp->SetLineColor(kGreen);

wDox->SetLineColor(kOrange);
wUpx->SetLineColor(kCyan);

TLegend *leg = new TLegend(0.7,0.7,0.9,0.9);
// leg->AddEntry(hNo, "Nominal", "l");
leg->AddEntry(hDo, "Down norm variation", "l");
leg->AddEntry(hUp, "Up norm variation", "l");
leg->AddEntry(wDox, "Down SF profile", "l")
leg->AddEntry(wUpx, "Up SF profile", "l")

hDo->Draw();
hUp->Draw("same");
wDox->Draw("same");
wUpx->Draw("same");

leg->Draw("same");
{% endhighlight %}

## Single-top wt acceptance

* Acceptance NP is computed from the difference with respect to alternative generators (Nominal is PwPy6, alternatives are PwPy6 low/high radiation, Diagram Substraction instead of Diagram Removal, PoHe++ and Ma5He++) (page 37 of modelling note) with sum in quadrature
* Normalisation NP (constrained) has prior estimate based on muRmuF, alpha s and PDF uncertainties with sum in quadrature

--> Important table in p. 42

In WSMaker, what is the difference between (src/systematiclistsbuilder_vhbbrun2.cpp) :
--> https://gitlab.cern.ch/atlas-physics/higgs/hbb/WSMaker/blob/master/HowTo.md#how-to-control-systematics-

* normFact : unconstrained normalisation factor
* sampleNormSys : normalisation uncertainty delta for the background
* normSys : additional uncertainties on processes chosen within the constructor of the SysConfig argument. This option can be used in order to decorrelate process normalisations between different channels to an extent defined by

--> normSys is identical to sampleNormSys, just more convenient for decorrelating categories/channels, ...
)
