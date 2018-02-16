---
title: ttbar sliced in TruthMET
date: '2017-12-06'
tags:
- filter
- truth
- ttbar
- VHbb
---
# Purpose
SUSY will have filtered ttbar samples with TruthMET> 200 GeV
--> Is it worth to propose a slicing for TruthMET < 200 ?
)
## Raw numbers of events and yields per slice
* a very basic slicing strategy might be :
)
{% highlight sh %}
| Category | Slice                        |
|----------|------------------------------|
| Low      | TruthMET < 100 GeV           |
| Medium   | 100 GeV < TruthMET < 200 GeV |
| High     | TruthMET > 200 GeV           |
{% endhighlight %}

### 2 jets 2 tags (MVA selection)
)
{% highlight sh %}
| Slice  | NEvents | Yield  |
| ------ | ------- | ------ |
| Low    | 87      | 26.59  |
| Medium | 1280    | 386.61 |
| High   | 190     | 62.90  |
| All    | 1557    | 476.1  |
{% endhighlight %}

### Fractions : 2 jets 2 tags (MVA selection)
)
{% highlight sh %}
| Slice  | NEvents | Yield  |
|--------|---------|--------|
| Low    | 5.6%    | 5.6%   |
| Medium | 82.2%   | 81.2%  |
| High   | 12.2%   | 13.2%  |
{% endhighlight %}

### 3 jets 2 tags (MVA selection)
)
{% highlight sh %}
| Slice  | NEvents | Yield   |
|--------|---------|---------|
| Low    | 550     | 165.79  |
| Medium | 8909    | 2643.49 |
| High   | 1967    | 591.26  |
| All    | 11426   | 3400.54 |
{% endhighlight %}

{% highlight sh %}
### Fractions : 3 jets 2 tags (MVA selection)

| Slice  | NEvents | Yield   |
| ------ | ------- | ------- |
| Low    | 4.8%    | 4.8%    |
| Medium | 77.9%   | 77.7%   |
| High   | 17.2%   | 17.4%   |
{% endhighlight %}

## Slices in mBB
* MVA selection, applying SM VHbb Reader on EPS CxAODs
)
### 2 tags 2 jets
![IMAGE](/images/q/DF0A9243CE1696F5ED9452BC1B00696A.jpg)
### 2 tags 3 jets
![IMAGE](/images/q/32BEA2849EF084B664C887306AAF03AB.jpg)
## Slices in mva28
)
### 2 tags 2 jets
![IMAGE](/images/q/853D300053723F451049F21F5C8D4474.jpg)
### 2 tags 3 jets
![IMAGE](/images/q/C919BC0F60CEAF961A6B2BE6C196C9A4.jpg)
## Slices in TruthMET (2 tags 2-3 jets)
![IMAGE](/images/q/D8AB43B51A53F612955085F8D8BE6329.jpg)
## Slices in TruthMET all n-jets all n-tags (all other cuts applied)
![IMAGE](/images/q/C07336A28C75E0FE9112CE915D2AFB1E.jpg)
{% highlight sh %}
THStack *hs = new THStack("hs","mva in TruthMET slices")

TH1F *h100m = new TH1F("h100m","h100m",20,-1.,1.)
TH1F *h100p200m = new TH1F("h100p200m","h100p200m",20,-1.,1.)
TH1F *h200p = new TH1F("h200p","h200p",20,-1.,1.)

Nominal->Draw("mva28>>h100p200m","EventWeight*(nJ==2)*(nTags==2)*(TruthMET>100)*(TruthMET<=200)")
Nominal->Draw("mva28>>h100m","EventWeight*(nJ==2)*(nTags==2)*(TruthMET<=100)")
Nominal->Draw("mva28>>h200p","EventWeight*(nJ==2)*(nTags==2)*(TruthMET>200)")

h200p->SetFillColor(kAzure+10)
h100p200m->SetFillColor(kPink-9)
h100m->SetFillColor(kSpring+10)

hs->Add(h100m)
hs->Add(h100p200m)
hs->Add(h200p)

TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
leg->AddEntry(h100m,"TruthMET<100GeV","f")
leg->AddEntry(h100p200m,"100<TruthMET<200GeV","f")
leg->AddEntry(h200p,"TruthMET>200GeV","f")

hs->Draw("hist")
leg->Draw("same")
{% endhighlight %}

# TruthMET without selection at DAOD level
* looking a few random files of sample :
  * **mc15_13TeV.410501.PowhegPythia8EvtGen_A14_ttbar_hdamp258p75_nonallhad.merge.DAOD_HIGG5D1.e5458_s2726_r7772_r7676_p2949**
![IMAGE](/images/q/10F556ED05E8F0A2D01E6A50E746665A.jpg)
### all n-jets all n-tags (no selection, HIGG5D1 DAOD)
)
{% highlight sh %}
| Slice  | NEvents  | Yield            |
| ------ | -------- | ---------------- |
| Low    | 9711814  | 7041811302.00    |
| Medium | 3862066  | 2789444888.00    |
| High   | 417988   | 296028135.00     |
| All    | 13991868 | 10127284325      |
{% endhighlight %}

### Fractions : all n-jets all n-tags (no selection, HIGG5D1 DAOD)
)
{% highlight sh %}
| Slice  | NEvents  | Yield  |
| ------ | -------- | ------ |
| Low    | 69.4     | 69.5   |
| Medium | 27.6     | 27.5   |
| High   | 2.9      | 2.9    |
| All    | 100%     | 100%   |
{% endhighlight %}

{% highlight sh %}
TChain *CollectionTree = new TChain("CollectionTree")
CollectionTree->Add("DAOD_HIGG5D1.1*")

THStack *hs = new THStack("hs","mva in TruthMET slices")

TH1F *h100m = new TH1F("h100m","h100m",100,0.,500.)
TH1F *h100p200m = new TH1F("h100p200m","h100p200m",100,0.,500.)
TH1F *h200p = new TH1F("h200p","h200p",100,0.,500.)

CollectionTree->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])/1.e3>>h100p200m","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])/1.e3>100)*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])/1.e3<=200)")
CollectionTree->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])/1.e3>>h100m","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])/1.e3<=100)")
CollectionTree->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])/1.e3>>h200p","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])/1.e3>200)")

h200p->SetFillColor(kAzure+10)
h100p200m->SetFillColor(kPink-9)
h100m->SetFillColor(kSpring+10)

hs->Add(h100m)
hs->Add(h100p200m)
hs->Add(h200p)

TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
leg->AddEntry(h100m,"TruthMET<100GeV","f")
leg->AddEntry(h100p200m,"100<TruthMET<200GeV","f")
leg->AddEntry(h200p,"TruthMET>200GeV","f")

hs->Draw("hist")
leg->Draw("same")
{% endhighlight %}

# Fix with DAODs without skimming on MET trigger and jets

![IMAGE](/images/q/F5D84DC6C1A1663C729676F917848187.jpg)
### all n-jets all n-tags (no selection, HIGG5D1 DAOD)
)
| Slice  | NEvents  | Yield            |
| ------ | -------- | ---------------- |
| Low    | 6754277 | 4900736496 |
| Medium | 1405841  | 1017577918 |
| High   | 139746 | 99787690 |
| All    | 8299864 | 6018102104 |
)
### Fractions : all n-jets all n-tags (no selection, HIGG5D1 DAOD)
)
| Slice  | NEvents  | Yield  |
| ------ | -------- | ------ |
| Low    | 81.3     | 81.4   |
| Medium | 17.0     | 16.9   |
| High   | 1.7      | 1.7    |
)
{% highlight sh %}
TChain *c = new TChain("CollectionTree")
c->Add("DAOD_HIGG5D1.v0_HIGG5D1_AOD*")

THStack *hs = new THStack("hs","TruthMET slices")

TH1F *h100m = new TH1F("h100m","h100m",50,0.,500.e3)
TH1F *h100p200m = new TH1F("h100p200m","h100p200m",50,0.,500.e3)
TH1F *h200p = new TH1F("h200p","h200p",50,0.,500.e3)

c->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>>h100m","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])<100.e3)")
c->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>>h100p200m","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])<200.e3)*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>100.e3)")
c->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>>h200p","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>200.e3)")

h200p->SetFillColor(kAzure+10)
h100p200m->SetFillColor(kPink-9)
h100m->SetFillColor(kSpring+10)

hs->Add(h100m)
hs->Add(h100p200m)
hs->Add(h200p)

TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
leg->AddEntry(h100m,"TruthMET<100GeV","f")
leg->AddEntry(h100p200m,"100<TruthMET<200GeV","f")
leg->AddEntry(h200p,"TruthMET>200GeV","f")

hs->Draw("hist")
leg->Draw("same")
{% endhighlight %}

# NTruthWZJets in DAODs
* requirements should be :
  * have at least one jet with reasonnable pT
https://gitlab.cern.ch/atlas/athena/blob/21.2/PhysicsAnalysis/DerivationFramework/DerivationFrameworkHiggs/share/HIGG5D1.py
--> count TruthWZJets with JetConstitScaleMomentum_pt > 20 GeV **--> is that the correct branch ??**
)
### NTruthWZJets20
![IMAGE](/images/q/5A0BB2221F1097793785C1A225BA0A06.jpg)
### NTruthWZJets30
![IMAGE](/images/q/FFE9DFE857026230F6F265AF635999D5.jpg)
# NTruthWZJets after full selection
* MVA selection
)
### NTruthWZJets20
![IMAGE](/images/q/3C5199FC4CD5910D102F62D792378059.jpg)
### NTruthWZJets30
![IMAGE](/images/q/531999D51FAF2AF20B7A4F369E2208B4.jpg)
# Conclusion and notes
* Low TruthMET :
  * Before selection, contributes to ~~~70%~~ 81% of the overall ttbar non all-had
  * After selection, contributes to ~5% of the overall ttbar non all-had
* Medium TruthMET :
  * Before selection, contributes to ~~~25%~~ 17% of the overall ttbar non all-had
  * After selection, contributes to ~80% of the overall ttbar non all-had
* High TruthMET :
  * Before selection, contributes to ~~~5%~~ 1.7% of the overall ttbar non all-had
  * After selection, contributes to ~15% of the overall ttbar non all-had
* nTruthWZJets20 > 6 : ~30% of the DAOD stat. is lost
* nTruthWZJets30 > 5 : ~30% of the DAOD stat. is lost
)
## Additional points
)
* would it be efficiento to filter on nTruthWZJets with tighter cut, e.g. nTruthWZJets30 >= 4 ?
  * what BDT score to events with nTruthWZJets30 >= 4 ?
  * quite tricky ... same shape
![IMAGE](/images/q/2EE15B1BF9284C28377D731A10D67990.jpg)
* what BDT score to events with nTruthJets20 >= 5 ?
![IMAGE](/images/q/E0F83786CF9C65F300432F12E9EF3E21.jpg)
{% highlight sh %}
TH1F *h5p = new TH1F("h5p","MVA",20, -1., 1.)
TH1F *h4m = new TH1F("h4m","MVA",20, -1., 1.)
Nominal->Draw("mva28>>h5p","EventWeight*(nTags==2)*(nJ<4)*(NTruthWZJets20>=5)","norm")
Nominal->Draw("mva28>>h4m","EventWeight*(nTags==2)*(nJ<4)*(NTruthWZJets20<5)","norm")
h5p->SetLineColor(kRed)
h5p->DrawNormalized()
h4m->DrawNormalized("same")
TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
leg->AddEntry(h5p, "5 and more TruthWZJets 20", "l")
leg->AddEntry(h4m, "4 and less TruthWZJets 20", "l")
leg->Draw("same")
{% endhighlight %}

# TruthMET with 50 GeV slices

![IMAGE](/images/q/A49A26109F8E8D22BE1FBC0E0C315D0A.jpg)
## unskimmed DAOD
)
| Slice     | NEvents  | Yield      |
| --------- | -------- | ---------- |
| h100m     | 6754277  | 4989593344 |
| h100p150m | 1108701  | 803078592  |
| h150p200m | 297140   | 213612512  |
| h200p250m | 88798    | 63896276   |
| h250p300m | 26560    | 19142764   |
| h300p     | 24388    | 16748701   |
| total     | 8299864  | 6106072189 |
)
| Slice     | NEvents  | Yield      |
| --------- | -------- | ---------- |
| h100m     | 0.813782 | 0.817153   |
| h100p150m | 0.133581 | 0.131521   |
| h150p200m | 0.035801 | 0.034984   |
| h200p250m | 0.010699 | 0.010464   |
| h250p300m | 0.003200 | 0.003135   |
| h300p     | 0.002938 | 0.002743   |
)
{% highlight sh %}
TChain *c = new TChain("CollectionTree")
c->Add("DAOD_HIGG5D1.v0_HIGG5D1_AOD*")

THStack *hs = new THStack("hs","TruthMET slices")

TH1F *h100m = new TH1F("h100m","h100m",50,0.,500.e3)
TH1F *h100p150m = new TH1F("h100p150m","h100p150m",50,0.,500.e3)
TH1F *h150p200m = new TH1F("h150p200m","h150p200m",50,0.,500.e3)
TH1F *h200p250m = new TH1F("h200p250m","h200p250m",50,0.,500.e3)
TH1F *h250p300m = new TH1F("h250p300m","h250p300m",50,0.,500.e3)
TH1F *h300p = new TH1F("h300p","h300p",50,0.,500.e3)

c->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>>h100m","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])<100.e3)")
c->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>>h100p150m","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])<150.e3)*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>100.e3)")
c->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>>h150p200m","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])<200.e3)*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>150.e3)")
c->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>>h200p250m","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])<250.e3)*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>200.e3)")
c->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>>h250p300m","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])<300.e3)*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>250.e3)")
c->Draw("sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>>h300p","EventInfoAuxDyn.mcEventWeights*(sqrt(MET_TruthAuxDyn.mpx[0]*MET_TruthAuxDyn.mpx[0]+MET_TruthAuxDyn.mpy[0]*MET_TruthAuxDyn.mpy[0])>300.e3)")

h100m->SetFillColor(kAzure - 2)
h100p150m->SetFillColor(kViolet)
h150p200m->SetFillColor(kPink)
h200p250m->SetFillColor(kOrange - 3)
h250p300m->SetFillColor(kSpring + 10)
h300p->SetFillColor(kTeal - 1)

hs->Add(h100m)
hs->Add(h100p150m)
hs->Add(h150p200m)
hs->Add(h200p250m)
hs->Add(h250p300m)
hs->Add(h300p)


TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
leg->AddEntry(h100m,"TruthMET<100GeV","f")
leg->AddEntry(h100p150m,"100<TruthMET<150GeV","f")
leg->AddEntry(h150p200m,"150<TruthMET<200GeV","f")
leg->AddEntry(h200p250m,"200<TruthMET<250GeV","f")
leg->AddEntry(h250p300m,"250<TruthMET<300GeV","f")
leg->AddEntry(h300p,"TruthMET>300GeV","f")

hs->Draw("hist")
leg->Draw("same")
{% endhighlight %}

## after selection
)
### 2 tags 2 jets MVA selection
)
| Slice     | NEvents| Yield       |
| --------- | ----- | ------------ |
| h100m     | 87  | 26.591883  |
| h100p150m | 647 | 202.491196 |
| h150p200m | 633 | 184.121017 |
| h200p250m | 139 | 45.553856  |
| h250p300m | 35  | 11.718002  |
| h300p     | 16  | 4.823153   |
| total     | 1557 | 475.299107 |
)
| Slice     | NEvents| Yield       |
| --------- | ----- | ------------ |
| h100m     | 0.055877  | 0.055948  |
| h100p150m | 0.415543 | 0.426029 |
| h150p200m | 0.406551 | 0.387379 |
| h200p250m | 0.089274 | 0.095843  |
| h250p300m | 0.022479  | 0.024654  |
| h300p     | 0.010276  | 0.010148   |
)
### 2 tags 3 jets MVA
| Slice     | NEvents| Yield       |
| --------- | ----- | ------------ |
| h100m     | 550   | 165.786694  |
| h100p150m | 3925  | 1163.850708 |
| h150p200m | 4984  | 1479.638184 |
| h200p250m | 1446  | 428.751251  |
| h250p300m | 358   | 109.889801  |
| h300p     | 163   | 50.135752   |
| total     | 11426 | 3398.052390 |
)
| Slice     | NEvents| Yield       |
| --------- | ----- | ------------ |
| h100m     | 0.048136   | 0.048789  |
| h100p150m | 0.343515  | 0.342505 |
| h150p200m | 0.436198  | 0.435437 |
| h200p250m | 0.126553  | 0.126176  |
| h250p300m | 0.031332   |0.032339  |
| h300p     | 0.014266   | 0.014754   |

)
{% highlight sh %}
TTree *c = (TTree*)Nominal

THStack *hs = new THStack("hs","TruthMET slices")

TH1F *h100m = new TH1F("h100m","h100m",50,0.,500)
TH1F *h100p150m = new TH1F("h100p150m","h100p150m",50,0.,500)
TH1F *h150p200m = new TH1F("h150p200m","h150p200m",50,0.,500)
TH1F *h200p250m = new TH1F("h200p250m","h200p250m",50,0.,500)
TH1F *h250p300m = new TH1F("h250p300m","h250p300m",50,0.,500)
TH1F *h300p = new TH1F("h300p","h300p",50,0.,500)

c->Draw("TruthMET>>h100m",    "EventWeight*(nTags==2)*(nJ<4)*(TruthMET<100)")
c->Draw("TruthMET>>h100p150m","EventWeight*(nTags==2)*(nJ<4)*(TruthMET<150)*(TruthMET>100)")
c->Draw("TruthMET>>h150p200m","EventWeight*(nTags==2)*(nJ<4)*(TruthMET<200)*(TruthMET>150)")
c->Draw("TruthMET>>h200p250m","EventWeight*(nTags==2)*(nJ<4)*(TruthMET<250)*(TruthMET>200)")
c->Draw("TruthMET>>h250p300m","EventWeight*(nTags==2)*(nJ<4)*(TruthMET<300)*(TruthMET>250)")
c->Draw("TruthMET>>h300p",    "EventWeight*(nTags==2)*(nJ<4)*(TruthMET>300)")

h100m->SetFillColor(kAzure - 2)
h100p150m->SetFillColor(kViolet)
h150p200m->SetFillColor(kPink)
h200p250m->SetFillColor(kOrange - 3)
h250p300m->SetFillColor(kSpring + 10)
h300p->SetFillColor(kTeal - 1)

hs->Add(h100m)
hs->Add(h100p150m)
hs->Add(h150p200m)
hs->Add(h200p250m)
hs->Add(h250p300m)
hs->Add(h300p)


TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
leg->AddEntry(h100m,"TruthMET<100GeV","f")
leg->AddEntry(h100p150m,"100<TruthMET<150GeV","f")
leg->AddEntry(h150p200m,"150<TruthMET<200GeV","f")
leg->AddEntry(h200p250m,"200<TruthMET<250GeV","f")
leg->AddEntry(h250p300m,"250<TruthMET<300GeV","f")
leg->AddEntry(h300p,"TruthMET>300GeV","f")

hs->Draw("hist")
leg->Draw("same")
{% endhighlight %}

# Optimisation des fractions de stat entre 100 GeV et 200 GeV de TruthMET

* si on fait deux slices de TruthMET entre 100 GeV et 200 GeV, quelles fractions d'evenements donner a chacune pour servir au mieux VHbb 0-lep ?
)
# Procedure 

* Scan de fractions de stat a repartir entre 100 GeV et 200 GeV
)
{% highlight sh %}
  MCStatSlices.emplace(0,    50*million);
  MCStatSlices.emplace(100,  50*frac*million);
  MCStatSlices.emplace(150,  50*(1-frac)*million);
  MCStatSlices.emplace(200,  10*million);
  MCStatSlices.emplace(300,  3*million);
  MCStatSlices.emplace(400,  2*million);
  MCStatSlices.emplace(1000, 1*million);
  MCStatSlices.emplace(10000, 0);
{% endhighlight %}

## 2 jets

![IMAGE](/images/q/545BCC1E766BD417F428F3B92240DF4F.jpg)
![IMAGE](/images/q/668BCC981FABB3A79A29E75AF0467297.jpg)
## 3 jets

![IMAGE](/images/q/6DD6F1706F1EEA0223C556380C618B67.jpg)
![IMAGE](/images/q/5068BB760B6643638BDB2A01EC298ADE.jpg)
# With Marumi's significance

* Z)
## 2 jets

* 65% of stat in 100-150 GeV is the best value
* Gain)
![IMAGE](/images/q/99CFA8CE8ED23A07E9A6FD459BA20624.jpg)
## 3 jets

* 72% of stat in 100-150 GeV is the best value
* Gain= 1.50994/1.50965)
![IMAGE](/images/q/51D0D150A45C6780BD5FB97BD749B8E6.jpg)
# Interet du slice 100-200 GeV demande par Valerio

* pas de slice (ni 100-200 ni SUSY)
  * 2j : 2.2765
  * 3j : 1.39995
* pas de slice 100-200 + Slices SUSY
  * 2j : 2.31572
  * 3j : 1.43197
  * Gain)
