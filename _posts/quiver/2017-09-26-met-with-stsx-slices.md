---
title: MET with STSX slices
date: '2017-09-26'
tags:
- STXS
- ttbar
---
Request for looking at the contamination of samples PowhegPythiaEvtGen_P2012CT10_ttbarMET200 and PowhegPythiaEvtGen_P2012CT10_ttbarMET300 within our Signal Region
)
### JobOptions
https://svnweb.cern.ch/trac/atlasoff/browser/Generators/MC15JobOptions/trunk/share/DSID407xxx/MC15.407012.PowhegPythiaEvtGen_P2012CT10_ttbarMET200_hdamp172p5_nonAH.py
https://svnweb.cern.ch/trac/atlasoff/browser/Generators/MC15JobOptions/trunk/share/DSID407xxx/MC15.407322.PowhegPythiaEvtGen_P2012CT10_ttbarMET300_hdamp172p5_nonAH.py
)
### Production jobs
| Task                                    | Input container                                                                                                              |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| https://bigpanda.cern.ch/task/12183811/ | mc15_13TeV.407012.PowhegPythiaEvtGen_P2012CT10_ttbarMET200_hdamp172p5_nonAH.merge.DAOD_HIGG5D1.e4023_s2608_r7725_r7676_p2949 |
| https://bigpanda.cern.ch/task/12183810/ | mc15_13TeV.407322.PowhegPythiaEvtGen_P2012CT10_ttbarMET300_hdamp172p5_nonAH.merge.DAOD_HIGG5D1.e5680_s2726_r7772_r7676_p2949 |
)
## Results
| Sample | 2 tags jets | 2 tags 3 jets |
| ------ | ----------- | ------------- |
| PwPy6  | 510.661808  | 3650.754410   |
| PwPy8  | 476.105722  | 3400.533659   |
| MET200 | 64.748327   | 587.710176    |
| MET300 | 6.778717    | 52.737960     |
)
### Yields
)
### Distributions
![IMAGE](/images/q/278E9ADD1F5F1D6C56C61BFE77EB9A1B.jpg)
* MET resolution study
--> truthMET:MET plots (x is MET)
### PwPy6
![IMAGE](/images/q/7FB4DEC6920A9D152B4C74597EF6173A.jpg)
## LOG scale
![IMAGE](/images/q/619BB0534F81A40E496519ED60015625.jpg)
