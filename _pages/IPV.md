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
excerpt: 'Definition <br /> <small><a>  </a></small> This domain includes indicators of intimate partner violence (IPV). [WHO](https://www.sciencedirect.com/science/article/abs/pii/S0140673602111330) defines IPV as any behaviour within an intimate relationship that causes physical, psychological or sexual harm to those in the relationship. IPV indicators are restricted to parents aged ≥16. <br /><br /> {::nomarkdown}<iframe style="display: inline-block;" src=" " frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'


---

## Definition

The [WHO](https://www.sciencedirect.com/science/article/abs/pii/S0140673602111330) defines IPV as  any behaviour within an intimate relationship that causes physical, psychological or sexual harm adults who are, or have been, intimate partners or family members. We restricted IPV indicators to parents aged ≥16 and their corresponding children to prevent misclassification of child maltreatment by the parents of younger parents.

Includes suspected indicators with coding terms mentioning historic IPV or maltreatment by an unspecified person. For instance, the “suspected IPV, NOS” indicator contains codes mentioning “[X]Maltreatment, by acquaintance or friend”,” Risk of non-accidental injury”, “Assault in the home”.

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9802196"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Intimate partner violence (453 - excluding codes requiring algorithms)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/IPV_no_algo_2023ACEsinEHRs.txt)

* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/acesinehrs/raw/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v2.pdf)

--------------------------------
## Implementation

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **Susp.mIPV,** Assault NOS (algo); mIPV NOS (Assault and high-risk algo, 30/100 days) | Include as mIPV  if assault recording co-occurs with any “high-risk presentation recording” 30 days before the assault or in 100-days post the assault recording. High-risk recordings are a composite variable of recordings related to parental conflicts, health visitors being sent to the home, nurse partnership referrals, superficial head injuries and bruises. We developed the composite variable using results from our systematic review.51  In the current study the algorithm showed PPVs ranging from 18%-30% of definitive mIPV (derivation cohort). |
 | **mIPV,** Assault NOS (algo), mIPV NOS (Assault and preg. incident and CM algo, 45 days) | Include as mIPV if assault recording co-occurs with any recordings of a safeguarding referral, child protection recording, or definitive CM indicator, or “pregnant state, incidental” (marked in codelist) within 45 days of the assault. UK guidelines state 45 days is the maximum timeframe for an initial outcome following a children’s social care assessment from the date of received safeguarding referral (see point 82, [“working together to safe guard children”](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf)). | 

--------------------------------
## Publications

[Syed S, Gilbert R, Feder G, Howe LD, Powell C, Howarth E, Deighton J, Lacey RE. Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England. The Lancet Public Health. 2023 Jul 1;8(7):e520-34.](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext)

[Syed S, Gonzalez-Izquierdo A, Allister J, Feder G, Li L, Gilbert R. Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study. The Lancet Digital Health. 2022 Jul 1;4(7):e482-96.](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(22)00061-9/fulltext)

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)

### [Go back](https://acesinehrs.com/domains/)

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