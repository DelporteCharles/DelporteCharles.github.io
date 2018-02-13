---
title: Truthtagging ttbar
date: '2017-12-22'
tags: []
---
# Purpose
* large stat. error contribution from ttbar bc
* apply truth tagging to ttbar events with c-labelled jets
* same procedure as V+jets

* apply rebinning transformation (same bins as inclusive bkg)
)
# Results
)
## 2 jets
)
![IMAGE](/images/q/C06FB0373E1BD90CA63FCD3F0939B8A9.jpg)
{% highlight sh %}
bin 0 has the lowest BDT score

Bin 0  Error dt = 1.65461  Error tt 0.311096 Ratio errtt2/errdt2 0.0353507
Bin 1  Error dt = 2.07171  Error tt 0.447781 Ratio errtt2/errdt2 0.0467165
Bin 2  Error dt = 1.86857  Error tt 0.552657 Ratio errtt2/errdt2 0.0874765
Bin 3  Error dt = 1.9129   Error tt 0.734446 Ratio errtt2/errdt2 0.147413
Bin 4  Error dt = 1.74179  Error tt 0.652893 Ratio errtt2/errdt2 0.140505
Bin 5  Error dt = 1.53244  Error tt 0.50419  Ratio errtt2/errdt2 0.108249
Bin 6  Error dt = 1.55775  Error tt 0.443466 Ratio errtt2/errdt2 0.0810445
Bin 7  Error dt = 0.925072 Error tt 0.349941 Ratio errtt2/errdt2 0.143099
Bin 8  Error dt = 1.21748  Error tt 0.368998 Ratio errtt2/errdt2 0.0918592
Bin 9  Error dt = 1.47533  Error tt 0.347939 Ratio errtt2/errdt2 0.0556196
Bin 10 Error dt = 1.41127  Error tt 0.365117 Ratio errtt2/errdt2 0.0669333
Bin 11 Error dt = 1.26756  Error tt 0.309564 Ratio errtt2/errdt2 0.0596436
Bin 12 Error dt = 1.21266  Error tt 0.331808 Ratio errtt2/errdt2 0.0748684
Bin 13 Error dt = 0.87143  Error tt 0.295633 Ratio errtt2/errdt2 0.11509
Bin 14 Error dt = 1.2143   Error tt 0.26832  Ratio errtt2/errdt2 0.048826
{% endhighlight %}

## 3 jets
)
![IMAGE](/images/q/E6B15EB5499E1619B26FB2E8F33F6EE0.jpg)
{% highlight sh %}
Bin 0  Error dt = 3.41429 Error tt 1.4499 Ratio errtt2/errdt2 0.180334
Bin 1  Error dt = 3.7338  Error tt 1.45936 Ratio errtt2/errdt2 0.152764
Bin 2  Error dt = 4.72531 Error tt 2.05988 Ratio errtt2/errdt2 0.19003
Bin 3  Error dt = 6.00446 Error tt 1.75359 Ratio errtt2/errdt2 0.0852921
Bin 4  Error dt = 5.5028  Error tt 1.78034 Ratio errtt2/errdt2 0.104674
Bin 5  Error dt = 3.97525 Error tt 1.73559 Ratio errtt2/errdt2 0.190619
Bin 6  Error dt = 3.72263 Error tt 1.62704 Ratio errtt2/errdt2 0.191028
Bin 7  Error dt = 3.5347  Error tt 1.23123 Ratio errtt2/errdt2 0.121332
Bin 8  Error dt = 4.41351 Error tt 1.1724 Ratio errtt2/errdt2 0.0705634
Bin 9  Error dt = 4.54472 Error tt 1.08479 Ratio errtt2/errdt2 0.0569742
Bin 10 Error dt = 3.85439 Error tt 1.09768 Ratio errtt2/errdt2 0.0811039
Bin 11 Error dt = 2.63543 Error tt 0.946685 Ratio errtt2/errdt2 0.129035
Bin 12 Error dt = 5.08874 Error tt 1.15969 Ratio errtt2/errdt2 0.0519359
Bin 13 Error dt = 1.76021 Error tt 0.743735 Ratio errtt2/errdt2 0.178529
Bin 14 Error dt = 1.59064 Error tt 0.717617 Ratio errtt2/errdt2 0.203535
{% endhighlight %}

root -l submitDir_ttbarFlav_DirectTagging/hist-ttbar_PwPy8EG.root submitDir_ttbarFlav_TruthTagging/hist-ttbar_PwPy8EG.root

Double_t xbins2j[16])
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
)
