---
layout: post
title: Impact of bTagging systematics in the SM VH(bb) cut-based analysis 
tags: 
    - btagging
    - VHbb
---

# Purpose
In ranking plots for L=150fb-1 prospects, and a priori for EPS as well, the first bTagging NP **b-jet tagging efficiency 0** ranks high in the MVA analysis and low in the cut-based analysis

[VH(bb) prospects for L=150fb-1](quiver-note-url/BCAB7800-29DB-4D33-9915-8202FCCDE136)

* MVA
![IMAGE](quiver-image-url/7BA11C06F26B7E42D25C74DEF916685D.jpg =586x775)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_0_125_Systs_use1tagFalse_mva_pulls_125.pdf](quiver-file-url/8ACB7CDD0BD1545847957B5DA3FB972E.pdf)
* Cuts
![IMAGE](quiver-image-url/D8989AF3FB9E192EAA794FC4B0A85C4B.jpg =581x775)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_cuts_fullRes_VHbbRun2_13TeV_lumi150scaled_cuts_0_125_Systs_use1tagFalse_mBB_pulls_125.pdf](quiver-file-url/249420C4F7D13350CB68EA751995E452.pdf)

# Method

* Compare the shapes and significances of the nominal vs up/down systematics of the systematic **SysFT_EFF_Eigen_B_0_AntiKt4EMTopoJets**
* MVA analysis with standard rebinning Trafo D(10,5)
* mBB analysis with rebinning mBB[30,200] bins of 10 GeV

* Systematic **SysFT_EFF_Eigen_B_0_AntiKt4EMTopoJets**

| Region             | Down     | Nominal  | Up       |
| ------------------ | -------- | -------- | -------- |
| 150ptv_SR_mva28 2j | 2.93877  | 2.85861  | 2.77857  |
| 150ptv_SR_mva28 3j | 1.99049  | 1.92678  | 1.86344  |
| Combined           | 3.549425 | 3.447337 | 3.345573 |
|                          |         |         |          |
| 150_200ptv_SRcuts_mBB 2j | 1.46898 | 1.43323 | 1.39757  |
| 150_200ptv_SRcuts_mBB 3j | 0.90755 | 0.883941| 0.860381 |
| 200ptv_SRcuts_mBB 2j     | 2.23326 | 2.17292 | 2.11265  |
| 200ptv_SRcuts_mBB 3j     | 1.37317 | 1.32941 | 1.28595  |
| Combined                 | 3.139206| 3.053590| 2.968234 |


* Systematic **SysFT_EFF_Eigen_B_1_AntiKt4EMTopoJets**

| Region                   | Down    | Nominal | Up  |
| ------------------------ | ------- | ------- | --- |
| 150ptv_SR_mva28 2j       | 2.92233 | 2.85861 | 2.79484 |
| 150ptv_SR_mva28 3j       | 1.97086 | 1.92678 | 1.88276 |
| Combined                 | 3.524812 | 3.447337 | 3.369854 |
|                          |          |          |          |
| 150_200ptv_SRcuts_mBB 2j | 1.45924 | 1.43323 | 1.4072 |
| 150_200ptv_SRcuts_mBB 3j | 0.8999  | 0.883941| 0.867984 |
| 200ptv_SRcuts_mBB 2j     | 2.22771 | 2.17292 | 2.11809 |
| 200ptv_SRcuts_mBB 3j     | 1.36498 | 1.32941 | 1.29387 |
| Combined                 | 3.124910| 3.053590| 2.982283 |

* Notes :

* on mBB, NP0 has null impact on the signal shape in 2 jets High Met 
