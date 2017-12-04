---
layout: post
title: Tau studies in ttbar samples
---

# Purpose

Interest in extending the SM VH(bb) analyis to events with taus in an additionnal category

![IMAGE](quiver-image-url/A69FC298ED256E92D0DA48E92F87CAEA.jpg =1350x803)

## Tau origin

* Truth matching with truth tau or partons with a dR association with R=0.2

![IMAGE](quiver-image-url/E350848D2D9AA6237AA8587AF5F8C1F3.jpg =1337x808)
![IMAGE](quiver-image-url/BFFEF2C9DE1A76B09B0E0B7B8BD4C118.jpg =1321x806)

| Value   | Meaning                         |
| ------- | ------------------------------- |
| 1       | TruthTau Had.                   |
| 2       | TruthTau Lept.                  |
| - pdgID | parton pdgID if no match in 1-2 |
| 0       | No truthmatch  at all           |



![IMAGE](quiver-image-url/CEC21A94AD8D72367910559EB868C931.jpg =1249x806)
* TruthMatch = 0 in red
* TruthMatch != 0 in blue

![IMAGE](quiver-image-url/7B21E4C0B4E52B87C881EA04038C14CE.jpg =1332x794)
![IMAGE](quiver-image-url/1BF7C40A4CAD3DFACF61E92C7ECF6A7B.jpg =1330x804)

## DeltaR(MET,Tau)
* ttbar :
![IMAGE](quiver-image-url/4AFF5E025A1157B513C80DA9D03C5DB9.jpg =1382x808)
* WHbb
![IMAGE](quiver-image-url/149AE312603E214A54166D1B3747067B.jpg =1374x806)
* in 2 tags
* ![IMAGE](quiver-image-url/06B217A77909BC935483ED2DCBFC8C8D.jpg =1407x511)

# Fixed tau origin
Conflicts Maker/PhPy8 with tau status for truthmatching
* re-run with PwPy6
![IMAGE](quiver-image-url/354699282E819CB6CA95CA82D4606F68.jpg =1286x802)

# DeltaPhi(MET, tau)
* ttbar
![IMAGE](quiver-image-url/A1C3483DFF47DAA2D8E64AA5603B335B.jpg =1378x814)
![IMAGE](quiver-image-url/FC1DA6A8EF4F1F97F5B427E142983AC8.jpg =1315x809)
  * ttbar single leptonic
  ![IMAGE](quiver-image-url/5C8EC5B110C4D7E6C551760C7BA7958F.jpg =1325x808)
  * ttbar dileptonic
  ![IMAGE](quiver-image-url/DC2B114F60835062165A8FA86E79F35B.jpg =1347x815)
* WH
![IMAGE](quiver-image-url/BF69F9032618E1D122828813F0CFD678.jpg =1333x809)
![IMAGE](quiver-image-url/56F05E506CB5783759678C43E41464B5.jpg =1336x805)

{% highlight sh %}
Nominal->Draw("TVector2::Phi_mpi_pi(tau1.Phi()-METp4.Phi())","EventWeight*(nJ<4)*(nTags==2)*(nTaus==1)*(nTruthLepW==1)","")
{% endhighlight %}
