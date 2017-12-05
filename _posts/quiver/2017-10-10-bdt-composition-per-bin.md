---
title: BDT composition per bin
date: '2017-10-10'
tags:
- ttbar
- VHbb
- znunub
- zvvb
---
* **Yields**
[mva28_trafo6_2j.txt](quiver-file-url/470B4377F09A5CCD35E9BBCAACFB3B4B.txt)
[mva28_trafo6_3j.txt](quiver-file-url/96F7D4621802E4670AE06B5B40778CF3.txt)

* **Stat. Error**
[mva28_trafo6_2j_Err.txt](quiver-file-url/A8ECB690767AB1EB22F260AEFFC7BDC4.txt)
[mva28_trafo6_3j_Err.txt](quiver-file-url/2E6B764FC95BD08D80BA392F5A88AE6D.txt)

2 jets :
| s        | bkg     | s/sqrt(bkg)|
|----------| ------- | ---------- |
| 75       | 285     | 4.44262    |
| 46.7412  | 2715.96 | 0.896888   |
| 0.396988 | 82.2562 | 0.0437717  |
| 0.162178 | 1.08601 | 0.155623   |
| 0.109951 | 545.382 | 0.00470813 |
| 0.258793 | 514.695 | 0.0114072  |
| 0.670815 | 464.996 | 0.0311084  |
| 1.41943  | 378.082 | 0.0729997  |
| 2.56218  | 244.018 | 0.164021   |
| 3.2782   | 159.684 | 0.259421   |
| 3.75214  | 109.332 | 0.358844   |
| 3.97351  | 76.9823 | 0.452876   |
| 4.16269  | 65.2123 | 0.515477   |
| 4.30538  | 45.3623 | 0.63924    |
| 4.31894  | 39.6621 | 0.685787   |
| 4.44386  | 25.6155 | 0.878029   |
| 4.46005  | 19.4747 | 1.01066    |
| 4.45464  | 14.5611 | 1.16739    |
| 4.57067  | 12.9006 | 1.27255    |

3 jets :
| s        | bkg     | s/sqrt(bkg)|
|----------| ------- | ---------- |
| 75       | 285      | 4.44262    |
| 51.8486  | 7611.28  | 0.594303   |
| 0.478265 | 134.265  | 0.041275   |
| 0.137697 | 0.684553 | 0.166426   |
| 0.323229 | 1445.24  | 0.00850238 |
| 0.478866 | 1371.03  | 0.0129327  |
| 1.00008  | 1228.12  | 0.0285374  |
| 1.90086  | 958.713  | 0.0613912  |
| 2.71069  | 734.683  | 0.100007   |
| 3.43124  | 522.557  | 0.150101   |
| 3.88951  | 382.222  | 0.198947   |
| 4.21908  | 273.757  | 0.254997   |
| 4.49263  | 208.453  | 0.311169   |
| 4.65634  | 151.114  | 0.378785   |
| 4.75988  | 118.346  | 0.437541   |
| 4.97126  | 86.1754  | 0.535519   |
| 4.9287   | 57.7683  | 0.648467   |
| 4.99142  | 43.1174  | 0.760147   |
| 5.09475  | 29.983   | 0.930433   |

Statistical errors can be recomputed bin by bin as sqrt(Sum_events(weight*weight))

{% highlight sh %}
# 2 jets signal processes


qqWlvH125  ggZvvH125  qqZvvH125   ggZllH125    qqZllH125    signal
0.2        0.2        0.2         0.2          0.2          33.541
0.0708018  0.0395905  0.889545    2.77527e-06  5.97959e-05  32.9717
0.247095   0.322839   0.42849     0.000576097  0.00100014   0.223593
0.0147607  0.0344894  0.00203732  0.877971     0.070742     0.104273
0.207563   0.182087   0.608675    0            0.00167419   0.0129208
0.318152   0.272014   0.408591    0.000247733  0.000995673  0.0179268
0.60837    0.177578   0.213662    6.18372e-05  0.000327569  0.0386348
0.273669   0.310808   0.414784    0.000178922  0.000559663  0.0402782
0.271404   0.332291   0.394885    0.000273108  0.00114705   0.0551584
0.276384   0.33044    0.3917      0.000398774  0.00107821   0.0726985
0.280046   0.348642   0.370452    0.000317336  0.00054171   0.0665092
0.171802   0.426342   0.400675    0.000258317  0.000922973  0.0694782
0.189682   0.314737   0.494105    0.000633892  0.000841711  0.072659
0.2032     0.335395   0.460226    0.000178517  0.00100043   0.0694851
0.226782   0.350268   0.421857    0.000343585  0.000749438  0.0671756
0.253226   0.316642   0.428414    0.000628304  0.00108882   0.0672393
0.22597    0.342725   0.428045    0.00194397   0.00131605   0.0608969
0.234887   0.269321   0.491992    0.00192069   0.00187939   0.0560007
0.277485   0.172148   0.548765    0.000324738  0.00127778   0.0531659
{% endhighlight %}

{% highlight sh %}
# 2 jets selected background processes

Zbb         Wbb         stopWt      ttbar       background
0.0526316   0.0526316   0.0526316   0.0526316   65.3835
0.839899    0.0377754   0.00112377  0.106233    1460.74
0.401674    0.07918     0.0324281   0.266405    28.3661
0.00174436  0.00764522  0.10525     0.00914665  0.32154
0.613822    0.0319854   0.00977773  0.15775     13.2964
0.444599    0.121852    0.00774747  0.274338    11.8429
0.374875    0.108624    0.0187572   0.287713    11.0112
0.244219    0.0673262   0.0852223   0.254429    12.4924
0.309502    0.070562    0.0211862   0.338136    7.95226
0.243725    0.0794369   0.0231873   0.414611    6.83013
0.401126    0.0591888   0.0318326   0.317146    5.01797
0.356849    0.0942905   0.0487202   0.326635    4.40522
0.368525    0.0765303   0.0275459   0.307365    3.90126
0.337107    0.127443    0.0664673   0.381642    3.43846
0.359378    0.102011    0.0931309   0.295759    3.1606
0.550179    0.0905457   0.024754    0.244643    2.97701
0.281031    0.145654    0.0647435   0.422064    1.96877
0.466005    0.071603    0.0450614   0.340058    1.65223
0.111723    0.165686    0.244074    0.446419    1.81742
{% endhighlight %}

{% highlight sh %}
# 3 jets signal processes

qqWlvH125  ggZvvH125  qqZvvH125   ggZllH125    qqZllH125    signal
0.2        0.2        0.2         0.2          0.2          33.541
0.0895129  0.115253   0.795153    5.22097e-06  7.54585e-05  33.6382
0.322188   0.387607   0.288697    0.000436879  0.00107178   0.268516
0.034212   0.0319666  0.00345101  0.795364     0.135006     0.0818766
0.929579   0.0482138  0.0220924   5.25362e-05  6.27019e-05  0.0687738
0.136147   0.394693   0.467314    0.000928291  0.000918155  0.024311
0.27622    0.353811   0.360801    0.000394792  0.0087729    0.0354739
0.210392   0.521258   0.26749     0.000246347  0.000613734  0.0573492
0.204664   0.444648   0.348621    0.000383959  0.00168275   0.0600407
0.169595   0.502946   0.324318    0.00112316   0.00201746   0.0661591
0.58775    0.228329   0.183315    0.000272036  0.00033393   0.0995471
0.161736   0.464914   0.372279    0.000445729  0.000625829  0.0735325
0.205287   0.476454   0.316845    0.000668939  0.000745463  0.0767028
0.268882   0.416587   0.312611    0.000614073  0.00130589   0.0774427
0.218261   0.441353   0.338583    0.000377361  0.00142593   0.0765215
0.233259   0.411123   0.354258    0.000488661  0.000872019  0.0723018
0.343498   0.351297   0.304168    0.000386219  0.000649976  0.0763345
0.22796    0.478966   0.291202    0.000419926  0.00145167   0.0751294
0.206302   0.435577   0.356861    0.000219135  0.00104071   0.0670739
{% endhighlight %}

{% highlight sh %}
# 3 jets background processes

Zbb         Wbb        stopWt      ttbar       background
0.0526316   0.0526316  0.0526316   0.0526316   65.3835
0.265336    0.0303274  0.00377619  0.691354    4089.75
0.157118    0.0794379  0.04895     0.571215    50.6015
0.00239745  0.010605   0.0524826   0.00334519  0.19445
0.164408    0.0177552  0.034149    0.610741    21.6177
0.185933    0.115852   0.0392508   0.48784     20.67
0.167637    0.0831648  0.0268721   0.543279    20.8397
0.151197    0.0848387  0.0829517   0.581175    17.3515
0.118256    0.133221   0.0403323   0.577931    16.4651
0.170975    0.0384453  0.063148    0.620433    12.9599
0.128755    0.151797   0.0717105   0.551779    11.8881
0.166672    0.0412966  0.0308829   0.598352    9.13857
0.175394    0.0569625  0.0425175   0.564612    8.60475
0.137933    0.0548445  0.0290366   0.701934    7.43762
0.0770069   0.0444326  0.128458    0.688927    7.55485
0.184512    0.105898   0.083799    0.537714    4.80889
0.0730167   0.0585992  0.0598081   0.783168    6.05009
0.164134    0.101553   0.372092    0.307923    3.64511
0.0943262   0.102332   0.076361    0.53457     2.68678
{% endhighlight %}

* BDT  new binning in the statistical transformation :
  * 2 jets : 1 45 115 229 367 476 547 597 638 678 712 740 765 792 818 1002
    * -1, -0.912, -0.772, -0.544, -0.268, -0.05, 0.092, 0.192, 0.274, 0.354, 0.422, 0.478, 0.528, 0.582, 0.634, 1.002

| index| Value  |
| ---- | ------ |
| 1    | -1     |
| 45   | -0.912 |
| 115  | -0.772 |
| 229  | -0.544 |
| 367  | -0.268 |
| 476  | -0.05  |
| 547  | 0.092  |
| 597  | 0.192  |
| 638  | 0.274  |
| 678  | 0.354  |
| 712  | 0.422  |
| 740  | 0.478  |
| 765  | 0.528  |
| 792  | 0.582  |
| 818  | 0.634  |
| 1002 | 1.002  |

  * 3 jets : 0 79 166 260 354 442 520 583 638 683 722 756 790 824 862 1002
    * -1.002, -0.844, -0.67, -0.482, -0.294, -0.118, 0.038, 0.164, 0.274, 0.364, 0.442, 0.51, 0.578, 0.646, 0.722, 1.002

| index| Value  |
| ---- | ------ |
| 0    | -1.002 |
| 79   | -0.844 |
| 166  | -0.67  | 
| 260  | -0.482 |
| 354  | -0.294 |
| 442  | -0.118 |
| 520  | 0.038  |
| 583  | 0.164  |
| 638  | 0.274  |
| 683  | 0.364  |
| 722  | 0.442  |
| 756  | 0.51   |
| 790  | 0.578  |
| 824  | 0.646  |
| 862  | 0.722  |
| 1002 | 1.002  |

Columns are :

|             |
| ----------- |
| Sample Name |
| Nentries    |
| Integral    |
| Stat error  |
| Relative stat error |
| bin 0       |
| ...         |
| bin 14      |

# Infos

* yield ratios are with respect to total sig for sig samples, to total bkg for bkg samples
* error ratios are with respect to total sig for sig samples, to total bkg for bkg samples
* error ratios are with respect to the square error ... e.g. err2 / sum(err2)(all samples)

# Results

* signal sample qqWH125 contributes a lot to the signal error with respect to its yield

## Yields in 2 jets

{% highlight javascript %}
sample   qqWlvH125  ggZvvH125  qqZvvH125  ttbar      Zbl         Zbc        Zbb        Wbl         Wbc          Wbb        stopWt
nEntries 0.2        0.2        0.2        0.0526316  0.0526316   0.0526316  0.0526316  0.0526316   0.0526316    0.0526316  0.0526316
Integral 0.1877     0.140358   0.665312   0.175299   0.0269859   0.0278668  0.492904   0.00915164  0.0103244    0.104533   0.0180297
Stat err 0.279971   0.320017   0.368681   0.177993   0.0772782   0.0896518  0.218559   0.0528291   0.0392616    0.0970373  0.0621
Rel. err 0.0781149  0.119405   0.0290209  0.0283161  0.0798606   0.089719   0.0123658  0.160985    0.106051     0.025888   0.0960537
bin 0    0.166093   0.163141   0.662922   0.153417   0.032319    0.0246194  0.610464   0.00816089  0.0119402    0.0358563  0.0113185
bin 1    0.204361   0.15233    0.637151   0.162524   0.0172742   0.026418   0.514585   0.00940779  0.0124202    0.138695   0.00837257
bin 2    0.22797    0.175203   0.591024   0.164297   0.0357646   0.0295762  0.501824   0.00348122  0.0106307    0.133272   0.0160703
bin 3    0.194258   0.161339   0.639585   0.181055   0.0257685   0.0350286  0.418861   0.0136613   0.0157972    0.120449   0.0262599
bin 4    0.174036   0.163488   0.656015   0.197466   0.0234975   0.0245114  0.401595   0.0144363   0.000882518  0.0898115  0.0166267
bin 5    0.180712   0.178792   0.633775   0.22451    0.0419461   0.0192246  0.389937   0.00213076  0.00701894   0.0996327  0.0207748
bin 6    0.186648   0.173878   0.634468   0.201166   0.0161061   0.0260498  0.434226   0.0139419   0.0109993    0.0937881  0.0213892
bin 7    0.168477   0.162356   0.663313   0.207515   0.0360832   0.0330966  0.435025   0.0085398   0.00959245   0.106817   0.0259617
bin 8    0.179367   0.165726   0.648746   0.195612   0.0219416   0.0304666  0.466849   0.0154883   0.00928391   0.0915922  0.0195362
bin 9    0.174563   0.149164   0.670254   0.194512   0.00366787  0.0293215  0.499168   0.00589474  -0.00126678  0.157234   0.037344
bin 10   0.187364   0.154013   0.652796   0.171533   0.00678283  0.0341679  0.499949   0.0166799   0.00538499   0.140878   0.0559108
bin 11   0.198899   0.132914   0.660217   0.21487    0.0193553   0.0467884  0.452901   0.0236928   0            0.167703   0.0307589
bin 12   0.200225   0.119595   0.671847   0.166667   0.0209319   0.0471618  0.499804   0.0142627   0            0.14194    0.0507954
bin 13   0.195965   0.103082   0.692424   0.185288   0.0320378   0.0188368  0.586828   -0.0189814  0.012467     0.0870765  0.0338075
bin 14   0.198686   0.059854   0.735165   0.162663   0.0151694   0.0119566  0.401742   0.014481    0            0.16532    0.148685
{% endhighlight %}

## Errors^2 in 2 jets

{% highlight javascript %}
sample   qqWlvH125  ggZvvH125  qqZvvH125   ttbar       Zbl         Zbc         Zbb         Wbl          Wbc          Wbb         stopWt      signal err background err
nEntries 0.2        0.2        0.2         0.0526316   0.0526316   0.0526316   0.0526316   0.0526316    0.0526316    0.0526316   0.0526316   33.541     65.3835
Integral 0.0708018  0.0395905  0.889545    0.106233    0.00251753  0.00268458  0.839899    0.000289534  0.000368495  0.0377754   0.00112377  32.9717    1460.74
Stat err 0.247095   0.322839   0.42849     0.266405    0.0502171   0.067586    0.401674    0.0234684    0.0129621    0.07918     0.0324281   0.223593   28.3661
Rel. err 0.0147607  0.0344894  0.00203732  0.00914665  0.0727545   0.0918254   0.00174436  0.295642     0.128299     0.00764522  0.10525     0.104273   0.32154
bin 0    0.207563   0.182087   0.608675    0.15775     0.0496372   0.0261832   0.613822    0.0220503    0.0123909    0.0319854   0.00977773  0.0129208  13.2964
bin 1    0.318152   0.272014   0.408591    0.274338    0.0422952   0.0272219   0.444599    0.0190617    0.0113061    0.121852    0.00774747  0.0179268  11.8429
bin 2    0.60837    0.177578   0.213662    0.287713    0.0723944   0.0296287   0.374875    0.0567223    0.0107297    0.108624    0.0187572   0.0386348  11.0112
bin 3    0.273669   0.310808   0.414784    0.254429    0.0271971   0.236126    0.244219    0.00971926   0.0167129    0.0673262   0.0852223   0.0402782  12.4924
bin 4    0.271404   0.332291   0.394885    0.338136    0.0863699   0.0264896   0.309502    0.0126483    0.0287265    0.070562    0.0211862   0.0551584  7.95226
bin 5    0.276384   0.33044    0.3917      0.414611    0.0934284   0.0239801   0.243725    0.028657     0.00310308   0.0794369   0.0231873   0.0726985  6.83013
bin 6    0.280046   0.348642   0.370452    0.317146    0.0499561   0.0301826   0.401126    0.0137382    0.0152215    0.0591888   0.0318326   0.0665092  5.01797
bin 7    0.171802   0.426342   0.400675    0.326635    0.0321763   0.0403272   0.356849    0.004576     0.00584582   0.0942905   0.0487202   0.0694782  4.40522
bin 8    0.189682   0.314737   0.494105    0.307365    0.0186747   0.0220464   0.368525    0.0121006    0.00492237   0.0765303   0.0275459   0.072659   3.90126
bin 9    0.2032     0.335395   0.460226    0.381642    0.0342906   0.0160826   0.337107    0.00653671   0.00992003   0.127443    0.0664673   0.0694851  3.43846
bin 10   0.226782   0.350268   0.421857    0.295759    0.0101027   0.0163157   0.359378    0.0710486    0.00609686   0.102011    0.0931309   0.0671756  3.1606
bin 11   0.253226   0.316642   0.428414    0.244643    0.00629083  0.0247762   0.550179    0.0258071    0            0.0905457   0.024754    0.0672393  2.97701
bin 12   0.22597    0.342725   0.428045    0.422064    0.0175998   0.0536729   0.281031    0.00900561   0            0.145654    0.0647435   0.0608969  1.96877
bin 13   0.234887   0.269321   0.491992    0.340058    0.0176298   0.0117727   0.466005    0.0279835    0.0120717    0.071603    0.0450614   0.0560007  1.65223
bin 14   0.277485   0.172148   0.548765    0.446419    0.00346662  0.00240559  0.111723    0.010566     0            0.165686    0.244074    0.0531659  1.81742
{% endhighlight %}

* The ttbar sample dominates the stat errors
* After ttbar, single top Wt is the second largest contribution to the stat error
* We should not worry to much about Wbc because of the 0-yield in last BDT bins : it already gives 0-yield in low-BDT bins, with small stat uncertainty
* Same conclusion for single top s and t samples : 0-yield in last BDT bins does not mean that we necessarily will have stat. issues if it truly shows 0-yield already in the low-BDT bins 
* We should focus on qqZH if we have to increase the stat in one of the signal samples

## Fraction of Errors^2 / Fraction Yield in 2 jets

{% highlight javascript %}
sample   qqWlvH125 ggZvvH125 qqZvvH125  ttbar     Zbl        Zbc        Zbb       Wbl        Wbc        Wbb       stopWt 
nEntries 1         1         1          1         1          1          1         1          1          1         1
Integral 0.377207  0.282068  1.33703    0.60601   0.0932906  0.0963361  1.70398   0.0316374  0.0356917  0.361373  0.0623288
Stat_err 0.882574  1.00882   1.16222    1.49672   0.649822   0.753872   1.83783   0.444232   0.330147   0.815975  0.522192
Rel._err 0.188961  0.288844  0.0702018  0.323019  0.911019   1.02348    0.141063  1.83646    1.20979    0.295319  1.09574
bin_0    1.24968   1.11613   0.91817    1.02824   1.53585    1.06352    1.0055    2.70195    1.03775    0.892044  0.863872
bin_1    1.55681   1.78569   0.641278   1.68798   2.44846    1.03043    0.863995  2.02616    0.910299   0.878561  0.925347
bin_2    2.66864   1.01356   0.361512   1.75118   2.02419    1.00178    0.747025  16.2938    1.00931    0.815055  1.1672
bin_3    1.40879   1.92643   0.648521   1.40526   1.05544    6.74095    0.583055  0.711445   1.05797    0.55896   3.24534
bin_4    1.55947   2.03251   0.601945   1.71238   3.67571    1.08071    0.770682  0.876146   32.5506    0.785668  1.27423
bin_5    1.52942   1.84818   0.618043   1.84674   2.22734    1.24737    0.625037  13.4492    0.442101   0.797297  1.11613
bin_6    1.5004    2.0051    0.583878   1.57654   3.10169    1.15865    0.923772  0.985389   1.38386    0.631091  1.48826
bin_7    1.01974   2.62597   0.604051   1.57403   0.891725   1.21847    0.820295  0.535844   0.609419   0.882729  1.87662
bin_8    1.05751   1.89914   0.761631   1.5713    0.851109   0.723625   0.789388  0.781274   0.530204   0.835555  1.40999
bin_9    1.16405   2.2485    0.686644   1.96205   9.34891    0.548492   0.675338  1.10891    -7.83091   0.810531  1.77987
bin_10   1.21038   2.27428   0.646231   1.72421   1.48945    0.477515   0.718829  4.25953    1.1322     0.724109  1.66571
bin_11   1.27314   2.38231   0.648899   1.13856   0.325018   0.529537   1.21479   1.08924    0          0.539917  0.804775
bin_12   1.12858   2.86571   0.637117   2.53238   0.840812   1.13806    0.562282  0.63141    0          1.02617   1.27459
bin_13   1.19862   2.61269   0.710536   1.83529   0.550281   0.624984   0.794108  -1.47426   0.968292   0.8223    1.33288
bin_14   1.3966    2.87613   0.746451   2.74444   0.228527   0.201193   0.278096  0.729646   0          1.00221   1.64155
{% endhighlight %}

## Yields in 3 jets

{% highlight javascript %}
sample   qqWlvH125  ggZvvH125  qqZvvH125  ttbar      Zbl        Zbc        Zbb        Wbl         Wbc         Wbb        stopWt
nEntries 0.2        0.2        0.2        0.0526316  0.0526316  0.0526316  0.0526316  0.0526316   0.0526316   0.0526316  0.0526316
Integral 0.194106   0.220253   0.578523   0.446775   0.0176763  0.0198254  0.276781   0.00869101  0.00740767  0.0935742  0.0330191
Stat err 0.318681   0.34954    0.301663   0.28484    0.0671774  0.0636507  0.149388   0.0430893   0.0331032   0.106222   0.083383
Rel. err 0.109982   0.106312   0.0349307  0.016429   0.0979333  0.0827328  0.0139083  0.12776     0.115155    0.0292519  0.065074
bin 0    0.361719   0.255002   0.377933   0.51508    0.0256974  0.017746   0.279355   0.0101303   0.00471701  0.0368752  0.0297222
bin 1    0.152784   0.211122   0.627153   0.404873   0.0163923  0.0199246  0.312594   0.00897646  0.0095019   0.105261   0.0261009
bin 2    0.181053   0.242836   0.566825   0.415209   0.0137855  0.0268793  0.282747   0.00953783  0.00872838  0.127752   0.0282994
bin 3    0.180785   0.273445   0.540545   0.430283   0.0142194  0.0179362  0.265728   0.00387581  0.00906471  0.120452   0.032055
bin 4    0.164974   0.256638   0.57064    0.488209   0.0204562  0.018308   0.224323   0.00899381  0.00692949  0.0998271  0.0358468
bin 5    0.162529   0.27721    0.553261   0.496847   0.0131016  0.0143534  0.238831   0.0049949   0.0081695   0.0740899  0.0400417
bin 6    0.176962   0.275721   0.541385   0.491604   0.0149304  0.0121438  0.22833    0.00634519  0.00707416  0.0867715  0.0424852
bin 7    0.171161   0.262173   0.561039   0.419989   0.0142281  0.023907   0.281506   0.018394    0.00217148  0.0796524  0.0338048
bin 8    0.191037   0.237224   0.564376   0.403656   0.0109223  0.0179385  0.301924   0.0103274   0.00773269  0.0840953  0.0402028
bin 9    0.205034   0.225214   0.562045   0.385698   0.0242803  0.0233041  0.314624   0.0107412   0.0051234   0.0913812  0.0319754
bin 10   0.20276    0.214218   0.575328   0.385963   0.0195359  0.0265217  0.277991   0.00969922  0.00792408  0.112215   0.0717741
bin 11   0.200294   0.204359   0.587994   0.33585    0.0318701  0.0244281  0.354123   0.00228743  0.00638816  0.118306   0.0420752
bin 12   0.219143   0.176806   0.596938   0.353268   0.0151962  0.0115049  0.331753   0.00227587  0.00539393  0.149259   0.0565694
bin 13   0.211441   0.180856   0.59948    0.243254   0.0118283  0.0416203  0.375853   0.0131758   0.00212483  0.150816   0.092555
bin 14   0.201134   0.142127   0.650112   0.315165   0.0164638  0.0208191  0.304498   0.0424774   0.00638087  0.175718   0.0582346
{% endhighlight %}

## Errors^2 in 3 jets

{% highlight javascript %}
sample   qqWlvH125  ggZvvH125  qqZvvH125   ttbar       Zbl         Zbc         Zbb         Wbl          Wbc          Wbb        stopWt      signal err background err
nEntries 0.2        0.2        0.2         0.0526316   0.0526316   0.0526316   0.0526316   0.0526316    0.0526316    0.0526316  0.0526316   33.541     65.3835
Integral 0.0895129  0.115253   0.795153    0.691354    0.00108219  0.00136135  0.265336    0.000261615  0.000190058  0.0303274  0.00377619  33.6382    4089.75
Stat err 0.322188   0.387607   0.288697    0.571215    0.0317719   0.0285235   0.157118    0.0130718    0.00771501   0.0794379  0.04895     0.268516   50.6015
Rel. err 0.034212   0.0319666  0.00345101  0.00334519  0.118867    0.0848312   0.00239745  0.202299     0.16435      0.010605   0.0524826   0.0818766  0.19445
bin 0    0.929579   0.0482138  0.0220924   0.610741    0.0744165   0.0182234   0.164408    0.01456      0.00542846   0.0177552  0.034149    0.0687738  21.6177
bin 1    0.136147   0.394693   0.467314    0.48784     0.0279186   0.0168924   0.185933    0.0185887    0.00927588   0.115852   0.0392508   0.024311   20.67
bin 2    0.27622    0.353811   0.360801    0.543279    0.0166367   0.0911158   0.167637    0.0122782    0.0151354    0.0831648  0.0268721   0.0354739  20.8397
bin 3    0.210392   0.521258   0.26749     0.581175    0.0118689   0.0113688   0.151197    0.00557692   0.00644951   0.0848387  0.0829517   0.0573492  17.3515
bin 4    0.204664   0.444648   0.348621    0.577931    0.042589    0.0144444   0.118256    0.014926     0.00600221   0.133221   0.0403323   0.0600407  16.4651
bin 5    0.169595   0.502946   0.324318    0.620433    0.0097138   0.0175841   0.170975    0.00809165   0.00448632   0.0384453  0.063148    0.0661591  12.9599
bin 6    0.58775    0.228329   0.183315    0.551779    0.0179591   0.0190427   0.128755    0.00465936   0.00433333   0.151797   0.0717105   0.0995471  11.8881
bin 7    0.161736   0.464914   0.372279    0.598352    0.0266016   0.014739    0.166672    0.0374048    0.00980344   0.0412966  0.0308829   0.0735325  9.13857
bin 8    0.205287   0.476454   0.316845    0.564612    0.0395452   0.0178147   0.175394    0.00845602   0.0040599    0.0569625  0.0425175   0.0767028  8.60475
bin 9    0.268882   0.416587   0.312611    0.701934    0.0188603   0.00993988  0.137933    0.00650945   0.00349145   0.0548445  0.0290366   0.0774427  7.43762
bin 10   0.218261   0.441353   0.338583    0.688927    0.013103    0.0134238   0.0770069   0.00357518   0.00280286   0.0444326  0.128458    0.0765215  7.55485
bin 11   0.233259   0.411123   0.354258    0.537714    0.0282558   0.0188639   0.184512    0.00168024   0.00441619   0.105898   0.083799    0.0723018  4.80889
bin 12   0.343498   0.351297   0.304168    0.783168    0.0118029   0.00355843  0.0730167   0.000472226  0.00135216   0.0585992  0.0598081   0.0763345  6.05009
bin 13   0.22796    0.478966   0.291202    0.307923    0.00425029  0.0202793   0.164134    0.00878882   0.00644602   0.101553   0.372092    0.0751294  3.64511
bin 14   0.206302   0.435577   0.356861    0.53457     0.00700684  0.00624997  0.0943262   0.160957     0.00507046   0.102332   0.076361    0.0670739  2.68678
{% endhighlight %}

* The error in the last bin of Wbl is probably due to some bad luck, looking at the previous bins where it shows very little contribution to the total stat error

## Fraction of Errors^2 / Fraction Yield in 3 jets

{% highlight javascript %}

sample   qqWlvH125 ggZvvH125 qqZvvH125  ttbar     Zbl        Zbc       Zbb       Wbl        Wbc        Wbb       stopWt
nEntries 1         1         1          1         1          1         1         1          1          1         1
Integral 0.461155  0.523276  1.37445    1.54743   0.0612227  0.068667  0.95865   0.0301018  0.0256569  0.3241    0.114364
Stat_err 1.011     1.10891   0.957018   2.00539   0.472955   0.448125  1.05174   0.303365   0.233059   0.747848  0.58705
Rel._err 0.311069  0.300687  0.0987959  0.203615  1.21375    1.02536   0.172375  1.58343    1.42721    0.362541  0.806506
bin_0    2.56989   0.189072  0.0584559  1.18572   2.89588    1.0269    0.588527  1.43727    1.15083    0.481494  1.14894
bin_1    0.891108  1.8695    0.745136   1.20492   1.70315    0.847816  0.594807  2.07083    0.976213   1.10062   1.50381
bin_2    1.52563   1.457     0.63653    1.30845   1.20683    3.38981   0.592887  1.28732    1.73404    0.650986  0.949564
bin_3    1.16377   1.90626   0.494852   1.35068   0.834698   0.633847  0.568992  1.4389     0.711496   0.704336  2.58779
bin_4    1.24058   1.73259   0.61093    1.18378   2.08196    0.788967  0.527168  1.65959    0.866183   1.33452   1.12513
bin_5    1.04348   1.81431   0.586193   1.24874   0.741421   1.22508   0.715883  1.61998    0.549155   0.518901  1.57706
bin_6    3.32133   0.828116  0.338604   1.12241   1.20285    1.5681    0.563899  0.734314   0.612557   1.74939   1.68789
bin_7    0.944935  1.77331   0.663553   1.42468   1.86965    0.616514  0.592073  2.03353    4.51463    0.51846   0.913566
bin_8    1.07459   2.00846   0.561408   1.39875   3.62059    0.993099  0.580921  0.818795   0.525031   0.677357  1.05758
bin_9    1.3114    1.84974   0.556203   1.81991   0.776774   0.426529  0.438406  0.606026   0.681471   0.600173  0.908092
bin_10   1.07645   2.0603    0.588504   1.78496   0.670714   0.506144  0.277012  0.368605   0.353714   0.39596   1.78975
bin_11   1.16458   2.01177   0.602486   1.60105   0.886593   0.772221  0.521039  0.734554   0.691309   0.895119  1.99165
bin_12   1.56746   1.98691   0.509547   2.21692   0.776701   0.309297  0.220094  0.207493   0.250682   0.392601  1.05725
bin_13   1.07813   2.64833   0.485758   1.26585   0.359332   0.487245  0.436697  0.667043   3.03366    0.673357  4.02023
bin_14   1.02569   3.0647    0.548922   1.69616   0.425591   0.300204  0.309776  3.78924    0.794634   0.582365  1.31125
{% endhighlight %}

# Code snippets

{% highlight javascript %}
# Table for yield ratios

awk '{print 
$1/($25+0.00000000000000000001) "   "  
$2/($25+0.00000000000000000001) "   "  
$3/($25+0.00000000000000000001) "   "  
$4/($25+0.00000000000000000001) "   "  
$5/($25+0.00000000000000000001) "   "  
$6/($25+0.00000000000000000001) "   "  
$7/($25+0.00000000000000000001) "   "  
$8/($25+0.00000000000000000001) "   "  
$9/($25+0.00000000000000000001) "   "  
$10/($25+0.00000000000000000001) "   "  
$11/($25+0.00000000000000000001) "   "  
$12/($25+0.00000000000000000001) "   "  
$13/($25+0.00000000000000000001) "   "  
$14/($25+0.00000000000000000001) "   "  
$15/($25+0.00000000000000000001) "   "  
$16/($25+0.00000000000000000001) "   "  
$17/($25+0.00000000000000000001) "   "  
$18/($25+0.00000000000000000001) "   "  
$19/($25+0.00000000000000000001) "   "  
$20/($25+0.00000000000000000001) "   "  
$21/($25+0.00000000000000000001) "   "  
$22/($25+0.00000000000000000001) "   "  
$23/($25+0.00000000000000000001) "   " 
$24/($25+0.00000000000000000001) "   " 
$25/($25+0.00000000000000000001) "   "}' mva28_trafo6_2j.txt | column -t
{% endhighlight %}

{% highlight javascript %}
# Table for yield ratios v2

less  mva28_trafo6_2j.txt  | column -t | awk 'NR>1 {sig=$1+$2+$3+$4+$5; bkg=$6+$7+$8+$9+$10+$11+$12+$13+$14+$15+$16+$17+$18+$19+$20+$21+$22+$23+$24; print  $1/(sig) "   "   $2/(sig) "   "   $3/(sig) "   "   $4/(sig) "   "   $5/(sig) "   "   $6/(bkg) "   "   $7/(bkg) "   "   $8/(bkg) "   "   $9/(bkg) "   "   $10/(bkg) "   "   $11/(bkg) "   "   $12/(bkg) "   "   $13/(bkg) "   "   $14/(bkg) "   "   $15/(bkg) "   "   $16/(bkg) "   "   $17/(bkg) "   "   $18/(bkg) "   "   $19/(bkg) "   "   $20/(bkg) "   "   $21/(bkg) "   "   $22/(bkg) "   "   $23/(bkg) "   "  $24/(bkg) "   " sig "   " bkg; } ' | column -t
{% endhighlight %}

{% highlight javascript %}
# Table for stat errors

less  mva28_trafo6_2j_Err.txt  | column -t | awk 'NR>1 {sig=$1*$1+$2*$2+$3*$3+$4*$4+$5*$5; bkg=$6*$6+$7*$7+$8*$8+$9*$9+$10*$10+$11*$11+$12*$12+$13*$13+$14*$14+$15*$15+$16*$16+$17*$17+$18*$18+$19*$19+$20*$20+$21*$21+$22*$22+$23*$23+$24*$24; print  $1*$1/(sig) "   "   $2*$2/(sig) "   "   $3*$3/(sig) "   "   $4*$4/(sig) "   "   $5*$5/(sig) "   "   $6*$6/(bkg) "   "   $7*$7/(bkg) "   "   $8*$8/(bkg) "   "   $9*$9/(bkg) "   "   $10*$10/(bkg) "   "   $11*$11/(bkg) "   "   $12*$12/(bkg) "   "   $13*$13/(bkg) "   "   $14*$14/(bkg) "   "   $15*$15/(bkg) "   "   $16*$16/(bkg) "   "   $17*$17/(bkg) "   "   $18*$18/(bkg) "   "   $19*$19/(bkg) "   "   $20*$20/(bkg) "   "   $21*$21/(bkg) "   "   $22*$22/(bkg) "   "   $23*$23/(bkg) "   "  $24*$24/(bkg) "   " sqrt(sig) "   " sqrt(bkg); } ' | column -t
{% endhighlight %}

# Sort main samples

awk '{print $1 "   "  $2 "   " $3  "   " $24 "   " $14 "   " $12 "   " $13 "   " $18 "   "  $19 "   " $20 "   " $21}' temp.txt | column -t
awk '{print $1 "   "  $2 "   " $3  "   " $24 "   " $14 "   " $12 "   " $13 "   " $18 "   "  $19 "   " $20 "   " $21 "   " $25 "   " $26}' temp.txt | column -t

{% highlight javascript %}
# Compute effective number of MC events

awk 'NR>1{print $1/$26*$1/$26 "    " $2/$27*$2/$27 "    " $3/$28*$3/$28 "    " $24/$49*$24/$49 "    " $5/$30*$5/$30 "    " $6/$*$1/$26 "    " $1/$26*$1/$26 "    " $1/$26*$1/$26 "    " $1/$26*$1/$26 "    " $1/$26*$1/$26 "    " $1/$26*$1/$26; qqWH+=  $1/$26*$1/$26;} END{print qqWH}' temp.txt | column -t
{% endhighlight %}
