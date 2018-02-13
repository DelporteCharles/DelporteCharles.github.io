---
title: Single Top Diagram Removal Substration uncertainty at EPS
date: '2017-12-21'
tags: []
---
# Purpose
* amongst modelling uncertainties which dominate the ranking plot, single top Wt acceptance has major role, and is dominated by the difference in acceptance between Diagram Removal vs Diagram Substration models
* computed on 1-lepton events (good acceptance), extrapolated to 0-lepton
* re-run in rivet
)
# samples and jobs

* top
  * mc15_13TeV.410062.PowhegPythiaEvtGen_P2012_Wt_DS_inclusive_top.evgen.EVNT.e4132/ : https://bigpanda.cern.ch/task/12850367/
  * mc15_13TeV.410013.PowhegPythiaEvtGen_P2012_Wt_inclusive_top.evgen.EVNT.e3753/ : https://bigpanda.cern.ch/task/12850353/
* anti-top
  * mc15_13TeV.410063.PowhegPythiaEvtGen_P2012_Wt_DS_inclusive_antitop.evgen.EVNT.e4132 : https://bigpanda.cern.ch/task/12850378/
  * mc15_13TeV.410014.PowhegPythiaEvtGen_P2012_Wt_inclusive_antitop.evgen.EVNT.e3753/ : https://bigpanda.cern.ch/task/12850362/
)
# Results
)
## 2 jets
)
### Top DS/DR
![IMAGE](/images/q/580C4CD1B76AE4EDE2BF60BFFB729D3E.jpg)
### Anti-top DS/DR
![IMAGE](/images/q/C88B89396DCA3A28565310241EF0FD9E.jpg)
## 3 jets
)
### Top DS/DR
![IMAGE](/images/q/51E64B173D73800517B6D8466BE0EA03.jpg)
### Anti-top DS/DR
![IMAGE](/images/q/BAE7B6B5E83C8E0CD8306228F5E7FCD9.jpg)
# Conclusion

* far from 28 % uncertainty on this systematic
  * 2 jets
    * top : 7.7%
    * atop : 9.5%
  * 3 jets
    * top : 4.7 %
    * atop : 3.7% 
* bias from non selecting b labelled jets ?
* [ ] wait for answer from Chloe/Valerio
)
 root -l Rivet_410013.root Rivet_410014.root Rivet_410062.root Rivet_410063.root

gStyle->SetOptStat(0);

TString hname)
