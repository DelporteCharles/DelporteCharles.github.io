---
layout: post
title: Single event run_1
tags: 
    - colorflow
---

# To-Do list
- [ ] Issue with Herwig parton status ?

`root -l /sps/atlas/d/delporte/COLORFLOW/athena/production/ppzgvvbb_herwig/DAOD/DAOD_TRUTH1.test2_ppzgvvbb.pool.root`
`CollectionTree->Scan("TruthParticlesAux.status:TruthParticlesAux.pdgId")`

- [ ] Issue with parton container ordering after Parton Shower ? (fix with dR for now : label may be a good check)
- [ ] Understand following plot
![dRBBQuarki.png](quiver-image-url/05CF499F6005B844263936DF3B5BB4A9.png =696x472)
![mBBQuarki.png](quiver-image-url/3CD10179CA8E0B3F02D3A4CEF4F98ECD.png =696x472)
* pT / Angular distance of b1 b2 smeared before PS only for ppzhvvbb (not for ppzgvvbb), but mass still 125 ...
* Could be status 22 in Pythia, but it appears to be 23 ...
* http://home.thep.lu.se/~torbjorn/pythia81html/ParticleProperties.html
- [ ] Also suspicious
![dRb1b1PSHist.png](quiver-image-url/4909E92E3147C1A39D9445CA3B4D4F02.png =696x472)
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
![cutflow_4.png](quiver-image-url/73F165BEC6495C89E8A71C5217CD5D4C.png =696x472)
* Quite large difference in efficiency with passMBB

# Inclusive cuts
![cuts_4.png](quiver-image-url/191E27FD4A45B5DE2566383CB0732583.png =696x472)

# Loose selection
## Leading jet
![dTheta1L_4.png](quiver-image-url/849F5C74A0E11E30CF90B536ECA2FF08.png =696x472)

## Sub-leading jet
![dTheta2L_4.png](quiver-image-url/EB91147894A3C954DD6B538D9A4D838E.png =696x472)

## Correlations
## ppzhvvbb
![ppzhvvbb_dTheta12L_4.png](quiver-image-url/ACF197AC6DEB2F93CFC92859B3842F8A.png =696x472)
## ppzhvvbb_herwig
![ppzhvvbb_herwig_dTheta12L_4.png](quiver-image-url/43527A4B5DDF306B851C5A0310054B6B.png =696x472)
## ppzgvvbb
![ppzgvvbb_dTheta12L_4.png](quiver-image-url/56DBAD401AE7CDCB0B900F6914455498.png =696x472)
## ppzgvvbb_herwig
![ppzgvvbb_herwig_dTheta12L_4.png](quiver-image-url/721EF0F1E026C734067B8B2B6C0F0CD5.png =696x472)
## ppzgvvbb_revert
![ppzgvvbb_revert_dTheta12L_4.png](quiver-image-url/C23007A6318ECD843E194C52DE02E3EC.png =696x472)
## ppzgvvbb_revert_herwig
![ppzgvvbb_revert_herwig_dTheta12L_4.png](quiver-image-url/F9F3760040273251F59B84DF37A8A860.png =696x472)

### Conclusion

# Tight selection
## Leading jet
![dTheta1T_4.png](quiver-image-url/1E256B070AC3460B1938C3FEE0D24132.png =696x472)
## Sub-leading jet
![dTheta2T_4.png](quiver-image-url/2CC1AE01D5979CF5E515CA5BDA9E9E52.png =696x472)

## Correlations
## ppzhvvbb
![ppzhvvbb_dTheta12T_4.png](quiver-image-url/BBFF8B59932A9A2E48B728E661980068.png =696x472)
## ppzhvvbb_herwig
![ppzhvvbb_herwig_dTheta12T_4.png](quiver-image-url/BB7D2855C3EB21CE636F14B197A4A82C.png =696x472)
## ppzgvvbb
![ppzgvvbb_dTheta12T_4.png](quiver-image-url/5B3D4A4EAF04151C2FB2D95E4A18073C.png =696x472)
## ppzgvvbb_herwig
![ppzgvvbb_herwig_dTheta12T_4.png](quiver-image-url/5633098D980E49C57CC145E14AB4E274.png =696x472)
## ppzgvvbb_revert
![ppzgvvbb_revert_dTheta12T_4.png](quiver-image-url/34F29470D1957AFDFD1EBFDDC0B2CA61.png =696x472)
## ppzgvvbb_revert_herwig
![ppzgvvbb_revert_herwig_dTheta12T_4.png](quiver-image-url/3A5FC5C9F06A27FAAE72E46AE0ABA57E.png =696x472)



### Conclusion

# Additionnal distributions
## mBB
![mBB_4.png](quiver-image-url/10F3BCF00781AE1F3318911ED12D11EB.png =696x472)

## dRBB
![dRBB_4.png](quiver-image-url/2602F52A211CACF76405934C2FFBB160.png =696x472)

## pTB1
![pTB1_4.png](quiver-image-url/61B69EBD5399F43EB4A6E661D559FC97.png =696x472)

## pTB2
![pTB2_4.png](quiver-image-url/A83725223FADD23B83820C50E60D317E.png =696x472)


