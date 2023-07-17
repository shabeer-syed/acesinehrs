---
layout: splash
title: "Child maltreatment"
permalink: /CM/
header:
  overlay_color: "#5e616c"
  overlay_image: /images/Child maltreatment aces in ehrs.jpg
  cta_label: 
  cta_url: 
  caption:
excerpt: 'Definition <br /> <small><a>  </a></small> This domain includes indicators of child maltreatment (CM). CM refers to any act of commission or omission by a parent or other caregiver that results in harm, potential for harm, or threat of harm to a child. Harm does not need to be intended <br /><br /> {::nomarkdown}<iframe style="display: inline-block;" src=" " frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'

---

{% include base_path %}

## Definition

Any recorded act of commission or omission by a parent or caregiver resulting in harm, the potential for harm or threat of child harm, including neglect, psychological, physical, sexual and emotional abuse. Harm does not need to be intended.[1](https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(08)61706-7/fulltext) In the UK, [statutory guidelines of CM](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf) include child exposure to IPV, and maternal evidence for omission or commission during pregnancy such as NAS and FAS.

Includes indicators such as neglect (pre-post birth), child protection recordings or out-of-home placements by social care services (see [code list browser](https://acesinehrs.com/codelist)).

Suspected CM included any maltreatment-related indicator with codes or measures describing presentations likely to refer to CM but without mentioning the underlying cause (e.g. harm caused by non-specified person), safeguarding procedures or child social service interventions.48 For instance, the “suspected CM, NOS” indicator contains codes mentioning “Victim of sexual abuse”, “Multi-professional risk assessment done”, “Assault in the home”

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9799589"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Child maltreatment (1312)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/CM_2023ACEsinEHRs.txt)

* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/ACEs/raw/main/ACEsinEHRs%20v1.2.pdf)

--------------------------------
## Implementation

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **CM,** FGM | Apply codes mentioning circumcision to female children only (e.g. "54314 - routine or ritual circumcision"). Code list includes markers for rule inclusion. | `cm_fgm <- merged_data %>% filter(Domain=="CM" & individual=="4" & gender=="female"` | 

--------------------------------
## Publications

[Syed S, Gilbert R, Feder G, Howe LD, Powell C, Howarth E, Deighton J, Lacey RE. Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England. The Lancet Public Health. 2023 Jul 1;8(7):e520-34.](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext)

[Syed S, Gonzalez-Izquierdo A, Allister J, Feder G, Li L, Gilbert R. Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study. The Lancet Digital Health. 2022 Jul 1;4(7):e482-96.](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(22)00061-9/fulltext)

[Gilbert R, Fluke J, O'Donnell M, Gonzalez-Izquierdo A, Brownell M, Gulliver P, Janson S, Sidebotham P. Child maltreatment: variation in trends and policies in six developed countries. The Lancet. 2012 Feb 25;379(9817):758-72.](https://www.sciencedirect.com/science/article/pii/S0140673611610878) Code list can be found [here](https://ars.els-cdn.com/content/image/1-s2.0-S0140673611610878-mmc1.pdf).

[Simkiss DE, Spencer NJ, Stallard N, Thorogood M. Health service use in families where children enter public care: a nested case control study using the General Practice Research Database. BMC health services research. 2012 Dec;12(1):1-2.](https://link.springer.com/article/10.1186/1472-6963-12-65)

[Royal College of General Practitioners. Child safeguarding toolkit.](https://elearning.rcgp.org.uk/mod/book/view.php?id=12531)

### [Go back](https://acesinehrs.com/domains/)

---
<span style="color:white"> Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate </span>

  [![](/images/logos/NIHR CPRU logo aces in ehrs footer.png)](https://www.ucl.ac.uk/children-policy-research/) | [![](/images/logos/ucl ich logo aces in ehrs.png)](https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0) | [![](/images/logos/university of oxford logo aces in ehrs.png)](https://www.ox.ac.uk/) | [![](/images/logos/NIHR Great ormond street hospital biomedical research centre logo aces in ehrs.png)](https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/) | [![](/images/logos/GOSH logo aces in ehrs.png)](https://www.gosh.nhs.uk/) | [![](/images/logos/University of bristol logo aces in ehrs.png)](https://www.bristol.ac.uk/) | [![](/images/logos/hdruk logo aces in ehrs.png)](https://www.hdruk.ac.uk/) | [![](/images/logos/caliber ucl logo aces in ehrs.png)](https://www.ucl.ac.uk/health-informatics/research/caliber) 
