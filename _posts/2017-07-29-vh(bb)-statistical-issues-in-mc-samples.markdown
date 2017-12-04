---
layout: post
title: VH(bb) statistical issues in MC samples
tags: 
    - statistics
    - VHbb
---

* Purpose : spot MC samples / slices missing statistics

## All samples

http://cdelport.web.cern.ch/cdelport//SMVHbb//plots_v28/index.html

## Last 5 BDT bins 
### 2 jets category

{% highlight javascript %}
cd /sps/atlas/d/delporte/SMVHbbRun2/CxAODFramework_tag28
vimdiff plots_v28/2tag2jet_150ptv_SR/yield_2tag2jet_150ptv_SR.txt  plots_last5binsYieldsTrafo2j/yield_2tag2jet_150ptv_SR_mva28_trafo6.txt
{% endhighlight %}

![IMAGE](quiver-image-url/0C6912DC8573AE4FE07B8780472D84A9.jpg =1386x378)

### 3 jets category 

{% highlight javascript %}
cd /sps/atlas/d/delporte/SMVHbbRun2/CxAODFramework_tag28
vimdiff plots_v28/2tag3jet_150ptv_SR/yield_2tag3jet_150ptv_SR.txt  plots_last5binsYieldsTrafo3j/yield_2tag3jet_150ptv_SR_mva28_trafo6.txt
{% endhighlight %}

![IMAGE](quiver-image-url/68308B104B6DFEA0501F48DA813AFBD6.jpg =1385x378)

## Contribution from each V+jet slice

{% highlight javascript %}
cd /sps/atlas/d/delporte/SMVHbbRun2/CxAODFramework_tag28
paste plots_v28/2tag2jet_150ptv_SR/yield_2tag2jet_150ptv_SR.txt sliceBreakdown/plots_ZnunuB_v221/yield_2tag2jet_150ptv_SR.txt | awk '{print "Histogram " $1 " : Entries " $7/($2+0.0001) " Yield " $8/($3+0.0001)}'
# to be generalised through some shell script
{% endhighlight %}

{% highlight javascript %}
Result :


{% endhighlight %}
