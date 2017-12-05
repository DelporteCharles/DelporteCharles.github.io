---
title: MET in ttbar events
date: '2017-11-15'
tags: []
---
# Purpose
* better understand the origin of recoMET > 150 in ttbar events
* most plots in 2-3j 2tags after full selection

https://svnweb.cern.ch/trac/atlasoff/browser/Generators/MC15JobOptions/trunk/share/DSID410xxx/MC15.410000.PowhegPythiaEvtGen_P2012_ttbar_hdamp172p5_nonallhad.py

## Understanding the nonallhad 

{% highlight sh %}
root -l ttbar_PwPy8EG/user.nwhallon.mc15_13TeV.410501.PwPy8EG_A14_ttbar_hdamp258p75_nonallhad.s2726.HIGG5D1.28-05_CxAOD.root/user.nwhallon.11149918._000001.CxAOD.root 
 CollectionTree->Scan("TruthParticles___NominalAuxDyn.pdgId:TruthParticles___NominalAuxDyn.status:TruthParticles___NominalAuxDyn.e")
{% endhighlight %}

{% highlight sh %}
***********************************************************
*    Row   * Instance * TruthPart * TruthPart * TruthPart *
***********************************************************
*        0 *        0 *         6 *        22 * 339215.53 *
*        0 *        1 *        -6 *        22 * 443397.28 *
*        0 *        2 *        24 *        22 * 160723.54 *
*        0 *        3 *         5 *        23 * 172398.18 *
*        0 *        4 *       -24 *        22 * 366797.53 *
*        0 *        5 *        -5 *        23 * 89583.546 *
*        0 *        6 *        -1 *        23 *  118947.5 *
*        0 *        7 *         2 *        23 * 41517.613 *
*        0 *        8 *        15 *        23 * 69350.429 *
*        0 *        9 *       -16 *        23 * 297447.09 *
*        0 *       10 *        15 *         2 * 69350.421 *
*        0 *       11 *       -16 *         1 * 297447.09 *

--> Event 0 has :
  W+ -> dbar u   : 160723.54 - 118947.5 - 41517.613 = 258.427000
  W- -> tau nutaubar : 366797 - 69350 - 297447 = 0

*        1 *        0 *         6 *        22 * 946104.81 *
*        1 *        1 *        -6 *        22 * 212530.70 *
*        1 *        2 *        24 *        22 * 574257.93 *
*        1 *        3 *         5 *        23 * 311078.93 *
*        1 *        4 *       -24 *        22 * 150873.62 *
*        1 *        5 *        -5 *        23 * 65454.550 *
*        1 *        6 *       -15 *         2 * 545113.37 *
*        1 *        7 *        16 *         1 * 28801.480 *
*        1 *        8 *         1 *        23 * 27643.168 *
*        1 *        9 *        -2 *        23 * 121780.64 *

--> Event 1 has :
  W+ -> taubar nutau : 574257.93 - 545113.37 - 28801.480 = 343.080000
  W- -> d ubar   : 150873.62 - 27643.168 - 121780.64 = 1449.812000

*        2 *        0 *         6 *        22 * 327585.96 *
*        2 *        1 *        -6 *        22 * 257544.12 *
*        2 *        2 *        24 *        22 * 249918.20 *
*        2 *        3 *         5 *        23 * 71037.335 *
*        2 *        4 *       -24 *        22 * 184664.37 *
*        2 *        5 *        -5 *        23 * 84284.265 *
*        2 *        6 *        -1 *        23 * 118276.26 *
*        2 *        7 *         2 *        23 * 123962.85 *
*        2 *        8 *        11 *        23 * 58160.867 *
*        2 *        9 *       -12 *        23 * 125986.64 *

W+ -> dbar u : 249918.20 - 118276.26 - 123962.85 = 7679.090000
W- -> e nuebar : 184664.37 - 58160.867 - 125986.64 = 516.863000
{% endhighlight %}

## Number of neutrinos per event
* very often 1 neutrino + 1 lepton in W dec, 72% of them 
![IMAGE](/images/q/IMAGE)

## Leptons flavour
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

# Single lepton events
![IMAGE](/images/q/IMAGE)

## pT of the neutrino / lepton
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

## dR of the neutrino / lepton to the lepton W
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

## pT of the leptonically/hadronically decaying Ws
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

## dPhi top b
![IMAGE](/images/q/IMAGE)

## nJ as a function of the hadronically decaying W

Average table :
|  nJ | pT W   |
| --- | ------ |
| 2   | 70 GeV |
| 3   | 91 GeV |
![IMAGE](/images/q/IMAGE)

# Dilepton events
![IMAGE](/images/q/IMAGE)
## pT of the neutrino / lepton pair
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

## pT of individual leptons / neutrinos
* nu/lep in red, anu/alep in blue

![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
--> the neutrinos are quite little collinear, and this is not correlated to pTvv
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
--> When pTv<100 and pTav< 100, it does not necessarily mean that they are collinear :
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
--> When neutrinos don't have sufficient pT/dR to produce MET>150, the MET-TruthMET difference is much larger (40 GeV instead of 10 GeV is one neutrino has very large pT) 
![IMAGE](/images/q/IMAGE)

## pT of the WW pair
* if 0-lepton reconstructed in a dilepton truthdecay, the truthMET consists of the vector sum of the pT of the Ws
* --> previous statement wrong, leptons accounted in the softtrk term of met
![IMAGE](/images/q/IMAGE)

## pT of the top in single/dilep events
* single lep in red
* dilep in blue
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

## single lepton tau vs e/mu pT
* taus are in blue
![IMAGE](/images/q/IMAGE)

## number of taus in dilep events
* 47% of events have 2 tau leptons -->should look at their respective decays in order to compute met ...
![IMAGE](/images/q/IMAGE)



