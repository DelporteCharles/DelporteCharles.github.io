---
title: Optimisation of the SM VHbb cut-based analysis
date: '2017-09-28'
tags: []
---
# Purpose
Optimise the cut based analysis, given that it is more robust than the MVA analysis and gives comparable performances

* dRRbb cut optimised in 1-lepton : https://indico.cern.ch/event/666694/contributions/2732739/attachments/1530946/2396135/VHbb_1lepton_20170927.pdf
* * MET < 250 : dRbb < ~~1.4~~ 1.6 instead of 1.8 if MET < 200
* * MET > 250 : dRbb < 1.2 instead of 1.2 if MET > 200

## Result
* Re-using the cuts optimised in the 1-lepton channel :
* Direct tagging for all

| Region             | Significance with 200 GeV | Significance with 250 GeV |
| ------------------ | ------------------------- | ------------------------- |
| 2j 150-200/250 GeV | 1.18923                   | 1.6336                    |
| 2j > 200/250 GeV   | 1.89115                   | 1.53613                   |
| 3j 150-200/250 GeV | 0.710155                  | 0.97543                   |
| 3j > 200/250 GeV   | 1.11866                   | 0.938928                  |
| Combination        | 2.59739 +/- 0.0555672     | 2.61943 +/- 0.0609429     |

## Proper optimisation
* Re-optimise dRBB cut for both regions 150-200, 200ptV and 150-250,250pTV
* Using truthtagging TTree (already available + more stat)

| Region             | Significance with 200 GeV | Significance with 250 GeV |
| ------------------ | ------------------------- | ------------------------- |
| 2j 150-200/250 GeV | 1.210941                  | 1.590978                  |
| 2j > 200/250 GeV   | 1.775484                  | 1.417695                  |
| 3j 150-200/250 GeV | 0.731590                  | 0.999954                  |
| 3j > 200/250 GeV   | 1.121310                  | 0.904395                  |
| Combination        | 2.532051                  | 2.521688                  |
[significance.pdf](quiver-file-url/0350AA4549BC17C02397BCEFBD191854.pdf)

* Same numbers in direct tagging

| Region             | Significance with 200 GeV | Significance with 250 GeV |
| ------------------ | ------------------------- | ------------------------- |
| 2j 150-200/250 GeV | 1.257920                  | 1.675475                  |
| 2j > 200/250 GeV   | 1.927718                  | 1.538189                  |
| 3j 150-200/250 GeV | 0.722211                  | 0.986955                  |
| 3j > 200/250 GeV   | 1.143036                  | 0.955580                  |
| Combination        | 2.669565                  | 2.657152                  |

| Region             | Optimal dRBB cut with 200 GeV | Optimal dRBB cut with 250 GeV |
| ------------------ | ----------------------------- | ----------------------------- |
| 2j 150-200/250 GeV | 1.45                          | 1.45                          |
| 2j > 200/250 GeV   | 1.15                          | 1.15                          |
| 3j 150-200/250 GeV | 1.6                           | 1.4                           |
| 3j > 200/250 GeV   | 1.3                           | 1.1                           |

[significance_directtag.pdf](quiver-file-url/A50D795F97ED8854307AF5301672B9E0.pdf)

* Same numbers with trafoD(10, 5, 0.05) applied in the significance evaluation

[significance_directtag_withtrafo.pdf](quiver-file-url/1FF0EE138E71C049EA2583A8F480FBEE.pdf)

| Region             | Significance with 200 GeV | Significance with 250 GeV |
| ------------------ | ------------------------- | ------------------------- |
| 2j 150-200/250 GeV | 1.226908                  | 1.670482                  |
| 2j > 200/250 GeV   | 1.921378                  | 1.538085                  |
| 3j 150-200/250 GeV | 0.720429                  | 0.966635                  |
| 3j > 200/250 GeV   | 1.135830                  | 0.950000                  |
| Combination        | 2.646908                  | 2.644447                  |

| Region             | Optimal dRBB cut with 200 GeV | Optimal dRBB cut with 250 GeV |
| ------------------ | ----------------------------- | ----------------------------- |
| 2j 150-200/250 GeV | 1.55                      | 1.45                      |
| 2j > 200/250 GeV   | 1.15                      | 1.15                      |
| 3j 150-200/250 GeV | 1.65                      | 1.60                      |
| 3j > 200/250 GeV   | 1.30                      | 1.05                      |

* Now, split the MET phase space into 3 regions 150-200-250-2000

[significance_directtag_3METRegions.pdf](quiver-file-url/F7D63D44BFB3661F4786820849822EEC.pdf)

| Region             | Significance | Optimal dRBB cut |
| ------------------ | ------------ | ---------------- |
| 2j 150-200 GeV     | 1.226908     | 1.55             |
| 2j 200-250 GeV     | 1.176616     | 1.30             |
| 2j >250 GeV        | 1.538085     | 1.15             |
| 3j 150-200 GeV     | 0.720429     | 1.65             |
| 3j 200-250 GeV     | 0.711136     | 1.35             |
| 3j >250 GeV        | 0.950000     | 1.05             |
| Combination        | 2.680050     |                  |

* Split the MET in the same regions as Yanhui's : 150-250-300-2000

[significance_directtag_3METRegions_150_250_300_2000.pdf](quiver-file-url/765F2EEA8B7DC51171DF0E354DAE869C.pdf)

| Region             | Significance | Optimal dRBB cut |
| ------------------ | ------------ | ---------------- |
| 2j 150-250 GeV     | 1.670482     | 1.450000             |
| 2j 250-300 GeV     | ~~**1.415330**~~     | 1.05             |
| 2j >300 GeV        | 1.039216     | 1.20             |
| 3j 150-250 GeV     | 0.966635     | 1.60             |
| 3j 250-300 GeV     | 0.589455     | 1.10             |
| 3j >300 GeV        | 0.782955     | 1.00             |
| Combination        | 2.787203     |                  |

**--> Improvement but very large stat uncertainty (to be quantified in the next update)**
![IMAGE](/images/q/IMAGE)

# Update : Jean-François requests

--> Test a few configurations
--> Same cuts in 2-jets and 3-jets, no transformation

* **150-200 (1.8) >200 (1.2)**

| Region     | Significance |
| ---------- | ------------ |
| 2j 150-200 |     1.190653 |
| 3j 150-200 |     0.699259 |
| 2j >200    |     1.927717 |
| 3j >200    |     1.124043 |
| Combined   |     2.624154 |

* **150-250 (1.6) >250 (1.2)**

| Region     | Significance |
| ---------- | ------------ |
| 2j 150-250 |     1.629444 |
| 3j 150-250 |     0.975674 |
| 2j >250    |     1.538191 |
| 3j >250    |     0.940575 |
| Combined   |     2.618729 |


* **150-250 (1.6) 250-300 (1.3) >300 (0.9)**

| Region     | Significance |
| ---------- | ------------ |
| 2j 150-250 |     1.629444 |
| 3j 150-250 |     0.975674 |
| 2j 250-300 |     1.169509 |
| 3j 250-300 |     0.586124 |
| 2j >300    |     0.970691 |
| 3j >300    |     0.755469 |
| Combined   |     2.613675 |


# JF plots

{% highlight c_cpp %}
TH1F *hsig=new TH1F("hsig","Signal",17,30,200)
TH1F *hbkg=new TH1F("hbkg","Background",17,30,200)
// TFile *_file0 = TFile::Open("sigDirectTag.root")
// TFile *_file1 = TFile::Open("bkgDirectTag.root")
_file0->cd()
Nominal->Draw("mBB>>hsig","EventWeight*(MET>300&&MET<500&&nJ==2&&nTags==2&&dRBB<0.9)")
_file1->cd()
Nominal->Draw("mBB>>hbkg","EventWeight*(MET>300&&MET<500&&nJ==2&&nTags==2&&dRBB<0.9)")
// hsig->SetLineColor(kRed)
hsig->Draw("text")
hbkg->Draw("text same")
{% endhighlight %}

# 2nd set of requests from Jean-François

* **150-200, dRBB < 1.8 :**

| Region     | Significance |
| ---------- | ------------ |
| 2j 150-200 |     1.190653 |
| 3j 150-200 |     0.699259 |

* **200-250, dRBB < 1.4 :**

| Region     | Significance |
| ---------- | ------------ |
| 2j 200-250 |     1.145406 |
| 3j 200-250 |     0.714522 |


* **250+, dRBB < 1.3 :**

| Region     | Significance |
| ---------- | ------------ |
| 2j 250-2000 |     1.504741 |
| 3j 250-2000 |     0.926466 |


**Combination : 2.617575**

