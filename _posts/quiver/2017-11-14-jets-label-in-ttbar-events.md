---
title: Jets label in ttbar events
date: '2017-11-14'
tags: []
---
# Purpose

Understand the ttbar composition in the view of designing a potential filter to increase the generation efficiency

https://indico.cern.ch/event/390200/contributions/2144797/attachments/1262002/1865790/ttbarCompositionStudies_private_04_2016.pdf

* Notes :
  * Identical selection, apart from :
    * Anti-QCD cut in 3 jets, mindPhiMETjet > 30 degrees instead of 20 degrees
    * moved from MV2c20 to MV2c10 I think
      * important bTagging algorithm update : better rejection against charm, ~same performace against light

https://indico.cern.ch/event/530666/contributions/2165520/attachments/1271429/1884234/Zaidan_VHbb_2016_05_11.pdf
![IMAGE](/images/q/IMAGE)

* **most plots normalised to unity**

## AllSignal jets

### 2 jets
![IMAGE](/images/q/IMAGE)

{% highlight sh %}
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==2)*(nTags==2)","colz norm text")
{% endhighlight %}

### 3 jets
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")
Nominal->Draw("j3Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")
Nominal->Draw("j3Flav:b2Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")

## Evolution with MET in all signal jets

* **looks like at high MET, the fraction of bb events decreases especially in favor of bc events**

### 2 jets
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

{% highlight sh %}
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==2)*(nTags==2)*(MET<200)","colz norm text")
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==2)*(nTags==2)*(MET>200)","colz norm text")
{% endhighlight %}

### 3 jets
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)*(MET<200)","colz norm text")
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)*(MET>200)","colz norm text")

## Leading2Signal jets

* **normalised to unity**

### 3 jets
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

{% highlight sh %}
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")
Nominal->Draw("j3Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")
Nominal->Draw("j3Flav:b2Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")
{% endhighlight %}

## Evolution with MET in Leading2Signal jets

* **same conclusion as all signal jets : looks like at high MET, the fraction of bb events decreases especially in favor of bc events**

### 3 jets
![IMAGE](/images/q/IMAGE)
![IMAGE](/images/q/IMAGE)

{% highlight sh %}
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)*(MET<200)","colz norm text")
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)*(MET>200)","colz norm text")
{% endhighlight %}



