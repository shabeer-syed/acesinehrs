---
layout: splash
title: "Intimate partner violence"
permalink: /IPV/
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

Any incident of threatening behaviour, violence or abuse (psychological, physical, sexual, financial or emotional) between adults who are, or have been, intimate partners or family members.[1](https://www.sciencedirect.com/science/article/abs/pii/S0140673602111330) We restricted mIPV indicators to mothers aged ≥16 and their corresponding children to prevent misclassification of CM in younger mothers.

Includes suspected indicators with coding terms mentioning historic mIPV or maltreatment by an unspecified person. For instance, the “suspected mIPV, NOS” indicator contains codes mentioning “[X]Maltreatment, by acquaintance or friend”,” Risk of non-accidental injury”, “Assault in the home”.

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9802196"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Maternal intimate partner violence (450 + 519 for assault algorithm)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/mIPV_codelist.txt)

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

### [Go back](https://shabeer-syed.github.io/ACEs/domains)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>
