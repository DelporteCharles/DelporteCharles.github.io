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
![dRBBQuarki.png](/images/q/05CF499F6005B844263936DF3B5BB4A9.png)
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
)
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
)
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
)
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
--> Focus on R)
# Cutflows
![cutflow_4.png](/images/q/73F165BEC6495C89E8A71C5217CD5D4C.png)
# Inclusive cuts
![cuts_4.png](/images/q/191E27FD4A45B5DE2566383CB0732583.png)
# Loose selection
## Leading jet
![dTheta1L_4.png](/images/q/849F5C74A0E11E30CF90B536ECA2FF08.png)
# Tight selection
## Leading jet
![dTheta1T_4.png](/images/q/1E256B070AC3460B1938C3FEE0D24132.png)
# Additionnal distributions
## mBB
![mBB_4.png](/images/q/10F3BCF00781AE1F3318911ED12D11EB.png)

)
