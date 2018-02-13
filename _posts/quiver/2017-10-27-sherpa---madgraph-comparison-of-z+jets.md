---
title: Sherpa - Madgraph comparison of Z+jets
date: '2017-10-27'
tags:
- Madgraph
- Sherpa
---
# Purpose

- discrepancy

* the ratio of cross sections shows 15% difference (Sherpa > Madgraph)
)
{% highlight sh %}
(1.0700E+04*0.9728*8.2160E-01 + 1.0702E+04*0.9728*1.1123E-01 + 1.0709E+04*0.9728*6.6175E-02 + 6.0323E+02*0.9728*6.8924E-01 + 6.0815E+02*0.9728*1.8243E-01 + 6.0332E+02*0.9728*0.1283  + 2.2228E+02*0.9728*6.0735E-01 + 2.2188E+02*0.9728*2.2527E-01 + 2.2247E+02*0.9728*1.5185E-01 + 4.7375E+01*0.9728*5.5887E-01 + 4.7397E+01*0.9728*2.6201E-01 + 4.7476E+01*0.9728*1.7514E-01 + 9.9099*0.9728*1.0000E+00 + 8.1809E-01*0.9728*1.0000E+00 ) / ( 8. + 1.2 + 0.38718 + 0.1 + 0.043472 ) / 1.e3
{% endhighlight %}

# Cutflows

Ordre des bins/coupures :
* 0 : all events (fill 0. )
* 1 : 0 leptons
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

![IMAGE](/images/q/0E14073D9461F40C01070D7615DE22A0.jpg)
## 3 jets

![IMAGE](/images/q/CC386D71D045649B26CDFA54907BFF7E.jpg)
## Observations sur les cutflows

* bin 0 : difference initiale sur les sections efficaces (pas dans les plots) --> Sherpa NLO et Madgraph LO ?
* bin 1 : difference sur la multiplicite des leptons lie au modelling de pT eta des leptons ?
* bin 2 : Il y a plus d'evenements a passer 2 jets en Madgraph qu'en Sherpa, ce qui corrige un peu la difference due a la coupure 0-leptons. Par contre en 3 jets, la difference augmente.
* bin 3 : modelling different de la MET, avec un turn-on vers 40 (60) GeV en 2 (3) jets ... au dela de 150 GeV, Sherpa est systematiquement en dessous de Madgraph
)
## MET 2 jets avant coupure

![IMAGE](/images/q/B0AB7C3E5DEB2F98A6696F82CFD93B86.jpg)
## MET 3 jets avant coupure

![IMAGE](/images/q/77739C3A166D08F94523F26E8388DD0E.jpg)
# Cutflows bb

* variations opposées en 2 et 3 jets, mais la coupure sur la MET rétablit Sherpa/MG < 1. dans les deux cas
* (le ratio n'est pas 1 dans le bin all surement a cause d'une composition different des saveurs de jets par rapport aux evenements inclusifs (qui eux ont la meme normalisation))
)
### 2 jets

![IMAGE](/images/q/DBA4B290C64A0CCA98DC58074C93E3DA.jpg)
### 3 jets

![IMAGE](/images/q/574F3E8ADB0A76B986BB3924513A82FF.jpg)
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
| Sample | DSID   | Dataset                                                                         | Job                                             | XSection    | genFilterEff |
| ------ | ----   | ------------------------------------------------------------------------------- | ------------------------------------------------| ----------- | ------------ |
| Sherpa | 364150 | mc15_13TeV.364150.Sherpa_221_NNPDF30NNLO_Znunu_MAXHTPTV140_280_BFilter.evgen.EVNT.e5308 | https://bigpanda.cern.ch/task/12723363/ | 0.22237 nb  | 0.15813      |
| MG_NP0 | 361515 | mc15_13TeV.361515.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np0.evgen.EVNT.e3898 | https://bigpanda.cern.ch/task/12851571/         | 8 nb        | 1            |
| MG_NP1 | 361516 | mc15_13TeV.361516.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np1.evgen.EVNT.e3898 | https://bigpanda.cern.ch/task/12851603/         | 1.2 nb      | 1            |
| MG_NP2 | 361517 | mc15_13TeV.361517.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np2.evgen.EVNT.e3898 | https://bigpanda.cern.ch/task/12851620/         | 0.38718 nb  | 1            |
| MG_NP3 | 361518 | mc15_13TeV.361518.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np3.evgen.EVNT.e3898 | https://bigpanda.cern.ch/task/12851635/         | 0.1 nb      | 1            |
| MG_NP4 | 361519 | mc15_13TeV.361519.MadGraphPythia8EvtGen_A14NNPDF23LO_Znunu_Np4.evgen.EVNT.e3898 | https://bigpanda.cern.ch/task/12851650/         | 0.043472 nb | 1            |
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

