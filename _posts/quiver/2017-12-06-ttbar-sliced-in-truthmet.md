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
    | Category | Slice |
    | -------- | ----- |
    | Low      | TruthMET < 100 GeV |
    | Medium   | 100 GeV < TruthMET < 200 GeV |
    | High     | TruthMET > 200 GeV |

### 2 jets 2 tags (MVA selection)

| Slice  | NEvents | Yield  |
| ------ | ------- | ------ |
| Low    | 87      | 26.59  |
| Medium | 1280    | 386.61 |
| High   | 190     | 62.90  |
| All    | 1557    | 476.1  |

### 3 jets 2 tags (MVA selection)

| Slice  | NEvents | Yield   |
| ------ | ------- | ------- |
| Low    | 550     | 165.79  |
| Medium | 8909    | 2643.49 |
| High   | 1967    | 591.26  |
| All    | 11426   | 3400.54 |
)
## Slices in mBB
)
### 2 jets
![IMAGE](/images/q/DF0A9243CE1696F5ED9452BC1B00696A.jpg)
### 3 jets
![IMAGE](/images/q/32BEA2849EF084B664C887306AAF03AB.jpg)
## Slices in mva28
)
### 2 jets
![IMAGE](/images/q/853D300053723F451049F21F5C8D4474.jpg)
### 3 jets
![IMAGE](/images/q/C919BC0F60CEAF961A6B2BE6C196C9A4.jpg)
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

