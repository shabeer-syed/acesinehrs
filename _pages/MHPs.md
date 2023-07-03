---
layout: splash
title: "Parental mental health problems"
permalink: /MHPs/
header:
  overlay_color: "#5e616c"
  overlay_image: /images/ACEsinEHRs home page 2023.jpg
  cta_label: 
  cta_url: 
  caption:
excerpt: 'Definition <br /> <small><a>  </a></small> Any act of commission or omission by a parent or other caregiver that results in harm, potential for harm, or threat of harm to a child. Harm does not need to be intended <br /><br /> {::nomarkdown}<iframe style="display: inline-block;" src=" " frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'

github:
  - excerpt: '{::nomarkdown}<iframe style="display: inline-block;" src="https://ghbtns.com/github-btn.html?user=mmistakes&repo=minimal-mistakes&type=star&count=true&size=large" frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="https://ghbtns.com/github-btn.html?user=mmistakes&repo=minimal-mistakes&type=fork&count=true&size=large" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'

intro:
  - excerpt: 'We have developed and validated indicators for identifying ACEs in routinely collected non-identifiable health care data of mothers and children presenting to GPs, A&E, hospitals before and after birth. This website provides information on definitions, concepts, measures, and  standardised tools to help users apply the developed ACE indicators to create “research-ready” datasets. [See the publication here.](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(22)00061-9/fulltext) See also the published [systematic review.](https://adc.bmj.com/content/archdischild/106/1/44.full.pdf)'

---

## Definition

This domain contains indicators of mutually exclusive symptom clusters aligning with disorder classifications laid out by DSM-5/ICD-10 excluding substance misuse. Some codes for self-harm (e.g. overdose) may be represented across both maternal mental health problems (mMHPs) and maternal substance misuse (MSM) domains. mMHPs indicators are ascertained using read codes, prescriptions, ICD-10 codes or by meeting the higher cut-off score on a validated self-report instrument or validated algorithms with prescriptions.[1](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-016-0274-7). Validated codes for mMHPs and MSM are also available via the [HDR UK CALIBER phenotype library](https://phenotypes.healthdatagateway.org/), with the mapping process described by [Kuan et al.](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(19)30012-3/fulltext)

Indicators are currently restricted to the mother's or child's record (e.g. maternal substance misuse)  due to methodological challenges in accurately linking children to their fathers (a long-standing issue of anonymised secondary and primary care data). However, once reliably linkage of fathers becomes available, the domains "parental mental health problems" and "parental substance misuse" will be updated to include potential fathers.

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9802273"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Maternal mental health problems (3960)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/mMHPs_codelist.txt)

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

[Syed, S., Gonzalez-Izquierdo, A., Allister, J., Feder, G., Li, L., & Gilbert, R. (2022). Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study. The Lancet Digital Health.](https://www.sciencedirect.com/science/article/pii/S2589750022000619)

[John A, McGregor J, Fone D, Dunstan F, Cornish R, Lyons RA, Lloyd KR. Case-finding for common mental disorders of anxiety and depression in primary care: an external validation of routinely collected data. BMC medical informatics and decision making. 2016 Dec;16(1):1-0.](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-016-0274-7)

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)

### [Go back](https://shabeer-syed.github.io/ACEs/domains)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>
