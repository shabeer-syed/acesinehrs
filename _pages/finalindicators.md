---
layout: splash
title: "Final validated indicators and domains"
permalink: /finalindicators/
header:
  overlay_color: "#5e616c"
  overlay_image: /images/ACEsinEHRs home page 2023.jpg
  cta_label: 
  cta_url: 
  caption:
excerpt: 'Definition <br /> <small><a>  </a></small> Any act of commission or omission by a parent or other caregiver that results in harm, potential for harm, or threat of harm to a child. Harm does not need to be intended <br /><br /> {::nomarkdown}<iframe style="display: inline-block;" src=" " frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'

---
{% include base_path %}

<div class="flourish-embed flourish-table" data-src="visualisation/8622661"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

## Download code lists
Right click on link to save as a ".txt" file (i.e. using option "save link as")

## All ACE indicators:

* [All ACEs (8864)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023ACEsinEHRs.txt)
* [All ACEs + crossmapped SNOMED CT (8864)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023_cross_mapped_snomed_medcode_prodcode_ICD910_ACEsinEHRs.txt)
* [All ACEs GP/CPRD only: medcodes, prodcodes, measures only (6618)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023_medcode_prodcode_CPRD_GOLD_ACEsinEHRs.txt)
* [All ACEs Hospital only: ICD, OPCS and HES-APC specific fields (2246)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023_ICD910_special_fields_HES_ACEsinEHRs.txt)

## Control documentation

* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/ACEs/raw/main/ACEsinEHRs%20v1.2.pdf)

**Think-family approach:** Unless specified, indicators refers to information recorded in the child, mother and father.
{: .notice--info}

**Note:** The indicators uses [control flow methods](https://advanced-r-solutions.rbind.io/control-flow.html) to implement rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).
{: .notice--danger}
