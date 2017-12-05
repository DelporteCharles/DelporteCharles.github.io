---
title: Z+jet filter strategy
date: '2017-10-04'
tags: []
---
# Purpose
What filtering strategy (pTV or Max(HT,pTV)) is the most interesting for 0-lepton ?
--> A priori pTV (MET) because we trigger on MET and produce CxAODs with MET>140

# Yield files

Major observations : Efficiency in Maker Derivations is much higher with the pTV filter
* visible in the ratio Out/In in the pTV and MAXHtPTV filtered samples of CxAOD26

# ChannelNumber / Sample name

## Sherpa 22

{% highlight javascript %}
363364        Sherpa_NNPDF30NNLO_Zmumu_Pt0_70_CVetoBVeto
363365        Sherpa_NNPDF30NNLO_Zmumu_Pt0_70_CFilterBVeto
363366        Sherpa_NNPDF30NNLO_Zmumu_Pt0_70_BFilter
363367        Sherpa_NNPDF30NNLO_Zmumu_Pt70_140_CVetoBVeto
363368        Sherpa_NNPDF30NNLO_Zmumu_Pt70_140_CFilterBVeto
363369        Sherpa_NNPDF30NNLO_Zmumu_Pt70_140_BFilter
363370        Sherpa_NNPDF30NNLO_Zmumu_Pt140_280_CVetoBVeto
363371        Sherpa_NNPDF30NNLO_Zmumu_Pt140_280_CFilterBVeto
363372        Sherpa_NNPDF30NNLO_Zmumu_Pt140_280_BFilter
363373        Sherpa_NNPDF30NNLO_Zmumu_Pt280_500_CVetoBVeto
363374        Sherpa_NNPDF30NNLO_Zmumu_Pt280_500_CFilterBVeto
363375        Sherpa_NNPDF30NNLO_Zmumu_Pt280_500_BFilterBVeto
363376        Sherpa_NNPDF30NNLO_Zmumu_Pt500_700_CVetoBVeto
363377        Sherpa_NNPDF30NNLO_Zmumu_Pt500_700_CFilterBVeto
363378        Sherpa_NNPDF30NNLO_Zmumu_Pt500_700_BFilter
363379        Sherpa_NNPDF30NNLO_Zmumu_Pt700_1000_CVetoBVeto
363380        Sherpa_NNPDF30NNLO_Zmumu_Pt700_1000_CFilterBVeto
363381        Sherpa_NNPDF30NNLO_Zmumu_Pt700_1000_BFilter
363382        Sherpa_NNPDF30NNLO_Zmumu_Pt1000_2000_CVetoBVeto
363383        Sherpa_NNPDF30NNLO_Zmumu_Pt1000_2000_CFilterBVeto
363384        Sherpa_NNPDF30NNLO_Zmumu_Pt1000_2000_BFilter
363385        Sherpa_NNPDF30NNLO_Zmumu_Pt2000_E_CMS_CVetoBVeto
363386        Sherpa_NNPDF30NNLO_Zmumu_Pt2000_E_CMS_CFilterBVet
363387        Sherpa_NNPDF30NNLO_Zmumu_Pt2000_E_CMS_BFilter
363388        Sherpa_NNPDF30NNLO_Zee_Pt0_70_CVetoBVeto
363389        Sherpa_NNPDF30NNLO_Zee_Pt0_70_CFilterBVeto
363390        Sherpa_NNPDF30NNLO_Zee_Pt0_70_BFilter
363391        Sherpa_NNPDF30NNLO_Zee_Pt70_140_CVetoBVeto
363392        Sherpa_NNPDF30NNLO_Zee_Pt70_140_CFilterBVeto
363393        Sherpa_NNPDF30NNLO_Zee_Pt70_140_BFilter
363394        Sherpa_NNPDF30NNLO_Zee_Pt140_280_CVetoBVeto
363395        Sherpa_NNPDF30NNLO_Zee_Pt140_280_CFilterBVeto
363396        Sherpa_NNPDF30NNLO_Zee_Pt140_280_BFilter
363397        Sherpa_NNPDF30NNLO_Zee_Pt280_500_CVetoBVeto
363398        Sherpa_NNPDF30NNLO_Zee_Pt280_500_CFilterBVeto
363399        Sherpa_NNPDF30NNLO_Zee_Pt280_500_BFilterBVeto
363400        Sherpa_NNPDF30NNLO_Zee_Pt500_700_CVetoBVeto
363401        Sherpa_NNPDF30NNLO_Zee_Pt500_700_CFilterBVeto
363402        Sherpa_NNPDF30NNLO_Zee_Pt500_700_BFilter
363403        Sherpa_NNPDF30NNLO_Zee_Pt700_1000_CVetoBVeto
363404        Sherpa_NNPDF30NNLO_Zee_Pt700_1000_CFilterBVeto
363405        Sherpa_NNPDF30NNLO_Zee_Pt700_1000_BFilter
363406        Sherpa_NNPDF30NNLO_Zee_Pt1000_2000_CVetoBVeto
363407        Sherpa_NNPDF30NNLO_Zee_Pt1000_2000_CFilterBVeto
363408        Sherpa_NNPDF30NNLO_Zee_Pt1000_2000_BFilter
363409        Sherpa_NNPDF30NNLO_Zee_Pt2000_E_CMS_CVetoBVeto
363410        Sherpa_NNPDF30NNLO_Zee_Pt2000_E_CMS_CFilterBVet
363411        Sherpa_NNPDF30NNLO_Zee_Pt2000_E_CMS_BFilter
363361        Sherpa_NNPDF30NNLO_Ztautau_Pt0_70_CVetoBVeto
363362        Sherpa_NNPDF30NNLO_Ztautau_Pt0_70_CFilterBVeto
363363        Sherpa_NNPDF30NNLO_Ztautau_Pt0_70_BFilter
363102        Sherpa_NNPDF30NNLO_Ztautau_Pt70_140_CVetoBVeto
363103        Sherpa_NNPDF30NNLO_Ztautau_Pt70_140_CFilterBVeto
363104        Sherpa_NNPDF30NNLO_Ztautau_Pt70_140_BFilter
363105        Sherpa_NNPDF30NNLO_Ztautau_Pt140_280_CVetoBVeto
363106        Sherpa_NNPDF30NNLO_Ztautau_Pt140_280_CFilterBVeto
363107        Sherpa_NNPDF30NNLO_Ztautau_Pt140_280_BFilter
363108        Sherpa_NNPDF30NNLO_Ztautau_Pt280_500_CVetoBVeto
363109        Sherpa_NNPDF30NNLO_Ztautau_Pt280_500_CFilterBVeto
363110        Sherpa_NNPDF30NNLO_Ztautau_Pt280_500_BFilterBVeto
363111        Sherpa_NNPDF30NNLO_Ztautau_Pt500_700_CVetoBVeto
363112        Sherpa_NNPDF30NNLO_Ztautau_Pt500_700_CFilterBVeto
363113        Sherpa_NNPDF30NNLO_Ztautau_Pt500_700_BFilter
363114        Sherpa_NNPDF30NNLO_Ztautau_Pt700_1000_CVetoBVeto
363115        Sherpa_NNPDF30NNLO_Ztautau_Pt700_1000_CFilterBVeto
363116        Sherpa_NNPDF30NNLO_Ztautau_Pt700_1000_BFilter
363117        Sherpa_NNPDF30NNLO_Ztautau_Pt1000_2000_CVetoBVeto
363118        Sherpa_NNPDF30NNLO_Ztautau_Pt1000_2000_CFilterBVeto
363119        Sherpa_NNPDF30NNLO_Ztautau_Pt1000_2000_BFilter
363120        Sherpa_NNPDF30NNLO_Ztautau_Pt2000_E_CMS_CVetoBVeto
363121        Sherpa_NNPDF30NNLO_Ztautau_Pt2000_E_CMS_CFilterBVeto
363122        Sherpa_NNPDF30NNLO_Ztautau_Pt2000_E_CMS_BFilter
363412        Sherpa_NNPDF30NNLO_Znunu_Pt0_70_CVetoBVeto
363413        Sherpa_NNPDF30NNLO_Znunu_Pt0_70_CFilterBVeto
363414        Sherpa_NNPDF30NNLO_Znunu_Pt0_70_BFilter
363415        Sherpa_NNPDF30NNLO_Znunu_Pt70_140_CVetoBVeto
363416        Sherpa_NNPDF30NNLO_Znunu_Pt70_140_CFilterBVeto
363417        Sherpa_NNPDF30NNLO_Znunu_Pt70_140_BFilter
363418        Sherpa_NNPDF30NNLO_Znunu_Pt140_280_CVetoBVeto
363419        Sherpa_NNPDF30NNLO_Znunu_Pt140_280_CFilterBVeto
363420        Sherpa_NNPDF30NNLO_Znunu_Pt140_280_BFilter
363421        Sherpa_NNPDF30NNLO_Znunu_Pt280_500_CVetoBVeto
363422        Sherpa_NNPDF30NNLO_Znunu_Pt280_500_CFilterBVeto
363423        Sherpa_NNPDF30NNLO_Znunu_Pt280_500_BFilter
363424        Sherpa_NNPDF30NNLO_Znunu_Pt500_700_CVetoBVeto
363425        Sherpa_NNPDF30NNLO_Znunu_Pt500_700_CFilterBVeto
363426        Sherpa_NNPDF30NNLO_Znunu_Pt500_700_BFilter
363427        Sherpa_NNPDF30NNLO_Znunu_Pt700_1000_CVetoBVeto
363428        Sherpa_NNPDF30NNLO_Znunu_Pt700_1000_CFilterBVeto
363429        Sherpa_NNPDF30NNLO_Znunu_Pt700_1000_BFilter
363430        Sherpa_NNPDF30NNLO_Znunu_Pt1000_2000_CVetoBVeto
363431        Sherpa_NNPDF30NNLO_Znunu_Pt1000_2000_CFilterBVeto
363432        Sherpa_NNPDF30NNLO_Znunu_Pt1000_2000_BFilter
363433        Sherpa_NNPDF30NNLO_Znunu_Pt2000_E_CMS_CVetoBVeto
363434        Sherpa_NNPDF30NNLO_Znunu_Pt2000_E_CMS_CFilterBVeto
363435        Sherpa_NNPDF30NNLO_Znunu_Pt2000_E_CMS_BFilter
{% endhighlight %}

## Sherpa 221

{% highlight javascript %}
364100        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV0_70_CVetoBVeto
364101        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV0_70_CFilterBVeto
364102        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV0_70_BFilter
364103        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV70_140_CVetoBVeto
364104        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV70_140_CFilterBVeto
364105        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV70_140_BFilter
364106        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV140_280_CVetoBVeto
364107        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV140_280_CFilterBVeto
364108        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV140_280_BFilter
364109        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV280_500_CVetoBVeto
364110        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV280_500_CFilterBVeto
364111        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV280_500_BFilter
364112        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV500_1000
364113        Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV1000_E_CMS
364114        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV0_70_CVetoBVeto
364115        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV0_70_CFilterBVeto
364116        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV0_70_BFilter
364117        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV70_140_CVetoBVeto
364118        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV70_140_CFilterBVeto
364119        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV70_140_BFilter
364120        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV140_280_CVetoBVeto
364121        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV140_280_CFilterBVeto
364122        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV140_280_BFilter
364123        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV280_500_CVetoBVeto
364124        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV280_500_CFilterBVeto
364125        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV280_500_BFilter
364126        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV500_1000
364127        Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV1000_E_CMS
364128        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV0_70_CVetoBVeto
364129        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV0_70_CFilterBVeto
364130        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV0_70_BFilter
364131        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV70_140_CVetoBVeto
364132        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV70_140_CFilterBVeto
364133        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV70_140_BFilter
364134        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV140_280_CVetoBVeto
364135        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV140_280_CFilterBVeto
364136        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV140_280_BFilter
364137        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV280_500_CVetoBVeto
364138        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV280_500_CFilterBVeto
364139        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV280_500_BFilter
364140        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV500_1000
364141        Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV1000_E_CMS
364142        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_CVetoBVeto
364143        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_CFilterBVeto
364144        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_BFilter
364145        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_CVetoBVeto
364146        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_CFilterBVeto
364147        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_BFilter
364148        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_CVetoBVeto
364149        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_CFilterBVeto
364150        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_BFilter
364151        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_CVetoBVeto
364152        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_CFilterBVeto
364153        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_BFilter
364154        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV500_1000
364155        Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV1000_E_CMS
{% endhighlight %}

## Madgraph

{% highlight javascript %}
361515   7518.4             1.2283         1.0            Z_MG               mc15_13TeV.361515.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np0
361516   1200.1             1.2283         1.0            Z_MG               mc15_13TeV.361516.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np1
361517   387.16             1.2283         1.0            Z_MG               mc15_13TeV.361517.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np2
361518   110.08             1.2283         1.0            Z_MG               mc15_13TeV.361518.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np3
361519   43.389             1.2283         1.0            Z_MG               mc15_13TeV.361519.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np4
{% endhighlight %}

## CxAOD26

### PTV Filter
| DSID   | In Maker     | Out Maker    | Weight          | Sample                      | Out/In       | XSection pb  |
| ------ | ------- | ------- | --------------- | --------------------------- | ------------ | ------------ |
| 363412 | 7952000 | 801     | 5267767.595836  | PTV_0_70_CVetoBVeto         |  0.000100729 |    1.122e+04 |
| 363413 | 4941000 | 999     | 2895544.753176  | PTV_0_70_CFilterBVeto       |  0.000202186 |    1.122e+04 |
| 363414 | 4927000 | 952     | 2613355.412099  | PTV_0_70_BFilter            |  0.000193221 |    1.122e+04 |
| 363415 | 2967000 | 123987  | 1376663.700830  | PTV_70_140_CVetoBVeto       |  0.0417887   |        404.0 |
| 363416 | 1980000 | 100793  | 1015015.028485  | PTV_70_140_CFilterBVeto     |  0.0509056   |        404.0 |
| 363417 | 2471000 | 111906  | 1262467.293281  | PTV_70_140_BFilter          |  **0.0452877**   |        404.0 |
| 363418 | 1946000 | 1240781 | 1068596.120936  | PTV_140_280_CVetoBVeto      |  0.637606    |        62.21 |
| 363419 | 1903000 | 1306642 | 1230026.079352  | PTV_140_280_CFilterBVeto    |  0.686622    |        62.21 |
| 363420 | 1983000 | 1275761 | 1359566.754346  | PTV_140_280_BFilter         |  **0.643349**    |        62.21 |
| 363421 | 1480000 | 1434245 | 944456.868093   | PTV_280_500_CVetoBVeto      |  0.969084    |        4.612 |
| 363422 | 991000  | 966928  | 746432.061863   | PTV_280_500_CFilterBVeto    |  0.975709    |        4.612 |
| 363423 | 984000  | 949039  | 814451.400598   | PTV_280_500_BFilter         |  **0.964471**    |        4.612 |
| 363424 | 989000  | 977446  | 714282.064698   | PTV_500_700_CVetoBVeto      |  0.988317    |       0.2871 |
| 363425 | 589000  | 582735  | 475752.457689   | PTV_500_700_CFilterBVeto    |  0.989363    |       0.2871 |
| 363426 | 591000  | 580434  | 526420.666568   |  PTV_500_700_BFilter        |  0.982122    |       0.2871 |
| 363427 | 150000  | 148277  | 101000.461664   |  PTV_700_1000_CVetoBVeto    |  0.988513    |      0.05102 |
| 363428 | 97000   |  95878  |  80945.344066   |  PTV_700_1000_CFilterBVeto  |  0.988433    |      0.05102 |
| 363429 | 99000   |  97283  |  89527.868552   | PTV_700_1000_BFilter        |  0.982657    |      0.05102 |
| 363430 | 99000   |  97331  |  72869.703318   | PTV_1000_2000_CVetoBVeto    |  0.983141    |     0.006491 |
| 363431 | 50000   |  49190  |  42122.993251   | PTV_1000_2000_CFilterBVeto  |  0.9838      |     0.006491 |
| 363432 | 50000   |  48916  |  44874.128457   | PTV_1000_2000_BFilter       |  0.97832     |     0.006491 |
| 363433 | 49000   |  47321  |  26411.386037   | PTV_2000_E_CMS_CVetoBVeto   |  0.965735    |    2.429e-05 |
| 363434 | 30000   |  29175  |  21409.903714   | PTV_2000_E_CMS_CFilterBVeto |  0.9725      |    2.429e-05 |
| 363435 | 5000    |   4839  |   3675.361879   | PTV_2000_E_CMS_BFilter      |  0.9678      |    2.429e-05 |

### MAXHTPTV Filter

| DSID   | In      | Out | Weight | Sample | Efficiency Out/In |
| ------ | ------- | --- | ------ | ------ | ----------------- |
| 364142 | 9923000 | 653 | 6556534.009083 | MAXHTPTV0_70_CVetoBVeto |  6.58067e-05 |
| 364143 | 7881000 | 963 | 4469945.171151 | MAXHTPTV0_70_CFilterBVeto |  0.000122193 |
| 364144 | 7926800 | 811 | 4001217.033898 | MAXHTPTV0_70_BFilter |  0.000102311 |
| 364145 | 14805000 | 207497 | 5324654.434868 | MAXHTPTV70_140_CVetoBVeto |  0.0140153 |
| 364146 | 14763800 | 223184 | 5348559.595827 | MAXHTPTV70_140_CFilterBVeto |  0.015117 |
| 364147 | 19728500 | 252213 | 6908641.604304 | MAXHTPTV70_140_BFilter |  **0.0127842** |
| 364148 | 14822800 | 3128015 | 8786406.073091 | MAXHTPTV140_280_CVetoBVeto |  0.211027 |
| 364149 | 12364500 | 2395253 | 8200906.721326 | MAXHTPTV140_280_CFilterBVeto |  0.19372 |
| 364150 | 9864900 | 1667032 | 6840968.190181 | MAXHTPTV140_280_BFilter |  **0.168986** |
| 364151 | 4937400 | 1946370 | 4262731.737315 | MAXHTPTV280_500_CVetoBVeto |  0.39421 |
| 364152 | 3445500 | 1207082 | 3174769.384160 | MAXHTPTV280_500_CFilterBVeto |  0.350336 |
| 364153 | 8887350 | 2913958 | 8353354.671824 | MAXHTPTV280_500_BFilter |  **0.327877** |
| 364154 | 9869000 | 4124030 | 9812913.476152 | MAXHTPTV500_1000 |  0.417877 |
| 364155 | 100000 | 50308 | 102593.592347 | MAXHTPTV1000_E_CMS |  0.50308 |

## CxAOD 28

| DSID   | In      | Out | Weight | Sample | Efficiency Out/In |
| ------ | ------- | --- | ------ | ------ | ----------------- |
| 364142 | 9923000.0 | 633.0 | 6556534.00908 |  MAXHTPTV0_70_CVetoBVeto |  6.37912e-05 |
| 364143 | 7881000.0 | 928.0 | 4469945.17115 |  MAXHTPTV0_70_CFilterBVeto |  0.000117752 |
| 364144 | 7926800.0 | 774.0 | 4001217.0339 |  MAXHTPTV0_70_BFilter |  9.76434e-05 |
| 364145 | 14805000.0 | 206084.0 | 5324654.43487 |  MAXHTPTV70_140_CVetoBVeto |  0.0139199 |
| 364146 | 14763800.0 | 218605.0 | 5348559.59583 |  MAXHTPTV70_140_CFilterBVeto |  0.0148068 |
| 364147 | 19728500.0 | 249878.0 | 6908641.6043 |  MAXHTPTV70_140_BFilter |  0.0126658 |
| 364148 | 14822800.0 | 3128989.0 | 8786406.07309 |  MAXHTPTV140_280_CVetoBVeto |  0.211093 |
| 364149 | 12364500.0 | 2388315.0 | 8200906.72133 |  MAXHTPTV140_280_CFilterBVeto |  0.193159 |
| 364150 | 19745300.0 | 3334939.0 | 13694888.3195 |  MAXHTPTV140_280_BFilter |  0.168898 |
| 364151 | 4937400.0 | 1947041.0 | 4262731.73731 |  MAXHTPTV280_500_CVetoBVeto |  0.394345 |
| 364152 | 3445500.0 | 1207024.0 | 3174769.38416 |  MAXHTPTV280_500_CFilterBVeto |  0.350319 |
| 364153 | 8887350.0 | 2914715.0 | 8353354.67182 |  MAXHTPTV280_500_BFilter |  0.327962 |
| 364154 | 9869000.0 | 4125521.0 | 9812913.47615 |  MAXHTPTV500_1000 |  0.418028 |
| 364155 | 4951000.0 | 2496530.0 | 5077324.08866 |  MAXHTPTV1000_E_CMS |  0.504248 |

# Reader selection yields, Valerio style table

{% highlight javascript %}
# awk instruction
less plots_ZJet_CxAOD26_Sherpa22/yield_2tag2jet_150ptv_SR_clean.txt | awk 'BEGIN {totalErr2=0} {totalErr2+=$4*$4; print $0 "      " $3/1659.93*100 "        " $4*$4/3130.19} END{print "totalErr2 = " sqrt(totalErr2)}'
{% endhighlight %}

## CxAOD 26

### Sherpa 22

{% highlight javascript %}
* 2 jets

sampleName       entries         integral         error  error/integ.      Fraction of total yield %   Fraction of total error^2 

Zv22_363104             5          3.5061       1.74353      0.497284      0.21122                     0.0971154              
Zv22_363105             1         1.51463       1.51463             1      0.0912466                   0.0732896              
Zv22_363106             1         2.37666       2.37666             1      0.143178                    0.180453              
Zv22_363107            33         8.40973       2.49863      0.297112      0.506632                    0.19945              
Zv22_363109             1         0.16825       0.16825             1      0.010136                    0.000904356              
Zv22_363110           130         2.02866      0.298527      0.147155      0.122214                    0.00284706              
Zv22_363112             1      0.00584871    0.00584871             1      0.000352347                 1.09282e-06              
Zv22_363113            27       0.0683804     0.0175172      0.256173      0.00411947                  9.80299e-06              
Zv22_363369             1        0.153216      0.153216             1      0.00923027                  0.000749959              
Zv22_363372           127          2.7304      0.415626      0.152221      0.164489                    0.00551867              
Zv22_363375            10        0.128108      0.114512      0.893864      0.00771767                  0.00041892              
Zv22_363416             1         35.1421       35.1421             1      2.11708                     39.4534              
Zv22_363417           130         117.384       18.3471        0.1563      7.07162                     10.7539              
Zv22_363418             4         34.6557       21.2289      0.612565      2.08778                     14.3974              
Zv22_363419           104         95.9347       18.7216      0.195149      5.77944                     11.1973              
Zv22_363420          7802         1218.64       26.8702     0.0220493      73.4151                     23.0659              
Zv22_363421             6       -0.220455       1.15169      -5.22416      -0.013281                   0.0423741              
Zv22_363422            73         8.35735       2.18509      0.261457      0.503476                    0.152534              
Zv22_363423          5242         124.265        3.4244     0.0275572      7.48616                     0.374626              
Zv22_363424             3       0.0445619     0.0575149       1.29067      0.00268457                  0.000105679              
Zv22_363425            23        0.172965     0.0781493      0.451822      0.01042                     0.00019511              
Zv22_363426          1643         3.87886      0.197005     0.0507894      0.233676                    0.00123989              
Zv22_363428             1       0.0183582     0.0183582             1      0.00110596                  1.07669e-05              
Zv22_363429           183        0.505213     0.0706112      0.139765      0.0304358                   0.000159286              
Zv22_363431             4      0.00672931    0.00936126       1.39112      0.000405397                 2.79961e-06              
Zv22_363432            62       0.0506529    0.00907181      0.179098      0.00305151                  2.62916e-06              
Zv22_363434             2     9.78395e-05   6.91847e-05      0.707125      5.89419e-06                 1.52915e-10              
Zv22_363435             4     0.000271956   0.000183997      0.676569      1.63836e-05                 1.08156e-09                

bkg:          15624       1659.93      100        0
totalStatErr = 55.9481
{% endhighlight %}

{% highlight javascript %}
* 3 jets

sampleName       entries         integral         error  error/integ.      Fraction of total yield %   Fraction of total error^2 
   
Zv22_363104             7       2.93961       1.49476       0.50849        0.110786                      0.0769655
Zv22_363107            51       19.3049         4.077      0.211189        0.727548                      0.572578
Zv22_363109             4      0.356358      0.181865      0.510345        0.0134301                     0.00113933
Zv22_363110           210       3.28583      0.297812     0.0906351        0.123834                      0.00305518
Zv22_363112             4     0.0456029     0.0250728      0.549807        0.00171865                    2.1655e-05
Zv22_363113            64      0.177331     0.0296053      0.166949        0.00668311                    3.0192e-05
Zv22_363116             3    0.00147912    0.00767338        5.1878        5.57439e-05                   2.02827e-06
Zv22_363119             5    0.00104432   0.000816468      0.781817        3.93575e-05                   2.29631e-08
Zv22_363369             4      0.852547      0.444765      0.521689        0.0321301                     0.00681419
Zv22_363371             2      0.896403      0.634016      0.707289        0.0337829                     0.0138469
Zv22_363372           232       5.42046      0.597084      0.110154        0.204282                      0.0122807
Zv22_363375            25      0.524305      0.128208       0.24453        0.0197596                     0.000566217
Zv22_363416             2       14.1144        9.9864      0.707533        0.531932                      3.43535
Zv22_363417           227       238.117       28.2976      0.118839        8.97397                       27.5837
Zv22_363418             8       43.2011       19.5246      0.451946        1.62813                       13.1316
Zv22_363419           110       116.807        17.575      0.150462        4.40213                       10.64
Zv22_363420          9119          1952       35.5456     0.0182099        73.5654                       43.5236
Zv22_363421             8      0.922451      0.997895       1.08179        0.0347646                     0.0343023
Zv22_363422           107       11.8282       3.31393      0.280173        0.445772                      0.378303
Zv22_363423          7538       230.768       4.10972     0.0178089        8.697                         0.581805
Zv22_363424             2    -0.0127646     0.0640348      -5.01658        -0.000481062                  0.000141249
Zv22_363425            36      0.692093       0.22345      0.322862        0.0260831                     0.00171994
Zv22_363426          3128       9.81498      0.261777     0.0266712        0.369899                      0.00236056
Zv22_363428             8     0.0079048     0.0564974       7.14723        0.00029791                    0.000109954
Zv22_363429           415       1.24189     0.0873394     0.0703278        0.0468034                     0.000262769
Zv22_363431             2    0.00884029    0.00634914      0.718205        0.000333166                   1.38862e-06
Zv22_363432           153      0.106963     0.0146764       0.13721        0.00403114                    7.4198e-06
Zv22_363434             5  -6.89901e-06   0.000122573      -17.7668        -2.60004e-07                  5.17538e-10
Zv22_363435            11   0.000319722    0.00016951      0.530179        1.20494e-05                   9.89791e-10

bkg:          21490       2653.42      100        0
totalStatErr = 53.8796
{% endhighlight %}

## CxAOD 28

### Sherpa 221

{% highlight javascript %}
* 2 jets

sampleName       entries         integral         error  error/integ.      Fraction of total yield %   Fraction of total error^2 

Z_364107             1       0.45828       0.45828             1           0.0284701                   0.0305542
Z_364108           129       2.70186      0.397822       0.14724           0.16785                     0.0230243
Z_364111            18      0.302236       0.14944       0.49445           0.018776                    0.00324895
Z_364112             1    -0.0174837     0.0174837            -1           -0.00108615                 4.44709e-05
Z_364131             1      -4.55101       4.55101            -1           -0.282726                   3.01318
Z_364133             2      0.425577      0.300968      0.707201           0.0264384                   0.013178
Z_364134             2       1.86513       1.37772      0.738669           0.115869                    0.276141
Z_364135             3       1.65917      0.997579      0.601253           0.103074                    0.144778
Z_364136           248       9.56135       1.17735      0.123136           0.593987                    0.20166
Z_364139           167       3.12677      0.489898      0.156679           0.194247                    0.0349157
Z_364140            19      0.373859      0.190152      0.508619           0.0232255                   0.00526031
Z_364146             4       6.20219       5.14412      0.829403           0.385303                    3.84974
Z_364147           272       27.2461       10.7761      0.395511           1.69263                     16.894
Z_364148             8       14.9204       7.65233      0.512876           0.926911                    8.51916
Z_364149           157       75.6182       11.3939      0.150677           4.69769                     18.8866
Z_364150         19691       1145.82       16.5863     0.0144755           71.1827                     40.0229
Z_364151             6      -1.59388        1.9448      -1.22017           -0.0990178                  0.550249
Z_364152            40       17.0909       4.56668        0.2672           1.06175                     3.03397
Z_364153         11577        291.46       5.37418     0.0184388           18.1066                     4.20179
Z_364154           545       16.8537       1.42836     0.0847509           1.04702                     0.296814
Z_364155            24        0.1651     0.0472089      0.285941           0.0102566                   0.000324233

bkg:          32915       1609.69      100        0
totalStatErr = 26.2179
{% endhighlight %}

{% highlight javascript %}
* 3 jets

sampleName       entries    integral         error  error/integ.      Fraction of total yield %   Fraction of total error^2 

Z_364105             1      0.178698      0.178698             1      0.00689522                  0.00187099
Z_364106             1      -1.55801       1.55801            -1      -0.0601172                  0.142224
Z_364108           235       5.02512      0.561957       0.11183      0.193899                    0.0185029
Z_364111            58       1.88213      0.285475      0.151676      0.0726237                   0.00477495
Z_364112             3     0.0352137     0.0476411       1.35291      0.00135875                  0.000132983
Z_364133             7       1.07091      0.975224      0.910652      0.041322                    0.0557239
Z_364134             1      -2.82036       2.82036            -1      -0.108826                   0.46606
Z_364135             1      0.488246      0.488246             1      0.0188394                   0.0139672
Z_364136           298        14.795       1.57693      0.106585      0.570878                    0.145699
Z_364138             3      0.756395      0.439748      0.581373      0.0291862                   0.0113303
Z_364139           325       9.07022      0.732121      0.080717      0.349983                    0.031405
Z_364140            25      0.636031      0.175049      0.275221      0.0245418                   0.00179536
Z_364141             1    0.00406431    0.00406431             1      0.000156825                 9.67846e-07
Z_364145             1       15.6245       15.6245             1      0.602885                    14.3036
Z_364146             5        26.549       18.7172      0.705005      1.02442                     20.5265
Z_364147           332       55.8044       9.73645      0.174475      2.15326                     5.55436
Z_364148            10        9.1132       15.0491       1.65135      0.351641                    13.2695
Z_364149           167       104.997       15.9265      0.151686      4.0514                      14.8619
Z_364150         20460       1544.66       20.0682      0.012992      59.6021                     23.5966
Z_364151             2       2.02229       1.55545      0.769154      0.0780319                   0.141757
Z_364152            94       33.3771       7.17451      0.214953      1.28789                     3.0159
Z_364153         19328       706.453       7.76019     0.0109847      27.2591                     3.5284
Z_364154          1521       62.5034       2.28882     0.0366192      2.41175                     0.306942
Z_364155           108      0.952879      0.129812      0.136231      0.0367677                   0.00098733

bkg:          42987       2591.62      100        0
totalStatErr = 41.3127
{% endhighlight %}

### Madgraph

{% highlight javascript %}
* 2 jets

sampleName       entries    integral         error  error/integ.      Fraction of total yield %   Fraction of total error^2 

Z_MG_361516           119       280.291       29.2696      0.104426      10.3003                  10.3644
Z_MG_361517           810       2032.72       82.5293     0.0406005      74.6997                  82.3998
Z_MG_361518           382       377.654       23.6184     0.0625397      13.8783                  6.74856
Z_MG_361519            32       30.5248        6.3511      0.208063      1.12174                  0.487986

bkg:           1343       2721.19      100        0
totalStatErr = 90.9173
{% endhighlight %}

{% highlight javascript %}
* 3 jets

sampleName       entries    integral         error  error/integ.      Fraction of total yield %   Fraction of total error^2 

Z_MG_361516            67       151.451       19.8961       0.13137      4.10644                  4.91293
Z_MG_361517           520       1228.51       68.8564     0.0560487      33.3098                  58.8428
Z_MG_361518          2264        1900.6       49.3195     0.0259495      51.5329                  30.1885
Z_MG_361519           538        407.57       22.0893     0.0541975      11.0509                  6.05576

bkg:           3389       3688.13      100        0
totalStatErr = 89.7631
{% endhighlight %}

# TruthMET Plots in CxAOD28 MAXHTPTV Filtered samples

![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

{% highlight javascript %}
THStack *hs = new THStack("hs","Stacked 2tag3jet MET");

Z_364147_2tag3jet_0ptv_SR_MET->RebinX(10)
Z_364150_2tag3jet_0ptv_SR_MET->RebinX(10)
Z_364153_2tag3jet_0ptv_SR_MET->RebinX(10)

Z_364147_2tag3jet_0ptv_SR_MET->SetFillColor(kAzure+10)
Z_364150_2tag3jet_0ptv_SR_MET->SetFillColor(kPink-9)
Z_364153_2tag3jet_0ptv_SR_MET->SetFillColor(kSpring+10)

Z_364147_2tag3jet_0ptv_SR_MET->SetMarkerColor(kAzure+10)
Z_364150_2tag3jet_0ptv_SR_MET->SetMarkerColor(kPink-9)
Z_364153_2tag3jet_0ptv_SR_MET->SetMarkerColor(kSpring+10)

Z_364147_2tag3jet_0ptv_SR_MET->SetMarkerStyle(21)
Z_364150_2tag3jet_0ptv_SR_MET->SetMarkerStyle(21)
Z_364153_2tag3jet_0ptv_SR_MET->SetMarkerStyle(21)

hs->Add(Z_364147_2tag3jet_0ptv_SR_MET)
hs->Add(Z_364150_2tag3jet_0ptv_SR_MET)
hs->Add(Z_364153_2tag3jet_0ptv_SR_MET)

TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
leg->AddEntry(Z_364147_2tag3jet_0ptv_SR_MET,"MAXMETPTV70_140_BFilter","f")
leg->AddEntry(Z_364150_2tag3jet_0ptv_SR_MET,"MAXMETPTV140_280_BFilter","f")
leg->AddEntry(Z_364153_2tag3jet_0ptv_SR_MET,"MAXMETPTV280_500_BFilter","f")

hs->Draw("hist")
leg->Draw("same")
{% endhighlight %}

### Summary for Valerio

* 2tag 2 jets

* * CxAOD 26 pTV Filter

| Sample | Filter              | nAOD      | Entries after selection | Yield after selection | Error after selection |
| ------ | ------------------- | --------- | ----------------------- | --------------------- | --------------------- |
| 363417 | BFilter pTV-70-140  | 2 471 000 |                     130 |                   117 |                 18.34 |
| 363420 | BFilter pTV-140-280 | 1 983 000 |                   7 802 |                 1 218 |                 26.87 |
| 363423 | BFilter pTV-280-500 | 984 000   |                    5242 |                   124 |                  3.42 |

* * CxAOD 28 MAXHTPtV Filter

| Sample | Filter                   | nAOD       | Entries after selection | Yield after selection | Error after selection |
| ------ | ------------------------ | ---------- | ----------------------- | --------------------- | --------------------- |
| 364147 | BFilter MAXHTPtV-70-140  | 19 728 500 |                     272 |                    27 |                 10.77 |
| 364150 | BFilter MAXHTPtV-140-280 | 19 745 300 |                  19 691 |                 1 145 |                 16.58 |
| 364153 | BFilter MAXHTPtV-280-500 | 8 887 350  |                  11 577 |                   291 |                  5.37 |

--> Purpose : Look how behaves the stat error with pTV filter if we had the same AOD stat as in CxAOD 28 :

err26' = err26 \* sqrt(nEntries26) / sqrt(nEntries26*nAOD28/nAOD26)

With the AOD stat of CxAODs 28 :

| Slice               | Error after selection with MAXHTPtV filter | Error after selection with PtV filter |
| ------------------- | ------------------------------------------ | ------------------------------------- |
| BFilter pTV-70-140  |                                      10.77 |                                 6.49  |
| BFilter pTV-140-280 |                                      16.58 |                                 8.57  |
| BFilter pTV-280-500 |                                       5.37 |                                  1.13 |
| Combined            |                                      20.48 |                                 10.81 |

* If we had to optimize the slicing in pTV, the TruthMET distribution at CxAOD level (selection = 2jets, MET reco > 140 GeV) shows that cutting on MET truth > 90 GeV allows to keep most events. Since we apply MET reco > 150 GeV in the analysis, a slice starting with low edge MET truth > 100 GeV should still be efficient.

![IMAGE](/images/q/IMAGE)

# Requests from Nicolas for the PMG presentation

* Distribution of TruthMET after full selection : done for Valerio a long time ago
  * Superimpose bb, bc, cc, and bl in a stack
  
  ![IMAGE](/images/q/IMAGE)
  ![IMAGE](/images/q/IMAGE)

{% highlight javascript %}
THStack *hs = new THStack("hs","Stacked 2tag2jet TruthMET");

Zbb_2tag2jet_150ptv_SR_TruthMET->RebinX(10)
Zbc_2tag2jet_150ptv_SR_TruthMET->RebinX(10)
Zbl_2tag2jet_150ptv_SR_TruthMET->RebinX(10)

Zbb_2tag2jet_150ptv_SR_TruthMET->SetFillColor(kAzure+10)
Zbc_2tag2jet_150ptv_SR_TruthMET->SetFillColor(kPink-9)
Zbl_2tag2jet_150ptv_SR_TruthMET->SetFillColor(kSpring+10)

Zbb_2tag2jet_150ptv_SR_TruthMET->SetMarkerColor(kAzure+10)
Zbc_2tag2jet_150ptv_SR_TruthMET->SetMarkerColor(kPink-9)
Zbl_2tag2jet_150ptv_SR_TruthMET->SetMarkerColor(kSpring+10)

Zbb_2tag2jet_150ptv_SR_TruthMET->SetMarkerStyle(21)
Zbc_2tag2jet_150ptv_SR_TruthMET->SetMarkerStyle(21)
Zbl_2tag2jet_150ptv_SR_TruthMET->SetMarkerStyle(21)

hs->Add(Zbl_2tag2jet_150ptv_SR_TruthMET)
hs->Add(Zbc_2tag2jet_150ptv_SR_TruthMET)
hs->Add(Zbb_2tag2jet_150ptv_SR_TruthMET)

TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
leg->AddEntry(Zbb_2tag2jet_150ptv_SR_TruthMET,"Zbb","f")
leg->AddEntry(Zbc_2tag2jet_150ptv_SR_TruthMET,"Zbc","f")
leg->AddEntry(Zbl_2tag2jet_150ptv_SR_TruthMET,"Zbl","f")

hs->Draw("hist")
leg->Draw("same")
{% endhighlight %}

* Get the ratio of cross sections between 70-100 to 100-140
![IMAGE](/images/q/IMAGE)

{% highlight javascript %}
TF1 *f = new TF1("fb","[0]*TMath::Exp([1]*x)",0,500);
f->SetParameter(0,30000) // 6000/exp(-ln(6000/1200)*70)
f->SetParameter(1,-0.023) // -ln(6000/1200)/70
f->Draw()

f->Integral(70,100)/f->Integral(100,140)
// (double) 1.652115

f->Integral(70,100)/f->Integral(70,140)
// (double) 0.622942

 f->Integral(100,140)/f->Integral(70,140)
// (double) 0.377058
{% endhighlight %}

* Compare the distribution of TruthMET with pT(Z) from TruthParticle neutrino with status = 3

{% highlight javascript %}
CollectionTree->Draw("sqrt((TruthParticles___NominalAuxDyn.px[0]+TruthParticles___NominalAuxDyn.px[1])*(TruthParticles___NominalAuxDyn.px[0]+TruthParticles___NominalAuxDyn.px[1])+(TruthParticles___NominalAuxDyn.py[0]+TruthParticles___NominalAuxDyn.py[1])*(TruthParticles___NominalAuxDyn.py[0]+TruthParticles___NominalAuxDyn.py[1]))")
{% endhighlight %}

![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

THStack *hs = new THStack("hs","Stacked 2tag2jet pTZ");

Zv22_363417_2tag2jet_0ptv_SR_pTZ->RebinX(5)
Zv22_363420_2tag2jet_0ptv_SR_pTZ->RebinX(5)
Zv22_363423_2tag2jet_0ptv_SR_pTZ->RebinX(5)

Zv22_363417_2tag2jet_0ptv_SR_pTZ->SetFillColor(kAzure+10)
Zv22_363420_2tag2jet_0ptv_SR_pTZ->SetFillColor(kPink-9)
Zv22_363423_2tag2jet_0ptv_SR_pTZ->SetFillColor(kSpring+10)

Zv22_363417_2tag2jet_0ptv_SR_pTZ->SetMarkerColor(kAzure+10)
Zv22_363420_2tag2jet_0ptv_SR_pTZ->SetMarkerColor(kPink-9)
Zv22_363423_2tag2jet_0ptv_SR_pTZ->SetMarkerColor(kSpring+10)

Zv22_363417_2tag2jet_0ptv_SR_pTZ->SetMarkerStyle(21)
Zv22_363420_2tag2jet_0ptv_SR_pTZ->SetMarkerStyle(21)
Zv22_363423_2tag2jet_0ptv_SR_pTZ->SetMarkerStyle(21)

hs->Add(Zv22_363417_2tag2jet_0ptv_SR_pTZ)
hs->Add(Zv22_363420_2tag2jet_0ptv_SR_pTZ)
hs->Add(Zv22_363423_2tag2jet_0ptv_SR_pTZ)

TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
leg->AddEntry(Zv22_363417_2tag2jet_0ptv_SR_pTZ,"70-140","f")
leg->AddEntry(Zv22_363420_2tag2jet_0ptv_SR_pTZ,"140-280","f")
leg->AddEntry(Zv22_363423_2tag2jet_0ptv_SR_pTZ,"280-500","f")

hs->Draw("hist")
leg->Draw("same")

![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

{% highlight javascript %}
THStack *hs = new THStack("hs","Stacked 2tag2jet pTZTruthMETratio");

Zv22_363417_2tag2jet_0ptv_SR_pTZTruthMETratio->SetMarkerColor(kAzure+10)
Zv22_363420_2tag2jet_0ptv_SR_pTZTruthMETratio->SetMarkerColor(kPink-9)
Zv22_363423_2tag2jet_0ptv_SR_pTZTruthMETratio->SetMarkerColor(kSpring+10)

Zv22_363417_2tag2jet_0ptv_SR_pTZTruthMETratio->SetMarkerStyle(21)
Zv22_363420_2tag2jet_0ptv_SR_pTZTruthMETratio->SetMarkerStyle(21)
Zv22_363423_2tag2jet_0ptv_SR_pTZTruthMETratio->SetMarkerStyle(21)

Zv22_363420_2tag2jet_0ptv_SR_pTZTruthMETratio->DrawNormalized("HIST p");
Zv22_363417_2tag2jet_0ptv_SR_pTZTruthMETratio->DrawNormalized("HIST p same");
Zv22_363423_2tag2jet_0ptv_SR_pTZTruthMETratio->DrawNormalized("HIST p same");

Zv22_363417_2tag2jet_0ptv_SR_pTZTruthMETratio->SetFillColor(kAzure+10)
Zv22_363420_2tag2jet_0ptv_SR_pTZTruthMETratio->SetFillColor(kPink-9)
Zv22_363423_2tag2jet_0ptv_SR_pTZTruthMETratio->SetFillColor(kSpring+10)

TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
leg->AddEntry(Zv22_363417_2tag2jet_0ptv_SR_pTZTruthMETratio,"70-140","f")
leg->AddEntry(Zv22_363420_2tag2jet_0ptv_SR_pTZTruthMETratio,"140-280","f")
leg->AddEntry(Zv22_363423_2tag2jet_0ptv_SR_pTZTruthMETratio,"280-500","f")

leg->Draw("same")
{% endhighlight %}

### Tatsuya 's requests

* **After full selection, CxAOD26 with pTZ slicing**

x-axis = pTZ (from neutrinos at parton level)
y-axis = MET reco

* **70<pTV<140 GeV**
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

* **140<pTV<280 GeV**
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

* **280<pTV<500 GeV**
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

### Notes from PMG

* Optimal filter analysis specifics ?
* What about non-B filtered samples ?
* Restricted to nunu ? -> y


