---
title: Retrieving HEPMC in ASCII format
date: '2017-08-22'
tags:
- daod
- hepmc
- truth
---
https://twiki.cern.ch/twiki/bin/view/AtlasProtected/TruthDAODTutorial#Dumping_HepMC_to_ASCI

{% highlight javascript %}
setupATLAS
asetup 20.1.8.1,AtlasDerivation,gcc48,here

get_files HepMCTruthReader_jobOptions.py
athena HepMCTruthReader_jobOptions.py > HepMCTruth.txt
{% endhighlight %}

