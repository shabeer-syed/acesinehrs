---
layout: splash
title: "All ACE domains & indicators"
permalink: /indicators/
header:
  overlay_color: "#5e616c"
  overlay_image: /images/ACEsinEHRs home page 2023.jpg
  cta_label: 
  cta_url: 
  caption:
excerpt: 'View definitions of domains and indicators. Download code lists.<br /> <small><a> <br /> {::nomarkdown}<iframe style="display: inline-block;" src=" " frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'

---

{% include base_path %}
[Download code lists](/indicators/#download-code-lists){: .btn .btn--info}{: .align-right}
<div class="flourish-embed flourish-table" data-src="visualisation/8622661"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

# Download code lists
* [ACEsinEHRs control documentation/release information](https://github.com/shabeer-syed/acesinehrs/raw/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v2.pdf) 


**Think-family approach:** Unless specified, indicators refers to information recorded in the child, mother and father.
{: .notice--info}

**Note:** The indicators uses [control flow methods](https://advanced-r-solutions.rbind.io/control-flow.html) to implement rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).
{: .notice--danger}

## All ACE indicators:
Right-click on link to save as a ".txt" file (i.e. using option "save link as")
*Total number of included ACE codes: 23164 (ACEs)

* [All ACEs (23164)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025ACEsinEHRs.txt)
* [All ACEs GP/CPRD GOLD/AURUM only: medcodes, prodcodes, measures only (20925)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025_medcode_prodcode_CPRD_GOLD_Aurum_ACEsinEHRs.txt)
* [All ACEs Hospital only: ICD, OPCS and HES-APC specific fields (2239)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025_ICD910_special_fields_HES_ACEsinEHRs.txt)

### By ACE domain:

* [Child maltreatment (3852)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/CM_2025ACEsinEHRs.txt)
*  [Intimate partner violence (3281 - incl. codes requiring algorithms)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/IPV_2025ACEsinEHRs.txt)
	*  [Intimate partner violence (2044 - excluding codes requiring algorithms)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/IPV_no_algo_2025ACEsinEHRs.txt)
* [High-risk presentation of CM (1774)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/HRPCM_2025ACEsinEHRs.txt)
* [Adverse family environment (2308)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/AFE_2025ACEsinEHRs.txt)
* [Parental mental health problems (9063)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/MHP_2025ACEsinEHRs.txt)
* [Parental substance misuse (2886)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/SM_2025ACEsinEHRs.txt)

#### [Covariates: non-ACEs used to add information to risk prediction models (8808)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Health%20comorbidities.txt)

### Code lists for rule-based exclusions
* [Accidents (3356)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/Accident_excl_2025ACEsinEHRs.txt)
* [Osteoporosis - Bone disease (406)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Osteoporosis%20Bone%20disease.txt)
* [Birth injuries or traumatic complications (238)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Birth%20injury%20or%20complication.txt)
* [Mother-to-child-transmissions (15)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Mother-to-child%20transmission.txt)

### Need more code lists?
Visit:
[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/hdruk%20small.png)](https://www.healthdatagateway.org/)

### [Go back](https://acesinehrs.com/ACE-domains/)

---
<span style="color:white"> Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate </span>

  [![](/images/logos/NIHR CPRU logo aces in ehrs footer.png)](https://www.ucl.ac.uk/children-policy-research/) | [![](/images/logos/ucl ich logo aces in ehrs.png)](https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0) | [![](/images/logos/university of oxford logo aces in ehrs.png)](https://www.ox.ac.uk/) | [![](/images/logos/NIHR Great ormond street hospital biomedical research centre logo aces in ehrs.png)](https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/) | [![](/images/logos/GOSH logo aces in ehrs.png)](https://www.gosh.nhs.uk/) | [![](/images/logos/University of bristol logo aces in ehrs.png)](https://www.bristol.ac.uk/) | [![](/images/logos/hdruk logo aces in ehrs.png)](https://www.hdruk.ac.uk/) | [![](/images/logos/caliber ucl logo aces in ehrs.png)](https://www.ucl.ac.uk/health-informatics/research/caliber) 
