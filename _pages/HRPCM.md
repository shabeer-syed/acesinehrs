---
layout: splash
title: "High-risk presentations of child maltreatment"
permalink: /HRPCM/
header:
  overlay_color: "#5e616c"
  overlay_image: /images/high risk presentations of child maltreatment aces in ehrs.jpg
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

This domain includes indicators consistent with NICE Clinical guidelines [CG89](https://www.nice.org.uk/guidance/cg89/chapter/Recommendations) and [NG76](https://www.nice.org.uk/guidance/ng76/chapter/Recommendations#recognising-child-abuse-and-neglect) on alerting features (risk presentations) that should raise clinical suspicions for CM. To be interpreted as warning signs of maltreatment in the face of uncertainty and the absence of evidence for CM. All indicators are recorded in the child, except for non-attendance of child appointments which uses both maternal and child records.

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9821663"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [High-risk presentation of CM (801)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/HRP_CM_codelist.txt)

* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/ACEs/raw/main/ACEsinEHRs%20v1.2.pdf)

--------------------------------
## Implementation

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **HRP-CM,** Child harm by undetermined intent; Lacerations, scars and abrasions; Thermal injuries; Unknown and unspecified causes of morbidity in child;Other and unspecified abdominal pain; Unspecified event in child, Obs for other suspected diseases and conditions in child | Include as HRP-CM when excluded co-occurring accident-related injuries recorded within +/-15 days of the event. Time frame selected based on the median time difference between data sources for some accidental injuries.  [NICE Clinical guideline [CG89]: 1.1.1-1.1.8; 1.1.15; 1.2.4, 1.2.5;  1.2.13](https://www.nice.org.uk/guidance/CG89/chapter/1-Guidance#physical-features) | 
 |**HRP-CM,** Eye trauma, NOS; Subarachnoid haemorrhage other; Subdural haematoma/retinal haemorrhage; Fractures, Intra-abdominal injuries, spinal injuries,  intracranial | Include as HRP-CM when excluded co-occurring accident-related injuries recorded within +/-15 days of the event, and when excluded birth-related injuries recorded <2 days post birth. [NICE Clinical guideline [CG89]: 1.1.11; 1.1.10](https://www.nice.org.uk/guidance/CG89/chapter/1-Guidance#physical-features) |
 |**HRP-CM,** Fractures, Intra-abdominal injuries, spinal injuries,  intracranial | Include as HRP-CM when excluded co-occurring accident-related injuries recorded within +/-15 days of the event, and when excluded birth-related injuries recorded <2 days post birth, and when excluded children with fragile bone disease (Osteoporosis), unless definitive CM is recorded within +/-30 days . [NICE Clinical guideline [CG89]: 1.1.9; 1.1.12;  1.1.13](https://www.nice.org.uk/guidance/CG89/chapter/1-Guidance#physical-features)) |

--------------------------------
## Publications

[Syed, S., Gonzalez-Izquierdo, A., Allister, J., Feder, G., Li, L., & Gilbert, R. (2022). Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study. The Lancet Digital Health.](https://www.sciencedirect.com/science/article/pii/S2589750022000619)

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)


### [Go back](https://shabeer-syed.github.io/ACEs/domains)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>
