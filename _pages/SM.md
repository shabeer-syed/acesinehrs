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
excerpt: 'Definition <br /> <small><a>  </a></small> This domain includes indicators of parental substance misuse (SM) / substance use disorder. SM refers to a cluster of cognitive, behavioral, and physiological symptoms associated with continued use of substances despite the significant substance-related problem <br /><br /> {::nomarkdown}<iframe style="display: inline-block;" src=" " frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'

---

## Definition
The DSM-5 defines a substance use disorder as a cluster of cognitive, behavioral, and physiological symptoms indicating that the individual continues using the substance despite significant substance-related problem. For parental substance misuse, we included any consumption of alcohol/drugs meeting threshold for harmful or addictive levels such as codes mentioning "dependence", "specialist/enhanced treatment", class A through C drugs (e.g. A: heroin, cocaine, ecstasy, LSD), self-report measures (≥35 alcohol units per week higher risk drinking)55 and validated measures with higher cut-off scores (≥20 AUDIT score, SADQ ≥31 scores etc). Indicators for alcohol consumption are also available via the [HDR UK CALIBER phenotype library](https://phenotypes.healthdatagateway.org/).

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

[Syed S, Gilbert R, Feder G, Howe LD, Powell C, Howarth E, Deighton J, Lacey RE. Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England. The Lancet Public Health. 2023 Jul 1;8(7):e520-34.](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext)

[Syed S, Gonzalez-Izquierdo A, Allister J, Feder G, Li L, Gilbert R. Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study. The Lancet Digital Health. 2022 Jul 1;4(7):e482-96.](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(22)00061-9/fulltext)

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)

[Department of Health. Alcohol guidelines review: report from the guidelines development group to the UK chief medical officers. London: Department of Health. January, 2016](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/545739/GDG_report-Jan2016.pdf)"

### [Go back](https://acesinehrs.com/domains/)

---
<span style="color:white"> Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate </span>

  [![](/images/logos/NIHR CPRU logo aces in ehrs footer.png)](https://www.ucl.ac.uk/children-policy-research/) | [![](/images/logos/ucl ich logo aces in ehrs.png)](https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0) | [![](/images/logos/university of oxford logo aces in ehrs.png)](https://www.ox.ac.uk/) | [![](/images/logos/NIHR Great ormond street hospital biomedical research centre logo aces in ehrs.png)](https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/) | [![](/images/logos/GOSH logo aces in ehrs.png)](https://www.gosh.nhs.uk/) | [![](/images/logos/University of bristol logo aces in ehrs.png)](https://www.bristol.ac.uk/) | [![](/images/logos/hdruk logo aces in ehrs.png)](https://www.hdruk.ac.uk/) | [![](/images/logos/caliber ucl logo aces in ehrs.png)](https://www.ucl.ac.uk/health-informatics/research/caliber) 
