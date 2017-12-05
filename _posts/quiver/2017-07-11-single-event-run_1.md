---
title: Single event run_1
date: '2017-07-11'
tags:
- colorflow
---
# To-Do list
- [ ] Issue with Herwig parton status ?

`root -l /sps/atlas/d/delporte/COLORFLOW/athena/production/ppzgvvbb_herwig/DAOD/DAOD_TRUTH1.test2_ppzgvvbb.pool.root`
`CollectionTree->Scan("TruthParticlesAux.status:TruthParticlesAux.pdgId")`

- [ ] Issue with parton container ordering after Parton Shower ? (fix with dR for now : label may be a good check)
- [ ] Understand following plot
![dRBBQuarki.png](/images/q/dRBBQuarki.png)
![mBBQuarki.png](/images/q/mBBQuarki.png)
* pT / Angular distance of b1 b2 smeared before PS only for ppzhvvbb (not for ppzgvvbb), but mass still 125 ...
* Could be status 22 in Pythia, but it appears to be 23 ...
* http://home.thep.lu.se/~torbjorn/pythia81html/ParticleProperties.html
- [ ] Also suspicious
![dRb1b1PSHist.png](/images/q/dRb1b1PSHist.png)
- [ ] Herwig Parton Shower leads to much less energy spread ?

# Single event study
* Studying one single event hadronized 100 000 times
* Event selected from [aMC@NLO p p > zh, z > vl vl~, h > b b~](quiver-note-url/7055977C-8582-474F-8C5B-C178E002D558)

### Event number 2 in unweighted_events.lhe

| Variable | Value      |
| -------- | ---------- |
| Mbb      | 124.999444 |
| dRbb     | 1.372611   |
| MET      | 158.759398 |
| dPhiVbb  | 3.587706   |
| pTb1     | 88.564032  |
| pTb2     | 96.316959  |

## Nominal Higgs event

{% highlight javascript %}
<event>
 8   1  0.1076800E-05  0.4978218E+03  0.7546771E-02  0.1014349E+00
       -2   -1    0    0    0  501  0.00000000000E+00  0.00000000000E+00  0.19485010094E+03  0.19485010094E+03  0.00000000000E+00 0.  1.
        2   -1    0    0  501    0  0.00000000000E+00  0.00000000000E+00 -0.31797080540E+03  0.31797080540E+03  0.00000000000E+00 0. -1.
       25    2    1    2    0    0 -0.93032735873E+02  0.12864469144E+03  0.99692722244E+02  0.22531765691E+03  0.12499944427E+03 0.  0.
       23    2    1    2    0    0  0.93032735873E+02 -0.12864469144E+03 -0.22281342671E+03  0.28750324943E+03  0.88361466344E+02 0.  0.
       14    1    4    4    0    0  0.48605111649E+02 -0.10999805969E+03 -0.20184968256E+03  0.23495813321E+03  0.00000000000E+00 0. -1.
      -14    1    4    4    0    0  0.44427624224E+02 -0.18646631753E+02 -0.20963744145E+02  0.52545116219E+02  0.00000000000E+00 0.  1.
        5    1    3    3  502    0 -0.82211340881E+02  0.32937565085E+02  0.29723361873E+01  0.88738450209E+02  0.47000000000E+01 0. -1.
       -5    1    3    3    0  502 -0.10821394993E+02  0.95707126355E+02  0.96720386057E+02  0.13657920670E+03  0.47000000000E+01 0. -1.
<mgrwt>
<rscale>  0 0.49782183E+03</rscale>
<asrwt>0</asrwt>
<pdfrwt beam="1">  1        2 0.48918585E-01 0.49782183E+03</pdfrwt>
<pdfrwt beam="2">  1       -2 0.29976939E-01 0.49782183E+03</pdfrwt>
<totfact> 0.10572441E+03</totfact>
</mgrwt>
</event>                                                                                                                              
{% endhighlight %}

## Beam color connected event

{% highlight javascript %}
<event>
 7   1  0.1076800E-05  0.4978218E+03  0.7546771E-02  0.1014349E+00
       -2   -1    0    0    0  502  0.00000000000E+00  0.00000000000E+00  0.19485010094E+03  0.19485010094E+03  0.00000000000E+00 0.  1.
        2   -1    0    0  501    0  0.00000000000E+00  0.00000000000E+00 -0.31797080540E+03  0.31797080540E+03  0.00000000000E+00 0. -1.
       23    2    1    2    0    0  0.93032735873E+02 -0.12864469144E+03 -0.22281342671E+03  0.28750324943E+03  0.88361466344E+02 0.  0.
       14    1    3    3    0    0  0.48605111649E+02 -0.10999805969E+03 -0.20184968256E+03  0.23495813321E+03  0.00000000000E+00 0. -1.
      -14    1    3    3    0    0  0.44427624224E+02 -0.18646631753E+02 -0.20963744145E+02  0.52545116219E+02  0.00000000000E+00 0.  1.
        5    1    1    2  501    0 -0.82211340881E+02  0.32937565085E+02  0.29723361873E+01  0.88738450209E+02  0.47000000000E+01 0. -1.
       -5    1    1    2    0  502 -0.10821394993E+02  0.95707126355E+02  0.96720386057E+02  0.13657920670E+03  0.47000000000E+01 0. -1.
<mgrwt>
<rscale>  0 0.49782183E+03</rscale>
<asrwt>0</asrwt>
<pdfrwt beam="1">  1        2 0.48918585E-01 0.49782183E+03</pdfrwt>
<pdfrwt beam="2">  1       -2 0.29976939E-01 0.49782183E+03</pdfrwt>
<totfact> 0.10572441E+03</totfact>
</mgrwt>
</event>
{% endhighlight %}

## Beam inverted color connected event

{% highlight javascript %}
<event>
 7   1  0.1076800E-05  0.4978218E+03  0.7546771E-02  0.1014349E+00
       2    -1    0    0    501  0  0.00000000000E+00  0.00000000000E+00  0.19485010094E+03  0.19485010094E+03  0.00000000000E+00 0.  1.
       -2   -1    0    0  0    502  0.00000000000E+00  0.00000000000E+00 -0.31797080540E+03  0.31797080540E+03  0.00000000000E+00 0. -1.
       23    2    1    2    0    0  0.93032735873E+02 -0.12864469144E+03 -0.22281342671E+03  0.28750324943E+03  0.88361466344E+02 0.  0.
       14    1    3    3    0    0  0.48605111649E+02 -0.10999805969E+03 -0.20184968256E+03  0.23495813321E+03  0.00000000000E+00 0. -1.
      -14    1    3    3    0    0  0.44427624224E+02 -0.18646631753E+02 -0.20963744145E+02  0.52545116219E+02  0.00000000000E+00 0.  1.
        5    1    1    2  501    0 -0.82211340881E+02  0.32937565085E+02  0.29723361873E+01  0.88738450209E+02  0.47000000000E+01 0. -1.
       -5    1    1    2    0  502 -0.10821394993E+02  0.95707126355E+02  0.96720386057E+02  0.13657920670E+03  0.47000000000E+01 0. -1.
<mgrwt>
<rscale>  0 0.49782183E+03</rscale>
<asrwt>0</asrwt>
<pdfrwt beam="1">  1        2 0.48918585E-01 0.49782183E+03</pdfrwt>
<pdfrwt beam="2">  1       -2 0.29976939E-01 0.49782183E+03</pdfrwt>
<totfact> 0.10572441E+03</totfact>
</mgrwt>
</event>
{% endhighlight %}

### Reminder of the selections
--> Focus on R = 0.4 jets for now (keep limited number of plots to understand !)

| bool              | pass                                           |
| ----------------- | ---------------------------------------------- |
| pass2BJets        | exactly 2 b-jets (B-hadrons ConeExclHadF)      |
| passJetAccept     | pT > 20 GeV, abseta < 2.5                      |
| passMBB           | mBB in [100, 150] GeV                          |
| passMET           | MET > 130 GeV to enhance stat. (158 GeV at ME) |
| passdPhiBB        | dPhiBB < 140                                   |
| passdPhiVBB       | dPhiVBB > 120                                  |
| passmindPhiMETJet | mindPhiMETJet > 20                             |

| Category | Cuts       |
| -------- | ---------- |
| Loose    | pass2BJets |
| Tight    | all cuts   |

# Cutflows
![cutflow_4.png](/images/q/cutflow_4.png)
* Quite large difference in efficiency with passMBB

# Inclusive cuts
![cuts_4.png](/images/q/cuts_4.png)

# Loose selection
## Leading jet
![dTheta1L_4.png](/images/q/dTheta1L_4.png)

## Sub-leading jet
![dTheta2L_4.png](/images/q/dTheta2L_4.png)

## Correlations
## ppzhvvbb
![ppzhvvbb_dTheta12L_4.png](/images/q/ppzhvvbb_dTheta12L_4.png)
## ppzhvvbb_herwig
![ppzhvvbb_herwig_dTheta12L_4.png](/images/q/ppzhvvbb_herwig_dTheta12L_4.png)
## ppzgvvbb
![ppzgvvbb_dTheta12L_4.png](/images/q/ppzgvvbb_dTheta12L_4.png)
## ppzgvvbb_herwig
![ppzgvvbb_herwig_dTheta12L_4.png](/images/q/ppzgvvbb_herwig_dTheta12L_4.png)
## ppzgvvbb_revert
![ppzgvvbb_revert_dTheta12L_4.png](/images/q/ppzgvvbb_revert_dTheta12L_4.png)
## ppzgvvbb_revert_herwig
![ppzgvvbb_revert_herwig_dTheta12L_4.png](/images/q/ppzgvvbb_revert_herwig_dTheta12L_4.png)

### Conclusion

# Tight selection
## Leading jet
![dTheta1T_4.png](/images/q/dTheta1T_4.png)
## Sub-leading jet
![dTheta2T_4.png](/images/q/dTheta2T_4.png)

## Correlations
## ppzhvvbb
![ppzhvvbb_dTheta12T_4.png](/images/q/ppzhvvbb_dTheta12T_4.png)
## ppzhvvbb_herwig
![ppzhvvbb_herwig_dTheta12T_4.png](/images/q/ppzhvvbb_herwig_dTheta12T_4.png)
## ppzgvvbb
![ppzgvvbb_dTheta12T_4.png](/images/q/ppzgvvbb_dTheta12T_4.png)
## ppzgvvbb_herwig
![ppzgvvbb_herwig_dTheta12T_4.png](/images/q/ppzgvvbb_herwig_dTheta12T_4.png)
## ppzgvvbb_revert
![ppzgvvbb_revert_dTheta12T_4.png](/images/q/ppzgvvbb_revert_dTheta12T_4.png)
## ppzgvvbb_revert_herwig
![ppzgvvbb_revert_herwig_dTheta12T_4.png](/images/q/ppzgvvbb_revert_herwig_dTheta12T_4.png)



### Conclusion

# Additionnal distributions
## mBB
![mBB_4.png](/images/q/mBB_4.png)

## dRBB
![dRBB_4.png](/images/q/dRBB_4.png)

## pTB1
![pTB1_4.png](/images/q/pTB1_4.png)

## pTB2
![pTB2_4.png](/images/q/pTB2_4.png)



