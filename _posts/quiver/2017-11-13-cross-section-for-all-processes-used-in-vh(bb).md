---
title: Cross-section for all processes used in VH(bb)
date: '2017-11-13'
tags: []
---
{% highlight sh %}
[delporte@cca002 CxAODFramework_tag28_DirectTagging]$ less FrameworkSub/data/XSections_13TeV.txt | grep Sherpa_221_NNPDF30NNLO_ | grep -v ttbar | grep 'Znunu\|Zee\|Zmumu\|Ztautau' | awk 'BEGIN{s=0;} {
print $0; s+=$2*$3*$4} END{print s}'
364100  1983.0      0.9751   8.2210E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV0_70_CVetoBVeto         
364101  1978.4      0.9751   1.1308E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV0_70_CFilterBVeto       
364102  1982.2      0.9751   6.4161E-02   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV0_70_BFilter            
364103  108.92      0.9751   6.8873E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV70_140_CVetoBVeto       
364104  109.42      0.9751   1.8596E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV70_140_CFilterBVeto     
364105  108.91      0.9751   1.1375E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV70_140_BFilter          
364106  39.878      0.9751   6.0899E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV140_280_CVetoBVeto      
364107  39.795      0.9751   2.3308E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV140_280_CFilterBVeto    
364108  39.908      0.9751   1.4618E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV140_280_BFilter         
364109  8.5375      0.9751   5.5906E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV280_500_CVetoBVeto      
364110  8.5403      0.9751   2.6528E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV280_500_CFilterBVeto    
364111  8.4932      0.9751   1.7559E-01   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV280_500_BFilter         
364112  1.7881      0.9751   1.0000E+00   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV500_1000                
364113  0.14769     0.9751   1.0000E+00   Z                 Sherpa_221_NNPDF30NNLO_Zmumu_MAXHTPTV1000_E_CMS              
364114  1981.8      0.9751   8.2106E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV0_70_CVetoBVeto           
364115  1980.8      0.9751   1.1295E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV0_70_CFilterBVeto         
364116  1981.7      0.9751   6.3809E-02   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV0_70_BFilter              
364117  110.5       0.9751   6.9043E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV70_140_CVetoBVeto         
364118  110.63      0.9751   1.8382E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV70_140_CFilterBVeto       
364119  110.31      0.9751   1.1443E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV70_140_BFilter            
364120  40.731      0.9751   6.1452E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV140_280_CVetoBVeto        
364121  40.67       0.9751   2.3044E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV140_280_CFilterBVeto      
364122  40.694      0.9751   1.4927E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV140_280_BFilter           
364123  8.6743      0.9751   5.6134E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV280_500_CVetoBVeto        
364124  8.6711      0.9751   2.6294E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV280_500_CFilterBVeto      
364125  8.6766      0.9751   1.7223E-01   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV280_500_BFilter           
364126  1.8081      0.9751   1.0000E+00   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV500_1000                  
364127  0.14857     0.9751   1.0000E+00   Z                 Sherpa_221_NNPDF30NNLO_Zee_MAXHTPTV1000_E_CMS                
364128  1981.6      0.9751   8.2142E-01   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV0_70_CVetoBVeto       
364129  1978.8      0.9751   1.1314E-01   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV0_70_CFilterBVeto     
364130  1981.8      0.9751   6.4453E-02   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV0_70_BFilter          
364131  110.37      0.9751   6.8883E-01   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV70_140_CVetoBVeto     
364132  110.51      0.9751   1.8290E-01   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV70_140_CFilterBVeto   
364133  1.1087E+02  0.9751   0.1283       Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV70_140_BFilter
364134  40.781      0.9751   6.0821E-01   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV140_280_CVetoBVeto    
364135  40.74       0.9751   2.2897E-01   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV140_280_CFilterBVeto  
364136  40.761      0.9751   1.3442E-01   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV140_280_BFilter       
364137  8.5502      0.9751   5.6036E-01   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV280_500_CVetoBVeto    
364138  8.6707      0.9751   2.6245E-01   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV280_500_CFilterBVeto  
364139  8.6804      0.9751   1.7313E-01   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV280_500_BFilter       
364140  1.8096      0.9751   1.0000E+00   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV500_1000              
364141  0.14834     0.9751   1.0000E+00   Z                 Sherpa_221_NNPDF30NNLO_Ztautau_MAXHTPTV1000_E_CMS            
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
17512.9
[delporte@cca002 CxAODFramework_tag28_DirectTagging]$ less FrameworkSub/data/XSections_13TeV.txt | grep Sherpa_221_NNPDF30NNLO_ | grep -v ttbar | grep 'Wenu\|Wmunu\|Wtaunu' | awk 'BEGIN{s=0;} {print $0; s+=$2*$3*$4} END{print s}'
364156  19143.0     0.9702   8.2380E-01   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV0_70_CVetoBVeto         
364157  19121.0     0.9702   1.3040E-01   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV0_70_CFilterBVeto       
364158  19135.0     0.9702   4.4118E-02   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV0_70_BFilter            
364159  944.85      0.9702   6.7463E-01   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV70_140_CVetoBVeto       
364160  937.78      0.9702   2.3456E-01   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV70_140_CFilterBVeto     
364161  944.63      0.9702   7.5648E-02   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV70_140_BFilter          
364162  339.54      0.9702   6.2601E-01   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV140_280_CVetoBVeto      
364163  340.06      0.9702   2.8947E-01   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV140_280_CFilterBVeto    
364164  339.54      0.9702   1.0872E-01   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV140_280_BFilter         
364165  72.067      0.9702   5.4647E-01   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV280_500_CVetoBVeto      
364166  72.198      0.9702   3.1743E-01   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV280_500_CFilterBVeto    
364167  72.045      0.9702   1.3337E-01   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV280_500_BFilter         
364168  15.01       0.9702   1.0000E+00   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV500_1000                
364169  1.2344      0.9702   1.0000E+00   W                 Sherpa_221_NNPDF30NNLO_Wmunu_MAXHTPTV1000_E_CMS              
364170  19127.0     0.9702   8.2447E-01   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV0_70_CVetoBVeto          
364171  19130.0     0.9702   1.3030E-01   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV0_70_CFilterBVeto        
364172  19135.0     0.9702   4.4141E-02   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV0_70_BFilter             
364173  942.58      0.9702   6.6872E-01   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV70_140_CVetoBVeto        
364174  945.67      0.9702   2.2787E-01   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV70_140_CFilterBVeto      
364175  945.15      0.9702   0.10341      W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV70_140_BFilter  #Filter eff from central page          
364176  339.81      0.9702   5.9691E-01   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV140_280_CVetoBVeto       
364177  339.87      0.9702   2.8965E-01   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV140_280_CFilterBVeto     
364178  339.48      0.9702   1.0898E-01   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV140_280_BFilter          
364179  72.084      0.9702   5.4441E-01   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV280_500_CVetoBVeto       
364180  72.128      0.9702   3.1675E-01   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV280_500_CFilterBVeto     
364181  72.113      0.9702   1.3391E-01   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV280_500_BFilter          
364182  15.224      0.9702   1.0000E+00   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV500_1000                 
364183  1.2334      0.9702   1.0000E+00   W                 Sherpa_221_NNPDF30NNLO_Wenu_MAXHTPTV1000_E_CMS               
364184  19152.0     0.9702   8.2495E-01   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV0_70_CVetoBVeto        
364185  19153.0     0.9702   1.2934E-01   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV0_70_CFilterBVeto      
364186  19163.0     0.9702   4.4594E-02   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV0_70_BFilter           
364187  947.65      0.9702   6.7382E-01   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV70_140_CVetoBVeto      
364188  946.73      0.9702   2.2222E-01   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV70_140_CFilterBVeto    
364189  943.3       0.9702   0.10391      W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV70_140_BFilter  #Filter Eff from central page       
364190  339.36      0.9702   5.9622E-01   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV140_280_CVetoBVeto     
364191  339.63      0.9702   2.9025E-01   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV140_280_CFilterBVeto   
364192  339.54      0.9702   1.1799E-01   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV140_280_BFilter        
364193  72.065      0.9702   5.4569E-01   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV280_500_CVetoBVeto     
364194  71.976      0.9702   3.1648E-01   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV280_500_CFilterBVeto   
364195  72.026      0.9702   1.3426E-01   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV280_500_BFilter        
364196  15.046      0.9702   1.0000E+00   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV500_1000               
364197  1.2339      0.9702   1.0000E+00   W                 Sherpa_221_NNPDF30NNLO_Wtaunu_MAXHTPTV1000_E_CMS             
59625.2
{% endhighlight %}

