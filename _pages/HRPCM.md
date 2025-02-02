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
excerpt: 'Definition <br /> <small><a>  </a></small> This domain includes indicators of high-risk presentations of child maltreatment (HRP-CM), consistent with NICE Clinical guidelines [CG89](https://www.nice.org.uk/guidance/cg89/chapter/Recommendations) and [NG76](https://www.nice.org.uk/guidance/ng76/chapter/Recommendations#recognising-child-abuse-and-neglect) on alerting features (risk presentations) that should raise clinical suspicions for CM. All indicators are recorded in the child, except for non-attendance of child appointments which uses both parent and child records. <br /><br /> {::nomarkdown}<iframe style="display: inline-block;" src=" " frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'

---

## Definition

This domain includes indicators consistent with NICE Clinical guidelines [CG89](https://www.nice.org.uk/guidance/cg89/chapter/Recommendations) and [NG76](https://www.nice.org.uk/guidance/ng76/chapter/Recommendations#recognising-child-abuse-and-neglect) on alerting features (risk presentations) that should raise clinical suspicions for CM. To be interpreted as warning signs of maltreatment in the face of uncertainty and the absence of evidence for CM. All indicators are recorded in the child, except for non-attendance of child appointments which uses both maternal and child records.

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9821663"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [High-risk presentation of CM (1774)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/HRPCM_2025ACEsinEHRs.txt)

* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/acesinehrs/raw/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v2.pdf)

--------------------------------
## Implementation

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **HRP-CM,** Child harm by undetermined intent; Lacerations, scars and abrasions; Thermal injuries; Unknown and unspecified causes of morbidity in child;Other and unspecified abdominal pain; Unspecified event in child, Obs for other suspected diseases and conditions in child | Include as HRP-CM when excluded co-occurring accident-related injuries recorded within +/-15 days of the event. Time frame selected based on the median time difference between data sources for some accidental injuries.  [NICE Clinical guideline [CG89]: 1.1.1-1.1.8; 1.1.15; 1.2.4, 1.2.5;  1.2.13](https://www.nice.org.uk/guidance/CG89/chapter/1-Guidance#physical-features) | 
 |**HRP-CM,** Eye trauma, NOS; Subarachnoid haemorrhage other; Subdural haematoma/retinal haemorrhage; Fractures, Intra-abdominal injuries, spinal injuries,  intracranial | Include as HRP-CM when excluded co-occurring accident-related injuries recorded within +/-15 days of the event, and when excluded birth-related injuries recorded <2 days post birth. [NICE Clinical guideline [CG89]: 1.1.11; 1.1.10](https://www.nice.org.uk/guidance/CG89/chapter/1-Guidance#physical-features) |
 |**HRP-CM,** Fractures, Intra-abdominal injuries, spinal injuries,  intracranial | Include as HRP-CM when excluded co-occurring accident-related injuries recorded within +/-15 days of the event, and when excluded birth-related injuries recorded <2 days post birth, and when excluded children with fragile bone disease (Osteoporosis), unless definitive CM is recorded within +/-30 days . [NICE Clinical guideline [CG89]: 1.1.9; 1.1.12;  1.1.13](https://www.nice.org.uk/guidance/CG89/chapter/1-Guidance#physical-features)) |

--------------------------------
## Publications

[Syed S, Gilbert R, Feder G, Howe LD, Powell C, Howarth E, Deighton J, Lacey RE. Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England. The Lancet Public Health. 2023 Jul 1;8(7):e520-34.](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext)

[Syed S, Gonzalez-Izquierdo A, Allister J, Feder G, Li L, Gilbert R. Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study. The Lancet Digital Health. 2022 Jul 1;4(7):e482-96.](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(22)00061-9/fulltext)

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)

### [Go back](https://acesinehrs.com/ACE-domains/)

---
<span style="color:white"> Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate </span>

  [![](/images/logos/NIHR CPRU logo aces in ehrs footer.png)](https://www.ucl.ac.uk/children-policy-research/) | [![](/images/logos/ucl ich logo aces in ehrs.png)](https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0) | [![](/images/logos/university of oxford logo aces in ehrs.png)](https://www.ox.ac.uk/) | [![](/images/logos/NIHR Great ormond street hospital biomedical research centre logo aces in ehrs.png)](https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/) | [![](/images/logos/GOSH logo aces in ehrs.png)](https://www.gosh.nhs.uk/) | [![](/images/logos/University of bristol logo aces in ehrs.png)](https://www.bristol.ac.uk/) | [![](/images/logos/hdruk logo aces in ehrs.png)](https://www.hdruk.ac.uk/) | [![](/images/logos/caliber ucl logo aces in ehrs.png)](https://www.ucl.ac.uk/health-informatics/research/caliber) 
  
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-HKLPGD444V"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-HKLPGD444V');
</script>
