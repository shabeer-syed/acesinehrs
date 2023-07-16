---
layout: splash
title: "Parental mental health problems"
permalink: /MHPs/
header:
  overlay_color: "#5e616c"
  overlay_image: /images/parental mental health problems aces in ehrs.jpg
  cta_label: 
  cta_url: 
  caption:
excerpt: 'Definition <br /> <small><a>  </a></small> Any act of commission or omission by a parent or other caregiver that results in harm, potential for harm, or threat of harm to a child. Harm does not need to be intended <br /><br /> {::nomarkdown}<iframe style="display: inline-block;" src=" " frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'


---

## Definition

This domain contains indicators of mutually exclusive symptom clusters aligning with disorder classifications laid out by DSM-5/ICD-10 excluding substance misuse. Some codes for self-harm (e.g. overdose) may be represented across both parental mental health problems (MHPs) and parental substance misuse (SM) domains. MHPs indicators are ascertained using read codes, prescriptions, ICD-10 codes or by meeting the higher cut-off score on a validated self-report instrument or validated algorithms with prescriptions.[1](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-016-0274-7). Validated codes for parental MHPs and parental SM are also available via the [HDR UK CALIBER phenotype library](https://phenotypes.healthdatagateway.org/), with the mapping process described by [Kuan et al.](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(19)30012-3/fulltext)


--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9802273"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Parental mental health problems (3711)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/MHP_2023ACEsinEHRs.txt)

* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/ACEs/raw/main/ACEsinEHRs%20v1.2.pdf)

--------------------------------
## Implementation

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **mMHPs,** Depression | Include if continuous data meets the cut-off assigned to each code (see code list): e.g. DASS-21 (sub-scales): ≥14; EDPS: ≥13; HADS (sub-scale): ≥11; HDRS (sub-scale): ≥ 14; PHQ-9: ≥10; SDS (Zungs's): ≥50 | `mmhps_depres_anx <- merged_data %>% filter(Domain=="mMHPs" & scale=="1" & data1 > cut_off)` | 
 | **mMHPs,** Anxiety | Include if continuous data meets the cut-off assigned to each code (see code list): e.g DASS-21: ≥10; HADS (sub-scale): ≥11; HDRS (sub-scale): ≥18; SAS (Zungs's):  ≥45 score; GAD-7: ≥8 | `as above.` | 
 | **mMHPs,** Anxiety or depressive symptoms, antidepressants or anxiolytics and mental health service referral/interventions received | Codes referring to anxiety symptoms (e.g., worrying) or depression (e.g. “feeling low”) are only considered a case of depression or an anxiety disorder when the patient was also given antidepressants and/or anxiolytic medication within 3-months or initiated psychological treatment  within 2-years. Comparison estimates for mothers in CPRD-MBL with and without this algorithm are provided by [Abel et al.](https://www.thelancet.com/cms/10.1016/S2468-2667(19)30059-3/attachment/2df04b45-aaff-40de-8118-79df6a9ef5ca/mmc1.pdf) Rule: Include symptoms/medications as an anxiety or depression indicator, if a previous diagnostic code or tier 3 intervention code exists (within 2-years), or if there is a co-occurrence of a prescription consistent with a symptom within 3-months (e.g. anxiolytics &  anxiety symptoms). e.g. Use the `Indicator (specific)==INSERT Antidepressant or Anxiolytic` to separate medication from other mMHPs  | `mmhps_depres_anx <- merged_data %>% filter(Domain=="mMHPs" & scale=="1" & data1 > cut_off)` | 

--------------------------------
## Publications

[Syed S, Gilbert R, Feder G, Howe LD, Powell C, Howarth E, Deighton J, Lacey RE. Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England. The Lancet Public Health. 2023 Jul 1;8(7):e520-34.](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext)

[Syed S, Gonzalez-Izquierdo A, Allister J, Feder G, Li L, Gilbert R. Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study. The Lancet Digital Health. 2022 Jul 1;4(7):e482-96.](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(22)00061-9/fulltext)

[John A, McGregor J, Fone D, Dunstan F, Cornish R, Lyons RA, Lloyd KR. Case-finding for common mental disorders of anxiety and depression in primary care: an external validation of routinely collected data. BMC medical informatics and decision making. 2016 Dec;16(1):1-0.](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-016-0274-7)

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)

### [Go back](https://acesinehrs.com/domains/)

---
<span style="color:white"> Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate </span>

  [![](/images/logos/NIHR CPRU logo aces in ehrs footer.png)](https://www.ucl.ac.uk/children-policy-research/) | [![](/images/logos/ucl ich logo aces in ehrs.png)](https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0) | [![](/images/logos/university of oxford logo aces in ehrs.png)](https://www.ox.ac.uk/) | [![](/images/logos/NIHR Great ormond street hospital biomedical research centre logo aces in ehrs.png)](https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/) | [![](/images/logos/GOSH logo aces in ehrs.png)](https://www.gosh.nhs.uk/) | [![](/images/logos/University of bristol logo aces in ehrs.png)](https://www.bristol.ac.uk/) | [![](/images/logos/hdruk logo aces in ehrs.png)](https://www.hdruk.ac.uk/) | [![](/images/logos/caliber ucl logo aces in ehrs.png)](https://www.ucl.ac.uk/health-informatics/research/caliber) 
