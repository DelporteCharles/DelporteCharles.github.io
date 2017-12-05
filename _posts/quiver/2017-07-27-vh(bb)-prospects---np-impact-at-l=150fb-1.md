---
title: VH(bb) prospects - NP impact at L=150fb-1
date: '2017-07-27'
tags:
- fit
- VHbb
---
References :
* Valerio : 
https://indico.cern.ch/event/654083/contributions/2667112/attachments/1495312/2326367/Projection.pdf
* Nicolas : 
https://indico.cern.ch/event/646119/contributions/2663749/attachments/1496956/2329878/FermionicCouplingsProspects.pdf

1) Generate a workspace at L=150 fb-1 with "usually floatting" normalization NP fixed to their EPS fit value (from the 2j category)

| Sample | SFval |
| ------ | ----- |
| ttbar  | 0.90  |
| Whf    | 1.22  |
| Zhf    | 1.30  |

2) Fit the Asimov dataset
3) Look for the impact of the other NP : changes with respect to EPS17 ?

## Prefit ranking
### EPS
![SMVHVZ_LHCP17_MVA_v05.default_fullRes_VHbbRun2_13TeV_default_012_125_Systs_use1tagFalse_mva_pulls_prefit_125.png](/images/q/SMVHVZ_LHCP17_MVA_v05.default_fullRes_VHbbRun2_13TeV_default_012_125_Systs_use1tagFalse_mva_pulls_prefit_125.png)

### L = 150 fb-1 prospect
![SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_012_125_Systs_use1tagFalse_mva_pulls_prefit_125.png](/images/q/SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_012_125_Systs_use1tagFalse_mva_pulls_prefit_125.png)

## PostFit ranking
| Syst List (EPS17 ranking)  | EPS rank | Rank in L=150fb-1 prospect |
| -------------------------- | -------- |-------------------------- |
| alpha_SysTheoryUEPSAcc     | 1 | 1                          |
| W+jets pTV                 | 2 | 2                          |
| Single top Wt acc.         | 3 |  9                          |
| b-jet tagging efficiency 1 | 4 | 5                          |
| 2-lepton tt mbb shape      | 5 | 3                          |
| Z+jets mbb shape           | 6 |  8                          |
| alpha_SysTheoryAcc_J2_qqVH | 7 |  4                          |
| c-jet tagging efficiency 1 | 8 |  13                         |
| b-jet tagging efficiency 0 | 9 | 6                          |
| ATLAS_norm_Zbb_J3          | 10 | -                          |
| Single top Wt mbb shape    | 11 | -                          |
| alpha_SysTheoryAcc_J3_qqVH | 12 | 7                          |
| alpha_SysTheoryUEPSAcc_J3  | 13 | 11                         |
| Luminosity                 | 14 | 15                         |
| Single top Wt pTV          | 15 | -                          |

Newcomers NP in the top15 :
| Rank | NP name                      |
| ---- | ---------------------------- |
| 10   | QCD scale for ggZH           |
| 12   |1NP_JET_Flavor_Composition_VV |
| 14   | tt mbb shape                 |


### EPS
![SMVHVZ_LHCP17_MVA_v05.default_fullRes_VHbbRun2_13TeV_default_012_125_Systs_use1tagFalse_mva_pulls_125.png](/images/q/SMVHVZ_LHCP17_MVA_v05.default_fullRes_VHbbRun2_13TeV_default_012_125_Systs_use1tagFalse_mva_pulls_125.png)

### L = 150 fb-1 prospect
![SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_012_125_Systs_use1tagFalse_mva_pulls_125.png](/images/q/SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_012_125_Systs_use1tagFalse_mva_pulls_125.png)

