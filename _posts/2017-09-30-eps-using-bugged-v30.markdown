---
layout: post
title: EPS using bugged v30
tags: 
    - bug
    - VHbb
---

# Context

Andy B. and Changqiao have been using the bugged version of v30 0-lepton inputs for EPS, which has non-up-to-date diboson modelling systematics

# Candidate commits for updated shapes

https://gitlab.cern.ch/CxAODFramework/CorrsAndSysts/commits/master/Root/CorrsAndSysts.cxx

## VH and VV PSUE systematics (Nicolas)
https://gitlab.cern.ch/CxAODFramework/CorrsAndSysts/commit/b64aea4a3c8fcd0516e867c841216b0299131f6e

## Bug fix for jets multiplicities (Nicolas)
https://gitlab.cern.ch/CxAODFramework/CorrsAndSysts/commit/d9d3943229addca837bc4cd0b33b3b3c17fc09e6

## (Valerio)
https://gitlab.cern.ch/CxAODFramework/CorrsAndSysts/commit/cdeaa63d63ca4bc5a07cd3367ace9219b85e4e8c
https://gitlab.cern.ch/CxAODFramework/CorrsAndSysts/blame/b64aea4a3c8fcd0516e867c841216b0299131f6e/Root/CorrsAndSysts.cxx

# Shape comparison of the updated syst

![IMAGE](quiver-image-url/2FD0DC29E7FC6A050627EAAA6CD3321D.jpg =1301x780)

{% highlight sh %}
    TF1 *m_f_SysVVMbbME_WZlvqq = new TF1("mBB__WZlvqq_PS_Sherpa_fit","[0]+[7]*(x/1e3)*(x/1e3)+[1]*TMath::Exp(-(x/1e3)/[2])+[3]*((TMath::Gaus(((x/1e3)-[4])/[6])+1)/(TMath::Gaus(((x/1e3)-[5])/[6])+1))-1",25e3,500e3);
    m_f_SysVVMbbME_WZlvqq->SetParameter(0,-31.3129);
    m_f_SysVVMbbME_WZlvqq->SetParameter(1,32.2119);
    m_f_SysVVMbbME_WZlvqq->SetParameter(2,15016.9);
    m_f_SysVVMbbME_WZlvqq->SetParameter(3,0.210291);
    m_f_SysVVMbbME_WZlvqq->SetParameter(4,94.0918);
    m_f_SysVVMbbME_WZlvqq->SetParameter(5,26.2236);
    m_f_SysVVMbbME_WZlvqq->SetParameter(6,15);
    m_f_SysVVMbbME_WZlvqq->SetParameter(7,3.91378e-06);
    
    m_f_SysVVMbbME_WZlvqq->GetHistogram()->SetTitle("SysVVMbbME_WZlvqq 2j");
    
    m_f_SysVVMbbME_WZlvqq->SetLineColor(kBlue);
    m_f_SysVVMbbME_WZlvqq->Draw()
    
    TF1 *m_f_SysVVMbbME_WZlvqq_new = new TF1("mBB__WZlvqq_PS_Sherpa_fit_new","[0]+[1]*tanh( (x/1e3-[2])/[3] )",25e3,500e3);
    m_f_SysVVMbbME_WZlvqq_new->SetParameter(0,0.28196    );
    m_f_SysVVMbbME_WZlvqq_new->SetParameter(1, 4.30023e-01);
    m_f_SysVVMbbME_WZlvqq_new->SetParameter(2,1.01083e+02);
    m_f_SysVVMbbME_WZlvqq_new->SetParameter(3,1.87708e+01);

    m_f_SysVVMbbME_WZlvqq_new->SetLineColor(kRed);
    m_f_SysVVMbbME_WZlvqq_new->Draw("same")
    
    TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
    leg->AddEntry(m_f_SysVVMbbME_WZlvqq, "Initial VVMbbME_WZlvqq", "l")
    leg->AddEntry(m_f_SysVVMbbME_WZlvqq_new, "Updated VVMbbME_WZlvqq", "l")

    leg->Draw("same")
    c1->SetGridx()
    c1->SetGridy()
{% endhighlight %}

![IMAGE](quiver-image-url/047952A553BC6A1A6E03AE8D5ABACA7E.jpg =1290x789)

    TF1 *m_f_SysVVMbbME_ZZvvqq= new TF1("mBB__ZZqqvv_PS_Sherpa_fit","[0]+[7]*(x/1e3)*(x/1e3)+[1]*TMath::Exp(-(x/1e3)/[2])+[3]*((TMath::Gaus(((x/1e3)-[4])/[6])+1)/(TMath::Gaus(((x/1e3)-[5])/[6])+1))-1",25e3,500e3);
    m_f_SysVVMbbME_ZZvvqq->SetParameter(0,-9.82225);
    m_f_SysVVMbbME_ZZvvqq->SetParameter(1,10.7876);
    m_f_SysVVMbbME_ZZvvqq->SetParameter(2,4292.31);
    m_f_SysVVMbbME_ZZvvqq->SetParameter(3,0.180446);
    m_f_SysVVMbbME_ZZvvqq->SetParameter(4,96.0217);
    m_f_SysVVMbbME_ZZvvqq->SetParameter(5,64.1412);
    m_f_SysVVMbbME_ZZvvqq->SetParameter(6,12.0295);
    m_f_SysVVMbbME_ZZvvqq->SetParameter(7,5.22119e-06);

    m_f_SysVVMbbME_ZZvvqq->GetHistogram()->SetTitle("SysVVMbbME_ZZvvqq 2j");

    m_f_SysVVMbbME_ZZvvqq->SetLineColor(kBlue);
    m_f_SysVVMbbME_ZZvvqq->Draw()
   
   
    TF1 *m_f_SysVVMbbME_ZZvvqq_new= new TF1("mBB__ZZqqvv_PS_Sherpa_fit_new","[0]+[1]*tanh( (x/1e3-[2])/[3] )",25e3,500e3);
    m_f_SysVVMbbME_ZZvvqq_new->SetParameter(0,0.24918    );
    m_f_SysVVMbbME_ZZvvqq_new->SetParameter(1,4.07409e-01);
    m_f_SysVVMbbME_ZZvvqq_new->SetParameter(2,9.51575e+01);
    m_f_SysVVMbbME_ZZvvqq_new->SetParameter(3,1.46196e+01);

    m_f_SysVVMbbME_ZZvvqq_new->SetLineColor(kRed);
    m_f_SysVVMbbME_ZZvvqq_new->Draw("same")
    
    TLegend *leg = new TLegend(0.7,0.7,0.9,0.9)
    leg->AddEntry(m_f_SysVVMbbME_ZZvvqq, "Initial VVMbbME_ZZvvqq", "l")
    leg->AddEntry(m_f_SysVVMbbME_ZZvvqq_new, "Updated VVMbbME_ZZvvqq", "l")

    leg->Draw("same")
    c1->SetGridx()
    c1->SetGridy()
