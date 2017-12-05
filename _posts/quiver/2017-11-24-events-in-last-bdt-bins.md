---
title: Events in last BDT bins
date: '2017-11-24'
tags: []
---
# Purpose
Pursue the analysis of the composition of the last BDT bins :
[BDT composition per bin](quiver-note-url/8C9F172A-0451-4C87-BEBB-8175956C29FD)

* checked how the bin stat. errors are computed : sqrt( SUM_{bins}{weight*weight} ) seems to give a perfect match
)
# ttbar
* study already performed in some way for Valerio : (mail on 21/02/2017)
[ttbarComposition.pdf](quiver-file-url/710DBB4A719381C66B8624BC8764B462.pdf)
)
### 2 jets events
)
**1rst BDT bin**
* contains only bc events
  * the 2nd b-quark generally has very low pT
* very high reco MET, in good agreement with the TruthMET
* single lepton decays with a truth tau, but no reconstructed tau
* in most cases, large pT neutrino and low pT tau except for one event (row 503019)
  * in the latter case, TruthMET probably origins from the huge pT neutrino in the tau decay (small dPhi(TruthMET, tau))
)
{% highlight sh %}
root [65] Nominal->Scan("EventWeight:mva28:mBB:MET:dRBB:pTB1:pTB2:nTaus:TruthMET:b1Flav:b2Flav:nTruthNuW:lep_pdgId:alep_pdgId:lep.Pt():lep.Eta():alep.Pt():alep.Eta():b.Pt():b.Eta():ab.Pt():ab.Eta():nu.Pt():anu.Pt():top.Pt():atop.Pt():TVector2::Phi_mpi_pi(lep.Phi()-TruthMETp4.Phi())","EventWeight*(nJ==2)*(nTags==2)*(mva28>0.634)","precision=3 colsize=3")
******************************************************************************************************************************************************************************
*    Row   * Eve * mva * mBB * MET * dRB * pTB * pTB * nTa * Tru * b1F * b2F * nTr * lep * ale * lep * lep * ale * ale * b.P * b.E * ab. * ab. * nu. * anu * top * ato * TVe *
******************************************************************************************************************************************************************************
*   265644 * 0.4 * 0.6 * 134 * 332 * 0.7 * 213 * 146 *   0 * 311 *   5 *   4 *   1 *  15 * -99 * 36. * 0.5 *   0 *   0 * 195 * 1.7 * 7.9 * -1. *   0 * 290 * 320 * 321 * 0.7 *
*   496113 * 0.3 * 0.6 * 128 * 275 * 0.8 * 212 * 98. *   0 * 274 *   4 *   5 *   1 * -99 * -15 *   0 *   0 * 5.0 * 0.5 * 8.8 * -0. * 112 * -1. * 277 *   0 * 275 * 289 * 2.2 *
*   503019 * 0.3 * 0.6 * 119 * 239 * 0.9 * 143 * 121 *   0 * 194 *   5 *   4 *   1 *  15 * -99 * 186 * 2.7 *   0 *   0 * 153 * 0.1 *  12 * 0.8 *   0 * 30. * 229 * 209 * -0. *
*   565835 * 1.0 * 0.7 * 127 * 307 * 0.7 * 193 * 145 *   0 * 303 *   5 *   4 *   1 *  15 * -99 * 74. * 0.4 *   0 *   0 * 178 * 0.2 * 20. * 0.7 *   0 * 242 * 292 * 299 * -0. *
******************************************************************************************************************************************************************************
{% endhighlight %}

{% highlight sh %}
root [29] sqrt(0.405*0.405+0.326*0.326+0.316*0.316+1.05*1.05)
(double) 1.213531
{% endhighlight %}

* bTagging might help to reach a better rejection of these bc events with more performant tagging algorithms / ~tighter WP
  * 1/2 events rejected moving from 70% to 60% bJet efficieny (-->49% to 36% signal efficiency at first order)
)
{% highlight sh %}
root [4] Nominal->Scan("EventWeight:mva28:mBB:pTB1:pTB2:b1Flav:b2Flav:MV2c10B1:MV2c10B2:MV2c10B1>0.934906:MV2c10B2>0.934906","EventWeight*(nJ==2)*(nTags==2)*(mva28>0.634)","precision=3 colsize=5")
****************************************************************************************************
*    Row   * Event * mva28 *   mBB *  pTB1 *  pTB2 * b1Fla * b2Fla * MV2c1 * MV2c1 * MV2c1 * MV2c1 *
****************************************************************************************************
*   265644 * 0.405 * 0.682 *   134 *   213 *   146 *     5 *     4 * 0.994 * 0.859 *     1 *     0 *
*   496113 * 0.326 * 0.666 *   128 *   212 *  98.5 *     4 *     5 * 0.955 *     1 *     1 *     1 *
*   503019 * 0.316 * 0.691 *   119 *   143 *   121 *     5 *     4 *  0.98 * 0.942 *     1 *     1 *
*   565835 *  1.05 * 0.724 *   127 *   193 *   145 *     5 *     4 * 0.928 * 0.926 *     0 *     0 *
****************************************************************************************************
{% endhighlight %}

**2nd BDT bin**
* mostly bc events
* mostly single-lepton events with a truth tau, sometimes reconstructed
  * one dilepton event, with 40 GeV electron and a very small pT muon
* TruthMET mostly origins from the neutrino, a few times (36475, 212842, 569282) from the tau decay product neutrino
* Event (569282) has a very large asymetry in top-atop transverse momentum, which increases TruthMET
)
{% highlight sh %}
root [66] Nominal->Scan("EventWeight:mva28:mBB:MET:dRBB:pTB1:pTB2:nTaus:TruthMET:b1Flav:b2Flav:nTruthNuW:lep_pdgId:alep_pdgId:lep.Pt():lep.Eta():alep.Pt():alep.Eta():b.Pt():b.Eta():ab.Pt():ab.Eta():nu.Pt():anu.Pt():top.Pt():atop.Pt():TVector2::Phi_mpi_pi(lep.Phi()-TruthMETp4.Phi())","EventWeight*(nJ==2)*(nTags==2)*(mva28>0.582&&mva28<0.634)","precision=3 colsize=3")
******************************************************************************************************************************************************************************
*    Row   * Eve * mva * mBB * MET * dRB * pTB * pTB * nTa * Tru * b1F * b2F * nTr * lep * ale * lep * lep * ale * ale * b.P * b.E * ab. * ab. * nu. * anu * top * ato * TVe *
******************************************************************************************************************************************************************************
*    36475 * 0.0 * 0.5 * 136 * 278 * 1.0 * 173 * 111 *   1 * 252 *   5 *   4 *   1 *  15 * -99 * 230 * -2. *   0 *   0 * 169 * -1. * 15. * -1. *   0 * 70. * 246 * 286 * 0.1 *
*    88337 * 0.3 * 0.6 * 120 * 211 * 1.0 * 137 * 100 *   0 * 188 *   5 *   5 *   2 *  11 * -13 * 41. * -0. * 6.7 * -0. * 58. * -0. * 144 * -0. * 206 * 21. * 176 * 183 * 2.5 *
*   184640 * 0.3 * 0.5 * 117 * 249 * 0.9 * 161 * 93. *   0 * 225 *   5 *   4 *   1 *  13 * -99 * 8.3 * 0.7 *   0 *   0 * 152 *  -1 * 25. * 1.2 *   0 * 225 * 209 * 195 * 2.3 *
*   194481 * 0.2 * 0.6 * 117 * 204 * 0.9 * 135 * 106 *   1 * 191 *   5 *   5 *   1 * -99 * -15 *   0 *   0 * 27. * 0.2 *  22 * -0. * 139 * -0. * 190 *   0 * 187 * 172 * 0.1 *
*   212842 * 0.3 * 0.6 * 117 * 177 * 1.1 * 108 * 99. *   1 * 173 *   5 *   4 *   1 *  15 * -99 * 130 * 0.6 *   0 *   0 * 112 * 0.6 * 18. * -1. *   0 * 69. * 168 * 180 * -0. *
*   336228 * 0.3 * 0.5 * 118 * 233 * 0.8 * 148 * 96. *   0 * 247 *   5 *   4 *   1 *  13 * -99 * 4.8 * 2.1 *   0 *   0 * 141 * 0.7 * 26. * 0.0 *   0 * 254 * 251 * 243 * -1. *
*   441960 * 0.4 * 0.6 * 128 * 214 * 0.9 * 127 * 124 *   1 * 198 *   4 *   5 *   1 *  15 * -99 * 70. * -0. *   0 *   0 * 131 * 0.4 * 8.9 * 0.3 *   0 * 165 * 250 * 236 * -0. *
*   442267 * 0.3 * 0.6 * 131 * 191 * 0.8 * 176 * 109 *   0 * 233 *   5 *   4 *   1 * -99 * -15 *   0 *   0 * 25. * -1. * 16. * -1. * 162 * 1.4 * 261 *   0 * 276 * 295 * 0.7 *
*   569282 * 0.3 * 0.6 * 127 * 314 * 0.8 * 240 * 77. *   0 * 213 *   5 *   4 *   1 *  15 * -99 * 205 * 0.5 *   0 *   0 * 115 * -0. * 13. * 2.0 *   0 * 105 * 183 * 305 * 0.1 *
******************************************************************************************************************************************************************************
==> 9 selected entries
(long long) 9
{% endhighlight %}

* bTagging might help to reach a better rejection of these bc events with more performant tagging algorithms / ~tighter WP
  * 2/3 events rejected moving from 70% to 60% bJet efficieny (-->49% to 36% signal efficiency at first order)
)
{% highlight sh %}
root [6] Nominal->Scan("EventWeight:mva28:mBB:pTB1:pTB2:b1Flav:b2Flav:MV2c10B1:MV2c10B2:MV2c10B1>0.934906:MV2c10B2>0.934906","EventWeight*(nJ==2)*(nTags==2)*(mva28>0.582)*(mva28<0.634)","precision=3 c****************************************************************************************************
*    Row   * Event * mva28 *   mBB *  pTB1 *  pTB2 * b1Fla * b2Fla * MV2c1 * MV2c1 * MV2c1 * MV2c1 *
****************************************************************************************************
*    36475 * 0.010 *  0.59 *   136 *   173 *   111 *     5 *     4 *   0.9 * 0.939 *     0 *     1 *
*    88337 * 0.335 * 0.621 *   120 *   137 *   100 *     5 *     5 * 0.985 * 0.864 *     1 *     0 *
*   184640 * 0.356 *  0.59 *   117 *   161 *  93.5 *     5 *     4 * 0.981 * 0.885 *     1 *     0 *
*   194481 * 0.238 * 0.631 *   117 *   135 *   106 *     5 *     5 * 0.999 * 0.842 *     1 *     0 *
*   212842 * 0.366 * 0.603 *   117 *   108 *  99.4 *     5 *     4 * 0.997 * 0.942 *     1 *     1 *
*   336228 * 0.311 * 0.587 *   118 *   148 *  96.5 *     5 *     4 * 0.998 * 0.964 *     1 *     1 *
*   441960 *  0.45 * 0.604 *   128 *   127 *   124 *     4 *     5 * 0.859 * 0.999 *     0 *     1 *
*   442267 * 0.322 * 0.608 *   131 *   176 *   109 *     5 *     4 * 0.857 * 0.874 *     0 *     0 *
*   569282 * 0.309 *  0.63 *   127 *   240 *  77.6 *     5 *     4 *     1 *  0.95 *     1 *     1 *
****************************************************************************************************
{% endhighlight %}

### 3 jets events
* majority of bc events
  * in half of the events, the other b is the 3rd jet is not even b labelled : one of the b is lost because of a very low transverse momentum
* 1/3 events have a reconstructed tau
)
{% highlight sh %}
root [70] Nominal->Scan("EventWeight:mva28:mBB:MET:dRBB:pTB1:pTB2:pTJ3:nTaus:TruthMET:b1Flav:b2Flav:j3Flav:nTruthNuW:lep_pdgId:alep_pdgId:lep.Pt():lep.Eta():alep.Pt():alep.Eta():b.Pt():b.Eta():ab.Pt():ab.Eta():nu.Pt():anu.Pt():top.Pt():atop.Pt():TVector2::Phi_mpi_pi(lep.Phi()-TruthMETp4.Phi())","EventWeight*(nJ==3)*(nTags==2)*(mva28>0.722)","precision=3 colsize=3")
{% endhighlight %}

![IMAGE](/images/q/AE147070C7669D4F1DB2FBE5341B3D62.jpg)
{% highlight sh %}
root [30] sqrt(0.263*0.263+0.223*0.223+0.505*0.505+0.596*0.596+0.386*0.386+0.449*0.449+0.444*0.444+0.207*0.207+0.286*0.286+0.324*0.324+0.264*0.264+0.292*0.292+0.344*0.344+0.378*0.378+0.306*0.306+0.492*0.492+0.409*0.409+0.312*0.312+0.565*0.565+0.332*0.332+0.453*0.453+0.311*0.311+0.351*0.351+0.585*0.585+0.376*0.376)
(double) 1.964988
{% endhighlight %}

* bTagging might help to reach a better rejection of these bc events with more performant tagging algorithms / ~tighter WP
  * 14/25 events rejected moving from 70% to 60% bJet efficieny (-->49% to 36% signal efficiency at first order)
)
{% highlight sh %}
root [7] Nominal->Scan("EventWeight:mva28:mBB:pTB1:pTB2:b1Flav:b2Flav:MV2c10B1:MV2c10B2:MV2c10B1>0.934906:MV2c10B2>0.934906","EventWeight*(nJ==3)*(nTags==2)*(mva28>0.722)","precision=3 colsize=5")
****************************************************************************************************
*    Row   * Event * mva28 *   mBB *  pTB1 *  pTB2 * b1Fla * b2Fla * MV2c1 * MV2c1 * MV2c1 * MV2c1 *
****************************************************************************************************
*    38467 * 0.263 * 0.728 *   121 *   250 *  87.7 *     5 *     4 *  0.98 * 0.876 *     1 *     0 *
*    84770 * 0.223 *  0.76 *   130 *   192 *   126 *     5 *     5 * 0.893 *     1 *     0 *     1 *
*    96751 * 0.505 * 0.736 *   134 *   185 *   161 *     4 *     5 * 0.888 * 0.915 *     0 *     0 *
*   123323 * 0.596 * 0.865 *   126 *   407 *   151 *     5 *     0 * 0.975 * 0.938 *     1 *     1 *
*   147958 * 0.386 *  0.82 *   122 *   218 *  96.8 *     4 *     5 * 0.978 *  0.99 *     1 *     1 *
*   166951 * 0.449 * 0.996 *   130 *   328 *   201 *     0 *     5 * 0.844 * 0.846 *     0 *     0 *
*   167305 * 0.444 * 0.762 *   131 *   189 *  98.1 *     4 *     5 * 0.962 *     1 *     1 *     1 *
*   210108 * 0.207 * 0.807 *   125 *   230 *   180 *     5 *     5 * 0.904 * 0.943 *     0 *     1 *
*   211575 * 0.286 * 0.731 *   124 *   182 *   123 *     5 *     4 * 0.997 * 0.976 *     1 *     1 *
*   234945 * 0.324 * 0.776 *   130 *   141 *   106 *     4 *     5 * 0.948 *     1 *     1 *     1 *
*   239503 * 0.264 * 0.726 *   130 *   127 *  92.9 *     5 *     5 * 0.993 * 0.999 *     1 *     1 *
*   274446 * 0.292 * 0.797 *   135 *   458 *  85.9 *     5 *     4 * 0.995 * 0.909 *     1 *     0 *
*   279607 * 0.344 * 0.726 *   132 *   224 *  98.6 *     5 *     4 * 0.996 * 0.927 *     1 *     0 *
*   377978 * 0.378 * 0.723 *   116 *   234 *  85.4 *     4 *     5 * 0.968 *     1 *     1 *     1 *
*   393459 * 0.306 * 0.736 *   130 *   151 *   118 *     4 *     5 * 0.956 * 0.939 *     1 *     1 *
*   424172 * 0.492 * 0.725 *   128 *   131 *   130 *     4 *     5 *  0.94 * 0.911 *     1 *     0 *
*   437517 * 0.409 * 0.733 *   118 *   139 *   133 *     0 *     5 * 0.954 * 0.936 *     1 *     1 *
*   449314 * 0.312 * 0.761 *   120 *   185 *   132 *     4 *     5 * 0.894 * 0.845 *     0 *     0 *
*   453195 * 0.565 * 0.734 *   124 *   182 *  91.9 *     5 *     4 *     1 * 0.984 *     1 *     1 *
*   458060 * 0.332 *  0.75 *   125 *   138 *  95.4 *     4 *     5 * 0.925 *     1 *     0 *     1 *
*   487670 * 0.453 * 0.746 *   123 *   148 *   113 *     0 *     5 * 0.934 * 0.985 *     0 *     1 *
*   493000 * 0.311 * 0.722 *   121 *   141 *  92.6 *     5 *     5 * 0.977 * 0.999 *     1 *     1 *
*   515224 * 0.351 * 0.976 *   119 *   244 *   225 *     5 *     4 *     1 * 0.846 *     1 *     0 *
*   567323 * 0.585 * 0.802 *   120 *   286 *  78.3 *     5 *     4 * 0.968 * 0.837 *     1 *     0 *
*   570103 * 0.376 * 0.876 *   136 *   238 *   224 *     5 *     0 * 0.997 * 0.834 *     1 *     0 *
{% endhighlight %}

## single top Wt
)
### 2 jets events
* contains almost only bc events
* ~half of the events have a reconstructed tau
)
**1rst BDT bin**
)
{% highlight sh %}
root [6] Nominal->Scan("EventWeight:mva28:mBB:MET:dRBB:pTB1:pTB2:nTaus:TruthMET:b1Flav:b2Flav:nTruthNuW:lep_pdgId:alep_pdgId:lep.Pt():lep.Eta():alep.Pt():alep.Eta():b.Pt():b.Eta():ab.Pt():ab.Eta():nu.Pt():anu.Pt():top.Pt():atop.Pt():TVector2::Phi_mpi_pi(lep.Phi()-TruthMETp4.Phi())","EventWeight*(nJ==2)*(nTags==2)*(mva28>0.634)","precision=3 colsize=3")
Error in <TTreeFormula::Compile>:  Bad numerical expression : "atop.Pt()"
******************************************************************************************************************************************************************************
*    Row   * Eve * mva * mBB * MET * dRB * pTB * pTB * nTa * Tru * b1F * b2F * nTr * lep * ale * lep * lep * ale * ale * b.P * b.E * ab. * ab. * nu. * anu * top * ato * TVe *
******************************************************************************************************************************************************************************
*     6692 * 0.2 * 0.6 * 122 * 326 * 0.7 * 252 * 100 *   0 * 74. *   5 *   5 *   2 *  13 * -15 * 262 * -0. * 10. * -1. * 102 * -0. * 258 * -0. * 10. * 86. * 122 *     * 0.1 *
*    14034 * 0.5 * 0.7 * 126 * 214 * 0.7 * 189 * 157 *   1 * 257 *   4 *   5 *   1 *  15 * -99 * 220 * 0.5 *   0 *   0 * 171 * -0. *   0 *   0 *   0 * 136 * 347 *     * 0.1 *
*    19646 * 0.2 * 0.6 * 119 * 299 * 0.8 * 168 * 120 *   0 * 308 *   5 *   4 *   1 *  15 * -99 * 15. * -1. *   0 *   0 * 139 * -1. *   0 *   0 *   0 * 290 * 247 *     * 0.2 *
*    29815 * 0.4 * 0.7 * 131 * 398 * 0.6 * 287 * 139 *   0 * 388 *   5 *   4 *   1 *  13 * -99 * 5.6 * 1.1 *   0 *   0 * 287 * -1. *   0 *   0 *   0 * 388 * 430 *     * -0. *
*    42495 * 0.3 * 0.7 * 118 * 452 * 0.5 * 218 * 185 *   1 * 409 *   4 *   5 *   1 *  15 * -99 * 384 * -1. *   0 *   0 * 186 * -1. * 14. * -3. *   0 * 52. * 427 *     * 0.0 *
******************************************************************************************************************************************************************************
==> 5 selected entries
(long long) 5
{% endhighlight %}

{% highlight sh %}
root [3] sqrt(0.285*0.285+0.578*0.578+0.277*0.277+0.465*0.465+0.314*0.314)
(double) 0.898253
{% endhighlight %}

**2nd BDT bin**
)
{% highlight sh %}
root [7] Nominal->Scan("EventWeight:mva28:mBB:MET:dRBB:pTB1:pTB2:nTaus:TruthMET:b1Flav:b2Flav:nTruthNuW:lep_pdgId:alep_pdgId:lep.Pt():lep.Eta():alep.Pt():alep.Eta():b.Pt():b.Eta():ab.Pt():ab.Eta():nu.Pt():anu.Pt():top.Pt():atop.Pt():TVector2::Phi_mpi_pi(lep.Phi()-TruthMETp4.Phi())","EventWeight*(nJ==2)*(nTags==2)*(mva28>0.582&&mva28<0.634)","precision=3 colsize=3")
Error in <TTreeFormula::Compile>:  Bad numerical expression : "atop.Pt()"
******************************************************************************************************************************************************************************
*    Row   * Eve * mva * mBB * MET * dRB * pTB * pTB * nTa * Tru * b1F * b2F * nTr * lep * ale * lep * lep * ale * ale * b.P * b.E * ab. * ab. * nu. * anu * top * ato * TVe *
******************************************************************************************************************************************************************************
*    24890 * 0.2 * 0.6 * 127 * 182 * 1.1 * 116 * 112 *   0 * 194 *   5 *   5 *   1 *  15 * -99 * 50. * -1. *   0 *   0 * 117 * -2. * 63. * -2. *   0 * 178 * 144 *     * -0. *
*    54509 * 0.2 * 0.5 * 117 * 182 * 0.9 * 229 * 69. *   1 * 241 *   5 *   4 *   1 *  15 * -99 * 212 * -1. *   0 *   0 * 215 * -0. * 20. * 0.2 *   0 * 83. * 242 *     * 0.1 *
******************************************************************************************************************************************************************************
==> 2 selected entries
(long long) 2
{% endhighlight %}

* bTagging might help to reach a better rejection of these bc events with more performant tagging algorithms / ~tighter WP
  * 6/7 events rejected moving from 70% to 60% bJet efficieny (-->49% to 36% signal efficiency at first order)
)
{% highlight sh %}
root [1] Nominal->Scan("EventWeight:mva28:mBB:pTB1:pTB2:b1Flav:b2Flav:MV2c10B1:MV2c10B2:MV2c10B1>0.934906:MV2c10B2>0.934906","EventWeight*(nJ==2)*(nTags==2)*(mva28>0.582)","precision=3 colsize=5")
****************************************************************************************************
*    Row   * Event * mva28 *   mBB *  pTB1 *  pTB2 * b1Fla * b2Fla * MV2c1 * MV2c1 * MV2c1 * MV2c1 *
****************************************************************************************************
*     6692 * 0.285 * 0.644 *   122 *   252 *   100 *     5 *     5 * 0.985 * 0.993 *     1 *     1 *
*    14034 * 0.578 * 0.721 *   126 *   189 *   157 *     4 *     5 * 0.875 * 0.995 *     0 *     1 *
*    19646 * 0.277 * 0.666 *   119 *   168 *   120 *     5 *     4 * 0.927 * 0.986 *     0 *     1 *
*    24890 * 0.216 * 0.625 *   127 *   116 *   112 *     5 *     5 * 0.934 * 0.993 *     0 *     1 *
*    29815 * 0.465 * 0.726 *   131 *   287 *   139 *     5 *     4 * 0.999 * 0.881 *     1 *     0 *
*    42495 * 0.314 *  0.71 *   118 *   218 *   185 *     4 *     5 * 0.832 * 0.946 *     0 *     1 *
*    54509 * 0.277 * 0.591 *   117 *   229 *  69.3 *     5 *     4 * 0.999 * 0.872 *     1 *     0 *
****************************************************************************************************
{% endhighlight %}

### 3 jets events
* majority of bb events, with 3rd jet light-labelled
* most events have a reconstructed tau
)
{% highlight sh %}
root [8] Nominal->Scan("EventWeight:mva28:mBB:MET:dRBB:pTB1:pTB2:pTJ3:nTaus:TruthMET:b1Flav:b2Flav:j3Flav:nTruthNuW:lep_pdgId:alep_pdgId:lep.Pt():lep.Eta():alep.Pt():alep.Eta():b.Pt():b.Eta():ab.Pt():ab.Eta():nu.Pt():anu.Pt():top.Pt():atop.Pt():TVector2::Phi_mpi_pi(lep.Phi()-TruthMETp4.Phi())","EventWeight*(nJ==3)*(nTags==2)*(mva28>0.722)","precision=3 colsize=3")
{% endhighlight %}

![IMAGE](/images/q/ED85D5A96806E142E9BD77BBC29CF75F.jpg)
{% highlight sh %}
root [4] sqrt(0.213*0.213+0.432*0.432+0.213*0.213+0.363*0.363+0.218*0.218+0.307*0.307)
(double) 0.742229
{% endhighlight %}

* bTagging might help to reach a better rejection of these bc events with more performant tagging algorithms / ~tighter WP
  * 4/6 events rejected moving from 70% to 60% bJet efficieny (-->49% to 36% signal efficiency at first order)
)
{% highlight sh %}
****************************************************************************************************
*    Row   * Event * mva28 *   mBB *  pTB1 *  pTB2 * b1Fla * b2Fla * MV2c1 * MV2c1 * MV2c1 * MV2c1 *
****************************************************************************************************
*    16814 * 0.213 * 0.793 *   115 *   151 *   149 *     5 *     5 * 0.996 * 0.888 *     1 *     0 *
*    19440 * 0.432 * 0.875 *   119 *   172 *   169 *     4 *     5 * 0.941 *     1 *     1 *     1 *
*    41728 * 0.213 * 0.952 *   127 *   227 *   224 *     5 *     5 * 0.885 * 0.999 *     0 *     1 *
*    48002 * 0.363 * 0.762 *   127 *   271 *  70.7 *     5 *     5 * 0.974 * 0.999 *     1 *     1 *
*    55299 * 0.218 * 0.759 *   119 *   219 *  81.7 *     5 *     5 * 0.888 *     1 *     0 *     1 *
*    56366 * 0.307 * 0.774 *   130 *   140 *   207 *     4 *     5 * 0.934 * 0.909 *     0 *     0 *
****************************************************************************************************
{% endhighlight %}

