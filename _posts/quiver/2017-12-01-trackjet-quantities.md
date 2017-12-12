---
title: TrackJet quantities
date: '2017-12-01'
tags:
- BDT
- VHbb
---
# Purpose
* look for new discriminating variables from track jets

* Significance

| Category | Default | Trackjets |
| ---------| ------- | --------- |
| 2 jets   | 2.34 +- 0.03 | 2.38 +- 0.03 |
| 3 jets   | 1.63 +- 0.02 | 1.65 +- 0.02
| Combined | 2.8558  | 2.9045 |

**New variables in red**
![IMAGE](/images/q/84BFB608081376C5908DA07194E3A17F.jpg)
{% highlight c_cpp %}
Testing training in directory : training_TrkJets_defaultVars/TMVA.root
Sensitivity 2j = 2.34426 +- 0.0306169
Sensitivity 3j = 1.63096 +- 0.0185295
Combined sensitivity = 2.8558

Testing training in directory : training_TrkJets/TMVA.root
Sensitivity 2j = 2.38815 +- 0.0344475
Sensitivity 3j = 1.65314 +- 0.0192968
Combined sensitivity = 2.9045
{% endhighlight %}

* **Note**
  * SumEt_TrkJ and MEt_TrkJ look the same and often have identical values because of the trackjet OR applied with jets and taus : often, only one trackjet is left (but nTrkJets does not have this OR)
)
![IMAGE](/images/q/45F6EE0CBB0C7A7A1263BAF72FF9CD1E.jpg)
![IMAGE](/images/q/1976041D41BA065AA07BA066AF00491A.jpg)
![IMAGE](/images/q/7154B066EE53C39A37D3787840A5CCD5.jpg)
{% highlight sh %}
--- BDTCategories_tag28_Tr...: Training finished
--- BDTCategories_tag28_Tr...: Begin ranking of input variables...
--- BDTCat_2j_1o2            : Ranking result (top variable is best ranked)
--- BDTCat_2j_1o2            : ------------------------------------------------
--- BDTCat_2j_1o2            : Rank : Variable       : Variable Importance
--- BDTCat_2j_1o2            : ------------------------------------------------
--- BDTCat_2j_1o2            :    1 : mBB            : 3.254e-01
--- BDTCat_2j_1o2            :    2 : dRBB           : 1.695e-01
--- BDTCat_2j_1o2            :    3 : dEtaBB         : 1.267e-01
--- BDTCat_2j_1o2            :    4 : pTB2           : 6.653e-02
--- BDTCat_2j_1o2            :    5 : dPhiMETdijet   : 6.453e-02
--- BDTCat_2j_1o2            :    6 : pTB1           : 5.017e-02
--- BDTCat_2j_1o2            :    7 : HT             : 4.600e-02
--- BDTCat_2j_1o2            :    8 : SoftSumET      : 4.595e-02
--- BDTCat_2j_1o2            :    9 : SumEt_TrkJ     : 3.201e-02
--- BDTCat_2j_1o2            :   10 : nTrkJets       : 2.712e-02
--- BDTCat_2j_1o2            :   11 : nTrkJOutsideBB : 2.480e-02
--- BDTCat_2j_1o2            :   12 : MET            : 1.511e-02
--- BDTCat_2j_1o2            :   13 : MEt_TrkJ       : 6.208e-03
--- BDTCat_2j_1o2            :   14 : nFatJets       : 0.000e+00
--- BDTCat_2j_1o2            :   15 : nTrkJInsideBB  : 0.000e+00
--- BDTCat_2j_1o2            : ------------------------------------------------
--- BDTCat_2j_2o2            : Ranking result (top variable is best ranked)
--- BDTCat_2j_2o2            : ------------------------------------------------
--- BDTCat_2j_2o2            : Rank : Variable       : Variable Importance
--- BDTCat_2j_2o2            : ------------------------------------------------
--- BDTCat_2j_2o2            :    1 : mBB            : 3.045e-01
--- BDTCat_2j_2o2            :    2 : dRBB           : 1.710e-01
--- BDTCat_2j_2o2            :    3 : dEtaBB         : 1.117e-01
--- BDTCat_2j_2o2            :    4 : SoftSumET      : 7.448e-02
--- BDTCat_2j_2o2            :    5 : pTB2           : 6.806e-02
--- BDTCat_2j_2o2            :    6 : HT             : 6.394e-02
--- BDTCat_2j_2o2            :    7 : dPhiMETdijet   : 4.782e-02
--- BDTCat_2j_2o2            :    8 : pTB1           : 3.983e-02
--- BDTCat_2j_2o2            :    9 : nTrkJets       : 3.828e-02
--- BDTCat_2j_2o2            :   10 : MET            : 2.790e-02
--- BDTCat_2j_2o2            :   11 : nTrkJOutsideBB : 1.985e-02
--- BDTCat_2j_2o2            :   12 : SumEt_TrkJ     : 1.703e-02
--- BDTCat_2j_2o2            :   13 : MEt_TrkJ       : 1.566e-02
--- BDTCat_2j_2o2            :   14 : nFatJets       : 0.000e+00
--- BDTCat_2j_2o2            :   15 : nTrkJInsideBB  : 0.000e+00
--- BDTCat_2j_2o2            : ------------------------------------------------
--- BDTCat_3j_1o2            : Ranking result (top variable is best ranked)
--- BDTCat_3j_1o2            : ------------------------------------------------
--- BDTCat_3j_1o2            : Rank : Variable       : Variable Importance
--- BDTCat_3j_1o2            : ------------------------------------------------
--- BDTCat_3j_1o2            :    1 : mBB            : 2.987e-01
--- BDTCat_3j_1o2            :    2 : dRBB           : 1.274e-01
--- BDTCat_3j_1o2            :    3 : pTB2           : 8.140e-02
--- BDTCat_3j_1o2            :    4 : mBBJ           : 7.524e-02
--- BDTCat_3j_1o2            :    5 : MET            : 7.202e-02
--- BDTCat_3j_1o2            :    6 : HT             : 6.563e-02
--- BDTCat_3j_1o2            :    7 : dPhiMETdijet   : 5.622e-02
--- BDTCat_3j_1o2            :    8 : nTrkJOutsideBB : 5.328e-02
--- BDTCat_3j_1o2            :    9 : pTJ3           : 4.003e-02
--- BDTCat_3j_1o2            :   10 : SumEt_TrkJ     : 3.442e-02
--- BDTCat_3j_1o2            :   11 : nTrkJets       : 3.079e-02
--- BDTCat_3j_1o2            :   12 : dEtaBB         : 2.510e-02
--- BDTCat_3j_1o2            :   13 : pTB1           : 1.946e-02
--- BDTCat_3j_1o2            :   14 : SoftSumET      : 1.903e-02
--- BDTCat_3j_1o2            :   15 : MEt_TrkJ       : 1.221e-03
--- BDTCat_3j_1o2            :   16 : nFatJets       : 0.000e+00
--- BDTCat_3j_1o2            :   17 : nTrkJInsideBB  : 0.000e+00
--- BDTCat_3j_1o2            : ------------------------------------------------
--- BDTCat_3j_2o2            : Ranking result (top variable is best ranked)
--- BDTCat_3j_2o2            : ------------------------------------------------
--- BDTCat_3j_2o2            : Rank : Variable       : Variable Importance
--- BDTCat_3j_2o2            : ------------------------------------------------
--- BDTCat_3j_2o2            :    1 : mBB            : 2.777e-01
--- BDTCat_3j_2o2            :    2 : dRBB           : 1.487e-01
--- BDTCat_3j_2o2            :    3 : pTB2           : 9.045e-02
--- BDTCat_3j_2o2            :    4 : mBBJ           : 7.164e-02
--- BDTCat_3j_2o2            :    5 : HT             : 6.628e-02
--- BDTCat_3j_2o2            :    6 : dPhiMETdijet   : 5.416e-02
--- BDTCat_3j_2o2            :    7 : MET            : 5.014e-02
--- BDTCat_3j_2o2            :    8 : pTJ3           : 4.815e-02
--- BDTCat_3j_2o2            :    9 : pTB1           : 4.035e-02
--- BDTCat_3j_2o2            :   10 : SumEt_TrkJ     : 3.495e-02
--- BDTCat_3j_2o2            :   11 : dEtaBB         : 2.364e-02
--- BDTCat_3j_2o2            :   12 : SoftSumET      : 2.337e-02
--- BDTCat_3j_2o2            :   13 : nTrkJets       : 2.306e-02
--- BDTCat_3j_2o2            :   14 : nTrkJOutsideBB : 2.167e-02
--- BDTCat_3j_2o2            :   15 : MEt_TrkJ       : 1.647e-02
--- BDTCat_3j_2o2            :   16 : nFatJets       : 9.265e-03
--- BDTCat_3j_2o2            :   17 : nTrkJInsideBB  : 0.000e+00
--- BDTCat_3j_2o2            : ------------------------------------------------
--- BDTCategories_tag28_Tr...: End of training                                              
--- BDTCategories_tag28_Tr...: Elapsed time for training with 7827096 events: 3.06e+03 sec
{% endhighlight %}

# Training against ttbar only
)
{% highlight sh %}
--- BDTCategories_tag28_Tr...: Training finished
--- BDTCategories_tag28_Tr...: Begin ranking of input variables...
--- BDTCat_2j_1o2            : Ranking result (top variable is best ranked)
--- BDTCat_2j_1o2            : ------------------------------------------------
--- BDTCat_2j_1o2            : Rank : Variable       : Variable Importance
--- BDTCat_2j_1o2            : ------------------------------------------------
--- BDTCat_2j_1o2            :    1 : mBB            : 2.226e-01
--- BDTCat_2j_1o2            :    2 : dRBB           : 1.548e-01
--- BDTCat_2j_1o2            :    3 : dPhiMETdijet   : 1.276e-01
--- BDTCat_2j_1o2            :    4 : MET            : 7.637e-02
--- BDTCat_2j_1o2            :    5 : HT             : 7.495e-02
--- BDTCat_2j_1o2            :    6 : SoftSumET      : 6.738e-02
--- BDTCat_2j_1o2            :    7 : pTB2           : 6.042e-02
--- BDTCat_2j_1o2            :    8 : pTB1           : 4.977e-02
--- BDTCat_2j_1o2            :    9 : dEtaBB         : 4.697e-02
--- BDTCat_2j_1o2            :   10 : SumEt_TrkJ     : 4.606e-02
--- BDTCat_2j_1o2            :   11 : nTrkJets       : 3.212e-02
--- BDTCat_2j_1o2            :   12 : nTrkJOutsideBB : 2.973e-02
--- BDTCat_2j_1o2            :   13 : MEt_TrkJ       : 1.118e-02
--- BDTCat_2j_1o2            :   14 : nFatJets       : 0.000e+00
--- BDTCat_2j_1o2            :   15 : nTrkJInsideBB  : 0.000e+00
--- BDTCat_2j_1o2            : ------------------------------------------------
--- BDTCat_2j_2o2            : Ranking result (top variable is best ranked)
--- BDTCat_2j_2o2            : ------------------------------------------------
--- BDTCat_2j_2o2            : Rank : Variable       : Variable Importance
--- BDTCat_2j_2o2            : ------------------------------------------------
--- BDTCat_2j_2o2            :    1 : mBB            : 2.346e-01
--- BDTCat_2j_2o2            :    2 : dRBB           : 1.315e-01
--- BDTCat_2j_2o2            :    3 : MET            : 1.107e-01
--- BDTCat_2j_2o2            :    4 : dPhiMETdijet   : 1.096e-01
--- BDTCat_2j_2o2            :    5 : HT             : 9.842e-02
--- BDTCat_2j_2o2            :    6 : pTB2           : 7.128e-02
--- BDTCat_2j_2o2            :    7 : SoftSumET      : 4.834e-02
--- BDTCat_2j_2o2            :    8 : MEt_TrkJ       : 4.800e-02
--- BDTCat_2j_2o2            :    9 : pTB1           : 3.951e-02
--- BDTCat_2j_2o2            :   10 : nTrkJOutsideBB : 3.577e-02
--- BDTCat_2j_2o2            :   11 : SumEt_TrkJ     : 2.790e-02
--- BDTCat_2j_2o2            :   12 : nTrkJets       : 2.419e-02
--- BDTCat_2j_2o2            :   13 : dEtaBB         : 2.016e-02
--- BDTCat_2j_2o2            :   14 : nFatJets       : 0.000e+00
--- BDTCat_2j_2o2            :   15 : nTrkJInsideBB  : 0.000e+00
--- BDTCat_2j_2o2            : ------------------------------------------------
--- BDTCat_3j_1o2            : Ranking result (top variable is best ranked)
--- BDTCat_3j_1o2            : ------------------------------------------------
--- BDTCat_3j_1o2            : Rank : Variable       : Variable Importance
--- BDTCat_3j_1o2            : ------------------------------------------------
--- BDTCat_3j_1o2            :    1 : mBB            : 2.066e-01
--- BDTCat_3j_1o2            :    2 : dRBB           : 1.216e-01
--- BDTCat_3j_1o2            :    3 : MET            : 1.063e-01
--- BDTCat_3j_1o2            :    4 : mBBJ           : 9.049e-02
--- BDTCat_3j_1o2            :    5 : pTB2           : 5.999e-02
--- BDTCat_3j_1o2            :    6 : pTJ3           : 5.909e-02
--- BDTCat_3j_1o2            :    7 : SoftSumET      : 5.534e-02
--- BDTCat_3j_1o2            :    8 : nTrkJOutsideBB : 5.012e-02
--- BDTCat_3j_1o2            :    9 : dPhiMETdijet   : 4.843e-02
--- BDTCat_3j_1o2            :   10 : SumEt_TrkJ     : 4.785e-02
--- BDTCat_3j_1o2            :   11 : pTB1           : 3.816e-02
--- BDTCat_3j_1o2            :   12 : nTrkJets       : 2.937e-02
--- BDTCat_3j_1o2            :   13 : nFatJets       : 2.621e-02
--- BDTCat_3j_1o2            :   14 : dEtaBB         : 2.254e-02
--- BDTCat_3j_1o2            :   15 : HT             : 1.908e-02
--- BDTCat_3j_1o2            :   16 : MEt_TrkJ       : 1.515e-02
--- BDTCat_3j_1o2            :   17 : nTrkJInsideBB  : 3.630e-03
--- BDTCat_3j_1o2            : ------------------------------------------------
--- BDTCat_3j_2o2            : Ranking result (top variable is best ranked)
--- BDTCat_3j_2o2            : ------------------------------------------------
--- BDTCat_3j_2o2            : Rank : Variable       : Variable Importance
--- BDTCat_3j_2o2            : ------------------------------------------------
--- BDTCat_3j_2o2            :    1 : mBB            : 1.943e-01
--- BDTCat_3j_2o2            :    2 : dRBB           : 1.304e-01
--- BDTCat_3j_2o2            :    3 : MET            : 9.823e-02
--- BDTCat_3j_2o2            :    4 : mBBJ           : 9.373e-02
--- BDTCat_3j_2o2            :    5 : pTB2           : 8.142e-02
--- BDTCat_3j_2o2            :    6 : pTJ3           : 7.012e-02
--- BDTCat_3j_2o2            :    7 : SoftSumET      : 5.526e-02
--- BDTCat_3j_2o2            :    8 : dPhiMETdijet   : 5.164e-02
--- BDTCat_3j_2o2            :    9 : SumEt_TrkJ     : 5.037e-02
--- BDTCat_3j_2o2            :   10 : pTB1           : 4.253e-02
--- BDTCat_3j_2o2            :   11 : nTrkJOutsideBB : 3.585e-02
--- BDTCat_3j_2o2            :   12 : dEtaBB         : 2.736e-02
--- BDTCat_3j_2o2            :   13 : HT             : 2.536e-02
--- BDTCat_3j_2o2            :   14 : nTrkJets       : 1.886e-02
--- BDTCat_3j_2o2            :   15 : MEt_TrkJ       : 1.635e-02
--- BDTCat_3j_2o2            :   16 : nFatJets       : 8.256e-03
--- BDTCat_3j_2o2            :   17 : nTrkJInsideBB  : 0.000e+00
--- BDTCat_3j_2o2            : ------------------------------------------------
--- BDTCategories_tag28_Tr...: End of training
{% endhighlight %}

### Rejection against ttbar events
![IMAGE](/images/q/8D0355178FE6746A53F48CA93C33E0B3.jpg)
### Rejection against all processes
![IMAGE](/images/q/49E85104804F99DB3DF648773EC5A000.jpg)
### Comparison plot
![IMAGE](/images/q/68C189C8FE0553F7C3154FF3A5A95271.jpg)
