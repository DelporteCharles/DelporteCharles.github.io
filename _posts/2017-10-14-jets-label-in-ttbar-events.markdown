---
layout: post
title: Jets label in ttbar events
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
![IMAGE](quiver-image-url/CD80126D98BDEE6BB8395B395C143E2C.jpg =960x656)

* **most plots normalised to unity**

## AllSignal jets

### 2 jets
![IMAGE](quiver-image-url/6F4A3E630AB71CBE47066E0A7FA920C7.jpg =1392x805)

{% highlight sh %}
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==2)*(nTags==2)","colz norm text")
{% endhighlight %}

### 3 jets
![IMAGE](quiver-image-url/ED336EDEE67AB184A2D90FF4271B1E0A.jpg =1388x805)
![IMAGE](quiver-image-url/4C5CF67F584ECF68EAB86A2B808ADC6F.jpg =1387x798)
![IMAGE](quiver-image-url/BEF315121FE32FBED9B70D030DC4F8C8.jpg =1386x801)

Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")
Nominal->Draw("j3Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")
Nominal->Draw("j3Flav:b2Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")

## Evolution with MET in all signal jets

* **looks like at high MET, the fraction of bb events decreases especially in favor of bc events**

### 2 jets
![IMAGE](quiver-image-url/11F1D9BFCCF4DA935B59C7B3D7CE5577.jpg =1391x810)
![IMAGE](quiver-image-url/BE6E43C202C44512D3ED1C62272C32DF.jpg =1389x804)

{% highlight sh %}
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==2)*(nTags==2)*(MET<200)","colz norm text")
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==2)*(nTags==2)*(MET>200)","colz norm text")
{% endhighlight %}

### 3 jets
![IMAGE](quiver-image-url/3B2BC8809C8E9A964F73FF3DF4764326.jpg =1382x801)
![IMAGE](quiver-image-url/CD1D8C0E181EB1142D805DBCFBA3F95C.jpg =1383x813)

Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)*(MET<200)","colz norm text")
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)*(MET>200)","colz norm text")

## Leading2Signal jets

* **normalised to unity**

### 3 jets
![IMAGE](quiver-image-url/EE7ABE74F789DBAE6D5555613D295B1F.jpg =1385x807)
![IMAGE](quiver-image-url/203216D92116D2441FC6DA0D807478CC.jpg =1386x806)
![IMAGE](quiver-image-url/305C0844F88C501F57E69C9BE105D701.jpg =1378x810)

{% highlight sh %}
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")
Nominal->Draw("j3Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")
Nominal->Draw("j3Flav:b2Flav","EventWeight*(nJ==3)*(nTags==2)","colz norm text")
{% endhighlight %}

## Evolution with MET in Leading2Signal jets

* **same conclusion as all signal jets : looks like at high MET, the fraction of bb events decreases especially in favor of bc events**

### 3 jets
![IMAGE](quiver-image-url/D69CFBCD45C7227EC09F2973461F773C.jpg =1385x803)
![IMAGE](quiver-image-url/9D2EB11E5BEC8EC286583EE1707421E4.jpg =1381x802)

{% highlight sh %}
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)*(MET<200)","colz norm text")
Nominal->Draw("b2Flav:b1Flav","EventWeight*(nJ==3)*(nTags==2)*(MET>200)","colz norm text")
{% endhighlight %}


