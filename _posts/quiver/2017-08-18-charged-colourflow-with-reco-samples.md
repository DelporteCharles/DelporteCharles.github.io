---
title: Charged ColourFlow with reco samples
date: '2017-08-18'
tags: []
---
Using private CxAOD produced with the hack 
[Charged ColourFlow in CxAODFramework](quiver-note-url/F1D604F1-9E69-41CE-82DC-D6655A523AC9)
)
* Makes use of reco samples, with Ghost-associated tracks to jets in order to compute colourflow
* Usual VH(bb) selection

* Samples are : 
  * ZH125
  * WH125
  * ttbar
  * Znunu_140-280_BFilter
)
# ColourFlow distributions

## jets denomination
* 1)
Conclusions :
* Observable effect with potential discrimination in the 2jet category : higer jets multiplicity probably complicates too much the colour pattern for such simple variables
* 3 jets category : Bump in 0 even for ttbar + small asymetry ... (distribution should have been symmetrized)
* Attempt to exploit these variables and their potential correlations in a BDT shows no improvement at all (neither in 2 jets nor in 3 jets) :
  * ttbar is no the majoritary background in 2 jets, where there is discrimination
  * other variables (mBB, dRBB) still present a much cleaner discrimination
)
