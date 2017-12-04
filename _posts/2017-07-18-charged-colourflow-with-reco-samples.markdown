---
layout: post
title: Charged ColourFlow with reco samples
---

Using private CxAOD produced with the hack 
[Charged ColourFlow in CxAODFramework](quiver-note-url/F1D604F1-9E69-41CE-82DC-D6655A523AC9)

* Makes use of reco samples, with Ghost-associated tracks to jets in order to compute colourflow
* Usual VH(bb) selection

* Samples are : 
  * ZH125
  * WH125
  * ttbar
  * Znunu_140-280_BFilter

# ColourFlow distributions

## jets denomination
* 1 = leading pT
* 2 = sub-leading pT
* 3 = non b-tagged jet

## 2tag 2jets
### Pairing 1-2
![2tag2jet_150ptv_SR_ColourFlowAngleJ12.png](quiver-image-url/5B7D204298F493EE1D46797FE6636748.png =696x472)
![2tag2jet_150ptv_SR_ColourFlowAngleJ21.png](quiver-image-url/0FCD25DC580E74A1423FE81E89C47BE4.png =696x472)

## 2tag 3jets
### Pairing 1-2
![2tag3jet_150ptv_SR_ColourFlowAngleJ12.png](quiver-image-url/2CBC949C8CC37EC6935AA4AC21E29E73.png =696x472)
![2tag3jet_150ptv_SR_ColourFlowAngleJ21.png](quiver-image-url/3FFE21F105F2655C32B2B5DF785AF4FE.png =696x472)
### Pairing 1-3
![2tag3jet_150ptv_SR_ColourFlowAngleJ13.png](quiver-image-url/BE12717BB2AFF658D69EFA062B518434.png =696x472)
![2tag3jet_150ptv_SR_ColourFlowAngleJ31.png](quiver-image-url/2677BBFE2541B794320610050977882E.png =696x472)
### Pairing 2-3
![2tag3jet_150ptv_SR_ColourFlowAngleJ23.png](quiver-image-url/831C18881FFBF4C8C9D197D3FE4C79D2.png =696x472)
![2tag3jet_150ptv_SR_ColourFlowAngleJ32.png](quiver-image-url/6C0E34F3B149B2471495ACE221297E08.png =696x472)

Conclusions :
* Observable effect with potential discrimination in the 2jet category : higer jets multiplicity probably complicates too much the colour pattern for such simple variables
* 3 jets category : Bump in 0 even for ttbar + small asymetry ... (distribution should have been symmetrized)
* Attempt to exploit these variables and their potential correlations in a BDT shows no improvement at all (neither in 2 jets nor in 3 jets) :
  * ttbar is no the majoritary background in 2 jets, where there is discrimination
  * other variables (mBB, dRBB) still present a much cleaner discrimination
