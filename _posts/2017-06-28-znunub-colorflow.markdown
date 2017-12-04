---
layout: post
title: ZnunuB colorflow
tags: 
    - colorflow
    - znunub
    - zvvb
---

[Original note : Samples comparison 1](quiver-note-url/634983E1-784F-4416-9F59-5F235DA0BE8E)

Purpose : understand why loose selection shows similar pull angle distributions in ZvvB and ZHvvbb, while tight selection does not
Context : different shapes looking at the pull angle distribution of the leading jet before (2bjets required) and after all VHbb cuts
Conclusion : ZvvB pull angle distribution is flattened by the mBB [100, 150] GeV cut (?)

## Loose selection
![dTheta1L_4.png](quiver-image-url/32954D0D1E44033D384C5FA3370898A7.png =696x472)
## Tight selection
![dTheta1T_4.png](quiver-image-url/D8DA021C1F787568F75C0621E5885C4C.png =696x472)

Procedure : draw the pull angle distribution at each step of the cutflow

# Selection
| step | bool              | pass                                           |
| ---- | ----------------- | ---------------------------------------------- |
| 0    | all               | at least 2 jets reconstructed                  |
| 1    | pass2BJets        | exactly 2 b-jets (B-hadrons ConeExclHadF)      |
| 2    | passJetAccept     | pT > 20 GeV, abseta < 2.5                      |
| 3    | passMBB           | mBB in [100, 150] GeV                          |
| 4    | passMET           | MET > 130 GeV to enhance stat. (158 GeV at ME) |
| 5    | passdPhiBB        | dPhiBB < 140                                   |
| 6    | passdPhiVBB       | dPhiVBB > 120                                  |
| 7    | passmindPhiMETJet | mindPhiMETJet > 20                             |

# Plots
## all
![dTheta1_4_cut0.png](quiver-image-url/302CD38D21BFC769C006710D72E0A326.png =696x472)
## pass2BJets
![dTheta1_4_cut1.png](quiver-image-url/869E00870B966B57FCE15E9A0099A674.png =696x472)
## passJetAccept
![dTheta1_4_cut2.png](quiver-image-url/7EC0EFDC44D0B7A4279815CA1990979A.png =696x472)
## passMBB
![dTheta1_4_cut3.png](quiver-image-url/10F5036058C76CEDB512D65CF380C18E.png =696x472)
## passMET
![dTheta1_4_cut4.png](quiver-image-url/FB4D725A75E2BCEC3843FEE3FA5A1EE3.png =696x472)
## passdPhiBB
![dTheta1_4_cut5.png](quiver-image-url/648D80E469E89381A95450636845C139.png =696x472)
## passdPhiVBB
![dTheta1_4_cut6.png](quiver-image-url/9B359C56AE9D7B99A5BD9BBD2E815A76.png =696x472)
## passmindPhiMETJet
![dTheta1_4_cut7.png](quiver-image-url/FAB792384C4DE67A6A04C409B3526ED5.png =696x472)
