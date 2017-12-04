---
layout: post
title: MET in ttbar events
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
![IMAGE](quiver-image-url/0962E0BDDD2FEFBF2A649992E167048C.jpg =1244x808)

## Leptons flavour
![IMAGE](quiver-image-url/625D3AF43CA19979DC52B58311C7D127.jpg =1263x808)
![IMAGE](quiver-image-url/4B2534EBC437EAB6AE060660F7662CA7.jpg =1245x809)

# Single lepton events
![IMAGE](quiver-image-url/BC57C25FBF03BD4943945A58743791F8.jpg =628x467)

## pT of the neutrino / lepton
![IMAGE](quiver-image-url/067B8674E1527574701AAE64A1B60D4E.jpg =1095x648)
![IMAGE](quiver-image-url/7955725F12AC2F087FE70CD0407146DB.jpg =1085x642)

## dR of the neutrino / lepton to the lepton W
![IMAGE](quiver-image-url/F81DC01F4E247CD9197C1103E1B9F3A0.jpg =1091x638)
![IMAGE](quiver-image-url/694869CFB0DAFE840AD4098ADE25A008.jpg =1095x634)

## pT of the leptonically/hadronically decaying Ws
![IMAGE](quiver-image-url/23F3C0B882266483FDCBF75EF6F248BE.jpg =1098x637)
![IMAGE](quiver-image-url/62E823E2896934FD4A2846ACD1E3C91B.jpg =1100x641)

## dPhi top b
![IMAGE](quiver-image-url/AABEAEA42798FD03A025F4D984EE4870.jpg =1356x489)

## nJ as a function of the hadronically decaying W

Average table :
|  nJ | pT W   |
| --- | ------ |
| 2   | 70 GeV |
| 3   | 91 GeV |
![IMAGE](quiver-image-url/CEEF1E052C633D54A41D6A9B22B28F0C.jpg =1106x640)

# Dilepton events
![IMAGE](quiver-image-url/8063F7F9CA18E29E4CCC02C6C9F635BF.jpg =675x467)
## pT of the neutrino / lepton pair
![IMAGE](quiver-image-url/6FC33925D4E0353D4F9BF519D0691C32.jpg =1319x792)
![IMAGE](quiver-image-url/76E6FEC8E4A1DAB01F7F2735BC0A4F82.jpg =1336x784)

## pT of individual leptons / neutrinos
* nu/lep in red, anu/alep in blue

![IMAGE](quiver-image-url/B296B9BF45CEE9B591480A8DA43B8820.jpg =1329x779)
![IMAGE](quiver-image-url/6C4C54DCAA699CD49DC8189ED79637B0.jpg =1315x785)
![IMAGE](quiver-image-url/941E06D835FADDF451E0F17AEC72B2C5.jpg =1342x799)
![IMAGE](quiver-image-url/15604859AE09984312A8C6E8D0CEB564.jpg =1024x608)
![IMAGE](quiver-image-url/B77738D77331FD7E93CCE6589CDB3F1D.jpg =1350x763)
--> the neutrinos are quite little collinear, and this is not correlated to pTvv
![IMAGE](quiver-image-url/73D25F6C3F5106D2536FC39F8D2BE698.jpg =1264x814)
![IMAGE](quiver-image-url/4BD62ADC4B17140E5BCE7356C3FABEAA.jpg =1344x803)
![IMAGE](quiver-image-url/F82B64E640558AC610A43CF2B830D548.jpg =1351x801)
--> When pTv<100 and pTav< 100, it does not necessarily mean that they are collinear :
![IMAGE](quiver-image-url/3CD5F6E44E794AA18E385D789F6FFEBC.jpg =1310x784)
![IMAGE](quiver-image-url/98B825DA763769EFF103CB1E721D9740.jpg =1318x802)![IMAGE](quiver-image-url/91223B79C56CDA13FEFB3A2BA9B1194F.jpg =1271x799)
--> When neutrinos don't have sufficient pT/dR to produce MET>150, the MET-TruthMET difference is much larger (40 GeV instead of 10 GeV is one neutrino has very large pT) 
![IMAGE](quiver-image-url/401091A9113BCFC00B560DEAC0246E5F.jpg =617x450)

## pT of the WW pair
* if 0-lepton reconstructed in a dilepton truthdecay, the truthMET consists of the vector sum of the pT of the Ws
* --> previous statement wrong, leptons accounted in the softtrk term of met
![IMAGE](quiver-image-url/2510D642AE6B055A0A8568E27EFFE96F.jpg =1328x787)

## pT of the top in single/dilep events
* single lep in red
* dilep in blue
![IMAGE](quiver-image-url/21F47147C0D9BD1648384448A5D61525.jpg =1142x715)
![IMAGE](quiver-image-url/25DFD6008713212C386CCFEC138EF10D.jpg =1342x790)

## single lepton tau vs e/mu pT
* taus are in blue
![IMAGE](quiver-image-url/9EDCE3521C3835DDBBAD22F7CA300168.jpg =1346x799)

## number of taus in dilep events
* 47% of events have 2 tau leptons -->should look at their respective decays in order to compute met ...
![IMAGE](quiver-image-url/72CEA09AA7A0B702480871BBF09E8B16.jpg =642x466)


