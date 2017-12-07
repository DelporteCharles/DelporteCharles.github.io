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

# Conclusion and notes
* Low TruthMET :
  * Before selection, contributes to ~70% of the overall ttbar non all-had
  * After selection, contributes to ~5% of the overall ttbar non all-had
* Medium TruthMET :
  * Before selection, contributes to ~25% of the overall ttbar non all-had
  * After selection, contributes to ~80% of the overall ttbar non all-had
* High TruthMET :
  * Before selection, contributes to ~5% of the overall ttbar non all-had
  * After selection, contributes to ~15% of the overall ttbar non all-had
)
