---
title: VH(bb) prospects for L=150fb-1
date: '2017-10-04'
tags:
- fit
- prospects
- VHbb
---
# Purpose
* Study the impact of systematics with 150 fb-1 integrated luminosity
* Compare the MVA and cut-based analysis
* Samples scaled to with the appropriate fit Scale Factors

[VH(bb) prospects - NP impact at L=150fb-1](quiver-note-url/8D7876FF-5982-4026-845C-64A91C519F34)

http://cdelport.web.cern.ch/cdelport//SMVHbb//plots_v28/index.html
http://cdelport.web.cern.ch/cdelport//SMVHbb//plots_v28_5bins/index.html

| Sample | Scale Factor |
| ------ | ------------ |
| ttbar  | 0.9          |
| Zhf    | 1.3          |
| Whf    | 1.22         |

To Do
* [x] runBreakdown
* [x] Understand the numbers "total unc" and "sum of sq"

{% highlight javascript %}
// https://svnweb.cern.ch/trac/atlasphys-hsg5/browser/Physics/Higgs/HSG5/Limits/InputPreparation/WSMaker/trunk/macros/drawPlot_pulls.C

484	    double sum_poi2 = 0.;
485	    for (int i = 0; i < nrNuis; ++i) { 
486	      double up = fabs(poi_up[i] - poi_hat[i]);
487	      double down = fabs(poi_up[i] - poi_hat[i]);
488	      sum_poi2 += pow((up+down)/2, 2);
489	    }

1435	    cout << "total unc = " << (fabs(sigma_tot_hi) + fabs(sigma_tot_lo)) / 2 << endl;
1436	    cout << "sum of sq = " << sqrt(sum_poi2) << endl;
{% endhighlight %}

# Results
## 012-leptons
### Post-fit impact
* MVA

| Rank      | Impact - (?) | Impact + (?) | Name |
| --------- | ------ | ---- | ---- |
| Rank 145: | 0      | 0    | alpha_SysJET_21NP_JET_EffectiveNP_8restTerm| 
| Rank 144: | 0 | 0 | alpha_SysJET_21NP_JET_EffectiveNP_6| 
| Rank 143: | 0 | 0 | alpha_SysMUON_MS| 
| Rank 142: | 0 | 0 | alpha_SysMUON_EFF_TrigSystUncertainty| 
| Rank 141: | 0 | 0 | alpha_SysVHQCDscaleMbb_ggZH| 
| Rank 140: | 0 | 0 | alpha_SysVHQCDscaleMbb| 
| Rank 139: | 0 | 0 | alpha_SysEL_EFF_Trigger_TOTAL_1NPCOR_PLUS_UNCOR| 
| Rank 138: | 0 | 0 | alpha_SysJET_21NP_JET_EffectiveNP_7| 
| Rank 137: | 0 | 0 | alpha_SysMUON_SCALE| 
| Rank 136: | 0 | 0 | alpha_SysMUON_SAGITTA_RESBIAS| 
| Rank 135: | 0 | 0 | alpha_SysVHPDFPTV_ggZH| 
| Rank 134: | 1e-05 | 1e-05 | alpha_SysZZUEPSResid_L0| 
| Rank 133: | 2e-05 | 1e-05 | alpha_SysMUON_EFF_SYS_LOWPT| 
| Rank 132: | 2e-05 | 1e-05 | alpha_SysMUON_EFF_STAT_LOWPT| 
| Rank 131: | 3e-05 | 3e-05 | alpha_SysVHPDFPTV| 
| Rank 130: | 3e-05 | 3e-05 | alpha_SysVHQCDscalePTV_ggZH| 
| Rank 129: | 2e-05 | 8e-05 | alpha_SysJET_21NP_JET_EffectiveNP_5| 
| Rank 128: | 8e-05 | 5e-05 | alpha_SysMUON_EFF_STAT| 
| Rank 127: | 8e-05 | 8e-05 | alpha_SysMJTrigger_multijetEl| 
| Rank 126: | 0.00013 | 4e-05 | alpha_SysTheoryPDFAcc_ggZH| 
| Rank 125: | 0.000149 | 3e-05 | alpha_SysTheoryAcc_JVeto_ggZH| 
| Rank 124: | 0.00012 | 7e-05 | alpha_SysFT_EFF_Eigen_Light_4| 
| Rank 123: | 0.00012 | 9e-05 | alpha_SysEL_EFF_Reco_TOTAL_1NPCOR_PLUS_UNCOR| 
| Rank 122: | 5e-05 | 0.00016 | alpha_SysMUON_ID| 
| Rank 121: | 0.00028 | 0 | alpha_SysStoptPTV| 
| Rank 120: | 0.000192 | 0.00013 | alpha_SysTheoryAcc_J3_ggZH| 
| Rank 119: | 0.000227 | 0.0002 | alpha_SysWZUEPSResid_L0| 
| Rank 118: | 0.00021 | 0.00026 | alpha_SysJET_21NP_JET_EffectiveNP_4| 
| Rank 117: | 0.000479 | 0.0001 | alpha_SysJET_21NP_JET_EtaIntercalibration_TotalStat| 
| Rank 116: | 0.0005 | 0.00022 | alpha_SysFT_EFF_extrapolation| 
| Rank 115: | 0.000675 | 8e-05 | alpha_SysZZNorm| 
| Rank 114: | 0.00044 | 0.0004 | alpha_SysZlNorm| 
| Rank 113: | 0.000464 | 0.00038 | alpha_SysVVPTVPSUE| 
| Rank 112: | 0.000455 | 0.00045 | alpha_SysVZUEPS_J3| 
| Rank 111: | 0.000574 | 0.00036 | alpha_SysVHQCDscalePTV| 
| Rank 110: | 0.000606 | 0.00042 | alpha_SysTheoryAcc_JVeto_qqVH| 
| Rank 109: | 0.000631 | 0.00049 | alpha_SysMJWOCorrection_multijetEl| 
| Rank 108: | 0.000574 | 0.00058 | alpha_SysMUON_ISO_STAT| 
| Rank 107: | 0.000685 | 0.00053 | alpha_SysZccZbbRatio| 
| Rank 106: | 0.000407 | 0.000841 | alpha_SysEG_RESOLUTION_ALL| 
| Rank 105: | 0.000639 | 0.00064 | alpha_SysVZUEPSAcc| 
| Rank 104: | 0.000667 | 0.00062 | alpha_SysstopsNorm| 
| Rank 103: | 0.000814 | 0.00054 | alpha_SysWbbNorm_L0| 
| Rank 102: | 0.000645 | 0.00072 | alpha_SysMET_SoftTrk_ResoPerp| 
| Rank 101: | 0.001469 | 2e-05 | alpha_SysZbbNorm_L0| 
| Rank 100: | 0.000817 | 0.00077 | alpha_SysMJSFsCR_multijetEl| 
| Rank 99: | 0.00073 | 0.001 | alpha_SysTheoryAcc_J2_ggZH| 
| Rank 98: | 0.000788 | 0.00101 | alpha_SysJET_JvtEfficiency| 
| Rank 97: | 0.000929 | 0.00088 | alpha_SysWlNorm| 
| Rank 96: | 0.000834 | 0.00108 | alpha_SysJET_21NP_JET_Flavor_Composition_ttbar_L2| 
| Rank 95: | 0.00115 | 0.00114 | alpha_SysMUON_ISO_SYS| 
| Rank 94: | 0.001325 | 0.00137 | alpha_SysVVPTVME| 
| Rank 93: | 0.001371 | 0.00133 | alpha_SysEL_EFF_Iso_TOTAL_1NPCOR_PLUS_UNCOR| 
| Rank 92: | 0.001504 | 0.0013 | alpha_SysVVMbbME| 
| Rank 91: | 0.001632 | 0.00145 | alpha_SysVZQCDscale_J2| 
| Rank 90: | 0.001409 | 0.00186 | alpha_SysJET_21NP_JET_EtaIntercalibration_NonClosure| 
| Rank 89: | 0.00025 | 0.00315 | alpha_SysJET_21NP_JET_Pileup_OffsetMu| 
| Rank 88: | 0.00177 | 0.00166 | alpha_SysWblWbbRatio| 
| Rank 87: | 0.001965 | 0.0015 | alpha_SysttbarNorm_DWhfCR_L1| 
| Rank 86: | 0.00176 | 0.00173 | alpha_SysMJReduced_multijetMu| 
| Rank 85: | 0.001823 | 0.00179 | alpha_SysTheoryQCDscale_qqVH| 
| Rank 84: | 0.001849 | 0.00183 | alpha_SysTheoryPDF_ggZH| 
| Rank 83: | 0.002051 | 0.00188 | alpha_SysMETTrigTop| 
| Rank 82: | 0.00211 | 0.00183 | alpha_SysVZQCDscale_JVeto| 
| Rank 81: | 0.002071 | 0.00191 | alpha_SysZclNorm| 
| Rank 80: | 0.002016 | 0.002 | alpha_SysFT_EFF_extrapolation_from_charm| 
| Rank 79: | 0.002314 | 0.00177 | alpha_SysMJNorm_2J_Mu| 
| Rank 78: | 0.002347 | 0.00199 | alpha_SysZbcZbbRatio| 
| Rank 77: | 0.002396 | 0.00219 | alpha_SysFT_EFF_Eigen_Light_2| 
| Rank 76: | 0.002547 | 0.00252 | alpha_SysTheoryPDFAcc_qqVH| 
| Rank 75: | 0.002492 | 0.00279 | alpha_SysMJReduced_multijetEl| 
| Rank 74: | 0.003157 | 0.00245 | alpha_SysMUON_EFF_SYS| 
| Rank 73: | 0.003364 | 0.00284 | alpha_SysVZQCDscale_J3| 
| Rank 72: | 0.003408 | 0.00293 | alpha_SysStoptMBB| 
| Rank 71: | 0.003582 | 0.00337 | alpha_SysWZNorm| 
| Rank 70: | 0.003679 | 0.00354 | alpha_SysWclNorm| 
| Rank 69: | 0.003932 | 0.00382 | alpha_SysVHUEPSPTV| 
| Rank 68: | 0.00058 | 0.0072 | alpha_SysMJNorm_3J_El| 
| Rank 67: | 0.004125 | 0.00421 | alpha_SysVHNLOEWK| 
| Rank 66: | 0.004471 | 0.00427 | alpha_SysstoptNorm| 
| Rank 65: | 0.005235 | 0.00424 | alpha_SysMJ2Tag_multijetMu| 
| Rank 64: | 0.00182 | 0.007704 | alpha_SysPRW_DATASF| 
| Rank 63: | 0.004479 | 0.00543 | alpha_SysWbbNorm_DWhfSR| 
| Rank 62: | 0.005571 | 0.00451 | alpha_SysJET_21NP_JET_Pileup_PtTerm| 
| Rank 61: | 0.005097 | 0.00524 | alpha_SysTheoryPDF_qqVH| 
| Rank 60: | 0.005856 | 0.00483 | alpha_SysttbarNorm_J2| 
| Rank 59: | 0.005854 | 0.00551 | alpha_SysMJ2Tag_multijetEl| 
| Rank 58: | 0.005803 | 0.00568 | alpha_SysZblZbbRatio| 
| Rank 57: | 0.00571 | 0.00591 | alpha_SysTheoryBRbb| 
| Rank 56: | 0.00902 | 0.003 | alpha_SysVHUEPSMbb| 
| Rank 55: | 0.006179 | 0.00615 | alpha_SysFT_EFF_Eigen_C_2| 
| Rank 54: | 0.006434 | 0.0063 | alpha_SysMJNorm_2J_El| 
| Rank 53: | 0.010624 | 0.002832 | alpha_SysJET_21NP_JET_Pileup_OffsetNPV| 
| Rank 52: | 0.007264 | 0.00685 | alpha_SysEL_EFF_ID_TOTAL_1NPCOR_PLUS_UNCOR| 
| Rank 51: | 0.007034 | 0.00711 | alpha_SysstopWtNorm| 
| Rank 50: | 0.00756 | 0.0072 | alpha_SysFT_EFF_Eigen_B_2| 
| Rank 49: | 0.006399 | 0.00837 | alpha_SysJET_21NP_JET_BJES_Response| 
| Rank 48: | 0.007706 | 0.00752 | alpha_SysWccWbbRatio| 
| Rank 47: | 0.009998 | 0.0054 | alpha_SysWMbb| 
| Rank 46: | 0.005413 | 0.01051 | alpha_SysMJNorm_3J_Mu| 
| Rank 45: | 0.015146 | 0.002174 | alpha_SysJET_21NP_JET_EffectiveNP_1| 
| Rank 44: | 0.011744 | 0.00588 | alpha_SysZPtV| 
| Rank 43: | 0.010489 | 0.00758 | alpha_SysJET_21NP_JET_Flavor_Composition_Top| 
| Rank 42: | 0.013718 | 0.004919 | ATLAS_norm_Wbb_J2| 
| Rank 41: | 0.009718 | 0.00982 | alpha_SysEG_SCALE_ALL| 
| Rank 40: | 0.014179 | 0.00585 | alpha_SysJET_21NP_JET_EffectiveNP_2| 
| Rank 39: | 0.016504 | 0.00402 | ATLAS_norm_ttbar_J3_L2_Y| 
| Rank 38: | 0.010228 | 0.01155 | alpha_SysJET_21NP_JET_EffectiveNP_3| 
| Rank 37: | 0.011164 | 0.01092 | alpha_SysTTbarPTV| 
| Rank 36: | 0.011459 | 0.01098 | alpha_SysWbcWbbRatio| 
| Rank 35: | 0.0227 | 0.00054 | ATLAS_norm_Zbb_J2| 
| Rank 34: | 0.011411 | 0.01448 | alpha_SysMET_SoftTrk_Scale| 
| Rank 33: | 0.012338 | 0.0137 | alpha_SysJET_21NP_JET_Flavor_Response| 
| Rank 32: | 0.020187 | 0.006604 | alpha_SysJET_21NP_JET_Pileup_RhoTopology| 
| Rank 31: | 0.015888 | 0.01102 | alpha_SysttbarNorm_L0| 
| Rank 30: | 0.020277 | 0.007781 | alpha_SysJET_21NP_JET_Flavor_Composition_Vjets| 
| Rank 29: | 0.014295 | 0.01406 | alpha_SysFT_EFF_Eigen_Light_3| 
| Rank 28: | 0.014675 | 0.01427 | alpha_SysFT_EFF_Eigen_C_0| 
| Rank 27: | 0.014392 | 0.01477 | alpha_SysMET_SoftTrk_ResoPara| 
| Rank 26: | 0.024372 | 0.00513 | alpha_SysJET_21NP_JET_EtaIntercalibration_Modelling| 
| Rank 25: | 0.015465 | 0.01432 | ATLAS_norm_ttbar_J2_L2_Y| 
| Rank 24: | 0.022719 | 0.00771 | ATLAS_norm_Zbb_J3| 
| Rank 23: | 0.017902 | 0.01817 | alpha_SysstoptAcc| 
| Rank 22: | 0.018248 | 0.01953 | alpha_SysStopWtPTV| 
| Rank 21: | 0.020093 | 0.01905 | alpha_SysTTbarPTV_L2| 
| Rank 20: | 0.018885 | 0.02089 | alpha_SysJET_JER_SINGLE_NP| 
| Rank 19: | 0.019712 | 0.02056 | alpha_SysFT_EFF_Eigen_Light_0| 
| Rank 18: | 0.021294 | 0.01991 | alpha_SysFT_EFF_Eigen_Light_1| 
| Rank 17: | 0.027383 | 0.0158 | ATLAS_norm_Wbb_J3| 
| Rank 16: | 0.022117 | 0.02112 | alpha_SysStopWtMBB| 
| Rank 15: | 0.017256 | 0.02771 | alpha_ATLAS_LUMI_2015_2016| 
| Rank 14: | 0.025224 | 0.02421 | alpha_SysTTbarMBB| 
| Rank 13: | 0.027342 | 0.02618 | alpha_SysFT_EFF_Eigen_C_1| 
| Rank 12: | 0.027276 | 0.0281 | alpha_SysJET_21NP_JET_Flavor_Composition_VV| 
| Rank 11: | 0.030184 | 0.02645 | alpha_SysTheoryUEPSAcc_J3| 
| Rank 10: | 0.028833 | 0.0293 | alpha_SysTheoryQCDscale_ggZH| 
| Rank 9: | 0.033597 | 0.03692 | alpha_SysstopWtAcc| 
| Rank 8: | 0.037766 | 0.0351 | alpha_SysZMbb| 
| Rank 7: | 0.037606 | 0.03533 | alpha_SysTheoryAcc_J3_qqVH| 
| Rank 6: | 0.036278 | 0.04163 | alpha_SysFT_EFF_Eigen_B_0| 
| Rank 5: | 0.047479 | 0.03952 | alpha_SysFT_EFF_Eigen_B_1| 
| Rank 4: | 0.043545 | 0.04526 | alpha_SysTheoryAcc_J2_qqVH| 
| Rank 3: | 0.048091 | 0.04676 | alpha_SysTTbarMBB_L2| 
| Rank 2: | 0.061598 | 0.06271 | alpha_SysWPtV| 
| Rank 1: | 0.107327 | 0.13625 | alpha_SysTheoryUEPSAcc|

 Top range from -0.143718 to 0.168992
 Bottom range from -1.05481 to 1.24031
total unc = 0.273621
sum of sq = 0.210897

{% highlight javascript %}
muhat: 1.00000

nll_val_true: 782136.703819

  Set of nuisance          Impact on error
       parameters          
----------------------------------------------------------
                    Total  +  0.276  -  0.232  +-  0.254
                 DataStat  +  0.108  -  0.107  +-  0.107
                 FullSyst  +  0.254  -  0.206  +-  0.230
  Floating normalizations  +  0.051  -  0.046  +-  0.049
       All normalizations  +  0.056  -  0.051  +-  0.054
   All but normalizations  +  0.249  -  0.199  +-  0.224
                 Jets MET  +  0.054  -  0.041  +-  0.047
                     BTag  +  0.079  -  0.069  +-  0.074
                  Leptons  +  0.012  -  0.010  +-  0.011
               Luminosity  +  0.022  -  0.017  +-  0.019
                  Diboson  +  0.041  -  0.027  +-  0.034
                    Zjets  +  0.041  -  0.041  +-  0.041
                    Wjets  +  0.053  -  0.046  +-  0.050
              Model ttbar  +  0.061  -  0.050  +-  0.056
         Model Single Top  +  0.046  -  0.041  +-  0.043
          Model Multi Jet  +  0.021  -  0.018  +-  0.020
       Signal Systematics  +  0.185  -  0.115  +-  0.150
                  MC stat  +  0.123  -  0.112  +-  0.118
Impact on error quadratically subtracted from total, except for:
DataStat All but normalizations 
----------------------------------------------------------

  Set of nuisance          Fractional impact on error
       parameters          (square of fraction of total)
----------------------------------------------------------
                 DataStat  +  0.15  -  0.21  +- 0.18
                 FullSyst  +  0.85  -  0.79  +- 0.82
  Floating normalizations  +  0.03  -  0.04  +- 0.04
       All normalizations  +  0.04  -  0.05  +- 0.04
   All but normalizations  +  0.81  -  0.74  +- 0.78
                 Jets MET  +  0.04  -  0.03  +- 0.03
                     BTag  +  0.08  -  0.09  +- 0.08
                  Leptons  +  0.00  -  0.00  +- 0.00
               Luminosity  +  0.01  -  0.01  +- 0.01
                  Diboson  +  0.02  -  0.01  +- 0.02
                    Zjets  +  0.02  -  0.03  +- 0.03
                    Wjets  +  0.04  -  0.04  +- 0.04
              Model ttbar  +  0.05  -  0.05  +- 0.05
         Model Single Top  +  0.03  -  0.03  +- 0.03
          Model Multi Jet  +  0.01  -  0.01  +- 0.01
       Signal Systematics  +  0.45  -  0.25  +- 0.35
                  MC stat  +  0.20  -  0.23  +- 0.21
----------------------------------------------------------
{% endhighlight %}

* Cuts

| Rank      | Impact - (?) | Impact + (?) | Name |
| --------- | ------ | ---- | ---- |
| Rank 132 | 0 | 0 | alpha_SysMUON_EFF_TrigSystUncertainty | 
| Rank 131 | 0 | 1e-05 | alpha_SysJET_21NP_JET_EffectiveNP_6 | 
| Rank 130 | 1e-05 | 0 | alpha_SysVHQCDscaleMbb_ggZH | 
| Rank 129 | 1e-05 | 1e-05 | alpha_SysVHPDFPTV_ggZH | 
| Rank 128 | 1e-05 | 3e-05 | alpha_SysVHQCDscaleMbb | 
| Rank 127 | 3e-05 | 2e-05 | alpha_SysJET_21NP_JET_EffectiveNP_5 | 
| Rank 126 | 4e-05 | 3e-05 | alpha_SysJET_21NP_JET_EffectiveNP_8restTerm | 
| Rank 125 | 6.9e-05 | 4e-05 | alpha_SysMUON_EFF_STAT | 
| Rank 124 | 6e-05 | 5e-05 | alpha_SysWWNorm | 
| Rank 123 | 6.6e-05 | 5e-05 | alpha_SysstoptNorm | 
| Rank 122 | 6.6e-05 | 5e-05 | alpha_SysMUON_EFF_STAT_LOWPT | 
| Rank 121 | 7.2e-05 | 5e-05 | alpha_SysMUON_EFF_SYS_LOWPT | 
| Rank 120 | 7.1e-05 | 6e-05 | alpha_SysEL_EFF_Reco_TOTAL_1NPCOR_PLUS_UNCOR | 
| Rank 119 | 0.000116 | 8e-05 | alpha_SysTheoryPDFAcc_ggZH | 
| Rank 118 | 0.000118 | 9e-05 | alpha_SysTheoryAcc_JVeto_ggZH | 
| Rank 117 | 0.00015 | 6e-05 | alpha_SysVHQCDscalePTV_ggZH | 
| Rank 116 | 0.000151 | 0.00014 | alpha_SysstopsNorm | 
| Rank 115 | 0.000155 | 0.00014 | alpha_SysWblWbbRatio | 
| Rank 114 | 0.00017 | 0.00016 | alpha_SysWlNorm | 
| Rank 113 | 0.000209 | 0.00016 | alpha_SysTheoryAcc_JVeto_qqVH | 
| Rank 112 | 0.00025 | 0.00023 | alpha_SysWclNorm | 
| Rank 111 | 0.000257 | 0.00024 | alpha_SysZlNorm | 
| Rank 110 | 0.000286 | 0.00029 | alpha_SysStoptPTV | 
| Rank 109 | 0.000511 | 0.00016 | alpha_SysVHPDFPTV | 
| Rank 108 | 0.000286 | 0.000436 | alpha_SysEL_EFF_ID_TOTAL_1NPCOR_PLUS_UNCOR | 
| Rank 107 | 0.000696 | 0.000276 | alpha_SysJET_21NP_JET_EffectiveNP_7 | 
| Rank 106 | 0.000637 | 0.000544 | alpha_SysMUON_SAGITTA_RHO | 
| Rank 105 | 0.000576 | 0.00063 | alpha_SysStoptMBB | 
| Rank 104 | 0.00065 | 0.00058 | alpha_SysMUON_ISO_STAT | 
| Rank 103 | 0.000104 | 0.00114 | alpha_SysMUON_MS | 
| Rank 102 | 0.000681 | 0.00066 | alpha_SysFT_EFF_extrapolation_from_charm | 
| Rank 101 | 0.000727 | 0.00074 | alpha_SysZclNorm | 
| Rank 100 | 0.000787 | 0.00071 | alpha_SysTheoryAcc_J3_ggZH | 
| Rank 99 | 0.00079 | 0.00077 | alpha_SysWZUEPSResid_L0 | 
| Rank 98 | 0.000827 | 0.0008 | alpha_SysWbcWbbRatio | 
| Rank 97 | 0.001306 | 0.00034 | alpha_SysFT_EFF_Eigen_B_2 | 
| Rank 96 | 0.000685 | 0.001018 | alpha_SysMUON_SCALE | 
| Rank 95 | 0.000776 | 0.00112 | alpha_SysVZUEPS_J3 | 
| Rank 94 | 0.001062 | 0.00107 | alpha_SysFT_EFF_Eigen_Light_4 | 
| Rank 93 | 0.001004 | 0.00128 | alpha_SysJET_JvtEfficiency | 
| Rank 92 | 0.00046 | 0.00184 | alpha_SysJET_21NP_JET_EtaIntercalibration_TotalStat | 
| Rank 91 | 0.001253 | 0.00125 | alpha_SysVHQCDscalePTV | 
| Rank 90 | 0.001281 | 0.00124 | alpha_SysstoptAcc | 
| Rank 89 | 0.001681 | 0.000906 | alpha_SysMUON_ID | 
| Rank 88 | 0.00138 | 0.0013 | alpha_SysTheoryAcc_J2_ggZH | 
| Rank 87 | 0.001608 | 0.00136 | alpha_SysMET_JetTrk_Scale | 
| Rank 86 | 0.000827 | 0.00216 | alpha_SysFT_EFF_Eigen_Light_0 | 
| Rank 85 | 0.000421 | 0.002608 | alpha_SysJET_21NP_JET_EffectiveNP_4 | 
| Rank 84 | 0.001876 | 0.00117 | alpha_SysVVPTVPSUE | 
| Rank 83 | 0.001379 | 0.00188 | alpha_SysMUON_SAGITTA_RESBIAS | 
| Rank 82 | 0.0027 | 0.00077 | alpha_SysEG_RESOLUTION_ALL | 
| Rank 81 | 0.00093 | 0.00256 | alpha_SysJET_21NP_JET_Pileup_OffsetMu | 
| Rank 80 | 0.001781 | 0.00172 | alpha_SysTheoryQCDscale_qqVH | 
| Rank 79 | 0.002089 | 0.00217 | alpha_SysstopWtNorm | 
| Rank 78 | 0.002342 | 0.00226 | alpha_SysWccWbbRatio | 
| Rank 77 | 0.00243 | 0.00231 | alpha_SysZZUEPSResid_L0 | 
| Rank 76 | 0.001893 | 0.00285 | alpha_SysMET_SoftTrk_ResoPerp | 
| Rank 75 | 0.002388 | 0.00239 | alpha_SysTheoryPDFAcc_qqVH | 
| Rank 74 | 0.002563 | 0.00238 | alpha_SysVVPTVME | 
| Rank 73 | 0.002482 | 0.00248 | alpha_SysTheoryPDF_ggZH | 
| Rank 72 | 0.002708 | 0.0024 | alpha_SysVZUEPSAcc | 
| Rank 71 | 0.002645 | 0.00262 | alpha_SysMUON_ISO_SYS | 
| Rank 70 | 0.002973 | 0.00242 | alpha_SysMUON_EFF_SYS | 
| Rank 69 | 0.002628 | 0.00293 | alpha_SysFT_EFF_Eigen_Light_1 | 
| Rank 68 | 0.002955 | 0.00277 | alpha_SysWZNorm | 
| Rank 67 | 0.003449 | 0.002388 | alpha_SysJET_21NP_JET_EffectiveNP_3 | 
| Rank 66 | 0.003163 | 0.00335 | alpha_SysFT_EFF_Eigen_C_2 | 
| Rank 65 | 0.003182 | 0.0034 | alpha_SysFT_EFF_Eigen_C_0 | 
| Rank 64 | 0.006779 | 0.000182 | alpha_SysJET_21NP_JET_Flavor_Composition_ttbar_L2 | 
| Rank 63 | 0.00368 | 0.0037 | alpha_SysEL_EFF_Iso_TOTAL_1NPCOR_PLUS_UNCOR | 
| Rank 62 | 0.00425 | 0.00351 | alpha_SysJET_JER_SINGLE_NP | 
| Rank 61 | 0.004108 | 0.00419 | alpha_SysVHNLOEWK | 
| Rank 60 | 0.00777 | 0.0006 | alpha_SysJET_21NP_JET_EtaIntercalibration_Modelling | 
| Rank 59 | 0.004613 | 0.00403 | ATLAS_norm_Zbb_J2 | 
| Rank 58 | 0.00794 | 0.00089 | alpha_SysJET_21NP_JET_EffectiveNP_2 | 
| Rank 57 | 0.004861 | 0.00431 | alpha_SysMETTrigTop | 
| Rank 56 | 0.005765 | 0.00357 | alpha_SysZccZbbRatio | 
| Rank 55 | 0.00705 | 0.00245 | alpha_SysEG_SCALE_ALL | 
| Rank 54 | 0.004906 | 0.00517 | alpha_SysMET_SoftTrk_Scale | 
| Rank 53 | 0.003613 | 0.00651 | alpha_SysJET_21NP_JET_Pileup_OffsetNPV | 
| Rank 52 | 0.005134 | 0.00508 | alpha_SysFT_EFF_Eigen_B_0 | 
| Rank 51 | 0.005175 | 0.00522 | alpha_SysMET_SoftTrk_ResoPara | 
| Rank 50 | 0.005192 | 0.00534 | alpha_SysTheoryPDF_qqVH | 
| Rank 49 | 0.005079 | 0.00555 | alpha_SysFT_EFF_Eigen_Light_2 | 
| Rank 48 | 0.005045 | 0.00569 | alpha_SysZbcZbbRatio | 
| Rank 47 | 0.009706 | 0.00111 | alpha_SysJET_21NP_JET_BJES_Response | 
| Rank 46 | 0.005619 | 0.00581 | alpha_SysTTbarPTV | 
| Rank 45 | 0.000384 | 0.011426 | alpha_SysJET_21NP_JET_Flavor_Composition_Top | 
| Rank 44 | 0.005992 | 0.00596 | alpha_SysFT_EFF_extrapolation | 
| Rank 43 | 0.006388 | 0.00626 | alpha_SysVHUEPSPTV | 
| Rank 42 | 0.006357 | 0.00658 | alpha_SysTheoryBRbb | 
| Rank 41 | 0.006619 | 0.00663 | alpha_SysVVMbbME | 
| Rank 40 | 0.007412 | 0.00616 | alpha_SysVZQCDscale_J2 | 
| Rank 39 | 0.007846 | 0.00597 | alpha_SysStopWtPTV | 
| Rank 38 | 0.009128 | 0.00577 | alpha_SysVZQCDscale_J3 | 
| Rank 37 | 0.008268 | 0.00724 | alpha_SysTTbarPTV_L2 | 
| Rank 36 | 0.007531 | 0.00804 | alpha_SysPRW_DATASF | 
| Rank 35 | 0.004216 | 0.01176 | alpha_SysStopWtMBB | 
| Rank 34 | 0.015367 | 0.00126 | alpha_SysJET_21NP_JET_Pileup_PtTerm | 
| Rank 33 | 0.0098 | 0.00694 | alpha_SysWMbb | 
| Rank 32 | 0.008987 | 0.00894 | alpha_SysZblZbbRatio | 
| Rank 31 | 0.010019 | 0.00805 | alpha_SysVZQCDscale_JVeto | 
| Rank 30 | 0.007667 | 0.011318 | alpha_SysJET_21NP_JET_EtaIntercalibration_NonClosure | 
| Rank 29 | 0.012917 | 0.00828 | alpha_SysVHUEPSMbb | 
| Rank 28 | 0.018955 | 0.0032 | alpha_SysJET_21NP_JET_Flavor_Response | 
| Rank 27 | 0.001042 | 0.021801 | alpha_SysJET_21NP_JET_EffectiveNP_1 | 
| Rank 26 | 0.012431 | 0.01187 | alpha_SysTTbarMBB | 
| Rank 25 | 0.012725 | 0.01288 | alpha_SysFT_EFF_Eigen_Light_3 | 
| Rank 24 | 0.014999 | 0.01093 | ATLAS_norm_Zbb_J3 | 
| Rank 23 | 0.000188 | 0.032036 | alpha_SysJET_21NP_JET_Pileup_RhoTopology | 
| Rank 22 | 0.019054 | 0.01453 | alpha_SysTheoryAcc_J3_qqVH | 
| Rank 21 | 0.018244 | 0.01553 | alpha_SysWPtV | 
| Rank 20 | 0.017891 | 0.01739 | alpha_SysZbbNorm_L0 | 
| Rank 19 | 0.018843 | 0.01989 | alpha_SysstopWtAcc | 
| Rank 18 | 0.026211 | 0.01638 | alpha_SysZMbb | 
| Rank 17 | 0.021158 | 0.02179 | alpha_SysttbarNorm_J2 | 
| Rank 16 | 0.021278 | 0.02331 | alpha_SysFT_EFF_Eigen_C_1 | 
| Rank 15 | 0.023272 | 0.02312 | alpha_SysJET_21NP_JET_Flavor_Composition_VV | 
| Rank 14 | 0.024448 | 0.02212 | alpha_SysZZNorm | 
| Rank 13 | 0.025612 | 0.02106 | alpha_SysWbbNorm_J2 | 
| Rank 12 | 0.02293 | 0.02666 | alpha_SysJET_21NP_JET_Flavor_Composition_Vjets | 
| Rank 11 | 0.027865 | 0.02886 | alpha_ATLAS_LUMI_2015_2016 | 
| Rank 10 | 0.028945 | 0.02971 | ATLAS_norm_ttbar_J2_L2_Y | 
| Rank 9 | 0.033185 | 0.02709 | alpha_SysWbbNorm_J3 | 
| Rank 8 | 0.033609 | 0.02724 | ATLAS_norm_ttbar_J3_L2_Y | 
| Rank 7 | 0.033108 | 0.02909 | alpha_SysTheoryUEPSAcc_J3 | 
| Rank 6 | 0.03137 | 0.03103 | alpha_SysZPtV | 
| Rank 5 | 0.032962 | 0.03353 | alpha_SysTheoryAcc_J2_qqVH | 
| Rank 4 | 0.03626 | 0.03313 | alpha_SysTTbarMBB_L2 | 
| Rank 3 | 0.037494 | 0.03977 | alpha_SysTheoryQCDscale_ggZH | 
| Rank 2 | 0.049628 | 0.05083 | alpha_SysFT_EFF_Eigen_B_1 | 
| Rank 1 | 0.104709 | 0.13252 | alpha_SysTheoryUEPSAcc |

 Top range from -0.171923 to 0.198215
 Bottom range from -1.29734 to 1.49574
total unc = 0.323871
sum of sq = 0.192477

{% highlight javascript %}
muhat: 1.00000

nll_val_true: 242104.362926

  Set of nuisance          Impact on error
       parameters          
----------------------------------------------------------
                    Total  +  0.321  -  0.274  +-  0.298
                 DataStat  +  0.160  -  0.157  +-  0.158
                 FullSyst  +  0.278  -  0.225  +-  0.252
  Floating normalizations  +  0.058  -  0.044  +-  0.051
       All normalizations  +  0.070  -  0.058  +-  0.064
   All but normalizations  +  0.264  -  0.208  +-  0.236
                 Jets MET  +  0.049  -  0.035  +-  0.042
                     BTag  +  0.063  -  0.048  +-  0.056
                  Leptons  +  0.004  -  0.003  +-  0.003
               Luminosity  +  0.033  -  0.023  +-  0.028
                  Diboson  +  0.046  -  0.029  +-  0.037
                    Zjets  +  0.049  -  0.042  +-  0.046
                    Wjets  +  0.038  -  0.028  +-  0.033
              Model ttbar  +  0.072  -  0.052  +-  0.062
         Model Single Top  +  0.021  -  0.021  +-  0.021
          Model Multi Jet  +  0.000  -  0.000  +-  0.000
       Signal Systematics  +  0.188  -  0.107  +-  0.148
                  MC stat  +  0.158  -  0.146  +-  0.152
Impact on error quadratically subtracted from total, except for:
DataStat All but normalizations 
----------------------------------------------------------

  Set of nuisance          Fractional impact on error
       parameters          (square of fraction of total)
----------------------------------------------------------
                 DataStat  +  0.25  -  0.33  +- 0.28
                 FullSyst  +  0.75  -  0.67  +- 0.72
  Floating normalizations  +  0.03  -  0.03  +- 0.03
       All normalizations  +  0.05  -  0.04  +- 0.05
   All but normalizations  +  0.68  -  0.57  +- 0.63
                 Jets MET  +  0.02  -  0.02  +- 0.02
                     BTag  +  0.04  -  0.03  +- 0.04
                  Leptons  +  0.00  -  0.00  +- 0.00
               Luminosity  +  0.01  -  0.01  +- 0.01
                  Diboson  +  0.02  -  0.01  +- 0.02
                    Zjets  +  0.02  -  0.02  +- 0.02
                    Wjets  +  0.01  -  0.01  +- 0.01
              Model ttbar  +  0.05  -  0.04  +- 0.04
         Model Single Top  +  0.00  -  0.01  +- 0.01
          Model Multi Jet  +  0.00  -  0.00  +- 0.00
       Signal Systematics  +  0.34  -  0.15  +- 0.25
                  MC stat  +  0.24  -  0.28  +- 0.26
----------------------------------------------------------
{% endhighlight %}

## 0-lepton
### Post-fit impact

* MVA

| Rank      | Impact | Pull | Name |
| --------- | ------ | ---- | ---- |
| Rank 100 | 2e-06 | 2e-06 | alpha_SysJET_21NP_JET_EffectiveNP_8restTerm | 
| Rank 99 | 7e-06 | 7e-06 | alpha_SysVHQCDscaleMbb | 
| Rank 98 | 9e-06 | 7e-06 | alpha_SysZlNorm | 
| Rank 97 | 7e-06 | 9e-06 | alpha_SysVHQCDscaleMbb_ggZH | 
| Rank 96 | 1.4e-05 | 1.7e-05 | alpha_SysFT_EFF_extrapolation_from_charm | 
| Rank 95 | 4e-05 | 3.8e-05 | alpha_SysstopsNorm | 
| Rank 94 | 0.000167 | 2e-05 | alpha_SysMETTrigTop | 
| Rank 93 | 0.00011 | 8.7e-05 | alpha_SysTheoryAcc_JVeto_ggZH | 
| Rank 92 | 0.000147 | 9.7e-05 | alpha_SysTheoryPDFAcc_ggZH | 
| Rank 91 | 0.000244 | 0.000147 | alpha_SysJET_JvtEfficiency | 
| Rank 90 | 0.000234 | 0.000297 | alpha_SysZZUEPSResid_L0 | 
| Rank 89 | 0.000317 | 0.000397 | alpha_SysJET_21NP_JET_Pileup_OffsetMu | 
| Rank 88 | 0.00061 | 0.000257 | alpha_SysZbcZbbRatio | 
| Rank 87 | 0.000392 | 0.000477 | alpha_SysVZUEPSAcc | 
| Rank 86 | 0.000542 | 0.000357 | alpha_SysVVPTVPSUE | 
| Rank 85 | 0.000476 | 0.000487 | alpha_SysWZUEPSResid_L0 | 
| Rank 84 | 0.000426 | 0.000567 | alpha_SysVZQCDscale_J2 | 
| Rank 83 | 0.000684 | 0.000637 | alpha_SysStoptMBB | 
| Rank 82 | 0.000682 | 0.000677 | alpha_SysTheoryAcc_JVeto_qqVH | 
| Rank 81 | 0.000867 | 0.000637 | alpha_SysJET_21NP_JET_EffectiveNP_4 | 
| Rank 80 | 0.000786 | 0.000757 | alpha_SysFT_EFF_Eigen_Light_4 | 
| Rank 79 | 0.001448 | 0.000147 | alpha_SysJET_21NP_JET_EffectiveNP_3 | 
| Rank 78 | 0.001246 | 0.001267 | alpha_SysWccWbbRatio | 
| Rank 77 | 0.000415 | 0.002267 | alpha_SysJET_21NP_JET_EffectiveNP_2 | 
| Rank 76 | 0.001361 | 0.001347 | alpha_SysTheoryAcc_J2_ggZH | 
| Rank 75 | 0.001513 | 0.001277 | alpha_SysJET_21NP_JET_Pileup_OffsetNPV | 
| Rank 74 | 0.001398 | 0.001477 | alpha_SysWZNorm | 
| Rank 73 | 0.001487 | 0.001417 | alpha_SysTheoryAcc_J3_ggZH | 
| Rank 72 | 0.001512 | 0.001487 | alpha_SysStoptPTV | 
| Rank 71 | 0.001553 | 0.001637 | alpha_SysVZUEPS_J3 | 
| Rank 70 | 0.001557 | 0.001667 | alpha_SysMET_SoftTrk_ResoPerp | 
| Rank 69 | 0.000107 | 0.003327 | alpha_SysJET_21NP_JET_Pileup_PtTerm | 
| Rank 68 | 0.001751 | 0.001747 | alpha_SysTheoryQCDscale_qqVH | 
| Rank 67 | 0.001792 | 0.001787 | alpha_SysZclNorm | 
| Rank 66 | 0.00178 | 0.001817 | alpha_SysZccZbbRatio | 
| Rank 65 | 0.001977 | 0.001667 | alpha_SysJET_21NP_JET_EtaIntercalibration_TotalStat | 
| Rank 64 | 0.001867 | 0.001867 | alpha_SysWlNorm | 
| Rank 63 | 0.001948 | 0.001927 | alpha_SysWblWbbRatio | 
| Rank 62 | 0.001982 | 0.001997 | alpha_SysTheoryPDF_ggZH | 
| Rank 61 | 0.004018 | 0.000438 | alpha_SysJET_21NP_JET_EtaIntercalibration_NonClosure | 
| Rank 60 | 0.002359 | 0.002327 | alpha_SysFT_EFF_Eigen_Light_2 | 
| Rank 59 | 0.004737 | 0.000243 | alpha_SysJET_21NP_JET_Flavor_Response | 
| Rank 58 | 0.00314 | 0.002427 | alpha_SysJET_21NP_JET_EffectiveNP_1 | 
| Rank 57 | 0.002832 | 0.002867 | alpha_SysTheoryPDFAcc_qqVH | 
| Rank 56 | 0.002798 | 0.003017 | alpha_SysVZQCDscale_JVeto | 
| Rank 55 | 0.003018 | 0.002977 | alpha_SysWbcWbbRatio | 
| Rank 54 | 0.003199 | 0.003067 | alpha_SysWclNorm | 
| Rank 53 | 0.002708 | 0.00357 | ATLAS_norm_Zbb_J3 | 
| Rank 52 | 0.003103 | 0.003257 | alpha_SysVVPTVME | 
| Rank 51 | 0.003289 | 0.003347 | alpha_SysVHNLOEWK | 
| Rank 50 | 0.003409 | 0.003377 | alpha_SysFT_EFF_extrapolation | 
| Rank 49 | 0.003409 | 0.003567 | alpha_SysVVMbbME | 
| Rank 48 | 0.002963 | 0.004167 | alpha_SysJET_JER_SINGLE_NP | 
| Rank 47 | 0.0037 | 0.003667 | alpha_SysstoptNorm | 
| Rank 46 | 0.003721 | 0.003687 | alpha_SysFT_EFF_Eigen_C_0 | 
| Rank 45 | 0.003294 | 0.004147 | alpha_SysTTbarMBB | 
| Rank 44 | 0.005062 | 0.003447 | alpha_SysZZNorm | 
| Rank 43 | 0.004415 | 0.004257 | alpha_SysVHUEPSPTV | 
| Rank 42 | 0.009244 | 0.000187 | alpha_SysJET_21NP_JET_BJES_Response | 
| Rank 41 | 0.005275 | 0.005417 | alpha_SysTheoryPDF_qqVH | 
| Rank 40 | 0.005854 | 0.005907 | alpha_SysVZQCDscale_J3 | 
| Rank 39 | 0.005979 | 0.005807 | alpha_SysZblZbbRatio | 
| Rank 38 | 0.008338 | 0.004487 | ATLAS_norm_Zbb_J2 | 
| Rank 37 | 0.006326 | 0.006537 | alpha_SysTheoryBRbb | 
| Rank 36 | 0.006515 | 0.006527 | alpha_SysstopWtNorm | 
| Rank 35 | 0.00698 | 0.006687 | alpha_SysFT_EFF_Eigen_B_2 | 
| Rank 34 | 0.007643 | 0.006987 | alpha_SysttbarNorm_J2 | 
| Rank 33 | 0.012955 | 0.004157 | alpha_SysWbbNorm_J2 | 
| Rank 32 | 0.008589 | 0.008717 | alpha_SysFT_EFF_Eigen_C_2 | 
| Rank 31 | 0.018122 | 0.002107 | alpha_SysVHUEPSMbb | 
| Rank 30 | 0.008596 | 0.011647 | alpha_SysMET_SoftTrk_Scale | 
| Rank 29 | 0.010391 | 0.011257 | alpha_SysTTbarPTV | 
| Rank 28 | 0.010088 | 0.012557 | alpha_SysWbbNorm_J3 | 
| Rank 27 | 0.009096 | 0.013947 | alpha_SysJET_21NP_JET_Flavor_Composition_Vjets | 
| Rank 26 | 0.013801 | 0.012837 | alpha_SysWMbb | 
| Rank 25 | 0.01388 | 0.014667 | alpha_SysStopWtPTV | 
| Rank 24 | 0.014433 | 0.014437 | alpha_SysFT_EFF_Eigen_Light_3 | 
| Rank 23 | 0.014662 | 0.016647 | alpha_SysFT_EFF_Eigen_Light_0 | 
| Rank 22 | 0.018031 | 0.015367 | alpha_SysTheoryUEPSAcc_J3 | 
| Rank 21 | 0.000675 | 0.040586 | alpha_SysJET_21NP_JET_Flavor_Composition_Top | 
| Rank 20 | 0.020949 | 0.020507 | alpha_SysFT_EFF_Eigen_Light_1 | 
| Rank 19 | 0.021878 | 0.021917 | alpha_SysMET_SoftTrk_ResoPara | 
| Rank 18 | 0.021423 | 0.022527 | alpha_SysTheoryQCDscale_ggZH | 
| Rank 17 | 0.033616 | 0.025227 | alpha_SysJET_21NP_JET_Flavor_Composition_VV | 
| Rank 16 | 0.030071 | 0.029737 | alpha_SysstoptAcc | 
| Rank 15 | 0.030014 | 0.030417 | alpha_SysPRW_DATASF | 
| Rank 14 | 0.033585 | 0.030827 | alpha_SysJET_21NP_JET_EtaIntercalibration_Modelling | 
| Rank 13 | 0.035097 | 0.032547 | alpha_SysTheoryAcc_J3_qqVH | 
| Rank 12 | 0.035004 | 0.035277 | alpha_ATLAS_LUMI_2015_2016 | 
| Rank 11 | 0.042143 | 0.038837 | alpha_SysStopWtMBB | 
| Rank 10 | 0.043869 | 0.040487 | alpha_SysZMbb | 
| Rank 9 | 0.048377 | 0.037656 | alpha_SysJET_21NP_JET_Pileup_RhoTopology | 
| Rank 8 | 0.043108 | 0.044947 | alpha_SysTheoryAcc_J2_qqVH | 
| Rank 7 | 0.06154 | 0.061517 | alpha_SysFT_EFF_Eigen_C_1 | 
| Rank 6 | 0.064658 | 0.064547 | alpha_SysWPtV | 
| Rank 5 | 0.065098 | 0.067027 | alpha_SysstopWtAcc | 
| Rank 4 | 0.072834 | 0.083147 | alpha_SysZPtV | 
| Rank 3 | 0.089096 | 0.093277 | alpha_SysFT_EFF_Eigen_B_1 | 
| Rank 2 | 0.090722 | 0.111987 | alpha_SysTheoryUEPSAcc | 
| Rank 1 | 0.129722 | 0.124547 | alpha_SysFT_EFF_Eigen_B_0 |

 Top range from -0.222435 to 0.242781
 Bottom range from -1.71471 to 1.87155
total unc = 0.407064
sum of sq = 0.271698


{% highlight javascript %}
muhat: 1.00000

nll_val_true: 29159.476655

  Set of nuisance          Impact on error
       parameters          
----------------------------------------------------------
                    Total  +  0.392  -  0.355  +-  0.373
                 DataStat  +  0.177  -  0.174  +-  0.176
                 FullSyst  +  0.350  -  0.309  +-  0.329
  Floating normalizations  +  0.004  -  0.022  +-  0.013
       All normalizations  +  0.030  -  0.039  +-  0.035
   All but normalizations  +  0.341  -  0.299  +-  0.320
                 Jets MET  +  0.078  -  0.064  +-  0.071
                     BTag  +  0.157  -  0.153  +-  0.155
                  Leptons  +  0.000  -  0.000  +-  0.000
               Luminosity  +  0.036  -  0.021  +-  0.028
                  Diboson  +  0.059  -  0.031  +-  0.045
                    Zjets  +  0.068  -  0.072  +-  0.070
                    Wjets  +  0.063  -  0.059  +-  0.061
              Model ttbar  +  0.022  -  0.022  +-  0.022
         Model Single Top  +  0.092  -  0.088  +-  0.090
          Model Multi Jet  +  0.000  -  0.000  +-  0.000
       Signal Systematics  +  0.188  -  0.090  +-  0.139
                  MC stat  +  0.201  -  0.201  +-  0.201
Impact on error quadratically subtracted from total, except for:
DataStat All but normalizations 
----------------------------------------------------------

  Set of nuisance          Fractional impact on error
       parameters          (square of fraction of total)
----------------------------------------------------------
                 DataStat  +  0.20  -  0.24  +- 0.22
                 FullSyst  +  0.80  -  0.76  +- 0.78
  Floating normalizations  +  0.00  -  0.00  +- 0.00
       All normalizations  +  0.01  -  0.01  +- 0.01
   All but normalizations  +  0.76  -  0.71  +- 0.73
                 Jets MET  +  0.04  -  0.03  +- 0.04
                     BTag  +  0.16  -  0.19  +- 0.17
                  Leptons  +  0.00  -  0.00  +- 0.00
               Luminosity  +  0.01  -  0.00  +- 0.01
                  Diboson  +  0.02  -  0.01  +- 0.01
                    Zjets  +  0.03  -  0.04  +- 0.04
                    Wjets  +  0.03  -  0.03  +- 0.03
              Model ttbar  +  0.00  -  0.00  +- 0.00
         Model Single Top  +  0.06  -  0.06  +- 0.06
          Model Multi Jet  +  0.00  -  0.00  +- 0.00
       Signal Systematics  +  0.23  -  0.06  +- 0.14
                  MC stat  +  0.26  -  0.32  +- 0.29
----------------------------------------------------------
{% endhighlight %}


* Cuts

| Rank      | Impact | Pull | Name |
| --------- | ------ | ---- | ---- |
| Rank 102 | 1e-05 | 1e-05 | alpha_SysVHQCDscaleMbb_ggZH | 
| Rank 101 | 2e-05 | 0 | alpha_SysVHQCDscaleMbb | 
| Rank 100 | 2e-05 | 3e-05 | alpha_SysJET_21NP_JET_EffectiveNP_5 | 
| Rank 99 | 4e-05 | 3e-05 | alpha_SysJET_21NP_JET_EffectiveNP_8restTerm | 
| Rank 98 | 5.1e-05 | 4e-05 | alpha_SysstoptNorm | 
| Rank 97 | 6e-05 | 5e-05 | alpha_SysZclNorm | 
| Rank 96 | 7.6e-05 | 6e-05 | alpha_SysWWNorm | 
| Rank 95 | 0.000121 | 0.0001 | alpha_SysTheoryAcc_JVeto_ggZH | 
| Rank 94 | 0.000122 | 0.0001 | alpha_SysTheoryPDFAcc_ggZH | 
| Rank 93 | 0.000154 | 0.00015 | alpha_SysWlNorm | 
| Rank 92 | 0.000156 | 0.00015 | alpha_SysstopsNorm | 
| Rank 91 | 0.000168 | 0.00014 | alpha_SysWblWbbRatio | 
| Rank 90 | 0.00018 | 0.00017 | alpha_SysStoptPTV | 
| Rank 89 | 0.000227 | 0.00018 | alpha_SysTheoryAcc_JVeto_qqVH | 
| Rank 88 | 0.000438 | 3e-05 | alpha_SysJET_21NP_JET_EtaIntercalibration_TotalStat | 
| Rank 87 | 0.000374 | 0.00027 | alpha_SysFT_EFF_Eigen_C_0 | 
| Rank 86 | 6.7e-05 | 0.00067 | alpha_SysFT_EFF_Eigen_Light_2 | 
| Rank 85 | 0.000607 | 0.00054 | alpha_SysStoptMBB | 
| Rank 84 | 0.000624 | 0.00059 | alpha_SysWclNorm | 
| Rank 83 | 0.00039 | 0.00176 | alpha_SysWbbNorm_J3 | 
| Rank 82 | 0.001112 | 0.00106 | alpha_SysWZUEPSResid_L0 | 
| Rank 81 | 0.001191 | 0.00115 | alpha_SysWbcWbbRatio | 
| Rank 80 | 0.001251 | 0.00122 | alpha_SysFT_EFF_extrapolation_from_charm | 
| Rank 79 | 0.00142 | 0.00125 | alpha_SysVZUEPS_J3 | 
| Rank 78 | 0.001822 | 0.00085 | alpha_SysZbcZbbRatio | 
| Rank 77 | 0.001828 | 0.00096 | alpha_SysTheoryAcc_J3_ggZH | 
| Rank 76 | 0.001587 | 0.00164 | alpha_SysTheoryAcc_J2_ggZH | 
| Rank 75 | 0.001697 | 0.00172 | alpha_SysTheoryPDF_ggZH | 
| Rank 74 | 0.001698 | 0.00174 | alpha_SysTheoryQCDscale_qqVH | 
| Rank 73 | 0.002637 | 0.00088 | alpha_SysJET_21NP_JET_EtaIntercalibration_Modelling | 
| Rank 72 | 0.002019 | 0.00194 | alpha_SysZccZbbRatio | 
| Rank 71 | 0.00213 | 0.001886 | alpha_SysMET_JetTrk_Scale | 
| Rank 70 | 0.001841 | 0.002546 | alpha_SysJET_21NP_JET_EffectiveNP_4 | 
| Rank 69 | 0.002341 | 0.00234 | alpha_SysFT_EFF_Eigen_Light_4 | 
| Rank 68 | 0.002064 | 0.00263 | alpha_SysFT_EFF_Eigen_Light_1 | 
| Rank 67 | 0.002674 | 0.00221 | alpha_SysVVPTVPSUE | 
| Rank 66 | 0.0012 | 0.00402 | alpha_SysJET_21NP_JET_EffectiveNP_3 | 
| Rank 65 | 0.002578 | 0.00265 | alpha_SysstoptAcc | 
| Rank 64 | 0.00221 | 0.00307 | alpha_SysJET_21NP_JET_Pileup_OffsetMu | 
| Rank 63 | 0.002753 | 0.00283 | alpha_SysTheoryPDFAcc_qqVH | 
| Rank 62 | 0.003122 | 0.00303 | alpha_SysWccWbbRatio | 
| Rank 61 | 0.003039 | 0.00313 | alpha_SysVHNLOEWK | 
| Rank 60 | 0.003269 | 0.0036 | alpha_SysJET_JvtEfficiency | 
| Rank 59 | 0.003475 | 0.00357 | alpha_SysstopWtNorm | 
| Rank 58 | 0.005676 | 0.00223 | alpha_SysMET_SoftTrk_Scale | 
| Rank 57 | 0.004176 | 0.00418 | alpha_SysMET_SoftTrk_ResoPara | 
| Rank 56 | 0.004583 | 0.00441 | alpha_SysVVPTVME | 
| Rank 55 | 0.004742 | 0.0045 | alpha_SysZZUEPSResid_L0 | 
| Rank 54 | 0.00472 | 0.00466 | alpha_SysFT_EFF_extrapolation | 
| Rank 53 | 0.004947 | 0.00462 | alpha_SysWZNorm | 
| Rank 52 | 0.004974 | 0.00471 | alpha_SysVZUEPSAcc | 
| Rank 51 | 0.002296 | 0.00752 | alpha_SysWMbb | 
| Rank 50 | 0.005196 | 0.00529 | alpha_SysVVMbbME | 
| Rank 49 | 0.002719 | 0.00804 | alpha_SysJET_21NP_JET_Pileup_OffsetNPV | 
| Rank 48 | 0.005629 | 0.00549 | alpha_SysVHUEPSPTV | 
| Rank 47 | 0.005771 | 0.00596 | alpha_SysFT_EFF_Eigen_C_2 | 
| Rank 46 | 0.006066 | 0.00623 | alpha_SysTheoryPDF_qqVH | 
| Rank 45 | 0.006578 | 0.00715 | alpha_SysFT_EFF_Eigen_Light_0 | 
| Rank 44 | 0.008216 | 0.005944 | alpha_SysJET_21NP_JET_BJES_Response | 
| Rank 43 | 0.007061 | 0.0073 | alpha_SysTheoryBRbb | 
| Rank 42 | 0.008144 | 0.00737 | alpha_SysZblZbbRatio | 
| Rank 41 | 0.008438 | 0.00736 | alpha_SysVZQCDscale_J2 | 
| Rank 40 | 0.009808 | 0.006061 | alpha_SysJET_21NP_JET_EtaIntercalibration_NonClosure | 
| Rank 39 | 0.008126 | 0.00782 | alpha_SysFT_EFF_Eigen_B_2 | 
| Rank 38 | 0.008215 | 0.00837 | alpha_SysFT_EFF_Eigen_Light_3 | 
| Rank 37 | 0.012298 | 0.00824 | alpha_SysVZQCDscale_JVeto | 
| Rank 36 | 0.011049 | 0.01026 | alpha_SysTTbarPTV | 
| Rank 35 | 0.009112 | 0.01351 | alpha_SysJET_JER_SINGLE_NP | 
| Rank 34 | 0.005859 | 0.016798 | alpha_SysJET_21NP_JET_EffectiveNP_2 | 
| Rank 33 | 0.003293 | 0.019393 | alpha_SysJET_21NP_JET_Pileup_PtTerm | 
| Rank 32 | 0.015451 | 0.00836 | alpha_SysVHUEPSMbb | 
| Rank 31 | 0.011295 | 0.01338 | alpha_SysStopWtPTV | 
| Rank 30 | 0.017793 | 0.00753 | alpha_SysVZQCDscale_J3 | 
| Rank 29 | 0.012534 | 0.01384 | alpha_SysZMbb | 
| Rank 28 | 0.013909 | 0.0139 | ATLAS_norm_Zbb_J3 | 
| Rank 27 | 0.013967 | 0.01499 | alpha_SysTheoryQCDscale_ggZH | 
| Rank 26 | 0.014786 | 0.0142 | alpha_SysMET_SoftTrk_ResoPerp | 
| Rank 25 | 0.011263 | 0.0186 | alpha_SysStopWtMBB | 
| Rank 24 | 0.01613 | 0.01484 | alpha_SysMETTrigTop | 
| Rank 23 | 0.018098 | 0.01346 | alpha_SysTheoryUEPSAcc_J3 | 
| Rank 22 | 0.01477 | 0.01701 | alpha_SysFT_EFF_Eigen_B_0 | 
| Rank 21 | 0.018542 | 0.01702 | alpha_SysWPtV | 
| Rank 20 | 0.029045 | 0.0073 | alpha_SysJET_21NP_JET_EffectiveNP_1 | 
| Rank 19 | 0.017876 | 0.02145 | alpha_SysttbarNorm_J2 | 
| Rank 18 | 0.022591 | 0.0169 | alpha_SysJET_21NP_JET_Flavor_Composition_Top | 
| Rank 17 | 0.024273 | 0.015464 | alpha_SysJET_21NP_JET_Flavor_Response | 
| Rank 16 | 0.018277 | 0.02223 | alpha_SysTTbarMBB | 
| Rank 15 | 0.02656 | 0.02739 | alpha_SysJET_21NP_JET_Flavor_Composition_VV | 
| Rank 14 | 0.026353 | 0.0335 | alpha_SysJET_21NP_JET_Flavor_Composition_Vjets | 
| Rank 13 | 0.009941 | 0.05174 | alpha_SysPRW_DATASF | 
| Rank 12 | 0.031119 | 0.03321 | alpha_SysstopWtAcc | 
| Rank 11 | 0.037957 | 0.02937 | alpha_SysTheoryAcc_J3_qqVH | 
| Rank 10 | 0.039961 | 0.03367 | alpha_SysZZNorm | 
| Rank 9 | 0.038019 | 0.03838 | alpha_SysFT_EFF_Eigen_C_1 | 
| Rank 8 | 0.038851 | 0.04082 | alpha_ATLAS_LUMI_2015_2016 | 
| Rank 7 | 0.043208 | 0.04471 | alpha_SysTheoryAcc_J2_qqVH | 
| Rank 6 | 0.07949 | 0.01075 | alpha_SysJET_21NP_JET_Pileup_RhoTopology | 
| Rank 5 | 0.051426 | 0.04598 | ATLAS_norm_Zbb_J2 | 
| Rank 4 | 0.043209 | 0.05587 | alpha_SysZPtV | 
| Rank 3 | 0.064979 | 0.06729 | alpha_SysFT_EFF_Eigen_B_1 | 
| Rank 2 | 0.075201 | 0.07752 | alpha_SysWbbNorm_J2 | 
| Rank 1 | 0.091145 | 0.11274 | alpha_SysTheoryUEPSAcc |

 Top range from -0.232909 to 0.254886
 Bottom range from -2.0659 to 2.26083
total unc = 0.42682
sum of sq = 0.217508

{% highlight javascript %}
muhat: 1.00000

nll_val_true: 28739.017796

  Set of nuisance          Impact on error
       parameters          
----------------------------------------------------------
                    Total  +  0.410  -  0.370  +-  0.390
                 DataStat  +  0.199  -  0.195  +-  0.197
                 FullSyst  +  0.359  -  0.314  +-  0.336
  Floating normalizations  +  0.065  -  0.074  +-  0.070
       All normalizations  +  0.101  -  0.099  +-  0.100
   All but normalizations  +  0.332  -  0.284  +-  0.308
                 Jets MET  +  0.073  -  0.059  +-  0.066
                     BTag  +  0.089  -  0.070  +-  0.079
                  Leptons  +  0.000  -  0.000  +-  0.000
               Luminosity  +  0.039  -  0.024  +-  0.031
                  Diboson  +  0.062  -  0.037  +-  0.050
                    Zjets  +  0.081  -  0.093  +-  0.087
                    Wjets  +  0.078  -  0.078  +-  0.078
              Model ttbar  +  0.036  -  0.032  +-  0.034
         Model Single Top  +  0.040  -  0.038  +-  0.039
          Model Multi Jet  +  0.000  -  0.000  +-  0.000
       Signal Systematics  +  0.188  -  0.085  +-  0.137
                  MC stat  +  0.237  -  0.230  +-  0.234
Impact on error quadratically subtracted from total, except for:
DataStat All but normalizations 
----------------------------------------------------------

  Set of nuisance          Fractional impact on error
       parameters          (square of fraction of total)
----------------------------------------------------------
                 DataStat  +  0.24  -  0.28  +- 0.26
                 FullSyst  +  0.76  -  0.72  +- 0.74
  Floating normalizations  +  0.02  -  0.04  +- 0.03
       All normalizations  +  0.06  -  0.07  +- 0.07
   All but normalizations  +  0.66  -  0.59  +- 0.62
                 Jets MET  +  0.03  -  0.03  +- 0.03
                     BTag  +  0.05  -  0.04  +- 0.04
                  Leptons  +  0.00  -  0.00  +- 0.00
               Luminosity  +  0.01  -  0.00  +- 0.01
                  Diboson  +  0.02  -  0.01  +- 0.02
                    Zjets  +  0.04  -  0.06  +- 0.05
                    Wjets  +  0.04  -  0.05  +- 0.04
              Model ttbar  +  0.01  -  0.01  +- 0.01
         Model Single Top  +  0.01  -  0.01  +- 0.01
          Model Multi Jet  +  0.00  -  0.00  +- 0.00
       Signal Systematics  +  0.21  -  0.05  +- 0.12
                  MC stat  +  0.33  -  0.39  +- 0.36
----------------------------------------------------------
{% endhighlight %}

## 012-leptons
### Pre-fit impact
* MVA
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_012_125_Systs_use1tagFalse_mva_pulls_prefit_125.pdf](quiver-file-url/0685DBD156B907B66478911292FEC80E.pdf)
* Cuts
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_cuts_fullRes_VHbbRun2_13TeV_lumi150scaled_cuts_012_125_Systs_use1tagFalse_mBB_pulls_prefit_125.pdf](quiver-file-url/81C2B93D5ADEAEC83C365E814527CEA3.pdf)
### Post-fit impact
* MVA
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_012_125_Systs_use1tagFalse_mva_pulls_125.pdf](quiver-file-url/A628DA00FE35F4917533DDAE38FEAD1B.pdf)
* Cuts
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_cuts_fullRes_VHbbRun2_13TeV_lumi150scaled_cuts_012_125_Systs_use1tagFalse_mBB_pulls_125.pdf](quiver-file-url/D97DAADC242BD97FC89C8CED2E4E08A2.pdf)

## 0-lepton
### Pre-fit impact
* MVA
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_0_125_Systs_use1tagFalse_mva_pulls_prefit_125.pdf](quiver-file-url/AEA6BCA183B27888B87EF96F82EC787E.pdf)
* Cuts
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_cuts_fullRes_VHbbRun2_13TeV_lumi150scaled_cuts_0_125_Systs_use1tagFalse_mBB_pulls_prefit_125.pdf](quiver-file-url/D9D07986EAE05CED2194FA87298DB3B1.pdf)
### Post-fit impact
* MVA
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_0_125_Systs_use1tagFalse_mva_pulls_125.pdf](quiver-file-url/8ACB7CDD0BD1545847957B5DA3FB972E.pdf)
* Cuts
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_cuts_fullRes_VHbbRun2_13TeV_lumi150scaled_cuts_0_125_Systs_use1tagFalse_mBB_pulls_125.pdf](quiver-file-url/249420C4F7D13350CB68EA751995E452.pdf)

## 1-lepton
### Pre-fit impact
* MVA
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_1_125_Systs_use1tagFalse_mva_pulls_prefit_125.pdf](quiver-file-url/1C43436CD33B83477CFEC81503295C19.pdf)
* Cuts

### Post-fit impact
* MVA
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_1_125_Systs_use1tagFalse_mva_pulls_125.pdf](quiver-file-url/9D5B2C26943BC3E55B494E18272C6766.pdf)
* Cuts

## 2-leptons
### Pre-fit impact
* MVA
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_2_125_Systs_use1tagFalse_mva_pulls_125.pdf](quiver-file-url/F008546E42D9133963A9288957CCCE38.pdf)
* Cuts
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_cuts_fullRes_VHbbRun2_13TeV_lumi150scaled_cuts_2_125_Systs_use1tagFalse_mBB_pulls_prefit_125.pdf](quiver-file-url/15752D824DD6514FBBC22BB6D7E149D2.pdf)
### Pre-fit impact
* MVA
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_2_125_Systs_use1tagFalse_mva_pulls_125.pdf](quiver-file-url/F008546E42D9133963A9288957CCCE38.pdf)
* Cuts
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_cuts_fullRes_VHbbRun2_13TeV_lumi150scaled_cuts_2_125_Systs_use1tagFalse_mBB_pulls_125.pdf](quiver-file-url/0126048484377FE4359236271197E5F7.pdf)

# Update 1 with Marumi's requests

## Ranking of NP with gamma_stat parameters

### 0-lepton Pre-fit impact

{% highlight javascript %}
Rank 130:  	0.008338  	0.004487  	ATLAS_norm_Zbb_J2
Rank 129:  	0.002708  	0.00357  	ATLAS_norm_Zbb_J3
Rank 128:  	2e-06  	2e-06  	alpha_SysJET_21NP_JET_EffectiveNP_8restTerm
Rank 127:  	7e-06  	7e-06  	alpha_SysVHQCDscaleMbb
Rank 126:  	9e-06  	7e-06  	alpha_SysZlNorm
Rank 125:  	7e-06  	9e-06  	alpha_SysVHQCDscaleMbb_ggZH
Rank 124:  	1.4e-05  	1.7e-05  	alpha_SysFT_EFF_extrapolation_from_charm
Rank 123:  	4e-05  	3.8e-05  	alpha_SysstopsNorm
Rank 122:  	0.000167  	2e-05  	alpha_SysMETTrigTop
Rank 121:  	0.00011  	8.7e-05  	alpha_SysTheoryAcc_JVeto_ggZH
Rank 120:  	0.000147  	9.7e-05  	alpha_SysTheoryPDFAcc_ggZH
Rank 119:  	0.000244  	0.000147  	alpha_SysJET_JvtEfficiency
Rank 118:  	0.000234  	0.000297  	alpha_SysZZUEPSResid_L0
Rank 117:  	0.000317  	0.000397  	alpha_SysJET_21NP_JET_Pileup_OffsetMu
Rank 116:  	0.004884  	0.006617  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_7
Rank 115:  	0.000392  	0.000477  	alpha_SysVZUEPSAcc
Rank 114:  	0.000542  	0.000357  	alpha_SysVVPTVPSUE
Rank 113:  	0.000476  	0.000487  	alpha_SysWZUEPSResid_L0
Rank 112:  	0.00061  	0.000257  	alpha_SysZbcZbbRatio
Rank 111:  	0.000426  	0.000567  	alpha_SysVZQCDscale_J2
Rank 110:  	0.000684  	0.000637  	alpha_SysStoptMBB
Rank 109:  	0.000682  	0.000677  	alpha_SysTheoryAcc_JVeto_qqVH
Rank 108:  	0.000867  	0.000637  	alpha_SysJET_21NP_JET_EffectiveNP_4
Rank 107:  	0.000786  	0.000757  	alpha_SysFT_EFF_Eigen_Light_4
Rank 106:  	0.001448  	0.000147  	alpha_SysJET_21NP_JET_EffectiveNP_3
Rank 105:  	0.001246  	0.001267  	alpha_SysWccWbbRatio
Rank 104:  	0.001361  	0.001347  	alpha_SysTheoryAcc_J2_ggZH
Rank 103:  	0.000415  	0.002267  	alpha_SysJET_21NP_JET_EffectiveNP_2
Rank 102:  	0.001513  	0.001277  	alpha_SysJET_21NP_JET_Pileup_OffsetNPV
Rank 101:  	0.001487  	0.001417  	alpha_SysTheoryAcc_J3_ggZH
Rank 100:  	0.001398  	0.001477  	alpha_SysWZNorm
Rank 99:  	0.001512  	0.001487  	alpha_SysStoptPTV
Rank 98:  	0.001553  	0.001637  	alpha_SysVZUEPS_J3
Rank 97:  	0.001557  	0.001667  	alpha_SysMET_SoftTrk_ResoPerp
Rank 96:  	0.046555  	0.065997  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_13
Rank 95:  	0.000107  	0.003327  	alpha_SysJET_21NP_JET_Pileup_PtTerm
Rank 94:  	0.001751  	0.001747  	alpha_SysTheoryQCDscale_qqVH
Rank 93:  	0.001792  	0.001787  	alpha_SysZclNorm
Rank 92:  	0.00178  	0.001817  	alpha_SysZccZbbRatio
Rank 91:  	0.001977  	0.001667  	alpha_SysJET_21NP_JET_EtaIntercalibration_TotalStat
Rank 90:  	0.001867  	0.001867  	alpha_SysWlNorm
Rank 89:  	0.001948  	0.001927  	alpha_SysWblWbbRatio
Rank 88:  	0.001982  	0.001997  	alpha_SysTheoryPDF_ggZH
Rank 87:  	0.004018  	0.000438  	alpha_SysJET_21NP_JET_EtaIntercalibration_NonClosure
Rank 86:  	0.002359  	0.002327  	alpha_SysFT_EFF_Eigen_Light_2
Rank 85:  	0.004737  	0.000243  	alpha_SysJET_21NP_JET_Flavor_Response
Rank 84:  	0.00314  	0.002427  	alpha_SysJET_21NP_JET_EffectiveNP_1
Rank 83:  	0.002832  	0.002867  	alpha_SysTheoryPDFAcc_qqVH
Rank 82:  	0.002798  	0.003017  	alpha_SysVZQCDscale_JVeto
Rank 81:  	0.003018  	0.002977  	alpha_SysWbcWbbRatio
Rank 80:  	0.003199  	0.003067  	alpha_SysWclNorm
Rank 79:  	0.003103  	0.003257  	alpha_SysVVPTVME
Rank 78:  	0.003289  	0.003347  	alpha_SysVHNLOEWK
Rank 77:  	0.003409  	0.003377  	alpha_SysFT_EFF_extrapolation
Rank 76:  	0.003409  	0.003567  	alpha_SysVVMbbME
Rank 75:  	0.0037  	0.003667  	alpha_SysstoptNorm
Rank 74:  	0.003721  	0.003687  	alpha_SysFT_EFF_Eigen_C_0
Rank 73:  	0.002963  	0.004167  	alpha_SysJET_JER_SINGLE_NP
Rank 72:  	0.004415  	0.004257  	alpha_SysVHUEPSPTV
Rank 71:  	0.012955  	0.004157  	alpha_SysWbbNorm_J2
Rank 70:  	0.005062  	0.003447  	alpha_SysZZNorm
Rank 69:  	0.009244  	0.000187  	alpha_SysJET_21NP_JET_BJES_Response
Rank 68:  	0.005275  	0.005417  	alpha_SysTheoryPDF_qqVH
Rank 67:  	0.005979  	0.005807  	alpha_SysZblZbbRatio
Rank 66:  	0.006326  	0.006537  	alpha_SysTheoryBRbb
Rank 65:  	0.006515  	0.006527  	alpha_SysstopWtNorm
Rank 64:  	0.00698  	0.006687  	alpha_SysFT_EFF_Eigen_B_2
Rank 63:  	0.005854  	0.005907  	alpha_SysVZQCDscale_J3
Rank 62:  	0.007643  	0.006987  	alpha_SysttbarNorm_J2
Rank 61:  	0.013247  	0.013017  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_5
Rank 60:  	0.008589  	0.008717  	alpha_SysFT_EFF_Eigen_C_2
Rank 59:  	0.003294  	0.004147  	alpha_SysTTbarMBB
Rank 58:  	0.018122  	0.002107  	alpha_SysVHUEPSMbb
Rank 57:  	0.008596  	0.011647  	alpha_SysMET_SoftTrk_Scale
Rank 56:  	0.010391  	0.011257  	alpha_SysTTbarPTV
Rank 55:  	0.009096  	0.013947  	alpha_SysJET_21NP_JET_Flavor_Composition_Vjets
Rank 54:  	0.013801  	0.012837  	alpha_SysWMbb
Rank 53:  	0.008718  	0.009157  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_6
Rank 52:  	0.005488  	0.005187  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_0
Rank 51:  	0.006145  	0.005797  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_0
Rank 50:  	0.014433  	0.014437  	alpha_SysFT_EFF_Eigen_Light_3
Rank 49:  	0.01388  	0.014667  	alpha_SysStopWtPTV
Rank 48:  	0.014662  	0.016647  	alpha_SysFT_EFF_Eigen_Light_0
Rank 47:  	0.05191  	0.074077  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_12
Rank 46:  	0.018031  	0.015367  	alpha_SysTheoryUEPSAcc_J3
Rank 45:  	0.010088  	0.012557  	alpha_SysWbbNorm_J3
Rank 44:  	0.020949  	0.020507  	alpha_SysFT_EFF_Eigen_Light_1
Rank 43:  	0.021423  	0.022527  	alpha_SysTheoryQCDscale_ggZH
Rank 42:  	0.021878  	0.021917  	alpha_SysMET_SoftTrk_ResoPara
Rank 41:  	0.000675  	0.040586  	alpha_SysJET_21NP_JET_Flavor_Composition_Top
Rank 40:  	0.005528  	0.000401  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_4
Rank 39:  	0.033616  	0.025227  	alpha_SysJET_21NP_JET_Flavor_Composition_VV
Rank 38:  	0.030071  	0.029737  	alpha_SysstoptAcc
Rank 37:  	0.003707  	0.009777  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_11
Rank 36:  	0.011192  	0.013807  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_8
Rank 35:  	0.030014  	0.030417  	alpha_SysPRW_DATASF
Rank 34:  	0.033585  	0.030827  	alpha_SysJET_21NP_JET_EtaIntercalibration_Modelling
Rank 33:  	0.035097  	0.032547  	alpha_SysTheoryAcc_J3_qqVH
Rank 32:  	0.035004  	0.035277  	alpha_ATLAS_LUMI_2015_2016
Rank 31:  	0.000646  	0.000157  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_1
Rank 30:  	0.003597  	0.001137  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_9
Rank 29:  	0.043108  	0.044947  	alpha_SysTheoryAcc_J2_qqVH
Rank 28:  	0.019024  	0.016587  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_2
Rank 27:  	0.048377  	0.037656  	alpha_SysJET_21NP_JET_Pileup_RhoTopology
Rank 26:  	0.042143  	0.038837  	alpha_SysStopWtMBB
Rank 25:  	0.043869  	0.040487  	alpha_SysZMbb
Rank 24:  	0.06154  	0.061517  	alpha_SysFT_EFF_Eigen_C_1
Rank 23:  	0.064658  	0.064547  	alpha_SysWPtV
Rank 22:  	0.065098  	0.067027  	alpha_SysstopWtAcc
Rank 21:  	0.011792  	0.013417  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_5
Rank 20:  	0.031624  	0.031597  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_3
Rank 19:  	0.013708  	0.013757  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_4
Rank 18:  	0.072834  	0.083147  	alpha_SysZPtV
Rank 17:  	0.013108  	0.015177  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_6
Rank 16:  	0.056852  	0.062527  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_10
Rank 15:  	0.024344  	0.026957  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_7
Rank 14:  	0.089096  	0.093277  	alpha_SysFT_EFF_Eigen_B_1
Rank 13:  	0.076149  	0.088137  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_14
Rank 12:  	0.090722  	0.111987  	alpha_SysTheoryUEPSAcc
Rank 11:  	0.049064  	0.051347  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_1
Rank 10:  	0.043542  	0.047587  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_8
Rank 9:  	0.006942  	0.012437  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_10
Rank 8:  	0.054911  	0.060517  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_9
Rank 7:  	0.06351  	0.061517  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_3
Rank 6:  	0.129722  	0.124547  	alpha_SysFT_EFF_Eigen_B_0
Rank 5:  	0.064167  	0.065277  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_2
Rank 4:  	0.092352  	0.098277  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_12
Rank 3:  	0.096283  	0.103797  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_11
Rank 2:  	0.11141  	0.113857  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_13
Rank 1:  	0.096015  	0.105247  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_14

 Top range from -0.222435 to 0.242781
 Bottom range from -1.71471 to 1.87155
total unc = 0.407064
sum of sq = 0.399777
{% endhighlight %}

![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_0_125_Systs_use1tagFalse_mva_pulls_prefit_125.pdf](quiver-file-url/A057B7D3F948768BBEF064D16868C72A.pdf)

### 0-lepton Post-fit impact

{% highlight javascript %}
Rank 130:  	2e-06  	2e-06  	alpha_SysJET_21NP_JET_EffectiveNP_8restTerm
Rank 129:  	7e-06  	7e-06  	alpha_SysVHQCDscaleMbb
Rank 128:  	9e-06  	7e-06  	alpha_SysZlNorm
Rank 127:  	7e-06  	9e-06  	alpha_SysVHQCDscaleMbb_ggZH
Rank 126:  	1.4e-05  	1.7e-05  	alpha_SysFT_EFF_extrapolation_from_charm
Rank 125:  	4e-05  	3.8e-05  	alpha_SysstopsNorm
Rank 124:  	0.000167  	2e-05  	alpha_SysMETTrigTop
Rank 123:  	0.00011  	8.7e-05  	alpha_SysTheoryAcc_JVeto_ggZH
Rank 122:  	0.000147  	9.7e-05  	alpha_SysTheoryPDFAcc_ggZH
Rank 121:  	0.000244  	0.000147  	alpha_SysJET_JvtEfficiency
Rank 120:  	0.000234  	0.000297  	alpha_SysZZUEPSResid_L0
Rank 119:  	0.000317  	0.000397  	alpha_SysJET_21NP_JET_Pileup_OffsetMu
Rank 118:  	0.000646  	0.000157  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_1
Rank 117:  	0.00061  	0.000257  	alpha_SysZbcZbbRatio
Rank 116:  	0.000392  	0.000477  	alpha_SysVZUEPSAcc
Rank 115:  	0.000542  	0.000357  	alpha_SysVVPTVPSUE
Rank 114:  	0.000476  	0.000487  	alpha_SysWZUEPSResid_L0
Rank 113:  	0.000426  	0.000567  	alpha_SysVZQCDscale_J2
Rank 112:  	0.000684  	0.000637  	alpha_SysStoptMBB
Rank 111:  	0.000682  	0.000677  	alpha_SysTheoryAcc_JVeto_qqVH
Rank 110:  	0.000867  	0.000637  	alpha_SysJET_21NP_JET_EffectiveNP_4
Rank 109:  	0.000786  	0.000757  	alpha_SysFT_EFF_Eigen_Light_4
Rank 108:  	0.001448  	0.000147  	alpha_SysJET_21NP_JET_EffectiveNP_3
Rank 107:  	0.001246  	0.001267  	alpha_SysWccWbbRatio
Rank 106:  	0.000415  	0.002267  	alpha_SysJET_21NP_JET_EffectiveNP_2
Rank 105:  	0.001361  	0.001347  	alpha_SysTheoryAcc_J2_ggZH
Rank 104:  	0.001513  	0.001277  	alpha_SysJET_21NP_JET_Pileup_OffsetNPV
Rank 103:  	0.001398  	0.001477  	alpha_SysWZNorm
Rank 102:  	0.001487  	0.001417  	alpha_SysTheoryAcc_J3_ggZH
Rank 101:  	0.001512  	0.001487  	alpha_SysStoptPTV
Rank 100:  	0.001553  	0.001637  	alpha_SysVZUEPS_J3
Rank 99:  	0.001557  	0.001667  	alpha_SysMET_SoftTrk_ResoPerp
Rank 98:  	0.000107  	0.003327  	alpha_SysJET_21NP_JET_Pileup_PtTerm
Rank 97:  	0.001751  	0.001747  	alpha_SysTheoryQCDscale_qqVH
Rank 96:  	0.001792  	0.001787  	alpha_SysZclNorm
Rank 95:  	0.00178  	0.001817  	alpha_SysZccZbbRatio
Rank 94:  	0.001977  	0.001667  	alpha_SysJET_21NP_JET_EtaIntercalibration_TotalStat
Rank 93:  	0.001867  	0.001867  	alpha_SysWlNorm
Rank 92:  	0.001948  	0.001927  	alpha_SysWblWbbRatio
Rank 91:  	0.001982  	0.001997  	alpha_SysTheoryPDF_ggZH
Rank 90:  	0.004018  	0.000438  	alpha_SysJET_21NP_JET_EtaIntercalibration_NonClosure
Rank 89:  	0.002359  	0.002327  	alpha_SysFT_EFF_Eigen_Light_2
Rank 88:  	0.003597  	0.001137  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_9
Rank 87:  	0.004737  	0.000243  	alpha_SysJET_21NP_JET_Flavor_Response
Rank 86:  	0.00314  	0.002427  	alpha_SysJET_21NP_JET_EffectiveNP_1
Rank 85:  	0.002832  	0.002867  	alpha_SysTheoryPDFAcc_qqVH
Rank 84:  	0.002798  	0.003017  	alpha_SysVZQCDscale_JVeto
Rank 83:  	0.005528  	0.000401  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_4
Rank 82:  	0.003018  	0.002977  	alpha_SysWbcWbbRatio
Rank 81:  	0.003199  	0.003067  	alpha_SysWclNorm
Rank 80:  	0.002708  	0.00357  	ATLAS_norm_Zbb_J3
Rank 79:  	0.003103  	0.003257  	alpha_SysVVPTVME
Rank 78:  	0.003289  	0.003347  	alpha_SysVHNLOEWK
Rank 77:  	0.003409  	0.003377  	alpha_SysFT_EFF_extrapolation
Rank 76:  	0.003409  	0.003567  	alpha_SysVVMbbME
Rank 75:  	0.002963  	0.004167  	alpha_SysJET_JER_SINGLE_NP
Rank 74:  	0.0037  	0.003667  	alpha_SysstoptNorm
Rank 73:  	0.003721  	0.003687  	alpha_SysFT_EFF_Eigen_C_0
Rank 72:  	0.003294  	0.004147  	alpha_SysTTbarMBB
Rank 71:  	0.005062  	0.003447  	alpha_SysZZNorm
Rank 70:  	0.004415  	0.004257  	alpha_SysVHUEPSPTV
Rank 69:  	0.009244  	0.000187  	alpha_SysJET_21NP_JET_BJES_Response
Rank 68:  	0.005488  	0.005187  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_0
Rank 67:  	0.005275  	0.005417  	alpha_SysTheoryPDF_qqVH
Rank 66:  	0.004884  	0.006617  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_7
Rank 65:  	0.005854  	0.005907  	alpha_SysVZQCDscale_J3
Rank 64:  	0.005979  	0.005807  	alpha_SysZblZbbRatio
Rank 63:  	0.006145  	0.005797  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_0
Rank 62:  	0.008338  	0.004487  	ATLAS_norm_Zbb_J2
Rank 61:  	0.006326  	0.006537  	alpha_SysTheoryBRbb
Rank 60:  	0.006515  	0.006527  	alpha_SysstopWtNorm
Rank 59:  	0.003707  	0.009777  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_11
Rank 58:  	0.00698  	0.006687  	alpha_SysFT_EFF_Eigen_B_2
Rank 57:  	0.007643  	0.006987  	alpha_SysttbarNorm_J2
Rank 56:  	0.012955  	0.004157  	alpha_SysWbbNorm_J2
Rank 55:  	0.008589  	0.008717  	alpha_SysFT_EFF_Eigen_C_2
Rank 54:  	0.008718  	0.009157  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_6
Rank 53:  	0.006942  	0.012437  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_10
Rank 52:  	0.018122  	0.002107  	alpha_SysVHUEPSMbb
Rank 51:  	0.008596  	0.011647  	alpha_SysMET_SoftTrk_Scale
Rank 50:  	0.010391  	0.011257  	alpha_SysTTbarPTV
Rank 49:  	0.010088  	0.012557  	alpha_SysWbbNorm_J3
Rank 48:  	0.009096  	0.013947  	alpha_SysJET_21NP_JET_Flavor_Composition_Vjets
Rank 47:  	0.011192  	0.013807  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_8
Rank 46:  	0.011792  	0.013417  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_5
Rank 45:  	0.013247  	0.013017  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_5
Rank 44:  	0.013801  	0.012837  	alpha_SysWMbb
Rank 43:  	0.013708  	0.013757  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_4
Rank 42:  	0.013108  	0.015177  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_6
Rank 41:  	0.01388  	0.014667  	alpha_SysStopWtPTV
Rank 40:  	0.014433  	0.014437  	alpha_SysFT_EFF_Eigen_Light_3
Rank 39:  	0.014662  	0.016647  	alpha_SysFT_EFF_Eigen_Light_0
Rank 38:  	0.018031  	0.015367  	alpha_SysTheoryUEPSAcc_J3
Rank 37:  	0.019024  	0.016587  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_2
Rank 36:  	0.000675  	0.040586  	alpha_SysJET_21NP_JET_Flavor_Composition_Top
Rank 35:  	0.020949  	0.020507  	alpha_SysFT_EFF_Eigen_Light_1
Rank 34:  	0.021878  	0.021917  	alpha_SysMET_SoftTrk_ResoPara
Rank 33:  	0.021423  	0.022527  	alpha_SysTheoryQCDscale_ggZH
Rank 32:  	0.024344  	0.026957  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_7
Rank 31:  	0.033616  	0.025227  	alpha_SysJET_21NP_JET_Flavor_Composition_VV
Rank 30:  	0.030071  	0.029737  	alpha_SysstoptAcc
Rank 29:  	0.030014  	0.030417  	alpha_SysPRW_DATASF
Rank 28:  	0.031624  	0.031597  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_3
Rank 27:  	0.033585  	0.030827  	alpha_SysJET_21NP_JET_EtaIntercalibration_Modelling
Rank 26:  	0.035097  	0.032547  	alpha_SysTheoryAcc_J3_qqVH
Rank 25:  	0.035004  	0.035277  	alpha_ATLAS_LUMI_2015_2016
Rank 24:  	0.042143  	0.038837  	alpha_SysStopWtMBB
Rank 23:  	0.043869  	0.040487  	alpha_SysZMbb
Rank 22:  	0.048377  	0.037656  	alpha_SysJET_21NP_JET_Pileup_RhoTopology
Rank 21:  	0.043108  	0.044947  	alpha_SysTheoryAcc_J2_qqVH
Rank 20:  	0.043542  	0.047587  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_8
Rank 19:  	0.049064  	0.051347  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_1
Rank 18:  	0.046555  	0.065997  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_13
Rank 17:  	0.054911  	0.060517  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_9
Rank 16:  	0.056852  	0.062527  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_10
Rank 15:  	0.06154  	0.061517  	alpha_SysFT_EFF_Eigen_C_1
Rank 14:  	0.06351  	0.061517  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_3
Rank 13:  	0.05191  	0.074077  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_12
Rank 12:  	0.064658  	0.064547  	alpha_SysWPtV
Rank 11:  	0.064167  	0.065277  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_2
Rank 10:  	0.065098  	0.067027  	alpha_SysstopWtAcc
Rank 9:  	0.072834  	0.083147  	alpha_SysZPtV
Rank 8:  	0.076149  	0.088137  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_14
Rank 7:  	0.089096  	0.093277  	alpha_SysFT_EFF_Eigen_B_1
Rank 6:  	0.092352  	0.098277  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_12
Rank 5:  	0.096283  	0.103797  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_11
Rank 4:  	0.096015  	0.105247  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_14
Rank 3:  	0.090722  	0.111987  	alpha_SysTheoryUEPSAcc
Rank 2:  	0.11141  	0.113857  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_13
Rank 1:  	0.129722  	0.124547  	alpha_SysFT_EFF_Eigen_B_0

 Top range from -0.222435 to 0.242781
 Bottom range from -1.71471 to 1.87155
total unc = 0.407064
sum of sq = 0.399777
{% endhighlight %}

![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_0_125_Systs_use1tagFalse_mva_pulls_125.pdf](quiver-file-url/52015AF45B267023D40E55093D5FD120.pdf)

## 012 Pre-fit impact
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_012_125_Systs_use1tagFalse_mva_pulls_prefit_125.pdf](quiver-file-url/012A87AFCB26E26D91B5934981390B1C.pdf)

{% highlight javascript %}
Rank 286:  	0  	0  	alpha_SysJET_21NP_JET_EffectiveNP_8restTerm
Rank 285:  	0  	0  	alpha_SysJET_21NP_JET_EffectiveNP_6
Rank 284:  	0.013718  	0.004919  	ATLAS_norm_Wbb_J2
Rank 283:  	0.0227  	0.00054  	ATLAS_norm_Zbb_J2
Rank 282:  	0.027383  	0.0158  	ATLAS_norm_Wbb_J3
Rank 281:  	0  	0  	alpha_SysMUON_MS
Rank 280:  	0.022719  	0.00771  	ATLAS_norm_Zbb_J3
Rank 279:  	0.016504  	0.00402  	ATLAS_norm_ttbar_J3_L2_Y
Rank 278:  	0  	0  	alpha_SysMUON_EFF_TrigSystUncertainty
Rank 277:  	0  	0  	alpha_SysVHQCDscaleMbb_ggZH
Rank 276:  	0  	0  	alpha_SysVHQCDscaleMbb
Rank 275:  	0  	0  	alpha_SysEL_EFF_Trigger_TOTAL_1NPCOR_PLUS_UNCOR
Rank 274:  	0.015465  	0.01432  	ATLAS_norm_ttbar_J2_L2_Y
Rank 273:  	0  	0  	alpha_SysJET_21NP_JET_EffectiveNP_7
Rank 272:  	0  	0  	alpha_SysMUON_SCALE
Rank 271:  	0  	0  	alpha_SysMUON_SAGITTA_RESBIAS
Rank 270:  	0  	0  	alpha_SysVHPDFPTV_ggZH
Rank 269:  	1e-05  	1e-05  	alpha_SysZZUEPSResid_L0
Rank 268:  	2e-05  	1e-05  	alpha_SysMUON_EFF_SYS_LOWPT
Rank 267:  	2e-05  	1e-05  	alpha_SysMUON_EFF_STAT_LOWPT
Rank 266:  	3e-05  	3e-05  	alpha_SysVHPDFPTV
Rank 265:  	3e-05  	3e-05  	alpha_SysVHQCDscalePTV_ggZH
Rank 264:  	0.001467  	0.00163  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_7
Rank 263:  	2e-05  	8e-05  	alpha_SysJET_21NP_JET_EffectiveNP_5
Rank 262:  	8e-05  	5e-05  	alpha_SysMUON_EFF_STAT
Rank 261:  	8e-05  	8e-05  	alpha_SysMJTrigger_multijetEl
Rank 260:  	0.00013  	4e-05  	alpha_SysTheoryPDFAcc_ggZH
Rank 259:  	0.000149  	3e-05  	alpha_SysTheoryAcc_JVeto_ggZH
Rank 258:  	0.00012  	7e-05  	alpha_SysFT_EFF_Eigen_Light_4
Rank 257:  	0.00012  	9e-05  	alpha_SysEL_EFF_Reco_TOTAL_1NPCOR_PLUS_UNCOR
Rank 256:  	5e-05  	0.00016  	alpha_SysMUON_ID
Rank 255:  	0.00028  	0  	alpha_SysStoptPTV
Rank 254:  	0.013095  	0.01631  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_11
Rank 253:  	0.000192  	0.00013  	alpha_SysTheoryAcc_J3_ggZH
Rank 252:  	0.000227  	0.0002  	alpha_SysWZUEPSResid_L0
Rank 251:  	0.00021  	0.00026  	alpha_SysJET_21NP_JET_EffectiveNP_4
Rank 250:  	0.003904  	0.00391  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_4
Rank 249:  	0.009046  	0.00999  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_8
Rank 248:  	0.000479  	0.0001  	alpha_SysJET_21NP_JET_EtaIntercalibration_TotalStat
Rank 247:  	0.0005  	0.00022  	alpha_SysFT_EFF_extrapolation
Rank 246:  	0.001108  	0.00129  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_6
Rank 245:  	0.000649  	0.0007  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_3
Rank 244:  	0.00044  	0.0004  	alpha_SysZlNorm
Rank 243:  	0.000464  	0.00038  	alpha_SysVVPTVPSUE
Rank 242:  	0.000455  	0.00045  	alpha_SysVZUEPS_J3
Rank 241:  	0.000574  	0.00036  	alpha_SysVHQCDscalePTV
Rank 240:  	0.000606  	0.00042  	alpha_SysTheoryAcc_JVeto_qqVH
Rank 239:  	0.001146  	0.00107  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_5
Rank 238:  	0.000631  	0.00049  	alpha_SysMJWOCorrection_multijetEl
Rank 237:  	0.000574  	0.00058  	alpha_SysMUON_ISO_STAT
Rank 236:  	0.000685  	0.00053  	alpha_SysZccZbbRatio
Rank 235:  	0.000407  	0.000841  	alpha_SysEG_RESOLUTION_ALL
Rank 234:  	0.002601  	0.0064  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_11
Rank 233:  	0.000667  	0.00062  	alpha_SysstopsNorm
Rank 232:  	0.000639  	0.00064  	alpha_SysVZUEPSAcc
Rank 231:  	0.000814  	0.00054  	alpha_SysWbbNorm_L0
Rank 230:  	0.000428  	0.00053  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_9
Rank 229:  	0.000605  	0.00191  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_10
Rank 228:  	0.000817  	0.00077  	alpha_SysMJSFsCR_multijetEl
Rank 227:  	0.00073  	0.001  	alpha_SysTheoryAcc_J2_ggZH
Rank 226:  	0.000929  	0.00088  	alpha_SysWlNorm
Rank 225:  	0.000788  	0.00101  	alpha_SysJET_JvtEfficiency
Rank 224:  	0.000834  	0.00108  	alpha_SysJET_21NP_JET_Flavor_Composition_ttbar_L2
Rank 223:  	0.00115  	0.00114  	alpha_SysMUON_ISO_SYS
Rank 222:  	0.000645  	0.00072  	alpha_SysMET_SoftTrk_ResoPerp
Rank 221:  	0.006088  	0.00629  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_5
Rank 220:  	0.001325  	0.00137  	alpha_SysVVPTVME
Rank 219:  	0.001371  	0.00133  	alpha_SysEL_EFF_Iso_TOTAL_1NPCOR_PLUS_UNCOR
Rank 218:  	0.001504  	0.0013  	alpha_SysVVMbbME
Rank 217:  	0.000759  	0.0003  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_1
Rank 216:  	0.001632  	0.00145  	alpha_SysVZQCDscale_J2
Rank 215:  	0.00025  	0.00315  	alpha_SysJET_21NP_JET_Pileup_OffsetMu
Rank 214:  	0.00176  	0.00173  	alpha_SysMJReduced_multijetMu
Rank 213:  	0.00177  	0.00166  	alpha_SysWblWbbRatio
Rank 212:  	0.001965  	0.0015  	alpha_SysttbarNorm_DWhfCR_L1
Rank 211:  	0.001823  	0.00179  	alpha_SysTheoryQCDscale_qqVH
Rank 210:  	0.002735  	0.00257  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_3
Rank 209:  	0.001849  	0.00183  	alpha_SysTheoryPDF_ggZH
Rank 208:  	0.001409  	0.00186  	alpha_SysJET_21NP_JET_EtaIntercalibration_NonClosure
Rank 207:  	0.002314  	0.00177  	alpha_SysMJNorm_2J_Mu
Rank 206:  	0.000925  	0.00074  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_1
Rank 205:  	0.002071  	0.00191  	alpha_SysZclNorm
Rank 204:  	0.002404  	0.00218  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_2
Rank 203:  	0.002051  	0.00188  	alpha_SysMETTrigTop
Rank 202:  	0.00083  	5e-05  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_6
Rank 201:  	0.002016  	0.002  	alpha_SysFT_EFF_extrapolation_from_charm
Rank 200:  	0.002242  	0.00215  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_4
Rank 199:  	0.00211  	0.00183  	alpha_SysVZQCDscale_JVeto
Rank 198:  	0.00012  	5e-05  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_4
Rank 197:  	0.002396  	0.00219  	alpha_SysFT_EFF_Eigen_Light_2
Rank 196:  	0.002547  	0.00252  	alpha_SysTheoryPDFAcc_qqVH
Rank 195:  	0.002347  	0.00199  	alpha_SysZbcZbbRatio
Rank 194:  	0.002492  	0.00279  	alpha_SysMJReduced_multijetEl
Rank 193:  	0.003364  	0.00284  	alpha_SysVZQCDscale_J3
Rank 192:  	0.000675  	8e-05  	alpha_SysZZNorm
Rank 191:  	0.003157  	0.00245  	alpha_SysMUON_EFF_SYS
Rank 190:  	0.003994  	0.00338  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_7
Rank 189:  	0.0059  	0.00561  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_1
Rank 188:  	0.00169  	0.00125  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_0
Rank 187:  	0.003408  	0.00293  	alpha_SysStoptMBB
Rank 186:  	0.000629  	0.00055  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_4
Rank 185:  	0.006716  	0.00692  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_6
Rank 184:  	0.00508  	0.00765  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_12
Rank 183:  	0.003932  	0.00382  	alpha_SysVHUEPSPTV
Rank 182:  	0.003582  	0.00337  	alpha_SysWZNorm
Rank 181:  	0.003679  	0.00354  	alpha_SysWclNorm
Rank 180:  	0.004125  	0.00421  	alpha_SysVHNLOEWK
Rank 179:  	0.00058  	0.0072  	alpha_SysMJNorm_3J_El
Rank 178:  	0.005856  	0.00483  	alpha_SysttbarNorm_J2
Rank 177:  	0.000438  	0.00054  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_6
Rank 176:  	0.000825  	0.00092  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_5
Rank 175:  	0.001214  	0.00113  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_4
Rank 174:  	0.004471  	0.00427  	alpha_SysstoptNorm
Rank 173:  	0.001469  	2e-05  	alpha_SysZbbNorm_L0
Rank 172:  	0.003299  	0.00314  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_4
Rank 171:  	0.004479  	0.00543  	alpha_SysWbbNorm_DWhfSR
Rank 170:  	0.000924  	0.00083  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_2
Rank 169:  	0.005235  	0.00424  	alpha_SysMJ2Tag_multijetMu
Rank 168:  	0.005097  	0.00524  	alpha_SysTheoryPDF_qqVH
Rank 167:  	0.008559  	0.01032  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_9
Rank 166:  	0.003904  	0.00332  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_2
Rank 165:  	0.001193  	0.00136  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_7
Rank 164:  	0.004617  	0.00513  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_12
Rank 163:  	0.005571  	0.00451  	alpha_SysJET_21NP_JET_Pileup_PtTerm
Rank 162:  	0.00571  	0.00591  	alpha_SysTheoryBRbb
Rank 161:  	0.00902  	0.003  	alpha_SysVHUEPSMbb
Rank 160:  	0.006815  	0.00633  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_8
Rank 159:  	0.003554  	0.00563  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_7
Rank 158:  	0.007209  	0.00869  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_13
Rank 157:  	0.005803  	0.00568  	alpha_SysZblZbbRatio
Rank 156:  	0.003865  	0.00476  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_7
Rank 155:  	0.002542  	0.00244  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_1
Rank 154:  	0.006179  	0.00615  	alpha_SysFT_EFF_Eigen_C_2
Rank 153:  	0.005854  	0.00551  	alpha_SysMJ2Tag_multijetEl
Rank 152:  	0.009289  	0.0117  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_9
Rank 151:  	0.005024  	0.00479  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_5
Rank 150:  	0.017262  	0.02792  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_14
Rank 149:  	0.010624  	0.002832  	alpha_SysJET_21NP_JET_Pileup_OffsetNPV
Rank 148:  	0.002411  	0.00276  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_11
Rank 147:  	0.006434  	0.0063  	alpha_SysMJNorm_2J_El
Rank 146:  	0.007034  	0.00711  	alpha_SysstopWtNorm
Rank 145:  	0.007264  	0.00685  	alpha_SysEL_EFF_ID_TOTAL_1NPCOR_PLUS_UNCOR
Rank 144:  	0.010489  	0.00758  	alpha_SysJET_21NP_JET_Flavor_Composition_Top
Rank 143:  	0.00309  	0.00136  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_8
Rank 142:  	0.007706  	0.00752  	alpha_SysWccWbbRatio
Rank 141:  	0.00756  	0.0072  	alpha_SysFT_EFF_Eigen_B_2
Rank 140:  	0.004472  	0.00404  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_1
Rank 139:  	0.00247  	0.00049  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_9
Rank 138:  	0.00182  	0.007704  	alpha_SysPRW_DATASF
Rank 137:  	8e-05  	0.00017  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_0
Rank 136:  	0.000238  	3e-05  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_5
Rank 135:  	0.005413  	0.01051  	alpha_SysMJNorm_3J_Mu
Rank 134:  	6e-05  	7e-05  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_3
Rank 133:  	0.015146  	0.002174  	alpha_SysJET_21NP_JET_EffectiveNP_1
Rank 132:  	0.006399  	0.00837  	alpha_SysJET_21NP_JET_BJES_Response
Rank 131:  	0.003347  	0.00347  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_10
Rank 130:  	0.003974  	0.00381  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_3
Rank 129:  	0.00479  	0.00346  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_0
Rank 128:  	0.020652  	0.02527  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_10
Rank 127:  	0.004085  	0.00207  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_0
Rank 126:  	0.002854  	0.00273  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_0
Rank 125:  	0.004727  	0.00508  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_9
Rank 124:  	0.009718  	0.00982  	alpha_SysEG_SCALE_ALL
Rank 123:  	0.014179  	0.00585  	alpha_SysJET_21NP_JET_EffectiveNP_2
Rank 122:  	0.001817  	0.00191  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_8
Rank 121:  	0.001195  	0.00093  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_0
Rank 120:  	0.010228  	0.01155  	alpha_SysJET_21NP_JET_EffectiveNP_3
Rank 119:  	0.000303  	0.00022  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_2
Rank 118:  	0.010789  	0.01573  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_12
Rank 117:  	0.002719  	0.00282  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_9
Rank 116:  	0.011459  	0.01098  	alpha_SysWbcWbbRatio
Rank 115:  	0.011164  	0.01092  	alpha_SysTTbarPTV
Rank 114:  	0.023553  	0.02979  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_13
Rank 113:  	0.000921  	9e-05  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_5
Rank 112:  	0.00012  	0.00047  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_10
Rank 111:  	0.000459  	0.00037  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_1
Rank 110:  	0.001326  	0.00157  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfCR_bin_0
Rank 109:  	0.009998  	0.0054  	alpha_SysWMbb
Rank 108:  	0.012338  	0.0137  	alpha_SysJET_21NP_JET_Flavor_Response
Rank 107:  	0.001986  	0.00199  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_4
Rank 106:  	0.009507  	0.01048  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_14
Rank 105:  	0.002694  	0.00383  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_5
Rank 104:  	0.003604  	0.00269  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_5
Rank 103:  	0.010701  	0.00673  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_1
Rank 102:  	0.000873  	0.00088  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_8
Rank 101:  	0.008988  	0.01021  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_8
Rank 100:  	0.011411  	0.01448  	alpha_SysMET_SoftTrk_Scale
Rank 99:  	0.014675  	0.01427  	alpha_SysFT_EFF_Eigen_C_0
Rank 98:  	0.014295  	0.01406  	alpha_SysFT_EFF_Eigen_Light_3
Rank 97:  	0.004736  	0.00551  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_6
Rank 96:  	0.005469  	0.00588  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_10
Rank 95:  	0.003716  	0.0041  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_5
Rank 94:  	0.017716  	0.02008  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_13
Rank 93:  	0.002855  	0.00228  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_0
Rank 92:  	0.014392  	0.01477  	alpha_SysMET_SoftTrk_ResoPara
Rank 91:  	0.008818  	0.00885  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_2
Rank 90:  	0.001539  	0.00145  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_4
Rank 89:  	0.000734  	0.00098  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_6
Rank 88:  	0.003252  	0.00135  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_0
Rank 87:  	0.020277  	0.007781  	alpha_SysJET_21NP_JET_Flavor_Composition_Vjets
Rank 86:  	0.00242  	0.00235  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_1
Rank 85:  	0.003866  	0.00388  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_4
Rank 84:  	0.024372  	0.00513  	alpha_SysJET_21NP_JET_EtaIntercalibration_Modelling
Rank 83:  	0.015888  	0.01102  	alpha_SysttbarNorm_L0
Rank 82:  	0.017902  	0.01817  	alpha_SysstoptAcc
Rank 81:  	0.005961  	0.0067  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_11
Rank 80:  	0.007376  	0.00725  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_3
Rank 79:  	0.006002  	0.00641  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_11
Rank 78:  	0.004928  	0.00484  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_1
Rank 77:  	0.020187  	0.006604  	alpha_SysJET_21NP_JET_Pileup_RhoTopology
Rank 76:  	0.011744  	0.00588  	alpha_SysZPtV
Rank 75:  	0.017256  	0.02771  	alpha_ATLAS_LUMI_2015_2016
Rank 74:  	0.026207  	0.0291  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_12
Rank 73:  	0.003697  	0.00364  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_3
Rank 72:  	0.00984  	0.00826  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfCR_bin_0
Rank 71:  	2e-05  	9e-05  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_5
Rank 70:  	0.005364  	0.00742  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_12
Rank 69:  	0.005058  	0.00451  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_6
Rank 68:  	0.0191  	0.02451  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_11
Rank 67:  	0.018248  	0.01953  	alpha_SysStopWtPTV
Rank 66:  	0.006813  	0.00741  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_12
Rank 65:  	0.021294  	0.01991  	alpha_SysFT_EFF_Eigen_Light_1
Rank 64:  	0.011294  	0.01254  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_7
Rank 63:  	0.007785  	0.00745  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_3
Rank 62:  	0.020819  	0.0244  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_14
Rank 61:  	0.019712  	0.02056  	alpha_SysFT_EFF_Eigen_Light_0
Rank 60:  	0.007191  	0.00682  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_3
Rank 59:  	0.008081  	0.00775  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_0
Rank 58:  	0.027276  	0.0281  	alpha_SysJET_21NP_JET_Flavor_Composition_VV
Rank 57:  	0.018408  	0.0179  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_2
Rank 56:  	0.028833  	0.0293  	alpha_SysTheoryQCDscale_ggZH
Rank 55:  	0.030184  	0.02645  	alpha_SysTheoryUEPSAcc_J3
Rank 54:  	0.027342  	0.02618  	alpha_SysFT_EFF_Eigen_C_1
Rank 53:  	0.007649  	0.00759  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_2
Rank 52:  	0.007874  	0.0084  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_14
Rank 51:  	0.02442  	0.03208  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_14
Rank 50:  	0.022117  	0.02112  	alpha_SysStopWtMBB
Rank 49:  	0.011274  	0.01266  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_13
Rank 48:  	0.002639  	0.00833  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_13
Rank 47:  	0.004074  	0.0041  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_2
Rank 46:  	0.008852  	0.00868  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_2
Rank 45:  	0.010096  	0.00964  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_2
Rank 44:  	0.012543  	0.01405  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_7
Rank 43:  	0.025059  	0.0282  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_10
Rank 42:  	0.015432  	0.01653  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_13
Rank 41:  	0.018885  	0.02089  	alpha_SysJET_JER_SINGLE_NP
Rank 40:  	0.032615  	0.03881  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_12
Rank 39:  	0.00704  	0.00711  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_4
Rank 38:  	0.037606  	0.03533  	alpha_SysTheoryAcc_J3_qqVH
Rank 37:  	0.017783  	0.01841  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_3
Rank 36:  	0.023627  	0.02587  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_9
Rank 35:  	0.032232  	0.03899  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_14
Rank 34:  	0.009646  	0.0097  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_5
Rank 33:  	0.006591  	0.00597  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_4
Rank 32:  	0.017983  	0.01949  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_8
Rank 31:  	0.01424  	0.01425  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_3
Rank 30:  	0.012994  	0.01273  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_0
Rank 29:  	0.043545  	0.04526  	alpha_SysTheoryAcc_J2_qqVH
Rank 28:  	0.047479  	0.03952  	alpha_SysFT_EFF_Eigen_B_1
Rank 27:  	0.023289  	0.02502  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_14
Rank 26:  	0.009387  	0.00976  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_6
Rank 25:  	0.020548  	0.01898  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_0
Rank 24:  	0.001053  	0.00401  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_10
Rank 23:  	0.033597  	0.03692  	alpha_SysstopWtAcc
Rank 22:  	0.025224  	0.02421  	alpha_SysTTbarMBB
Rank 21:  	0.020093  	0.01905  	alpha_SysTTbarPTV_L2
Rank 20:  	0.012765  	0.01306  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_7
Rank 19:  	0.013936  	0.01488  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_10
Rank 18:  	0.015221  	0.0085  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_0
Rank 17:  	0.02124  	0.02106  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_1
Rank 16:  	0.061598  	0.06271  	alpha_SysWPtV
Rank 15:  	0.015887  	0.01614  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_8
Rank 14:  	0.014197  	0.01403  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_1
Rank 13:  	0.04871  	0.05545  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_14
Rank 12:  	0.035486  	0.04069  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_13
Rank 11:  	0.034591  	0.03868  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_12
Rank 10:  	0.026659  	0.02469  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_3
Rank 9:  	0.018207  	0.01891  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_9
Rank 8:  	0.036278  	0.04163  	alpha_SysFT_EFF_Eigen_B_0
Rank 7:  	0.043667  	0.04638  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_13
Rank 6:  	0.038617  	0.0423  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_11
Rank 5:  	0.028972  	0.02852  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_2
Rank 4:  	0.019492  	0.02055  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_11
Rank 3:  	0.107327  	0.13625  	alpha_SysTheoryUEPSAcc
Rank 2:  	0.037766  	0.0351  	alpha_SysZMbb
Rank 1:  	0.048091  	0.04676  	alpha_SysTTbarMBB_L2

 Top range from -0.143718 to 0.168992
 Bottom range from -1.05481 to 1.24031
total unc = 0.273621
sum of sq = 0.273584
{% endhighlight %}

## 012 Post-fit impact
![IMAGE](/images/q/IMAGE)
[SMVHVZ_LHCP17_MVA_v05.lumi150scaled_fullRes_VHbbRun2_13TeV_lumi150scaled_012_125_Systs_use1tagFalse_mva_pulls_125.pdf](quiver-file-url/B9A0E8745A5AD44054B5D0FD9AEC1540.pdf)

{% highlight javascript %}
Rank 286:  	0  	0  	alpha_SysJET_21NP_JET_EffectiveNP_8restTerm
Rank 285:  	0  	0  	alpha_SysJET_21NP_JET_EffectiveNP_6
Rank 284:  	0  	0  	alpha_SysMUON_MS
Rank 283:  	0  	0  	alpha_SysMUON_EFF_TrigSystUncertainty
Rank 282:  	0  	0  	alpha_SysVHQCDscaleMbb_ggZH
Rank 281:  	0  	0  	alpha_SysVHQCDscaleMbb
Rank 280:  	0  	0  	alpha_SysEL_EFF_Trigger_TOTAL_1NPCOR_PLUS_UNCOR
Rank 279:  	0  	0  	alpha_SysJET_21NP_JET_EffectiveNP_7
Rank 278:  	0  	0  	alpha_SysMUON_SCALE
Rank 277:  	0  	0  	alpha_SysMUON_SAGITTA_RESBIAS
Rank 276:  	0  	0  	alpha_SysVHPDFPTV_ggZH
Rank 275:  	1e-05  	1e-05  	alpha_SysZZUEPSResid_L0
Rank 274:  	2e-05  	1e-05  	alpha_SysMUON_EFF_SYS_LOWPT
Rank 273:  	2e-05  	1e-05  	alpha_SysMUON_EFF_STAT_LOWPT
Rank 272:  	3e-05  	3e-05  	alpha_SysVHPDFPTV
Rank 271:  	3e-05  	3e-05  	alpha_SysVHQCDscalePTV_ggZH
Rank 270:  	2e-05  	8e-05  	alpha_SysJET_21NP_JET_EffectiveNP_5
Rank 269:  	2e-05  	9e-05  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_5
Rank 268:  	8e-05  	5e-05  	alpha_SysMUON_EFF_STAT
Rank 267:  	6e-05  	7e-05  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_3
Rank 266:  	8e-05  	8e-05  	alpha_SysMJTrigger_multijetEl
Rank 265:  	0.00013  	4e-05  	alpha_SysTheoryPDFAcc_ggZH
Rank 264:  	0.00012  	5e-05  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_4
Rank 263:  	0.000149  	3e-05  	alpha_SysTheoryAcc_JVeto_ggZH
Rank 262:  	0.00012  	7e-05  	alpha_SysFT_EFF_Eigen_Light_4
Rank 261:  	0.00012  	9e-05  	alpha_SysEL_EFF_Reco_TOTAL_1NPCOR_PLUS_UNCOR
Rank 260:  	5e-05  	0.00016  	alpha_SysMUON_ID
Rank 259:  	8e-05  	0.00017  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_0
Rank 258:  	0.000238  	3e-05  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_5
Rank 257:  	0.00028  	0  	alpha_SysStoptPTV
Rank 256:  	0.000192  	0.00013  	alpha_SysTheoryAcc_J3_ggZH
Rank 255:  	0.000227  	0.0002  	alpha_SysWZUEPSResid_L0
Rank 254:  	0.00021  	0.00026  	alpha_SysJET_21NP_JET_EffectiveNP_4
Rank 253:  	0.000303  	0.00022  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_2
Rank 252:  	0.000479  	0.0001  	alpha_SysJET_21NP_JET_EtaIntercalibration_TotalStat
Rank 251:  	0.00012  	0.00047  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_10
Rank 250:  	0.0005  	0.00022  	alpha_SysFT_EFF_extrapolation
Rank 249:  	0.000675  	8e-05  	alpha_SysZZNorm
Rank 248:  	0.000459  	0.00037  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_1
Rank 247:  	0.00044  	0.0004  	alpha_SysZlNorm
Rank 246:  	0.000464  	0.00038  	alpha_SysVVPTVPSUE
Rank 245:  	0.00083  	5e-05  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_6
Rank 244:  	0.000455  	0.00045  	alpha_SysVZUEPS_J3
Rank 243:  	0.000574  	0.00036  	alpha_SysVHQCDscalePTV
Rank 242:  	0.000428  	0.00053  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_9
Rank 241:  	0.000438  	0.00054  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_6
Rank 240:  	0.000921  	9e-05  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_5
Rank 239:  	0.000606  	0.00042  	alpha_SysTheoryAcc_JVeto_qqVH
Rank 238:  	0.000759  	0.0003  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_1
Rank 237:  	0.000631  	0.00049  	alpha_SysMJWOCorrection_multijetEl
Rank 236:  	0.000574  	0.00058  	alpha_SysMUON_ISO_STAT
Rank 235:  	0.000629  	0.00055  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_4
Rank 234:  	0.000685  	0.00053  	alpha_SysZccZbbRatio
Rank 233:  	0.000407  	0.000841  	alpha_SysEG_RESOLUTION_ALL
Rank 232:  	0.000639  	0.00064  	alpha_SysVZUEPSAcc
Rank 231:  	0.000667  	0.00062  	alpha_SysstopsNorm
Rank 230:  	0.000649  	0.0007  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_3
Rank 229:  	0.000814  	0.00054  	alpha_SysWbbNorm_L0
Rank 228:  	0.000645  	0.00072  	alpha_SysMET_SoftTrk_ResoPerp
Rank 227:  	0.001469  	2e-05  	alpha_SysZbbNorm_L0
Rank 226:  	0.000817  	0.00077  	alpha_SysMJSFsCR_multijetEl
Rank 225:  	0.000925  	0.00074  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_1
Rank 224:  	0.000734  	0.00098  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_6
Rank 223:  	0.00073  	0.001  	alpha_SysTheoryAcc_J2_ggZH
Rank 222:  	0.000825  	0.00092  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_5
Rank 221:  	0.000873  	0.00088  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_8
Rank 220:  	0.000924  	0.00083  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_2
Rank 219:  	0.000788  	0.00101  	alpha_SysJET_JvtEfficiency
Rank 218:  	0.000929  	0.00088  	alpha_SysWlNorm
Rank 217:  	0.000834  	0.00108  	alpha_SysJET_21NP_JET_Flavor_Composition_ttbar_L2
Rank 216:  	0.001195  	0.00093  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_0
Rank 215:  	0.001146  	0.00107  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_5
Rank 214:  	0.00115  	0.00114  	alpha_SysMUON_ISO_SYS
Rank 213:  	0.001214  	0.00113  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_4
Rank 212:  	0.001108  	0.00129  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_6
Rank 211:  	0.000605  	0.00191  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_10
Rank 210:  	0.001193  	0.00136  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_7
Rank 209:  	0.001325  	0.00137  	alpha_SysVVPTVME
Rank 208:  	0.001371  	0.00133  	alpha_SysEL_EFF_Iso_TOTAL_1NPCOR_PLUS_UNCOR
Rank 207:  	0.001504  	0.0013  	alpha_SysVVMbbME
Rank 206:  	0.001326  	0.00157  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfCR_bin_0
Rank 205:  	0.00169  	0.00125  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_0
Rank 204:  	0.00247  	0.00049  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_9
Rank 203:  	0.001539  	0.00145  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_4
Rank 202:  	0.001632  	0.00145  	alpha_SysVZQCDscale_J2
Rank 201:  	0.001467  	0.00163  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_7
Rank 200:  	0.001409  	0.00186  	alpha_SysJET_21NP_JET_EtaIntercalibration_NonClosure
Rank 199:  	0.00025  	0.00315  	alpha_SysJET_21NP_JET_Pileup_OffsetMu
Rank 198:  	0.00177  	0.00166  	alpha_SysWblWbbRatio
Rank 197:  	0.001965  	0.0015  	alpha_SysttbarNorm_DWhfCR_L1
Rank 196:  	0.00176  	0.00173  	alpha_SysMJReduced_multijetMu
Rank 195:  	0.001823  	0.00179  	alpha_SysTheoryQCDscale_qqVH
Rank 194:  	0.001849  	0.00183  	alpha_SysTheoryPDF_ggZH
Rank 193:  	0.001817  	0.00191  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_8
Rank 192:  	0.002051  	0.00188  	alpha_SysMETTrigTop
Rank 191:  	0.00211  	0.00183  	alpha_SysVZQCDscale_JVeto
Rank 190:  	0.001986  	0.00199  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_4
Rank 189:  	0.002071  	0.00191  	alpha_SysZclNorm
Rank 188:  	0.002016  	0.002  	alpha_SysFT_EFF_extrapolation_from_charm
Rank 187:  	0.002314  	0.00177  	alpha_SysMJNorm_2J_Mu
Rank 186:  	0.002347  	0.00199  	alpha_SysZbcZbbRatio
Rank 185:  	0.002242  	0.00215  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_4
Rank 184:  	0.00309  	0.00136  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_8
Rank 183:  	0.002404  	0.00218  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_2
Rank 182:  	0.002396  	0.00219  	alpha_SysFT_EFF_Eigen_Light_2
Rank 181:  	0.003252  	0.00135  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_0
Rank 180:  	0.00242  	0.00235  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_1
Rank 179:  	0.002542  	0.00244  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_1
Rank 178:  	0.001053  	0.00401  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_10
Rank 177:  	0.002547  	0.00252  	alpha_SysTheoryPDFAcc_qqVH
Rank 176:  	0.002855  	0.00228  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_0
Rank 175:  	0.002411  	0.00276  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_11
Rank 174:  	0.002492  	0.00279  	alpha_SysMJReduced_multijetEl
Rank 173:  	0.002735  	0.00257  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_3
Rank 172:  	0.002719  	0.00282  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_9
Rank 171:  	0.002854  	0.00273  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_0
Rank 170:  	0.003157  	0.00245  	alpha_SysMUON_EFF_SYS
Rank 169:  	0.004085  	0.00207  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_0
Rank 168:  	0.003364  	0.00284  	alpha_SysVZQCDscale_J3
Rank 167:  	0.003604  	0.00269  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_5
Rank 166:  	0.003408  	0.00293  	alpha_SysStoptMBB
Rank 165:  	0.003299  	0.00314  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_4
Rank 164:  	0.002694  	0.00383  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_5
Rank 163:  	0.003347  	0.00347  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_10
Rank 162:  	0.003582  	0.00337  	alpha_SysWZNorm
Rank 161:  	0.003679  	0.00354  	alpha_SysWclNorm
Rank 160:  	0.003904  	0.00332  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_2
Rank 159:  	0.003697  	0.00364  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_3
Rank 158:  	0.003994  	0.00338  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_7
Rank 157:  	0.003866  	0.00388  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_4
Rank 156:  	0.003932  	0.00382  	alpha_SysVHUEPSPTV
Rank 155:  	0.00058  	0.0072  	alpha_SysMJNorm_3J_El
Rank 154:  	0.003974  	0.00381  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_3
Rank 153:  	0.003904  	0.00391  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_4
Rank 152:  	0.003716  	0.0041  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_5
Rank 151:  	0.004074  	0.0041  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_2
Rank 150:  	0.00479  	0.00346  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_0
Rank 149:  	0.004125  	0.00421  	alpha_SysVHNLOEWK
Rank 148:  	0.004472  	0.00404  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_1
Rank 147:  	0.003865  	0.00476  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_7
Rank 146:  	0.004471  	0.00427  	alpha_SysstoptNorm
Rank 145:  	0.002601  	0.0064  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_11
Rank 144:  	0.003554  	0.00563  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_7
Rank 143:  	0.005235  	0.00424  	alpha_SysMJ2Tag_multijetMu
Rank 142:  	0.00182  	0.007704  	alpha_SysPRW_DATASF
Rank 141:  	0.005058  	0.00451  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_6
Rank 140:  	0.004617  	0.00513  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_12
Rank 139:  	0.004928  	0.00484  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_1
Rank 138:  	0.004727  	0.00508  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_9
Rank 137:  	0.005024  	0.00479  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_5
Rank 136:  	0.004479  	0.00543  	alpha_SysWbbNorm_DWhfSR
Rank 135:  	0.005571  	0.00451  	alpha_SysJET_21NP_JET_Pileup_PtTerm
Rank 134:  	0.004736  	0.00551  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_6
Rank 133:  	0.005097  	0.00524  	alpha_SysTheoryPDF_qqVH
Rank 132:  	0.005856  	0.00483  	alpha_SysttbarNorm_J2
Rank 131:  	0.002639  	0.00833  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_13
Rank 130:  	0.005469  	0.00588  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_10
Rank 129:  	0.005854  	0.00551  	alpha_SysMJ2Tag_multijetEl
Rank 128:  	0.005803  	0.00568  	alpha_SysZblZbbRatio
Rank 127:  	0.0059  	0.00561  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_1
Rank 126:  	0.00571  	0.00591  	alpha_SysTheoryBRbb
Rank 125:  	0.00902  	0.003  	alpha_SysVHUEPSMbb
Rank 124:  	0.006179  	0.00615  	alpha_SysFT_EFF_Eigen_C_2
Rank 123:  	0.006088  	0.00629  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_5
Rank 122:  	0.006002  	0.00641  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_11
Rank 121:  	0.006591  	0.00597  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_4
Rank 120:  	0.005961  	0.0067  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_11
Rank 119:  	0.00508  	0.00765  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_12
Rank 118:  	0.006434  	0.0063  	alpha_SysMJNorm_2J_El
Rank 117:  	0.005364  	0.00742  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_12
Rank 116:  	0.006815  	0.00633  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_8
Rank 115:  	0.010624  	0.002832  	alpha_SysJET_21NP_JET_Pileup_OffsetNPV
Rank 114:  	0.006716  	0.00692  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_6
Rank 113:  	0.007191  	0.00682  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmBBMVA_Dtopemucr_bin_3
Rank 112:  	0.007264  	0.00685  	alpha_SysEL_EFF_ID_TOTAL_1NPCOR_PLUS_UNCOR
Rank 111:  	0.007034  	0.00711  	alpha_SysstopWtNorm
Rank 110:  	0.00704  	0.00711  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_4
Rank 109:  	0.006813  	0.00741  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_12
Rank 108:  	0.007376  	0.00725  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_3
Rank 107:  	0.00756  	0.0072  	alpha_SysFT_EFF_Eigen_B_2
Rank 106:  	0.006399  	0.00837  	alpha_SysJET_21NP_JET_BJES_Response
Rank 105:  	0.007706  	0.00752  	alpha_SysWccWbbRatio
Rank 104:  	0.007785  	0.00745  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_3
Rank 103:  	0.007649  	0.00759  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_2
Rank 102:  	0.009998  	0.0054  	alpha_SysWMbb
Rank 101:  	0.008081  	0.00775  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_0
Rank 100:  	0.007209  	0.00869  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_13
Rank 99:  	0.005413  	0.01051  	alpha_SysMJNorm_3J_Mu
Rank 98:  	0.007874  	0.0084  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_14
Rank 97:  	0.015146  	0.002174  	alpha_SysJET_21NP_JET_EffectiveNP_1
Rank 96:  	0.010701  	0.00673  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_1
Rank 95:  	0.008852  	0.00868  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_2
Rank 94:  	0.011744  	0.00588  	alpha_SysZPtV
Rank 93:  	0.008818  	0.00885  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_2
Rank 92:  	0.010489  	0.00758  	alpha_SysJET_21NP_JET_Flavor_Composition_Top
Rank 91:  	0.00984  	0.00826  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfCR_bin_0
Rank 90:  	0.013718  	0.004919  	ATLAS_norm_Wbb_J2
Rank 89:  	0.008559  	0.01032  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_9
Rank 88:  	0.009046  	0.00999  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_8
Rank 87:  	0.009387  	0.00976  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_6
Rank 86:  	0.008988  	0.01021  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_8
Rank 85:  	0.009646  	0.0097  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_5
Rank 84:  	0.009718  	0.00982  	alpha_SysEG_SCALE_ALL
Rank 83:  	0.010096  	0.00964  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_2
Rank 82:  	0.009507  	0.01048  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_14
Rank 81:  	0.014179  	0.00585  	alpha_SysJET_21NP_JET_EffectiveNP_2
Rank 80:  	0.016504  	0.00402  	ATLAS_norm_ttbar_J3_L2_Y
Rank 79:  	0.009289  	0.0117  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_9
Rank 78:  	0.010228  	0.01155  	alpha_SysJET_21NP_JET_EffectiveNP_3
Rank 77:  	0.011164  	0.01092  	alpha_SysTTbarPTV
Rank 76:  	0.011459  	0.01098  	alpha_SysWbcWbbRatio
Rank 75:  	0.0227  	0.00054  	ATLAS_norm_Zbb_J2
Rank 74:  	0.015221  	0.0085  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_0
Rank 73:  	0.011294  	0.01254  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_7
Rank 72:  	0.011274  	0.01266  	gamma_stat_Region_BMin150_J2_T2_L2_Y2015_distmva_DSR_bin_13
Rank 71:  	0.012994  	0.01273  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_0
Rank 70:  	0.012765  	0.01306  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_7
Rank 69:  	0.011411  	0.01448  	alpha_SysMET_SoftTrk_Scale
Rank 68:  	0.012338  	0.0137  	alpha_SysJET_21NP_JET_Flavor_Response
Rank 67:  	0.010789  	0.01573  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_12
Rank 66:  	0.012543  	0.01405  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_7
Rank 65:  	0.020187  	0.006604  	alpha_SysJET_21NP_JET_Pileup_RhoTopology
Rank 64:  	0.015888  	0.01102  	alpha_SysttbarNorm_L0
Rank 63:  	0.020277  	0.007781  	alpha_SysJET_21NP_JET_Flavor_Composition_Vjets
Rank 62:  	0.014197  	0.01403  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_1
Rank 61:  	0.014295  	0.01406  	alpha_SysFT_EFF_Eigen_Light_3
Rank 60:  	0.01424  	0.01425  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_3
Rank 59:  	0.013936  	0.01488  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_10
Rank 58:  	0.014675  	0.01427  	alpha_SysFT_EFF_Eigen_C_0
Rank 57:  	0.014392  	0.01477  	alpha_SysMET_SoftTrk_ResoPara
Rank 56:  	0.013095  	0.01631  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_11
Rank 55:  	0.024372  	0.00513  	alpha_SysJET_21NP_JET_EtaIntercalibration_Modelling
Rank 54:  	0.015465  	0.01432  	ATLAS_norm_ttbar_J2_L2_Y
Rank 53:  	0.022719  	0.00771  	ATLAS_norm_Zbb_J3
Rank 52:  	0.015432  	0.01653  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_13
Rank 51:  	0.015887  	0.01614  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_8
Rank 50:  	0.017902  	0.01817  	alpha_SysstoptAcc
Rank 49:  	0.017783  	0.01841  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_3
Rank 48:  	0.018408  	0.0179  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_2
Rank 47:  	0.018207  	0.01891  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_9
Rank 46:  	0.017983  	0.01949  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_8
Rank 45:  	0.018248  	0.01953  	alpha_SysStopWtPTV
Rank 44:  	0.017716  	0.02008  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_13
Rank 43:  	0.020093  	0.01905  	alpha_SysTTbarPTV_L2
Rank 42:  	0.020548  	0.01898  	gamma_stat_Region_BMax150_BMin75_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_0
Rank 41:  	0.018885  	0.02089  	alpha_SysJET_JER_SINGLE_NP
Rank 40:  	0.019492  	0.02055  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_11
Rank 39:  	0.019712  	0.02056  	alpha_SysFT_EFF_Eigen_Light_0
Rank 38:  	0.021294  	0.01991  	alpha_SysFT_EFF_Eigen_Light_1
Rank 37:  	0.02124  	0.02106  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_1
Rank 36:  	0.027383  	0.0158  	ATLAS_norm_Wbb_J3
Rank 35:  	0.022117  	0.02112  	alpha_SysStopWtMBB
Rank 34:  	0.0191  	0.02451  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_11
Rank 33:  	0.017256  	0.02771  	alpha_ATLAS_LUMI_2015_2016
Rank 32:  	0.017262  	0.02792  	gamma_stat_Region_BMin150_J3_T2_L1_Y2015_distmva_DWhfSR_bin_14
Rank 31:  	0.020819  	0.0244  	gamma_stat_Region_BMax150_BMin75_J2_T2_L2_Y2015_distmva_DSR_bin_14
Rank 30:  	0.020652  	0.02527  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_10
Rank 29:  	0.023289  	0.02502  	gamma_stat_Region_BMin150_incJet1_J3_T2_L2_Y2015_distmva_DSR_bin_14
Rank 28:  	0.025224  	0.02421  	alpha_SysTTbarMBB
Rank 27:  	0.023627  	0.02587  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_9
Rank 26:  	0.026659  	0.02469  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_3
Rank 25:  	0.025059  	0.0282  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_10
Rank 24:  	0.023553  	0.02979  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_13
Rank 23:  	0.027342  	0.02618  	alpha_SysFT_EFF_Eigen_C_1
Rank 22:  	0.026207  	0.0291  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_12
Rank 21:  	0.027276  	0.0281  	alpha_SysJET_21NP_JET_Flavor_Composition_VV
Rank 20:  	0.02442  	0.03208  	gamma_stat_Region_BMin150_J3_T2_L0_Y2015_distmva_DSR_bin_14
Rank 19:  	0.030184  	0.02645  	alpha_SysTheoryUEPSAcc_J3
Rank 18:  	0.028972  	0.02852  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_2
Rank 17:  	0.028833  	0.0293  	alpha_SysTheoryQCDscale_ggZH
Rank 16:  	0.033597  	0.03692  	alpha_SysstopWtAcc
Rank 15:  	0.032232  	0.03899  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_14
Rank 14:  	0.032615  	0.03881  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_12
Rank 13:  	0.037766  	0.0351  	alpha_SysZMbb
Rank 12:  	0.037606  	0.03533  	alpha_SysTheoryAcc_J3_qqVH
Rank 11:  	0.034591  	0.03868  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_12
Rank 10:  	0.035486  	0.04069  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_13
Rank 9:  	0.036278  	0.04163  	alpha_SysFT_EFF_Eigen_B_0
Rank 8:  	0.038617  	0.0423  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_11
Rank 7:  	0.047479  	0.03952  	alpha_SysFT_EFF_Eigen_B_1
Rank 6:  	0.043545  	0.04526  	alpha_SysTheoryAcc_J2_qqVH
Rank 5:  	0.043667  	0.04638  	gamma_stat_Region_BMin150_J2_T2_L0_Y2015_distmva_DSR_bin_13
Rank 4:  	0.048091  	0.04676  	alpha_SysTTbarMBB_L2
Rank 3:  	0.04871  	0.05545  	gamma_stat_Region_BMin150_J2_T2_L1_Y2015_distmva_DWhfSR_bin_14
Rank 2:  	0.061598  	0.06271  	alpha_SysWPtV
Rank 1:  	0.107327  	0.13625  	alpha_SysTheoryUEPSAcc

 Top range from -0.143718 to 0.168992
 Bottom range from -1.05481 to 1.24031
total unc = 0.273621
sum of sq = 0.273584
{% endhighlight %}

### Expected significances

| Channel | Expected significance MVA | Expected significance cuts |
| ------- | ------------------------- | -------------------------- |
| 0       | 2.81986                   | 2.74655                    |
| 1       | 2.56337                   | x                          |
| 2       | 3.29832                   | 2.84917                    |
| 012     | 4.97016                   | 4.00753                    |

### Expected significance without MC stat NP

| Channel | Expected significance MVA | Expected significance cuts |
| ------- | ------------------------- | -------------------------- |
| 0       | 3.59129                   | 3.77926                    |
| 1       | 3.5218                    | x                          |
| 2       | 3.73324                   | 3.35952                    |
| 012     | 6.38604                   | 5.19082                    |

