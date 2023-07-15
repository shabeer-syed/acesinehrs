---
layout: splash
title: "Parental substance misuse"
permalink: /SM/
header:
  overlay_color: "#5e616c"
  overlay_image: /images/parental substance misuse aces in ehrs.jpg
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

Any consumption of alcohol/drugs meeting threshold for harmful or addictive levels such as codes mentioning "dependence", "specialist/enhanced treatment", class A through C drugs (e.g. A: heroin, cocaine, ecstasy, LSD), self-report measures (≥35 alcohol units per week higher risk drinking)55 and validated measures with higher cut-off scores (≥20 AUDIT score, SADQ ≥31 scores etc). Indicators for alcohol consumption are also available via the [HDR UK CALIBER phenotype library](https://phenotypes.healthdatagateway.org/).

Indicators are currently restricted to the mother's or child's record (e.g. maternal substance misuse)  due to methodological challenges in accurately linking children to their fathers (a long-standing issue of anonymised secondary and primary care data). However, once reliably linkage of fathers becomes available, the domains "parental mental health problems" and "parental substance misuse" will be updated to include potential fathers.

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9802228"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Parental substance misuse (1091)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/SM_2023ACEsinEHRs.txt)

* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/ACEs/raw/main/ACEsinEHRs%20v1.2.pdf)

--------------------------------
## Implementation

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **MSM,** Alcohol misuse Severe | Include if continuous data meets the cut-off assigned to each code (see code list): e.g. AUDIT: ≥20; AUDIT-PC: ≥10; SADQ ≥31; ≥35 alcohol units per week (analogous to higher-risk drinking/harmful drinking/alcohol dependence; [see NICE guidelines](https://www.nice.org.uk/guidance/ph24/chapter/7-Glossary)); >200 mg alcohol per 100 ml blood is classed as potential high-risk offender when driving in England/Wales (see UK gov) (applies to hospital admission codes in this study). | `msm_alcohol <- merged_data %>% filter(Domain=="MSM" & Indicator_1=="Alcohol misuse" & scale=="1" & data1 > cut_off)`|

--------------------------------
## Publications

[Syed, S., Gonzalez-Izquierdo, A., Allister, J., Feder, G., Li, L., & Gilbert, R. (2022). Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study. The Lancet Digital Health.](https://www.sciencedirect.com/science/article/pii/S2589750022000619) 

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)

[Department of Health. Alcohol guidelines review: report from the guidelines development group to the UK chief medical officers. London: Department of Health. January, 2016](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/545739/GDG_report-Jan2016.pdf)"

### [Go back](https://acesinehrs.com/domains/)

---
<span style="color:white"> Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate </span>

  [![](/images/logos/NIHR CPRU logo aces in ehrs footer.png)](https://www.ucl.ac.uk/children-policy-research/) | [![](/images/logos/ucl ich logo aces in ehrs.png)](https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0) | [![](/images/logos/university of oxford logo aces in ehrs.png)](https://www.ox.ac.uk/) | [![](/images/logos/NIHR Great ormond street hospital biomedical research centre logo aces in ehrs.png)](https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/) | [![](/images/logos/GOSH logo aces in ehrs.png)](https://www.gosh.nhs.uk/) | [![](/images/logos/University of bristol logo aces in ehrs.png)](https://www.bristol.ac.uk/) | [![](/images/logos/hdruk logo aces in ehrs.png)](https://www.hdruk.ac.uk/) | [![](/images/logos/caliber ucl logo aces in ehrs.png)](https://www.ucl.ac.uk/health-informatics/research/caliber) 
