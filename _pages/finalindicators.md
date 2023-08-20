---
layout: splash
title: "All ACE domains & indicators"
permalink: /finalindicators/
header:
  overlay_color: "#5e616c"
  overlay_image: /images/ACEsinEHRs home page 2023.jpg
  cta_label: 
  cta_url: 
  caption:
excerpt: 'View definitions of domains and indicators. Download code lists.<br /> <small><a> <br /> {::nomarkdown}<iframe style="display: inline-block;" src=" " frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'

---

{% include base_path %}
[Download code lists](/finalindicators/#download-code-lists){: .btn .btn--info}{: .align-right}
<div class="flourish-embed flourish-table" data-src="visualisation/8622661"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

# Download code lists
* [ACEsinEHRs control documentation/release information](https://github.com/shabeer-syed/acesinehrs/raw/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v2.pdf) 


**Think-family approach:** Unless specified, indicators refers to information recorded in the child, mother and father.
{: .notice--info}

**Note:** The indicators uses [control flow methods](https://advanced-r-solutions.rbind.io/control-flow.html) to implement rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).
{: .notice--danger}

## All ACE indicators:
Right-click on link to save as a ".txt" file (i.e. using option "save link as")
*Total number of included ACE codes: 8802 (ACEs) + 8808 (covariates)*
*Total number of excluded/tested codes: 7671*

* [All ACEs (8864)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023ACEsinEHRs.txt)
* [All ACEs + crossmapped SNOMED CT (8864)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023_cross_mapped_snomed_medcode_prodcode_ICD910_ACEsinEHRs.txt)
* [All ACEs GP/CPRD only: medcodes, prodcodes, measures only (6618)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023_medcode_prodcode_CPRD_GOLD_ACEsinEHRs.txt)
* [All ACEs Hospital only: ICD, OPCS and HES-APC specific fields (2246)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023_ICD910_special_fields_HES_ACEsinEHRs.txt)

### By ACE domain:

* [Child maltreatment (1312)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/CM_2023ACEsinEHRs.txt)
* [Intimate partner violence (972 including 519 codes for assault algorithm)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/IPV_2023ACEsinEHRs.txt)
	* [Intimate partner violence (453 - excluding codes requiring algorithms)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/IPV_no_algo_2023ACEsinEHRs.txt)
* [High-risk presentation of CM (801)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/HRPCM_2023ACEsinEHRs.txt)
* [Adverse family environment (977)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/AFE_2023ACEsinEHRs.txt)
* [Parental mental health problems (3711)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/MHP_2023ACEsinEHRs.txt)
* [Parental substance misuse (1091)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/SM_2023ACEsinEHRs.txt)

#### [Covariates: non-ACEs used to add information to risk prediction models (8808)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Health%20comorbidities.txt)

### Code lists for rule-based exclusions
* [Accidents (2017)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Accidents.txt)
* [Osteoporosis - Bone disease (406)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Osteoporosis%20Bone%20disease.txt)
* [Birth injuries or traumatic complications (238)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Birth%20injury%20or%20complication.txt)
* [Mother-to-child-transmissions (15)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Mother-to-child%20transmission.txt)

### Need more code lists?
Visit:
[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/hdruk%20small.png)](https://phenotypes.healthdatagateway.org/)

### [Go back](https://acesinehrs.com/domains/) 

---
<span style="color:white"> Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate </span>

  [![](/images/logos/NIHR CPRU logo aces in ehrs footer.png)](https://www.ucl.ac.uk/children-policy-research/) | [![](/images/logos/ucl ich logo aces in ehrs.png)](https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0) | [![](/images/logos/university of oxford logo aces in ehrs.png)](https://www.ox.ac.uk/) | [![](/images/logos/NIHR Great ormond street hospital biomedical research centre logo aces in ehrs.png)](https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/) | [![](/images/logos/GOSH logo aces in ehrs.png)](https://www.gosh.nhs.uk/) | [![](/images/logos/University of bristol logo aces in ehrs.png)](https://www.bristol.ac.uk/) | [![](/images/logos/hdruk logo aces in ehrs.png)](https://www.hdruk.ac.uk/) | [![](/images/logos/caliber ucl logo aces in ehrs.png)](https://www.ucl.ac.uk/health-informatics/research/caliber) 