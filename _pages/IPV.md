---
layout: splash
title: "Intimate partner violence"
permalink: /IPV/
header:
  overlay_color: "#5e616c"
  overlay_image: /images/Intimate partner violence aces in ehrs.jpg
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

Any incident of threatening behaviour, violence or abuse (psychological, physical, sexual, financial or emotional) between adults who are, or have been, intimate partners or family members.[1](https://www.sciencedirect.com/science/article/abs/pii/S0140673602111330) We restricted mIPV indicators to mothers aged ≥16 and their corresponding children to prevent misclassification of CM in younger mothers.

Includes suspected indicators with coding terms mentioning historic mIPV or maltreatment by an unspecified person. For instance, the “suspected mIPV, NOS” indicator contains codes mentioning “[X]Maltreatment, by acquaintance or friend”,” Risk of non-accidental injury”, “Assault in the home”.

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9802196"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Intimate partner violence (453 - excluding codes requiring algorithms)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/IPV_no_algo_2023ACEsinEHRs.txt)

* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/ACEs/raw/main/ACEsinEHRs%20v1.2.pdf)

--------------------------------
## Implementation

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **Susp.mIPV,** Assault NOS (algo); mIPV NOS (Assault and high-risk algo, 30/100 days) | Include as mIPV  if assault recording co-occurs with any “high-risk presentation recording” 30 days before the assault or in 100-days post the assault recording. High-risk recordings are a composite variable of recordings related to parental conflicts, health visitors being sent to the home, nurse partnership referrals, superficial head injuries and bruises. We developed the composite variable using results from our systematic review.51  In the current study the algorithm showed PPVs ranging from 18%-30% of definitive mIPV (derivation cohort). |
 | **mIPV,** Assault NOS (algo), mIPV NOS (Assault and preg. incident and CM algo, 45 days) | Include as mIPV if assault recording co-occurs with any recordings of a safeguarding referral, child protection recording, or definitive CM indicator, or “pregnant state, incidental” (marked in codelist) within 45 days of the assault. UK guidelines state 45 days is the maximum timeframe for an initial outcome following a children’s social care assessment from the date of received safeguarding referral (see point 82, [“working together to safe guard children”](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf)). | 

--------------------------------
## Publications

[Syed, S., Gonzalez-Izquierdo, A., Allister, J., Feder, G., Li, L., & Gilbert, R. (2022). Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study. The Lancet Digital Health.](https://www.sciencedirect.com/science/article/pii/S2589750022000619)

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)

### [Go back](https://acesinehrs.com/domains/)

---
<span style="color:white"> Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate </span>

  [![](/images/logos/NIHR CPRU logo aces in ehrs footer.png)](https://www.ucl.ac.uk/children-policy-research/) | [![](/images/logos/ucl ich logo aces in ehrs.png)](https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0) | [![](/images/logos/university of oxford logo aces in ehrs.png)](https://www.ox.ac.uk/) | [![](/images/logos/NIHR Great ormond street hospital biomedical research centre logo aces in ehrs.png)](https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/) | [![](/images/logos/GOSH logo aces in ehrs.png)](https://www.gosh.nhs.uk/) | [![](/images/logos/University of bristol logo aces in ehrs.png)](https://www.bristol.ac.uk/) | [![](/images/logos/hdruk logo aces in ehrs.png)](https://www.hdruk.ac.uk/) | [![](/images/logos/caliber ucl logo aces in ehrs.png)](https://www.ucl.ac.uk/health-informatics/research/caliber) 
