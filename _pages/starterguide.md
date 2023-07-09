---
layout: single
classes:
  - wide
title: "Getting started"
permalink: /starterguide/
header:
  overlay_color: "#5e616c"
  overlay_image: /images/ACEsinEHRs getting started page.jpg
  cta_label: 
  cta_url: 
  caption:
excerpt: 'A quick introduction to incorporating validated indicators, code lists and scripts for measuring intervenable and clinically relevant ACEs using EHRs.<br /> <small><a> We are passionate about using EHRs to advance healthcare, social justice, and policy for families affected by adversity. However, ACEs in EHRs are not easily accessible and can be challenging to implement without guidance. </a></small><br /><br /> {::nomarkdown}<iframe style="display: inline-block;" src=" " frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'
last_modified_at: 2021-06-07T08:48:05-04:00
redirect_from:
  - /theme-setup/
sidebar:
  nav: "docs"

---

{% include base_path %}

Welcome to the marvellous world of EHRs! We provide a tutorial in how to implement clinically validated indicators for identifying ACEs among families using EHRs of mothers, fathers and children presenting to healthcare throughout the early life course.

# How does it work?
To use the ACE indicators, you will need:
* **Access to an EHR data source for research:** Obtain authorised and de-identified data of children and parents for research purposes. Most ACEs are captured in primary care. Several data sources in the UK provide linked primary care data of children and parents , including the [Clinical Practice Research Datalink (CPRD)](https://cprd.com/),[The Health Improvement Network (THIN)](https://www.the-health-improvement-network.com/), [QResearch](https://www.qresearch.org/).  Access to CPRD requires [protocol approval](https://cprd.com/research-applications) via CPRD’s Research Data Governance Process. Please visit the [Health Data Research Innovation Gateway](https://www.healthdatagateway.org) for more information on available data sources.
* **OR: Access to your organisation's locally stored EHR data:** Obtain authorised access to your service's/NHS trust's locally stored EHRs of children and parents for service-related and research purposes. Many NHS trusts provide streamlined processes to access data sources like Clinical Record Interactive Search ([1](https://slam.nhs.uk/clinical-record-interactive-search),[2](https://www.oxfordhealth.nhs.uk/research/toolkit/cris/),[3](https://www.southernhealth.nhs.uk/about-us/research/research-and-innovation/clinical-record-interactive-search)). These local data sources often have a data structure consistent with national data sources like [HES-APC](https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/hospital-episode-statistics). Contact your local contact person for academic support, process regarding data extraction, and data information analyses. 
* **Data linkage of child and parent data:** Implement robust data linkage of child and parent EHRs. Providers like CPRD allows you to access already established linkages of mother-child data. For linkage of mother child data in other EHR databases, please see methods described elsewhere [1](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0164667),[2](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext),[3](https://onlinelibrary.wiley.com/doi/full/10.1002/pds.4811). For paternal linkage, please see methods described [here](https://www.thelancet.com/cms/10.1016/S2468-2667(23)00119-6/attachment/9c50602c-ebd2-445f-ae3b-de30e2a1db14/mmc1.pdf)
* **ACE Indicators:** You are in the right place. We describe the ACEs below. Once you're ready please head over to the [download section](https://acesinehrs.com/starterguide/#download-code-lists), where we provide a comprehensive list of validated ACE indicators based on established research and definitions.
* **Data preparation and standardisation:** Extract the necessary data elements from the EHRs related to ACE indicators, and relevant health outcomes. Prepare the data by cleaning and structuring it in a format ready for merging with relevant ACEs code list.
* **Apply algorithms for ACE indicators:** Apply appropriate ACE algorithms using R, Python or any data management language to ensure you obtain validated indicators in the linked child and parent data.

![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/implement%20centered1.png)

# Domains and indicators
We developed two measures of ACEs for electronic health records (EHRs):
* Domains (ie, grouped indicators) and;
* Indicators (ie, grouped codes or measures)
  * Indicator 2
    * Indicator 1
      * Most specific indicator
        * Code (alphanumerical code attached to an event description)

Indicators represent a variable of grouped codes or measures for a potential recorded ACE in mothers, fathers or children. The ACEs follows a hierarchical structure, with three levels of specificity of the underlying ACE construct. The structure range from the most specific ACE category (specific indicator), to broader categories (indicator 1 and 2), to the six overall ACE domains consistent with the original [ACE study](/about/).

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/domains%20and%20indicators%201.png)](/domains/)

**Note:** The ability to use specific indicators depends on your sample size. We recommend restricting the disaggregation of specific indicators to those present in 250 or more unique children. For many studies, it will be most appropriate to use the six ACE domains only and avoid disaggregation into specific indicators unless required to answer your research question.
{: .notice--danger}

**Think-family approach:** Unless specified, indicators refers to information recorded in the child, mother and father. To properly study ACEs requires a "think-family" approach - that is, we need both children's and parents' data! Think-family means we recognise that the health and well-being of children are intricately tied to their parents' experiences and health outcomes.
{: .notice--info}

![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/ehrs%20of%20aces%20indicator.png "workflow")
<div class="flourish-embed flourish-hierarchy" data-src="visualisation/7087179"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

# Code lists
Mapped Codes attached to each ACE indicator are stored in [code lists](/domains/). Each data source will have different coding systems. The current ACEs indicators include ICD-9/10 codes (hospital/death records), Read codes, SNOMED-CT codes, medcodes, prodcodes, gemscripts (general practice), and codes for obtaining continuous data or coded information from speciality fields in CPRD GOLD, HES-APC, HES-A&E and HES-OP.

We have converted several original codes so the codelists contains one column of research ready codes which ensures  efficieint intergration of information from multiple coding systems without accidental de-duplication. See code list dictionary for more information.

## Code list dictionary

 | Provided variable | Description | 
 | --- | --- | 
 | **Code** | Data ready code. Contains CPRD GOLD medcodes and prodcodes (as used in the data provided by CPRD with added prefixes to prodcode), ICD-9/10 (removed punctuations for ICD), and OPSC-4 codes. Prefixes *`d_`* added to prodcodes and *`p_`* to OPSC-4 codes. Prefixes prevents de-duplication as different systems may use the same code for different descriptions. |
 | **Code original** | Original code as entered into respective system (removed punctuations for ICD) |
 | **Coding term** | Original code description |
 | **Indicator code** | Indicator code name | 
 | **Indicator specific** | Most specific indicator |
 | **Indicator 1** | Main ACE indicator combining multiple codes or measures as used in  validation paper | 
 | **Indicator 2** | Broader ACE indicator combining multiple codes or measures |
 | **Domain** | ACE domain grouping all indicators together (applicable for the overall code list) | 
 | **Severity** | Where applicable, this variable indicates the severity classification of the code description. *e.g. For alcohol misuse, `mild`, `moderate`, `severe`.* |
 | **Scale** | `1`=Indicates that the code and severity classifications are dependent on extra clinical information (e.g. frequency of alcohol consumption). By default, this is set to *`Mild`* for alcohol. See rule-based algorithms. |
 | **Reference** | `1`=code is part of family violence reference standard, `2`=code can be used as a broader measure of family violence |
 | **Individual** | `1`=code applies to child only, `2`=code applies to mother only, `3`=code applies to mother or child (i.e. either), `4`=code only applicable to female children |
 | **Coding systems** | `GP/primary care:` Read, OXMIS, Prodcode (prescriptions or items), CPRD REFERRAL FHSASPEC (field specific), CPRD REFERRAL NHSSPEC (field specific). `HES-APC/secondary care/ONS:` ICD-10, OPCS-4, ICD-9 (applies to ONS < year 2000), HES-APC DISDEST OR ADMISORC (field specific) |

### Example code attached to ACE indicator

| Code | Coding  term  | Indicator 1 | Indicator 2 |  domain | severity | scale | reference | individual | coding system |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 912 | [D]Anorexia	Anorexia | Anorexia | Eating disorders | Parental mental health problem | diagnostic |  |  | 2 | Read | 

# Data preparation and standardisation
Implementing the ACE indicators using code lists requires preparing and re-structuring your data sets into a uniform format. The data standardisation allows you to directly merge code lists and indicators to the data set to apply their attached algorithms.

**Skills check** <i class="fas fa-exclamation-triangle" style="color: #e3740d;"></i> Implementing the ACE indicators in more complex data sets like primary care data (GP records) requires knowledge of how to re-structure, manipulate and combine multiple large data sets into one or multiple new files. Depending on resources available, we recommend beginner to intermediate skills in a programming language of choice (e.g., Python, R). Many data management tasks involves a [split-apply-combine strategy](https://www.jstatsoft.org/article/view/v059i10), that is, the ability to "..break up a big problem into manageable pieces, operate on each piece independently and then put all the pieces back together. (Wickham, 2014, p1)"
{: .notice--danger}

## Data extraction and re-structering 
* Having identified your cohort, we recommend using a streaming approach to first extract only relevant patient data from the different files  by matching the patient IDs in each file against your separate list of patient IDs (i.e. cohort). This is an intermediate step which allows for data cleaning on smaller data files before applying the coded ACE indicators. The "streaming approach" refers to reading and processing data in chunks or sequentially, rather than loading the entire dataset into memory at once. In R the streaming approach is achieved by using *data.table::fread()* function with the *data.table = FALSE argument.*
* * Keep only essential data fields/variables to reduce file size. e.g. In the CPRD clinical file, the vairables *"constype, sysdate, data8"* can easily be omitted, as they are rarely used for the ACEs.
* Restructure all files and data fields (variables) into the same long format, and rename variable into consistent names. For example, the ONS mortality and HES-APC databases are provided by CPRD in wide format and needs restructuring.
* Add an extra variable to each data file to label the original data source (HES, CPRD clinical), as the data will be compiled into one file later.

## Data cleaning and code standardisation
* Clean and remove any punctuations, white spaces or trailing alphanumerics from data fields with relevant codes
* For each file, convert all data fields into the same classes (e.g. character, date) and machine readible format (e.g., R and Python likes dates as: year-month-day)
* Make sure to convert codes (see code list dictionary for pre-fixes) that share the same alphanumeric code as other codes into new unique codes to avoid deduplication, preserving their orginal linked ACE indicator. For example, Prodcodes (i.e. medications/prescriptions), medcodes (i.e. diagnoses/symptoms) and ICD-9 codes share thousands of the same alphanumeric codes but with different meanings and event descriptions.
  ```ruby
  For example: "11246 (prodcode) - Lofexidine 200 microgram tablets" vs. 11246 (medcode) – At risk violence in the home"
  ```
* To perserve each code's uniqueness, we have added pre-fixes to each relevant code list, which affect most data sources coding systems. We list all prefixes for data preparation below.
* Save all new files.

| Data source & Coding system | Prefix added | example | 
| --- | --- | --- |
| CPRD GOLD: Prodcode (Gemscript product code) | d_ | d_727 - Sertraline 100mg tablets | 
| ONS Mortality data collected ≤2000 & HES-APC ≤1998: ICD-9 | e_ | e_5713 - Alcoholic liver damage unspecified | 
| HES-APC: OPCS-4 | p_ | p_X66 - Cognitive behavioural therapy | 
| HES-A&E: A&E specific diagnosis system | aed_ | aed_144 - Poisoning (inc overdose) - other, inc alcohol | 
| HES-A&E: A&E speciality field "treatment" | aet_ | aet_54 - Social worker intervention | 
| HES-A&E: A&E speciality field "investigations" | aei_ | aei_21 - Pregnancy test |  
| HES-OP: OP speciality field "treatment" | opt_ | opt_711 - child and Adolescent Psychiatry Service |  

## Data integration and ACEs retrival process
* Once you've cleaned and restructured the multiple separate files, we recommend you re-apply the streaming approach to new files and extracting only relevant ACE data by matching the data fiels with codes in each file against your ACEs code lists.
* Depending on research purposes, we recommend binding all files into one combined "master database" with all relevant ACE data which should now follow a consistent unified format for easier retrival.

# Algorithms
Most indicators are derived using algorithms that identify and extract information from EHRs using clinically coded healthcare information (for example ICD-10, Read codes, SNOMED-CT). Algorithms are freely available on this webpage.

For GP records, we define indicators by combining information recorded in Read codes, prescriptions, referral fields and validated self-report measures (continuous variables needing re-coding) routinely administered by GPs or nurses (e.g. alcohol use).

For hospital and death registration records, we define indicators by combining codes from the International Classification of Diseases 9th/10th edition (ICD-9/10), the Classification of Interventions and Procedures (OPCS-4) and HES-APC discharge/admission fields. We also provide cross-mapped unvalidated indicators for newer systems (ICD-11/SNOMED CT) for further evaluation. Browse code lists [here](https://acesinehrs.com/codelistbrowse/).

**Note:** The indicators uses [control flow methods](https://advanced-r-solutions.rbind.io/control-flow.html) to implement rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).
{: .notice--danger}

Whilst most indicators are ready to use by merging the correct code list with your data, some indicators requires rule-based algorithms as listed below. 

* 1-2. Merge code lists with the data file containing the target population

```ruby
e.g. ensure correct ages for children/mothers
```
* 3.1 Convert continuous measures to binary indicators**

Use the additional "cut-off" variable provided in code lists (i.e. data > cut_off):

```ruby
 Example "one liner" in R or Python with dplyr:
mmhps_alcohol <- merged_data %>% filter(Domain=="mMHPs" & Indicator 1=="Alcohol misuse" & scale=="1" & data1 > cut_off)
```
* 3.2 Apply more advanced [control flow methods](https://adv-r.hadley.nz/control-flow.html)

Apply multiple rule-based algorithims (age critera, accident exclusions etc) using control flow (data dependent "if then assumptions") are widley covered by the data science community ([1](https://adv-r.hadley.nz/control-flow.html) [2](https://advanced-r-solutions.rbind.io/control-flow.html)).


# Download code lists
* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/ACEs/raw/main/ACEsinEHRs%20v1.2.pdf)
Right click on link to save as a ".txt" file (i.e. using option "save link as")
*Total number of included ACE codes: 8802 (ACEs) + 8808 (covariates)*
*Total number of excluded/tested codes: 7671*

## All ACE indicators:

* [All ACEs (8864)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023ACEsinEHRs.txt)
* [All ACEs + crossmapped SNOMED CT (8864)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023_cross_mapped_snomed_medcode_prodcode_ICD910_ACEsinEHRs.txt)
* [All ACEs GP/CPRD only: medcodes, prodcodes, measures only (6618)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023_medcode_prodcode_CPRD_GOLD_ACEsinEHRs.txt)
* [All ACEs Hospital only: ICD, OPCS and HES-APC specific fields (2246)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/ACEs_2023_ICD910_special_fields_HES_ACEsinEHRs.txt)

### By ACE domain:

* [Child maltreatment (1312)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/CM_2023ACEsinEHRs.txt)
* [Intimate partner violence (972 including 519 codes for assault algorithm)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/IPV_2023ACEsinEHRs.txt)
	* [Intimate partner violence (453 - excluding codes requring algorithms)](https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/codelists/IPV_no_algo_2023ACEsinEHRs.txt)
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

---
<span style="color:red"> The information is not intended for clinical use. No data is stored in this library.</span>
<span style="color:white"> Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate </span>

  [![](/images/logos/NIHR CPRU logo aces in ehrs footer.png)](https://www.ucl.ac.uk/children-policy-research/) | [![](/images/logos/ucl ich logo aces in ehrs.png)](https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0) | [![](/images/logos/university of oxford logo aces in ehrs.png)](https://www.ox.ac.uk/) | [![](/images/logos/NIHR Great ormond street hospital biomedical research centre logo aces in ehrs.png)](https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/) | [![](/images/logos/GOSH logo aces in ehrs.png)](https://www.gosh.nhs.uk/) | [![](/images/logos/University of bristol logo aces in ehrs.png)](https://www.bristol.ac.uk/) | [![](/images/logos/hdruk logo aces in ehrs.png)](https://www.hdruk.ac.uk/) | [![](/images/logos/caliber ucl logo aces in ehrs.png)](https://www.ucl.ac.uk/health-informatics/research/caliber) 
