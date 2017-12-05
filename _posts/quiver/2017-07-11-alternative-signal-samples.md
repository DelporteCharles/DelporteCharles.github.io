---
title: Alternative signal samples
date: '2017-07-11'
tags:
- ggH
- ttH
- VBFH
- VHbb
- WH
- ZH
---
Which impact of alternative signal samples on the VH analysis ?

### Cross sections

| chan   | Xsec[pb]  | kFact | filtereff  | HistSvc_name   | physically_descriptive_name |
| -------| ----------| ----- |----------- | -------------- | -----------------------------
| 342282 | 30.196    | 1.00  | 1.00       | ggH125_inc     | PowhegPythia8EvtGen_CT10_AZNLOCTEQ6L1_ggH125_inc |
| 342283 | 3.828     | 1.00  | 1.00       | VBFH125_inc    | PowhegPythia8EvtGen_CT10_AZNLOCTEQ6L1_VBFH125_inc |
| 343365 | 0.048237   | 1.00  | 1.00       | ttH125_dilep   | aMcAtNloPythia8EvtGen_A14_NNPDF23_NNPDF30ME_ttH125_dilep |
| 343366 | 0.458070  | 1.00  | 4.3783E-01 | ttH125_semilep | aMcAtNloPythia8EvtGen_A14_NNPDF23_NNPDF30ME_ttH125_semilep |
| 343367 | 0.457850  | 1.00  | 4.5627E-01 | ttH125_allhad  | aMcAtNloPythia8EvtGen_A14_NNPDF23_NNPDF30ME_ttH125_allhad |
| 342284 | 1.102     | 1.00  | 1.00       | WH125_inc      | Pythia8EvtGen_A14NNPDF23LO_WH125_inc |
| 342285 | 0.600720  | 1.00  | 1.00       | ZH125_inc      | Pythia8EvtGen_A14NNPDF23LO_ZH125_inc |

### Comments on the Cross sections
- The cross-section * 0.58 for ZH is larger than that of the nominal sample because it is also inclusive in Z decay
- - https://svnweb.cern.ch/trac/atlasoff/browser/Generators/MC15JobOptions/trunk/share/DSID342xxx/MC15.342285.Pythia8EvtGen_A14NNPDF23LO_ZH125_inc.py
- - https://svnweb.cern.ch/trac/atlasoff/browser/Generators/MC15JobOptions/trunk/share/DSID345xxx/MC15.345056.PowhegPythia8EvtGen_NNPDF3_AZNLO_ZH125J_MINLO_vvbb_VpT.py

### Comments on the procedure
- ttH : merge samples
- WH / ZH : contamination comes from other decays than H->bb

### Yields
| Sample name    | Yield 2 jets | Yield 3 jets |
| -----------    | ------------ | ------------ |
| ggH125_inc     | 0            | 0            |
| VBFH125_inc    | 0            | 0            |
| ttH125_allhad  | 0            | 4.454061e-03 |
| ttH125_semilep | 3.253839e-02 | 3.376862e-01 |
| ttH125_dilep   | 4.616329e-02 | 2.367366e-01 |

| Sample name      | Yield 2 jets | Yield 3 jets |
| ---------------- | ------------ | ------------ |
| WH125 all flavours | 1.093704e+01 | 9.586789e+00 |
| WH125 bb         | 1.093704e+01 | 9.586789e+00 |
| Nominal sample   | 8.77331      | 10.0641      |
|                  |              |              |
| ZH125 all flavours | 2.353835e+01 | 2.154479e+01 |
| ZH125 bb         | 2.320183e+01 | 2.134803e+01 |
| Nominal sample   | ~ 38         | ~ 41.7       |

### Comments on the final numbers
Histogram ttH125_dilep has 68 entries in 2jets, and 441 entries in 3jets

