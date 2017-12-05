---
title: Single event run_0
date: '2017-07-13'
tags:
- colorflow
---
# Single event study
* Studying one single event hadronized 100 000 times
--> This event has mBB = 333 GeV, hence not passing the nominal VH(bb) selection ... to be replaced with another ME.

## Nominal event

{% highlight javascript %}
<event>                                                                                                                                  
 7   1  0.1716775E-08  0.3806288E+03  0.7546771E-02  0.1072767E+00                                                                       
        2   -1    0    0  501    0  0.00000000000E+00  0.00000000000E+00  0.78612500155E+03  0.78612500155E+03  0.00000000000E+00 0. -1.
       -2   -1    0    0    0  502 -0.00000000000E+00 -0.00000000000E+00 -0.12830183999E+03  0.12830183999E+03  0.00000000000E+00 0.  1.
       23    2    1    2    0    0 -0.80472871886E+02  0.16529246825E+03  0.41435022168E+03  0.46258906084E+03  0.92222827041E+02 0.  0.
       12    1    3    3    0    0 -0.26618011284E+02 -0.49880281338E+01  0.54206088300E+02  0.60594545614E+02  0.00000000000E+00 0. -1.
      -12    1    3    3    0    0 -0.53854860602E+02  0.17028049638E+03  0.36014413338E+03  0.40199451522E+03  0.00000000000E+00 0.  1.
        5    1    1    2  501    0  0.21030227951E+03 -0.91415952404E+02  0.12560807438E+03  0.26150220547E+03  0.47000000000E+01 0. -1.
       -5    1    1    2    0  502 -0.12982940762E+03 -0.73876515846E+02  0.11786486551E+03  0.19033557523E+03  0.47000000000E+01 0.  1.
<mgrwt>                                                                                                                                  
<rscale>  0 0.32634131E+03</rscale>                                                                                                      
<asrwt>0</asrwt>                                                                                                                         
<pdfrwt beam="1">  1        2 0.12094231E+00 0.38062883E+03</pdfrwt>                                                                     
<pdfrwt beam="2">  1       -2 0.19738745E-01 0.38062883E+03</pdfrwt>                                                                     
<totfact> 0.77979038E+02</totfact>                                                                                                       
</mgrwt>                                                                                                                                 
</event>                                                                                                                                 
{% endhighlight %}

## Color Reverted event

{% highlight javascript %}
<event>                                                                                                                                  
 7   1  0.1716775E-08  0.3806288E+03  0.7546771E-02  0.1072767E+00                                                                       
       -2   -1    0    0    0  502  0.00000000000E+00  0.00000000000E+00  0.78612500155E+03  0.78612500155E+03  0.00000000000E+00 0. -1.
        2   -1    0    0  501    0 -0.00000000000E+00 -0.00000000000E+00 -0.12830183999E+03  0.12830183999E+03  0.00000000000E+00 0.  1.
       23    2    1    2    0    0 -0.80472871886E+02  0.16529246825E+03  0.41435022168E+03  0.46258906084E+03  0.92222827041E+02 0.  0.
       12    1    3    3    0    0 -0.26618011284E+02 -0.49880281338E+01  0.54206088300E+02  0.60594545614E+02  0.00000000000E+00 0. -1.
      -12    1    3    3    0    0 -0.53854860602E+02  0.17028049638E+03  0.36014413338E+03  0.40199451522E+03  0.00000000000E+00 0.  1.
        5    1    1    2  501    0  0.21030227951E+03 -0.91415952404E+02  0.12560807438E+03  0.26150220547E+03  0.47000000000E+01 0. -1.
       -5    1    1    2    0  502 -0.12982940762E+03 -0.73876515846E+02  0.11786486551E+03  0.19033557523E+03  0.47000000000E+01 0.  1.
<mgrwt>                                                                                                                                  
<rscale>  0 0.32634131E+03</rscale>                                                                                                      
<asrwt>0</asrwt>                                                                                                                        
<pdfrwt beam="1">  1        2 0.12094231E+00 0.38062883E+03</pdfrwt>                                                                     
<pdfrwt beam="2">  1       -2 0.19738745E-01 0.38062883E+03</pdfrwt>                                                                     
<totfact> 0.77979038E+02</totfact>                                                                                                       
</mgrwt>                                                                                                                                 
</event>                                                                                                                                  
{% endhighlight %}

### Reminder of the selections
- [ ] Here remind the cuts applied

### Colors
| Sample          | Color  | 
| --------------- | ------ |
| ppzgvvb         | Blue   |
| ppzgvvbb_revert | Violet |
| ppzavvbb        | Green  |

# Loose selection

## Leading jet
### Jet radius = 0.4
![dTheta1L_4.png](/images/q/dTheta1L_4.png)
### Jet radius = 0.7
![dTheta1L_7.png](/images/q/dTheta1L_7.png)
### Jet radius = 1.0
![dTheta1L_10.png](/images/q/dTheta1L_10.png)

## Sub-leading jet
### Jet radius = 0.4
![dTheta2L_4.png](/images/q/dTheta2L_4.png)
### Jet radius = 0.7
![dTheta2L_7.png](/images/q/dTheta2L_7.png)
### Jet radius = 1.0
![dTheta2L_10.png](/images/q/dTheta2L_10.png)

### Conclusion
The larger is the jet, the sharper is the dTheta distribution

# Tight selection
(with coarser binning)

## Leading jet
### Jet radius = 0.4
![dTheta1T_4.png](/images/q/dTheta1T_4.png)
### Jet radius = 0.7
![dTheta1T_7.png](/images/q/dTheta1T_7.png)
### Jet radius = 1.0
![dTheta1T_10.png](/images/q/dTheta1T_10.png)

## Sub-leading jet
### Jet radius = 0.4
![dTheta2T_4.png](/images/q/dTheta2T_4.png)
### Jet radius = 0.7
![dTheta2T_7.png](/images/q/dTheta2T_7.png)
### Jet radius = 1.0
![dTheta2T_10.png](/images/q/dTheta2T_10.png)

### Conclusion
- Large change in shape for the tight selection, sub-leading jet with radius 1.0
- Missing statistics in tight selection phase space ?
- [x] Check : what cut is removing that many events ? The only difference being the parton shower, either all events should pass, either none of them ...
- - The mBB invariant mass was 330 GeV, hence nominal Matrix Element did not pass the cut 110 GeV < mBB < 140 GeV



