---
title: FCNC TruthMatching
date: '2018-02-27'
tags:
- fcnc
---
# Purpose

* Voir quelle proportion des objets reco utilises dans l'analyse nous viennent des TruthParticles visées
)
# Sample

* Wmqq
)
# Selection

* habituelle avec les categories de tagging
  * avec les coupures de C-Tagging calibrées
  * avec la coupure FJVT
  * 1) avec jets pt > 30 et tout eta 
  * 2) avec jets pt > 25 et abseta < 2.5
)
# Matching

* un objet est matched si dans son utilisation dans le calcul des mTops et vis a vis du b/c-tagging, il presente dR < 0.4 avec l'objet truth correspondant
* pour les deux quarks dans W->qq du top SM, je match d'abord le leading quark avec le jet le plus proche (parmi les deux jets non b-tagged utilise dans le top SM), et le subleading quark est alors associe a l'autre jet
* s'il n'y a pas de jet b-tagged ou qu'il y en a plusieurs, ils sont ordonnés en pT pour savoir lequel doit matcher à quel quark
)
# Bins

* 4 : b, c, q0 et q1 matched (q0 et q1 dans W->qq)
* 3 : b et c matched, mais pas q0 et/ou q1
* 2 : c matched mais pas b
* 1 : b matched mais pas c
* 0 : ni b ni c matched
)
# Principales observations

* en Tight A : bon matching bcqq et bc (4eme et 5eme bins), entre 30% et 40% chacun
* en Tight B : on match plus souvent le b mais pas le c (2eme bin) : normal, c'est la categorie un bTag mais pas de cTag
  * mais dans 1/5 des evenements, on a quand meme tous les bons objets (5eme bin)
  * dans encore 1/5 des evenements, on a quand meme la bonne paire bc (4eme bin)
* en Tight C : on match plus souvent le c mais pas le b (normal, c'est la categorie un cTag mais pas de bTag)

* dans ces categories tight, on a plutot interet a garder les coupures actuelles sur les jets (30 GeV tout eta) plutot que 25 GeV abseta < 2.5

* en Loose A : c'est le matching bc mais il manque au moins un des quarks de Wqq qui domine (3eme bin), autour de 60%-70%, donc rien de choquant : on a un mauvais jet dans le top2, c'est normal qu'il y aie besoin d'une fenetre en masse plus large
* en Loose B : idem, mais contribution plus importante de b matched sans le c (2eme bin), et un peu de ni b ni c matchés (1er bin)
* en Loose C : on match tres souvent le c mais pas le b, dans des proportions similaires a la categorie tight :
)
# Tight A

![IMAGE](/images/q/71D52E9B93C88B487B4E16C74E3F205C.jpg)
# Tight B

![IMAGE](/images/q/7C0605F7491CCDFF6D06DD85D49CCD4E.jpg)
# Tight C

![IMAGE](/images/q/0218856917E265983A4E56E83A60DCA1.jpg)
# Loose A

![IMAGE](/images/q/BA627220AE2634E1AE2EF3753884B613.jpg)
# Loose B

![IMAGE](/images/q/7C7CC1A741FD9E90C875E45DA6569291.jpg)
# Loose C

![IMAGE](/images/q/E5630FE54118508908B2795546F25637.jpg)
# Distributions

* toutes categories (Tight, Loose, ABC) confondues ... mais chaque evenements est accepte au moins dans l'une des categories
)
![at leading q eta(j) (leading q best match).png](/images/q/0E6588E8ED275C75E7F09AF4B1C22B81.png)
![at leading q pT(j) (leading q best match).png](/images/q/232A7628536062AC87EB35F2838F9ABE.png)
![at subleading q eta(j) (leading q best match).png](/images/q/92AE025C4F43C355CD1BBDC7B78D9CD6.png)
![at subleading q pT(j) (leading q best match).png](/images/q/10DC571389912BAEF22D1B115B892F92.png)
![eta(bjet).png](/images/q/FF8C219BE807865C355F70C2DBB8C43C.png)
![eta(bquark).png](/images/q/A6C925C27DF700A1F2663D32E5D5B4F0.png)
![eta(cjet).png](/images/q/0A54B9AE5BFB9A148CE1EB5259C1D6F0.png)
![eta(cquark).png](/images/q/08E93B03CAB2A9F190577F7C39CEC6BB.png)
![eta(leading q) (leading q best match).png](/images/q/D2A33B231D0CFEA30C496027299BA6B2.png)
![eta(subleading q) (leading q best match).png](/images/q/5C3945B30181727B867E3C3DD203D1ED.png)
![pT(bjet).png](/images/q/8DD3F36B4CCAA30D2278ED35916CE51A.png)
![pT(bquark).png](/images/q/6EE310098EFF2189C5CCF7805F71E9C3.png)
![pT(cjet).png](/images/q/5D6F1D678BF378BEE3009E30E1194E0E.png)
![pT(cquark).png](/images/q/742E1E70DAFCB2AA485FF6F5CBA57702.png)
![pT(leading q) (leading q best match).png](/images/q/0B02C74DF302F83048C8EC8E600ED5A6.png)
![pT(subleading q) (leading q best match).png](/images/q/3EFAE310ABDB42067CBDB0B083EE62FC.png)
![ratio pT(bquark,bjet).png](/images/q/233A67296CE0B082F74598564AB08062.png)
![ratio pT(cquark,cjet).png](/images/q/0E2EC18BA1911741C056AFA8A3F8A3E8.png)
![ratio pT(leading q,j) (leading q best match).png](/images/q/475402682A588EC38CCF77717DDA2C5D.png)
![ratio pT(subleading q,j) (leading q best match).png](/images/q/F9BF66EEA8204715FC77A68B26471329.png)

)

)
