---
title: FCNC TruthLevel discriminating variables
date: '2018-02-13'
tags:
- fcnc
---
# Purpose

* find discriminating variables from the truth event with particles at 'Matrix Element' level
* available for signal sample, but not for backgrounds (no relevant MC) : still, can give some ideas
)
# Samples

* ttWmqq only for now (v0)
)
# Selection

* apply the pre-selection at reco level on events
  * 1 lepton et >= 2 jets (pas encore de plots)
  * 0 lepton et >= 4 jets
* look at some distributions of the event at truth level
  * not the full reco selection is applied, just requiring at least on b-Tagged reco jet in my macro
  * dans les prochaines iterations, peut-etre plus utile de faire ces plots pour les evenements passant la selection reco, qui est deja plutot loose
)
# Commentaires

Quelques variables pourraient montrer une bonne discrimination d'apres les shapes (pas trop smoothed), mais a confirmer en comparaison au bruit de fond :
* dR(gam, gam) mais qui sera surement tres correle a la coupure sur m(gam, gam), donc ca piquera surement aussi dans le bruit de fond
* pT leading gamma
* pT b-jet
* min dR(b-jet, jet additionnels)
* coupure superieure sur le pT du subleading quark du W SM ? je testerai les associations en delta R entre ce quark et le subleading jet au niveau reco, voir si ca peut vraiment motiver une coupure 
)
# top Exotic (tcH)
)
## dR(c,H)
![IMAGE](/images/q/D60621B4670E27BC7D7D6CEBDA5612B7.jpg)
## dPhi(c,H)
![IMAGE](/images/q/1472906913DB15BED95B21007475881A.jpg)
### dR(gam, gam)
![IMAGE](/images/q/E732CC871C4F554F048B79DF0A3C92A1.jpg)
## dPhi(gam, gam)
![IMAGE](/images/q/539D6ABE157EB72684925EE6F8FF6A97.jpg)
### pT(H)
![IMAGE](/images/q/B99A8F16E822E12A295F6CB03F156B62.jpg)
### eta(H)
![IMAGE](/images/q/83FE0B5F72B797946971313B07E20D99.jpg)
### pT(c)
![IMAGE](/images/q/DB527907D1EF5ABEDEF0C1BB7EA783AF.jpg)
### eta(c)
![IMAGE](/images/q/36D3806E020598E8AEE756B7D687FB53.jpg)
### pT(leading gam)
![IMAGE](/images/q/A8DCF74F6CB96758EB43A63C370F11E3.jpg)
### pT(subleading gam)
![IMAGE](/images/q/230DCF7218822FB5C2DE5D434596E71E.jpg)
### eta(leading gam)
![IMAGE](/images/q/5DD6487E7BFBD58B458BFB2C645E85BC.jpg)
### eta(subleading gam)
![IMAGE](/images/q/CE5DBE97ADDD53E0DEBDD4B6DC1A8D9B.jpg)
### min dR(c, gam)
![IMAGE](/images/q/8F33F39B037231EAE82AE393586EC63C.jpg)
### min dPhi(c, gam)
![IMAGE](/images/q/AE3BB7CA678E1317AD068CB93DCFE1AE.jpg)
# top SM
)
## pT (b)
![IMAGE](/images/q/A23197B3CDE3AED6DFE0FA3751FC34F1.jpg)
## eta (b)
![IMAGE](/images/q/736A7E2FA9489C6AF663D584FBA77860.jpg)
## pT (leading quark from the W)
![IMAGE](/images/q/09BFCDDDE3BC96474BABECC55B3C8B9B.jpg)
## eta (leading quark from the W)
![IMAGE](/images/q/37A56B0876D39EE895F068B14D3A8D92.jpg)
## pT (subleading quark from the W)
![IMAGE](/images/q/D3A22AC1770A5674AFE69CB2127B8EBC.jpg)
## eta (subleading quark from the W)
![IMAGE](/images/q/A783B6936FC5FD35DBC226391AA07DF3.jpg)
## min dR(b, quark from the W)
![IMAGE](/images/q/5CF7D3CCC383848F0F40BBBA3F421CF1.jpg)
## min dPhi(b, quark from the W)
![IMAGE](/images/q/0F0E152117AF66747FC14BF639C616EC.jpg)
## dR(b, W)
![IMAGE](/images/q/86ED2D5EE60BD446B3D525333A9A4D5D.jpg)
## dPhi(b, W)
![IMAGE](/images/q/922BF8F5E21478F06ED31B9BD84B4754.jpg)
