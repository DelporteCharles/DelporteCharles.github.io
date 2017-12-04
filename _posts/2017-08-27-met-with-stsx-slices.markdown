---
layout: post
title: MET with STSX slices
tags: 
    - STXS
    - ttbar
---

Request for looking at the contamination of samples PowhegPythiaEvtGen_P2012CT10_ttbarMET200 and PowhegPythiaEvtGen_P2012CT10_ttbarMET300 within our Signal Region

### JobOptions
https://svnweb.cern.ch/trac/atlasoff/browser/Generators/MC15JobOptions/trunk/share/DSID407xxx/MC15.407012.PowhegPythiaEvtGen_P2012CT10_ttbarMET200_hdamp172p5_nonAH.py
https://svnweb.cern.ch/trac/atlasoff/browser/Generators/MC15JobOptions/trunk/share/DSID407xxx/MC15.407322.PowhegPythiaEvtGen_P2012CT10_ttbarMET300_hdamp172p5_nonAH.py

### Production jobs
| Task                                    | Input container                                                                                                              |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| https://bigpanda.cern.ch/task/12183811/ | mc15_13TeV.407012.PowhegPythiaEvtGen_P2012CT10_ttbarMET200_hdamp172p5_nonAH.merge.DAOD_HIGG5D1.e4023_s2608_r7725_r7676_p2949 |
| https://bigpanda.cern.ch/task/12183810/ | mc15_13TeV.407322.PowhegPythiaEvtGen_P2012CT10_ttbarMET300_hdamp172p5_nonAH.merge.DAOD_HIGG5D1.e5680_s2726_r7772_r7676_p2949 |

## Results
| Sample | 2 tags jets | 2 tags 3 jets |
| ------ | ----------- | ------------- |
| PwPy6  | 510.661808  | 3650.754410   |
| PwPy8  | 476.105722  | 3400.533659   |
| MET200 | 64.748327   | 587.710176    |
| MET300 | 6.778717    | 52.737960     |

### Yields

### Distributions
![IMAGE](quiver-image-url/278E9ADD1F5F1D6C56C61BFE77EB9A1B.jpg =795x563)
![IMAGE](quiver-image-url/6603CCE57F2EB6553A9836933ED94CD2.jpg =776x567)

* MET resolution study
--> truthMET:MET plots (x is MET)
### PwPy6
![IMAGE](quiver-image-url/7FB4DEC6920A9D152B4C74597EF6173A.jpg =675x460)
![IMAGE](quiver-image-url/99604F93CA942CD3F9055F6A601B68A9.jpg =666x447)
### PwPy8
![IMAGE](quiver-image-url/E5509989192C0286EE612D0BF6B6C224.jpg =663x455)
![IMAGE](quiver-image-url/577EF3C62A33F84322C8B105C5B429A2.jpg =666x459)
### MET200
![IMAGE](quiver-image-url/21522ECBD2403417E3B6A64A4B27BF9A.jpg =679x453)
![IMAGE](quiver-image-url/C035053B9979635C2A3C48E9D4C0983E.jpg =671x454)
### MET300
![IMAGE](quiver-image-url/051AA7EA2AF997D288D009DE9AC155EF.jpg =671x443)
![IMAGE](quiver-image-url/36123ECFCE78799DEF106599AD373864.jpg =671x463)

## LOG scale
![IMAGE](quiver-image-url/619BB0534F81A40E496519ED60015625.jpg =783x562)
![IMAGE](quiver-image-url/7D083CDAD3352A40438593487DAFC9D5.jpg =792x560)
