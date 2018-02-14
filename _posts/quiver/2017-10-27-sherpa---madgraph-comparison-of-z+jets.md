---
title: Sherpa - Madgraph comparison of Z+jets
date: '2017-10-27'
tags:
- Madgraph
- Sherpa
---
# Purpose

- discrepancy
)
# Conclusions

* pas de difference sur les XSections (Sh/MG ~ 0.989) --> pas de rescaling dans les nombres ci-dessous
* Difference sur le modelling de nJets (plots degeneres avec la coupure 0-lepton, mais on peut supposer que nJets est la plus grosse source de mismodelling)
  * en 2 jets : Sh/MG ~ 1.039 (lights) -- 1.047 (bl) -- 0.74 (bb)
  * en 3 jets : Sh/MG ~ 1.114 (lights) -- 1.261 (bl) -- 0.98 (bb)
    * ces variations vont dans le sens contraire au ratio des yields apres toutes les coupures (Sh/MG < 1 a la fin)
    * dependance sur la composition en saveur des jets, notamment bb 2 jets ...
* Difference de modelling importante de pT(Z) qui colle bien avec la distribution de MET egalement
  * en 2 jets : turn-on vers 40 GeV --> MG >> Sh pour PT(Z) > 150 GeV
  * en 3 jets : turn-on vers 60 GeV --> MG >> Sh pour PT(Z) > 150 GeV
  * renverse les valeurs de ratio Sh/MG
    * en 2 jets : Sh/MG ~ 0.81 (toutes saveurs de jets) (0.76 sur les evenements bb)
    * en 3 jets : Sh/MG ~ 0.86 (toutes saveurs de jets) (0.85 sur les evenements bb)
* Dans la note modelling, la systematique de shape ZPTV est estimee par comparaison data/MC en 2-leptons
  * trend similaire a ce que je vois dans le ratio Sh/MG des distribution de pTZ et MET
    * en 2-lepton, la shape commence à 0 GeV --> turn-on vers 50 GeV
    * en 0-lepton, la SR commence à 150 GeV --> impact sur la normalisation qui devrait se faire correctement d'apres Nicolas
    * sauf que dans un fit 0-lepton seul (et fit combine egalement), il n'y a pas de pull du NP de la shape ZPTV (tres peu dans le fit 0-1-2)
    * en fait c'est surement le NP de normalisation flottante qui absorbe tout pour les deux
)
# Cutflows

Ordre des bins/coupures :
* 0 : all events (fill 0. )
* 1 : 0 leptons (coupures plus bas) + au moins 2 signal-jets (pT > 20 GeV et abseta < 2.5)
* 2 : 2 ou 3 jets
* 3 : MET >= 150 GeV
* 4 : dPhi MET/MPT < pi/2
* 5 : min dPhi MET/jets < 20 degrees
* 6 : SumPt > 120 (150) GeV en 2 (3) jets
* 7 : pTB1 > 45 GeV
* 8 : dPhi BB < 140 degrees
* 9 : dPhi MET/BB > 120
)
### Precisions

* Sherpa est en rouge
* Madgraph est en bleu
* les ratios représentent Sherpa/Madgraph
* plots avec un rescaling a la meme somme des poids initiale
)
# Cutflows inclusifs sur la saveur des jets (cutflows bb plus bas)
)
## 2 jets

![IMAGE](/images/q/F063AB3764BD42BDB8887061A8F37D28.jpg)
## 3 jets

![IMAGE](/images/q/56E605602024577E431A0219A6CC7985.jpg)
# distributions presque sans coupures

* avant coupure)
## MET 2 jets avant coupure

![IMAGE](/images/q/22DA11DE45A4B9326E4E39A733EE94E5.jpg)
## MET 3 jets avant coupure

![IMAGE](/images/q/EAB22033578CDED04296949A0F57AB9A.jpg)
## pTV 2 jets avant coupure

![IMAGE](/images/q/07B5628A03ACB2708BFE2F7B5C79AEDF.jpg)
## pTV 3 jets avant coupure

![IMAGE](/images/q/983E681085C4B0A4FE06E2A085DF37D1.jpg)
# Comparaison à la modelling note d'EPS

* page 37 de la modelling note
  * systematique evaluee sur les data 2-lepton : il y a une trend le long de pTV de 0 a 600 GeV
  * est-ce que ca induit un changement de normalisation dans 0-lepton au dessus de 150 GeV (le turn-on dans 2-leptons est vers 60 GeV)
    * normalement oui d'apres Nicolas
)
![IMAGE](/images/q/0ED3FAF94C55EB9406C80C5EE708920C.jpg)
* page 177 de la supporting note
  * pas de pull du NP ZPTV dans le fit 0-lepton seul
  * d'apres Nicolas, completement degenere avec le NP de normalisation flottante pour Zbb, donc il va augmenter beaucoup de SF et peu tirer sur ZPTV
)
![IMAGE](/images/q/01B297101530A30FA39D62199A7DF176.jpg)
* dans le fit combine, il n'y a pas de gros pull non plus de ce NP
![IMAGE](/images/q/7BDA22AC2A90495AB1A5A8230250B910.jpg)
# Cutflows bb

* attention : le bin all est rempli apres la coupure nsignaljets > 1, a l'inverse des cutflows inclusifs en saveur
)
### 2 jets

![IMAGE](/images/q/F1BFB00B7F80B3B44480D7D92D6C2B3B.jpg)
### 3 jets

![IMAGE](/images/q/99E431A2EBCC8628E5A65222314698E0.jpg)
## Coupures sur les leptons et les jets dans RIVET

)
{% highlight sh %}
      // Definition of all the cuts applied
      // to electrons
      const double e_pt_cut_loose = 7*GeV;
      const double e_eta_cut_loose = 2.47;
      const double e_iso_track_cut_loose = 0.1;
      const double e_pt_cut_medium = 25*GeV;
      const double e_eta_cut_medium = 2.47;
      const double e_iso_track_cut_tight = 0.04;
      const double e_iso_calo_cut_tight = 0.04;
      // to muons
      const double m_pt_cut_loose = 7*GeV;
      const double m_eta_cut_loose = 2.7;
      const double m_iso_track_cut_loose = 0.1;
      const double m_pt_cut_medium = 25*GeV;
      const double m_eta_cut_medium = 2.5;
      const double m_iso_track_cut_tight = 0.04;
      const double m_iso_calo_cut_tight = 0.04;
            
            
            
      // to central jets
      const double centraljet_pt_cut = 20*GeV;
      const double centraljet_eta_cut = 2.5;
      // to forward jets
      const double additional_jet_pt_cut = 30*GeV;
      const double additional_jet_eta_cut = 4.5;
      
{% endhighlight %}

## Samples
)
{% highlight sh %}
361515   7518.4             1.2283         1.0            MadZnunu                 mc15_13TeV.361515.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np0
361516   1200.1             1.2283         1.0            MadZnunu                 mc15_13TeV.361516.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np1
361517   387.16             1.2283         1.0            MadZnunu                 mc15_13TeV.361517.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np2
361518   110.08             1.2283         1.0            MadZnunu                 mc15_13TeV.361518.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np3
361519   43.389             1.2283         1.0            MadZnunu                 mc15_13TeV.361519.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np4
{% endhighlight %}

{% highlight sh %}
364142      1.0700E+04       0.9728       8.2160E-01      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_CVetoBVeto
364143      1.0702E+04       0.9728       1.1123E-01      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_CFilterBVeto
364144      1.0709E+04       0.9728       6.6175E-02      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_BFilter
364145      6.0323E+02       0.9728       6.8924E-01      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_CVetoBVeto
364146      6.0815E+02       0.9728       1.8243E-01      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_CFilterBVeto
364147      6.0332E+02       0.9728       0.1283          Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_BFilter
364148      2.2228E+02       0.9728       6.0735E-01      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_CVetoBVeto
364149      2.2188E+02       0.9728       2.2527E-01      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_CFilterBVeto
364150      2.2247E+02       0.9728       1.5185E-01      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_BFilter
364151      4.7375E+01       0.9728       5.5887E-01      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_CVetoBVeto
364152      4.7397E+01       0.9728       2.6201E-01      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_CFilterBVeto
364153      4.7476E+01       0.9728       1.7514E-01      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_BFilter
364154      9.9099           0.9728       1.0000E+00      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV500_1000
364155      8.1809E-01       0.9728       1.0000E+00      Z            Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV1000_E_CMS
{% endhighlight %}

# Investigation on the 10% efficiency on the 0-lepton cut
)
## B Filter cutflow (364150)
![IMAGE](/images/q/835E1EED944B91BB5ADC8B513F08F0FE.jpg)
## C Filter B Veto cutflow (364149)
![IMAGE](/images/q/97FA84EF0FDB46E0DC08C0CDB9E9C46C.jpg)
## C Veto B Veto cutflow (364148)
![IMAGE](/images/q/325B67F2065A2CB584DCC9E76B31B9C3.jpg)
## Comparison macro
)
{% highlight sh %}
root -l Rivet_364142.root Rivet_364143.root Rivet_364144.root Rivet_364145.root Rivet_364146.root Rivet_364147.root Rivet_364148.root Rivet_364149.root Rivet_364150.root Rivet_364151.root Rivet_364152.root Rivet_364153.root Rivet_364154.root Rivet_364155.root Rivet_361515.root Rivet_361516.root Rivet_361517.root Rivet_361518.root Rivet_361519.root

gStyle->SetOptStat(0);

// TString histName = "Lep0_bb_Cuts3j";
// TString histName = "Lep0_Cuts3j";
TString histName = "SAMPLEl_0lepton_0ptag2jet_vpt150_MET_cut0";


h_Sherpa42 = (TH1F*)_file0->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_Sherpa43 = (TH1F*)_file1->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_Sherpa44 = (TH1F*)_file2->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_Sherpa45 = (TH1F*)_file3->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_Sherpa46 = (TH1F*)_file4->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_Sherpa47 = (TH1F*)_file5->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_Sherpa48 = (TH1F*)_file6->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_Sherpa49 = (TH1F*)_file7->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_Sherpa50 = (TH1F*)_file8->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_Sherpa51 = (TH1F*)_file9->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));

h_Sherpa52 = (TH1F*)_file10->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));

h_Sherpa53 = (TH1F*)_file11->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));

h_Sherpa54 = (TH1F*)_file12->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));

h_Sherpa55 = (TH1F*)_file13->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));

h_MG_NP0 = (TH1F*)_file14->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_MG_NP1 = (TH1F*)_file15->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_MG_NP2 = (TH1F*)_file16->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_MG_NP3 = (TH1F*)_file17->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));
h_MG_NP4 = (TH1F*)_file18->Get(TString::Format("MC_VH2BB_2015_Official/%s", histName.Data()));

h_Sherpa42->Scale(1.0700E+04*0.9728*8.2160E-01/h_Sherpa42->Integral());
h_Sherpa43->Scale(1.0702E+04*0.9728*1.1123E-01/h_Sherpa42->Integral());
h_Sherpa44->Scale(1.0709E+04*0.9728*6.6175E-02/h_Sherpa42->Integral());
h_Sherpa45->Scale(6.0323E+02*0.9728*6.8924E-01/h_Sherpa45->Integral());
h_Sherpa46->Scale(6.0815E+02*0.9728*1.8243E-01/h_Sherpa46->Integral());
h_Sherpa47->Scale(6.0332E+02*0.9728*0.1283/h_Sherpa47->Integral());
h_Sherpa48->Scale(2.2228E+02*0.9728*6.0735E-01/h_Sherpa48->Integral());
h_Sherpa49->Scale(2.2188E+02*0.9728*2.2527E-01/h_Sherpa49->Integral());
h_Sherpa50->Scale(2.2247E+02*0.9728*1.5185E-01/h_Sherpa50->Integral());
h_Sherpa51->Scale(4.7375E+01*0.9728*5.5887E-01/h_Sherpa51->Integral());
h_Sherpa52->Scale(4.7397E+01*0.9728*2.6201E-01/h_Sherpa52->Integral());
h_Sherpa53->Scale(4.7476E+01*0.9728*1.7514E-01/h_Sherpa53->Integral());
h_Sherpa54->Scale(9.9099*0.9728*1.0000E+00/h_Sherpa54->Integral());
h_Sherpa55->Scale(8.1809E-01*0.9728*1.0000E+00/h_Sherpa55->Integral());

// h_Sherpa42->Scale(1.0700E+04*0.9728*8.2160E-01/h_Sherpa42->GetBinContent(1));
// h_Sherpa43->Scale(1.0702E+04*0.9728*1.1123E-01/h_Sherpa42->GetBinContent(1));
// h_Sherpa44->Scale(1.0709E+04*0.9728*6.6175E-02/h_Sherpa42->GetBinContent(1));
// h_Sherpa45->Scale(6.0323E+02*0.9728*6.8924E-01/h_Sherpa45->GetBinContent(1));
// h_Sherpa46->Scale(6.0815E+02*0.9728*1.8243E-01/h_Sherpa46->GetBinContent(1));
// h_Sherpa47->Scale(6.0332E+02*0.9728*0.1283/h_Sherpa47->GetBinContent(1));
// h_Sherpa48->Scale(2.2228E+02*0.9728*6.0735E-01/h_Sherpa48->GetBinContent(1));
// h_Sherpa49->Scale(2.2188E+02*0.9728*2.2527E-01/h_Sherpa49->GetBinContent(1));
// h_Sherpa50->Scale(2.2247E+02*0.9728*1.5185E-01/h_Sherpa50->GetBinContent(1));
// h_Sherpa51->Scale(4.7375E+01*0.9728*5.5887E-01/h_Sherpa51->GetBinContent(1));
// h_Sherpa52->Scale(4.7397E+01*0.9728*2.6201E-01/h_Sherpa52->GetBinContent(1));
// h_Sherpa53->Scale(4.7476E+01*0.9728*1.7514E-01/h_Sherpa53->GetBinContent(1));
// h_Sherpa54->Scale(9.9099*0.9728*1.0000E+00/h_Sherpa54->GetBinContent(1));
// h_Sherpa55->Scale(8.1809E-01*0.9728*1.0000E+00/h_Sherpa55->GetBinContent(1));

TH1F* h_Sh = new TH1F;
*h_Sh = *h_Sherpa42;
h_Sh->Add(h_Sherpa43);
h_Sh->Add(h_Sherpa44);
h_Sh->Add(h_Sherpa45);
h_Sh->Add(h_Sherpa46);
h_Sh->Add(h_Sherpa47);
h_Sh->Add(h_Sherpa48);
h_Sh->Add(h_Sherpa49);
h_Sh->Add(h_Sherpa50);
h_Sh->Add(h_Sherpa51);
h_Sh->Add(h_Sherpa52);
h_Sh->Add(h_Sherpa53);
h_Sh->Add(h_Sherpa54);
h_Sh->Add(h_Sherpa55);

h_Sh->Scale(1./h_Sh->GetBinContent(1));

// h_MG_NP0->Scale(8./h_MG_NP0->GetBinContent(1));
// h_MG_NP1->Scale(1.2/h_MG_NP1->GetBinContent(1));
// h_MG_NP2->Scale(0.38718/h_MG_NP2->GetBinContent(1));
// h_MG_NP3->Scale(0.1/h_MG_NP3->GetBinContent(1));
// h_MG_NP4->Scale(0.043472/h_MG_NP4->GetBinContent(1));

h_MG_NP0->Scale(8./h_MG_NP0->Integral());
h_MG_NP1->Scale(1.2/h_MG_NP1->Integral());
h_MG_NP2->Scale(0.38718/h_MG_NP2->Integral());
h_MG_NP3->Scale(0.1/h_MG_NP3->Integral());
h_MG_NP4->Scale(0.043472/h_MG_NP4->Integral());

TH1F* h_MG = new TH1F;
*h_MG = *h_MG_NP0;
h_MG->Add(h_MG_NP1);
h_MG->Add(h_MG_NP2);
h_MG->Add(h_MG_NP3);
h_MG->Add(h_MG_NP4);

h_MG->Scale(1./h_MG->GetBinContent(1));

auto c1 = new TCanvas("c1", "A ratio Sherpa/Madgraph Zjet");
auto rp = new TRatioPlot(h_Sh, h_MG);
c1->SetTicks(0, 1);
rp->Draw();
c1->Update();
{% endhighlight %}

# EVTGen Datasets for Rivet
)
{% highlight sh %}
# DAOD list from https://gitlab.cern.ch/CxAODFramework/FrameworkSub/blob/master/In/CxAOD28/list_sample_grid.mc15c_13TeV_25ns_bg_nominal_HIGG5D1.txt

#mc15_13TeV.364142.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_CVetoBVeto.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
#mc15_13TeV.364143.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_CFilterBVeto.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
mc15_13TeV.364144.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_BFilter.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
#mc15_13TeV.364145.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_CVetoBVeto.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
#mc15_13TeV.364146.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_CFilterBVeto.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
mc15_13TeV.364147.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_BFilter.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
#mc15_13TeV.364148.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_CVetoBVeto.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
#mc15_13TeV.364149.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_CFilterBVeto.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
mc15_13TeV.364150.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_BFilter.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
#mc15_13TeV.364151.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_CVetoBVeto.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
#mc15_13TeV.364152.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_CFilterBVeto.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
mc15_13TeV.364153.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_BFilter.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
mc15_13TeV.364154.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV500_1000.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
mc15_13TeV.364155.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV1000_E_CMS.merge.DAOD_HIGG5D1.e5308_s2726_r7772_r7676_p2949
{% endhighlight %}

{% highlight sh %}
# EVGen :

# BFilter
mc15_13TeV.364144.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_BFilter.evgen.EVNT.e5308
mc15_13TeV.364147.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_BFilter.evgen.EVNT.e5308
mc15_13TeV.364150.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_BFilter.evgen.EVNT.e5308
mc15_13TeV.364153.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_BFilter.evgen.EVNT.e5308

# CFilterBVeto
mc15_13TeV.364143.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_CFilterBVeto.evgen.EVNT.e5308
mc15_13TeV.364146.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_CFilterBVeto.evgen.EVNT.e5308
mc15_13TeV.364149.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_CFilterBVeto.evgen.EVNT.e5308
mc15_13TeV.364152.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_CFilterBVeto.evgen.EVNT.e5308

# CVetoBVeto
mc15_13TeV.364142.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV0_70_CVetoBVeto.evgen.EVNT.e5308
mc15_13TeV.364145.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV70_140_CVetoBVeto.evgen.EVNT.e5308
mc15_13TeV.364148.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_CVetoBVeto.evgen.EVNT.e5308
mc15_13TeV.364151.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV280_500_CVetoBVeto.evgen.EVNT.e5308

# Unfiltered slices
mc15_13TeV.364154.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV500_1000.evgen.EVNT.e5308
mc15_13TeV.364155.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV1000_E_CMS.evgen.EVNT.e5308
{% endhighlight %}

