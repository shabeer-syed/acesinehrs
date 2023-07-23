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
last_modified_at: 2023-07-09T08:48:05-04:00
redirect_from:
  - /theme-setup/
sidebar:
  nav: "docs"

---

{% include base_path %}

Welcome to the marvellous world of EHRs! This page provides a guide to get you started using measuring intervenable and clinically relevant ACEs using EHRs of families presenting to healthcare throughout the early life course.

# How does it work?
---
To use the ACE indicators, you will need:
* **Access to an EHR data source for research:** Obtain authorised and de-identified data of children and parents for research purposes. Most ACEs are captured in primary care. Several data sources in the UK provide linked primary care data of children and parents, including the [Clinical Practice Research Datalink (CPRD)](https://cprd.com/),[The Health Improvement Network (THIN)](https://www.the-health-improvement-network.com/), [QResearch](https://www.qresearch.org/).  Access to CPRD requires [protocol approval](https://cprd.com/research-applications) via CPRD’s Research Data Governance Process. Please visit the [Health Data Research Innovation Gateway](https://www.healthdatagateway.org) for more information on available data sources.
* **OR: Access to your organisation's locally stored EHR data:** Obtain authorised access to your service's/NHS trust's locally stored EHRs of children and parents for service-related and research purposes. Many NHS trusts provide streamlined processes to access data sources like Clinical Record Interactive Search ([1](https://slam.nhs.uk/clinical-record-interactive-search),[2](https://www.oxfordhealth.nhs.uk/research/toolkit/cris/),[3](https://www.southernhealth.nhs.uk/about-us/research/research-and-innovation/clinical-record-interactive-search)). These local data sources often have a data structure consistent with national data sources like [HES-APC](https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/hospital-episode-statistics). Contact your local contact person for academic and research support relevant to data information analyses.
* **Data linkage of child and parent data:** Implement robust data linkage of child and parent EHRs. Providers like CPRD allow you to access already established linkages of mother-child data. For linkage of mother-child data in other EHR databases, please see methods described elsewhere [1](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0164667),[2](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext),[3](https://onlinelibrary.wiley.com/doi/full/10.1002/pds.4811). For paternal linkage, please see methods described [here](https://www.thelancet.com/cms/10.1016/S2468-2667(23)00119-6/attachment/9c50602c-ebd2-445f-ae3b-de30e2a1db14/mmc1.pdf).
* **ACE Indicators:** You are in the right place. Most indicators are derived using algorithms that identify and extract information from EHRs using clinically coded healthcare information (for example, ICD-10, Read codes, SNOMED-CT). We describe the ACEs and how to apply the algorithms below. Once you're ready, please head over to the [download section](https://acesinehrs.com/starterguide/#download-code-lists), where we provide a comprehensive list of validated ACE indicators based on established research and definitions.
* **Data preparation and standardisation:** Extract the necessary data elements from the EHRs related to ACE indicators and relevant health outcomes. Prepare the data by cleaning and structuring it in a format ready for merging with the appropriate ACEs code list.
* **Apply algorithms for ACE indicators:** Apply appropriate ACE algorithms using R, Python or any data management language to ensure you obtain validated indicators in the linked child and parent data.

![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/implement%20centered1.png)

# ACE indicators
---
## Domains and indicators
We developed two measures of ACEs for electronic health records (EHRs):
* **Domains** (ie, grouped indicators) and;
* **Indicators** (ie, grouped codes or measures)
  * Indicator 2
    * Indicator 1
      * Most specific indicator
        * Code (alphanumerical code attached to an event description)

Indicators represent a variable of grouped codes or measures for a potential recorded ACE in mothers, fathers or children. The ACEs follow a hierarchical structure, with three levels of specificity of the underlying ACE construct. The structure ranges from the most specific ACE category (specific indicator) to broader categories (indicators 1 and 2), to the six overall ACE domains consistent with the original [ACE study](/about/). 

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/domains%20and%20indicators%201.png)](/domains/)

**Note:** The ability to use specific indicators depends on your sample size. We recommend restricting the disaggregation of specific indicators to those present in 250 or more unique children. For many studies, it will be most appropriate to use the six ACE domains only and avoid disaggregation into specific indicators unless required to answer your research question.
{: .notice--danger}

**Think-family approach:** Unless specified, indicators refer to information recorded in the child's, the mother's and the father's records. Properly studying ACEs requires a "think-family" approach - we need both children's and parents' data! Think-family means we recognise that the health and well-being of children are intricately tied to their parents' experiences and health outcomes.
{: .notice--info}

![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/ehrs%20of%20aces%20indicator.png "workflow")
<div class="flourish-embed flourish-hierarchy" data-src="visualisation/7087179"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

## Code lists
We provide mapped codes for each ACE indicator stored in [code lists](/domains/). Each data source will have different coding systems. The current ACEs indicators include ICD-9/10 codes (hospital/death records), Read codes, SNOMED-CT codes, medcodes, prodcodes, gemscripts (general practice), and codes for obtaining continuous data or coded information from speciality fields in CPRD GOLD, HES-APC, HES-A&E and HES-OP.

We have converted several original codes so the code lists contain one column of research-ready codes. This ensures efficient information integration from multiple coding systems without accidental deduplication. See code list dictionary and conversion table below for more information.

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
---
Now, let's get the data ready for analysis! 
Unlike data sets such as the [Hospital Episode Statistics](https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/hospital-episode-statistics) where everything is nicely placed into one file, EHRs from primary care are messier and located in multiple separate files with different structures and format. Therefore, implementing the ACE indicators using code lists requires preparing and restructuring your data sets into a uniform format. The data standardisation allows you to directly merge code lists and indicators to the data set to apply their attached algorithms.

## Steps - data preparation:
* **Extract the raw data files using SQL** 
* **Restructure each data file** (ie. creating new data files with consistent format)
  * **Data clean & standardise each file** (ie, add prefixes to codes, remove waste etc)
    * Retrieve data from standardised files & bind into a "master ACE data file"
      * Merge code list with the master file
        * Apply algorithms & keep relevant record

**IMPORTANT!** <i class="fas fa-exclamation-triangle" style="color: #e3740d;"></i> IImplementing the ACE indicators in more complex data sets like primary care data (GP records) requires restructuring, manipulating and combining multiple large data sets into one or multiple new files using a programming language of choice (e.g., Python, R). This section provides only brief information on data management specific to the implementation of the ACE indicators. Many data management tasks involve a [split-apply-combine strategy](https://www.jstatsoft.org/article/view/v059i10), that is, the ability to "..break up a big problem into manageable pieces, operate on each piece independently and then put all the pieces back together (Wickham, 2014, p1)".  This information is therefore intended as supplementary recommendations to users who already have skills in  programming languages like R, Python, or SQL. To learn how to use R for data management, we recommend reading [*"R for Data Science (2e)*" by Hadley Wickham, Mine Çetinkaya-Rundel and Garrett Grolemund](https://r4ds.hadley.nz/), freely available online.
{: .notice--danger}

## Data extraction and restructuring 
### Restructuring the data
* *Restructuring data files and fields*. Having extracted your raw files, we need to restructure all files and data fields (variables) into a consistent "long format", and rename variable into consistent names. The consistent structure ensures we can easily bind all files into one combined file later. For example, the ONS mortality and HES-APC databases are provided by CPRD in wide format and needs restructuring.
* Drop any irrelevant data fields/variables to reduce file size. e.g. In the CPRD clinical file, the variables *"constype, sysdate, data8"* can easily be omitted, as they are rarely used for the ACEs.
* Make sure to add an extra variable to each data file to label the original data source (HES, CPRD clinical) before saving it.

## Data cleaning and code standardisation
Most large EHR files contain various types of errors, such as missing values, inconsistent formats, or invalid entries. Data cleaning ensures consistency across different variables and datasets.

* Clean and remove any punctuations, white spaces or trailing alphanumeric from data fields with relevant codes

```ruby
aces_data$medcode <- gsub("\\s+","",aces_data$medcode) #removes white/blank spaces
aces_data$medcode <- gsub("\\.","",aces_data$medcode) #removes punctuations
```

* For each file, convert all data fields into the same classes (e.g. character, date) and machine-readable format (e.g., R and Python likes dates as: year-month-day)

```ruby
# R dplyr example of converting a data frame to character class
# and restructuring a date variable provided in the incorrect format
 
aces_data <- aces_data %>% mutate_all(as.character) %>% 
 separate(date_example_variable,c("day","month","year"),sep="-",remove=T) %>% 
 unite(new_date_variable,c("year","month","day"),sep="-",remove=T) 
```
* Make sure to convert codes (see prefixes below) that share the same alphanumeric code as other codes into new unique codes to avoid deduplication to preserve their original linked ACE indicator. For example, Prodcodes (i.e. medications/prescriptions), medcodes (i.e. diagnoses/symptoms) and ICD-9 codes share thousands of the same alphanumeric codes but with different meanings and event descriptions.
* `For example: "11246 (prodcode) - Lofexidine 200 microgram tablets" vs. 11246 (medcode) – At risk violence in the home`

## Conversation table of codes requiring prefixes
* To preserve each code's uniqueness, we have added prefixes to each relevant code list, which affect most coding systems. We list all prefixes for data preparation below.
* In R or Python, we recommend using the "dplyr::unite" function or "R::paste0()". In Stata, you can use the "Concatenation" function (see Stata documentation).

| Data source & Coding system | Prefix added | example | 
| --- | --- | --- |
| CPRD GOLD: Prodcode (Gemscript product code) | d_ | d_727 - Sertraline 100mg tablets | 
| ONS Mortality data collected ≤2000 & HES-APC ≤1998: ICD-9 | e_ | e_5713 - Alcoholic liver damage unspecified | 
| HES-APC: OPCS-4 | p_ | p_X66 - Cognitive behavioural therapy | 
| HES-A&E: A&E specific diagnosis system | aed_ | aed_144 - Poisoning (inc overdose) - other, inc alcohol | 
| HES-A&E: A&E speciality field "treatment" | aet_ | aet_54 - Social worker intervention | 
| HES-A&E: A&E speciality field "investigations" | aei_ | aei_21 - Pregnancy test |  
| HES-OP: OP speciality field "treatment" | opt_ | opt_711 - child and Adolescent Psychiatry Service |  

## Derive ACEs "master file" with only relevant data
* Having identified your cohort and restructured the multiple separate files, the next step is to extract the relevant data from each file and bind this into a new one "combined file" with only ACE data.
* *Streaming data extraction.*  To extract only relevant patient ACE data, we  recommend you apply a streaming approach to the new standardise files by iterating over (i.e. repeating the matching) each patient ID in each file against your separate list of patient IDs (i.e. cohort) and your separare ACEs code lists.

* A "streaming approach" refers to reading and processing data in chunks or sequentially rather than loading the entire dataset into memory at once. Whilst *SQL* is useful for handling larger databases, R or Python can also apply *streaming* by first loading your list of relevant patient IDs and then extracting relevant data using package functions like: *data.table::fread(.... ,data.table=F)* with *dplyr::filter* and *fastmatch::%fin%*.

* In the final step, we recommend (depending on research purposes) binding all retrieved ACE files into one combined "master database" with only relevant ACE data, which should now follow a consistent unified format for easier retrieval. The above steps can be incoperated into one step. Here is an example in R which extract relevant patient data from multiple files (assuming they have the same underlying file structure) into one new file without loading everything into working memory:

```ruby
# Step 1: Set up the working directory
setwd("path/to/ehr/files")
# Step 2: Install and load required packages
install.packages(c("data.table", "readr","tidyverse","fastmatch"))
library(data.table)
library(readr)
library(tidyverse)
library(fastmatch)
# Step 3: Read the patient ID list and code list
patient_id_list <- read_csv("patient_id_list.csv")  # Adjust the file name and format as per your data
# Step 4: Stream through EHR files, match with patient ID, and save relevant data to new files
for (ehr_file in list.files(pattern = "*.txt")) {  # Adjust the pattern as per your file extension
  output_file <- paste0("output_", ehr_file)  # Generate output file name

  # Create output file and write column names
  fwrite(data.frame(), output_file)  # Creates an empty file
  fwrite(names(data.table::fread(ehr_file, nrows = 0, header = TRUE, data.table = FALSE)), output_file, append = TRUE)  # Write column names
  
  # Stream through EHR file and extract relevant data
  ehr_stream <- data.table::fread(ehr_file, header = TRUE, data.table = FALSE, header = T, data.table =F,colClasses="character",nThread=8)
    relevant_data <- ehr_stream %>% filter(patient_id %fin% patient_id_list$patient_id)
      # Append relevant data to output file
    fwrite(relevant_data, output_file, append = TRUE, quote = FALSE, row.names = FALSE,col.names=T)
}
```

## Deriving variables
### Introduction
* Most indicators are ready to be used after merging the correct code list with your prepared ACE data file. However, many indicators rely on rule-based algorithms to ensure coded measures meet appropriate cut-off criteria and prevent misclassifications. Algorithms include age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).
 * For GP records, we define indicators by combining information recorded in Read codes, prescriptions, referral fields and validated self-report measures (continuous variables needing re-coding) routinely administered by GPs or nurses (e.g. alcohol use).
 * For hospital and death registration records, we define indicators by combining codes from the International Classification of Diseases 9th/10th edition (ICD-9/10), the Classification of Interventions and Procedures (OPCS-4) and HES-APC discharge/admission fields.

**Time restrictions:** The validated ACE indicators are time sensitive and apply any time between 2 years before birth and 10 years after birth. However, most child maltreatment and high-risk presentations of child maltreatment are limited to 2 years before to 3, or 5 years after birth. Ascertaining the correct exposure time in relation to children's birthdate is essential.
{: .notice--danger}

## Applying algorithms using the code lists built-in helper functions
Here, we list steps to apply rule-based algorithms and obtain valid indicators:

* **1. Merge code lists.** Merge the new combined "ACE specific data file" with your relevant code list. *Note: In the above R script example, the code list is already automatically merged with the new combined "ACE specific data file"*.
* *Keep only unique recordings.* After merging the code lists, many recordings will be duplicated as the ACE codes are iterated over both children’s and parents IDs. In R or Python, we recommend  removing duplicate recordings using  `e.g. "aces_data %>% dplyr::distinct(patid,medcode,eventdate,system,source,individual,.keep_all=T)`

* **2. Filter/subset the data against 1-2 criteria** The ACEs code lists were developed with built-in "helper variables". After merging the code lists with your ACE-specific file, you should have extra variables to filter or subset values against and retain only data with valid indicators. We provide an example below using "if-then" assumptions to rows where the "Code" column value is present in the code list, and additional conditions are met.

```ruby
mmhps_depres_anx <- merged_data %>% filter(Domain=="mMHPs" & scale=="1" & data1 > cut_off

#In this case we retained only mental health measures/scales that met validated cut-off critera
# In addition to selecting the specific domain, helper variables include:
#"Scale==1" (keep measures with continious data) 
# data1 "cut_off" (keep only values in data1 above cut-off score)
```

* To apply multiple if-then assumptions against a standalone code list we rely on [control flow methods](https://advanced-r-solutions.rbind.io/control-flow.html). Here is a generic example using "dplyr:case_when:"

```ruby
data <- data %>%
  mutate(Binary_Variable = case_when(
    Code %in% code_list & Field1 > 10 & Field2 == "Value" ~ 1,
    Code %in% code_list & Field1 <= 10 & Field2 != "Value" ~ 0,
    TRUE ~ NA
  ))
```
* **3. Applying multiple rule-based criteria.** Some indicator requires creating new variables to apply multiple rules simultaneously.  
* An example includes the algorithm for depression based on medication and non-diagnostic symptoms. Here, you will need to filter the data based on the presence of any of the coded depressive symptoms or medications and the co-occurrence of any diagnosis or intervention received within the past 2 years.

```ruby
# Step 1: Load the required packages
library(dplyr)

# Step 2: Import the EHR data
ehr_data <- read.csv("ehr_data.csv")  # Replace "ehr_data.csv" with the actual file path and name

# Step 3: Define the criteria for depression
# Define the symptoms or medications associated with depression
depression_symptoms <- c("symptom1", "symptom2", "symptom3")
depression_medications <- c("medication1", "medication2", "medication3")

# Define the previous collection of codes within the past 2 years
previous_codes <- c("code1", "code2", "code3")

# Step 4: Apply the algorithm to identify depression cases
depression_cases <- ehr_data %>%
  filter(
    # Check if any of the depression symptoms or medications are present
    any_of(depression_symptoms) |
    any_of(depression_medications),
    
    # Check if any of the previous codes are present within the past 2 years
    any_of(previous_codes) & visit_date >= (Sys.Date() - 365 * 2)
  )

# Step 5: Explore the identified depression cases
summary(depression_cases)
```

* Finally, once you applied the algorithms, keep only one ACE indicator or domain per each unique child (e.g., using "dplyr's  "distinct()" function) within the relevant study period before merging it back to your cohort.

# Download code lists
* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/acesinehrs/raw/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v2.pdf)
Right-click on link to save as a ".txt" file (i.e. using option "save link as")
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
