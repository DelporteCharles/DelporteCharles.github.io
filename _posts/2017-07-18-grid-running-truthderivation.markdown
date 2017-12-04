---
layout: post
title: Grid running TruthDerivation
tags: 
    - computing
    - daod
    - derivation
    - truth
---


## Useful links
https://twiki.cern.ch/twiki/bin/view/AtlasComputing/TransformConfiguration
https://twiki.cern.ch/twiki/bin/view/AtlasProtected/TruthDAODTutorial
https://twiki.cern.ch/twiki/bin/view/AtlasProtected/TruthDAOD

{% highlight javascript %}
export EOS_MGM_URL=root://eosatlas.cern.ch
export RUCIO_ACCOUNT=cdelport
setupATLAS 
lsetup rucio
lsetup panda
voms-proxy-init -voms atlas
{% endhighlight %}

{% highlight javascript %}
pathena --trf \
"Reco_tf.py --inputEVNTFile %IN --outputDAODFile %OUT.pool.root --reductionConf TRUTH1" \
--inDS mc15_13TeV.410249.Sherpa_221_NNPDF30NNLO_ttbar_AllHadronic_MEPS_NLO.evgen.EVNT.e5450 \
--outDS user.cdelport.mc15_13TeV.410249.Sherpa_221_NNPDF30NNLO_ttbar_AllHadronic_MEPS_NLO.TRUTH1
{% endhighlight %}
