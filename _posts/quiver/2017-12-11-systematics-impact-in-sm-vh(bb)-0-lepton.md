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
## Single-top wt acceptance
In WSMaker, what is the difference between (src/systematiclistsbuilder_vhbbrun2.cpp) :
* normFact (a priori : floatting normalisation)
* normSys ?
* sampleNormSys ?
)
