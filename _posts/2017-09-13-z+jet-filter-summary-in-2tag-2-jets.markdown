---
layout: post
title: Z+jet filter summary in 2tag 2 jets
tags: 
    - filter
    - MC
    - VHbb
---

* This note is a quick summary of [Z+jet filter strategy](quiver-note-url/03421471-9CEB-457E-A54D-5ED51183CA27)

--> Purpose : Look how behaves the stat error with pTV filter if we had the same AOD stat as in CxAOD 28 :

* 2tag 2 jets

* * CxAOD 26 pTV Filter

| Sample | Filter              | nAOD      | Entries after selection | Yield after selection | Error after selection |
| ------ | ------------------- | --------- | ----------------------- | --------------------- | --------------------- |
| 363417 | BFilter pTV-70-140  | 2 471 000 |                     130 |                   117 |                 18.34 |
| 363420 | BFilter pTV-140-280 | 1 983 000 |                   7 802 |                 1 218 |                 26.87 |
| 363423 | BFilter pTV-280-500 | 984 000   |                    5242 |                   124 |                  3.42 |

* * CxAOD 28 MAXHTPtV Filter

| Sample | Filter                   | nAOD       | Entries after selection | Yield after selection | Error after selection |
| ------ | ------------------------ | ---------- | ----------------------- | --------------------- | --------------------- |
| 364147 | BFilter MAXHTPtV-70-140  | 19 728 500 |                     272 |                    27 |                 10.77 |
| 364150 | BFilter MAXHTPtV-140-280 | 19 745 300 |                  19 691 |                 1 145 |                 16.58 |
| 364153 | BFilter MAXHTPtV-280-500 | 8 887 350  |                  11 577 |                   291 |                  5.37 |

err26' = err26 \* sqrt(nEntries26) / sqrt(nEntries26*nAOD28/nAOD26)

With the AOD stat of CxAODs 28 :

| Slice               | Error after selection with MAXHTPtV filter | Error after selection with PtV filter |
| ------------------- | ------------------------------------------ | ------------------------------------- |
| BFilter pTV-70-140  |                                      10.77 |                                 6.49  |
| BFilter pTV-140-280 |                                      16.58 |                                 8.57  |
| BFilter pTV-280-500 |                                       5.37 |                                  1.13 |
| Combined            |                                      20.48 |                                 10.81 |

* If we had to optimize the slicing in pTV, the TruthMET distribution at CxAOD level (selection = 2jets, MET reco > 140 GeV) shows that cutting on MET truth > 90 GeV allows to keep most events. Since we apply MET reco > 150 GeV in the analysis, a slice starting with low edge MET truth > 100 GeV should still be efficient.

![IMAGE](quiver-image-url/1158856E9CE65BC02D31F86B31F7EAD0.jpg =1241x783)


