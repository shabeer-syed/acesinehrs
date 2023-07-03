---
layout: single
title: "Quick-Start Guide"
permalink: /starterguide/
excerpt: "How to quickly install and setup Minimal Mistakes for use with GitHub Pages."
last_modified_at: 2021-06-07T08:48:05-04:00
redirect_from:
  - /theme-setup/
toc: true
toc_label: "My Table of Contents"
toc_icon: "cog"
toc_sticky: true

---


[!["Buy Me A Coffee"](https://user-images.githubusercontent.com/1376749/120938564-50c59780-c6e1-11eb-814f-22a0399623c5.png)](https://www.buymeacoffee.com/mmistakes)

[![Support via PayPal](https://cdn.jsdelivr.net/gh/twolfson/paypal-github-button@1.0.0/dist/button.svg)](https://www.paypal.me/mmistakes)
{: style="margin-top: 0.5em;"}

## How does it work?

![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/implement%20centered1.png)

## Indicators and algorithms
We developed two measures of ACEs for electronic health records (EHRs):
* Domains (ie, grouped indicators) and;
* Indicators (ie, grouped codes or measures)

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/domains%20and%20indicators%201.png)](https://shabeer-syed.github.io/ACEs/domains)

Most indicators are derived using algorithms that identify and extract information from EHRs using clinically coded healthcare information (for example ICD-10, Read codes, SNOMED-CT). Algorithms are freely available on this webpage.

For GP records, we define indicators by combining information recorded in Read codes, prescriptions, referral fields and validated self-report measures (continuous variables needing re-coding) routinely administered by GPs or nurses (e.g. alcohol use).

For hospital and death registration records, we define indicators by combining codes from the International Classification of Diseases 9th/10th edition (ICD-9/10), the Classification of Interventions and Procedures (OPCS-4) and HES-APC discharge/admission fields. We also provide cross-mapped unvalidated indicators for newer systems (ICD-11/SNOMED CT) for further evaluation. Browse code lists [here](https://acesinehrs.com/codelist).

Unless specified, indicators refers to information recorded in both child and maternal records.

**Note:** The indicators uses [control flow methods](https://advanced-r-solutions.rbind.io/control-flow.html) to implement rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).
{: .notice--warning}

## Download code lists
Right click on link to save as a ".txt" file (i.e. using option "save link as")

*Total number of included ACE codes: 8802 (ACEs) + 8808 (covariates)*

*Total number of excluded/tested codes: 7671*

## Control documentation


* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/ACEs/raw/main/ACEsinEHRs%20v1.2.pdf)

### All ACE indicators:

* [All ACEs (8830)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ALL_ACEs_codelist.txt)
* [All ACEs + crossmapped SNOMED CT and ICD-11 (10650)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ACEs_crossmaped_snomedCT_icd11.txt)
* [All ACEs GP/CPRD only: medcodes, prodcodes, measures only (6639)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ACEs_readcode_gemscript_CPRD_gold_only.txt)
* [All ACEs Hospital only: ICD, OPCS and HES-APC specific fields (2191)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ACEs_icd_hosp.txt)

### By ACE domain:

* [Child maltreatment (1306)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/CM_codelist.txt)
* [Maternal intimate partner violence (263 + 185 for assault algorithm)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/IPV_codelist.txt)
	* [Maternal intimate partner violence (263 - excluding codes requring algorithms)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/IPV_no_algo_codelist.txt)
* [High-risk presentation of CM (801)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/HRP_CM_codelist.txt)
* [Adverse family environment (972)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/AFE_codelist.txt)
* [Maternal mental health problems (3960)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/mMHPs_codelist.txt)
* [Maternal substance misuse (1090)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/MSM_codelist.txt)

#### [Covariates: non-ACEs used to add information to risk prediction models (8808)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Health%20comorbidities.txt)

### Code lists for rule-based exclusions
* [Accidents (2017)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Accidents.txt)
* [Osteoporosis - Bone disease (406)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Osteoporosis%20Bone%20disease.txt)
* [Birth injuries or traumatic complications (238)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Birth%20injury%20or%20complication.txt)
* [Mother-to-child-transmissions (15)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Mother-to-child%20transmission.txt)

### Need more code lists?
Visit:
[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/hdruk%20small.png)](https://phenotypes.healthdatagateway.org/)

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

## Example

| Code | Coding  term  | Indicator 1 | Indicator 2 |  domain | severity | scale | reference | individual | coding system |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 912 | [D]Anorexia	Anorexia | Anorexia | Eating disorders | Maternal mental health problem | diagnostic |  |  | 2 | Read | 

## Suggested implementation of indicators


Whilst most indicators are ready to use by merging the correct code list with your data, some indicators requires rule-based algorithms as listed below. 

### 1-2. Merge code lists with the data file containing the target population
e.g. ensure correct ages for children/mothers

![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/merge%20codelist.png)

### 3.1 Convert continuous measures to binary indicators using the additional "cut-off" variable provided (i.e. data > cut_off)**

e.g. Example "one liner" in R or Python with dplyr:

 `e.g. mmhps_alcohol <- merged_data %>% filter(Domain=="mMHPs" & Indicator 1=="Alcohol misuse" & scale=="1" & data1 > cut_off)`

### 3.2 Apply more advanced [control flow methods](https://adv-r.hadley.nz/control-flow.html)

Apply multiple rule-based algorithims (age critera, accident exclusions etc) using control flow (data dependent "if then assumptions") are widley covered by the data science community ([1](https://adv-r.hadley.nz/control-flow.html) [2](https://advanced-r-solutions.rbind.io/control-flow.html)).

![alt text](![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/case%20when.jpg)

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/home%20view%20domains.png)](https://shabeer-syed.github.io/ACEs/domains) | [![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png)](https://shabeer-syed.github.io/ACEs/codelist)


[^structure]: See [**Structure** page]({{ "/docs/structure/" | relative_url }}) for a list of theme files and what they do.


**ProTip:** Be sure to remove `/docs` and `/test` if you forked Minimal Mistakes. These folders contain documentation and test pages for the theme and you probably don't want them littering up your repo.
{: .notice--info}


### Gem-based method

With Gem-based themes, directories such as the `assets`, `_layouts`, `_includes`, and `_sass` are stored in the theme’s gem, hidden from your immediate view. This allows for easier installation and updating as you don't have to manage any of the theme files. 

To install as a Gem-based theme:

1. Add the following to your `Gemfile`:

   ```ruby
   gem "minimal-mistakes-jekyll"
   ```

2. Fetch and update bundled gems by running the following [Bundler](https://bundler.io/) command:

   ```bash
   bundle
   ```

3. Set the `theme` in your project's Jekyll `_config.yml` file:

   ```yaml
   theme: minimal-mistakes-jekyll
   ```

To update the theme run `bundle update`.

### Remote theme method

Remote themes are similar to Gem-based themes, but do not require `Gemfile` changes or whitelisting making them ideal for sites hosted with GitHub Pages.

To install as a remote theme:

1. Create/replace the contents of your `Gemfile` with the following:

   ```ruby
   source "https://rubygems.org"

   gem "github-pages", group: :jekyll_plugins
   gem "jekyll-include-cache", group: :jekyll_plugins
   ```

2. Add `jekyll-include-cache` to the `plugins` array of your `_config.yml`.

3. Fetch and update bundled gems by running the following [Bundler](https://bundler.io/) command:

   ```bash
   bundle
   ```

4. Add `remote_theme: "mmistakes/minimal-mistakes@4.24.0"` to your `_config.yml` file. Remove any other `theme:` or `remote_theme:` entry.

You may also optionally specify a branch, [tag](https://github.com/mmistakes/minimal-mistakes/tags), or commit to use by appending an @ and the Git ref (e.g., `mmistakes/minimal-mistakes@4.9.0` or `mmistakes/minimal-mistakes@bbf3cbc5fd64a3e1885f3f99eb90ba92af84063d`). This is useful when rolling back to older versions of the theme. If you don't specify a Git ref, the latest on `master` will be used.

**Looking for an example?** Use the [Minimal Mistakes remote theme starter](https://github.com/mmistakes/mm-github-pages-starter/generate) for the quickest method of getting a GitHub Pages hosted site up and running. Generate a new repository from the starter, replace sample content with your own, and configure as needed.
{: .notice--info}

---

**Note:** Your Jekyll site should be viewable immediately at <http://USERNAME.github.io>. If it's not, you can force a rebuild by **Customizing Your Site** (see below for more details).
{: .notice--warning}

If you're hosting several Jekyll based sites under the same GitHub username you will have to use Project Pages instead of User Pages. Essentially you rename the repo to something other than **USERNAME.github.io** and create a `gh-pages` branch off of `master`. For more details on how to set things up check [GitHub's documentation](https://help.github.com/articles/user-organization-and-project-pages/).

<figure>
  <img src="{{ '/assets/images/mm-gh-pages.gif' | relative_url }}" alt="creating a new branch on GitHub">
</figure>

You can also install the theme by copying all of the theme files[^structure] into your project.

To do so fork the [Minimal Mistakes theme](https://github.com/mmistakes/minimal-mistakes/fork), then rename the repo to **USERNAME.github.io** --- replacing **USERNAME** with your GitHub username.

<figure>
  <img src="{{ '/assets/images/mm-theme-fork-repo.png' | relative_url }}" alt="fork Minimal Mistakes">
</figure>

**GitHub Pages Alternatives:** Looking to host your site for free and install/update the theme painlessly? [Netlify][netlify-jekyll], [GitLab Pages][gitlab-jekyll], and [Continuous Integration (CI) services][ci-jekyll] have you covered. In most cases all you need to do is connect your repository to them, create a simple configuration file, and install the theme following the [Ruby Gem Method](#ruby-gem-method) above.
{: .notice--info}

[netlify-jekyll]: https://www.netlify.com/blog/2015/10/28/a-step-by-step-guide-jekyll-3.0-on-netlify/
[gitlab-jekyll]: https://about.gitlab.com/2016/04/07/gitlab-pages-setup/
[ci-jekyll]: https://jekyllrb.com/docs/deployment/automated/#continuous-integration-service

### Remove the Unnecessary

If you forked or downloaded the `minimal-mistakes-jekyll` repo you can safely remove the following folders and files:

- `.editorconfig`
- `.gitattributes`
- `.github`
- `/docs`
- `/test`
- `CHANGELOG.md`
- `minimal-mistakes-jekyll.gemspec`
- `README.md`
- `screenshot-layouts.png`
- `screenshot.png`

**Note:** If forking the theme be sure to update `Gemfile` as well. The one found at the root of the project is for building the theme's Ruby gem and is missing dependencies. To properly setup a [`Gemfile`](https://github.com/mmistakes/minimal-mistakes/blob/master/docs/Gemfile) with the theme, consult the "[Install Dependencies](https://mmistakes.github.io/minimal-mistakes/docs/installation/#install-dependencies)" section.
{: .notice--warning}

## Setup Your Site

Depending on the path you took installing Minimal Mistakes you'll setup things a little differently.

**ProTip:** The source code and content files for this site can be found in the [`/docs` folder](https://github.com/mmistakes/minimal-mistakes/tree/master/docs) if you want to copy or learn from them.
{: .notice--info}

### Starting Fresh

Starting with an empty folder and `Gemfile` you'll need to copy or re-create this [default `_config.yml`](https://github.com/mmistakes/minimal-mistakes/blob/master/_config.yml) file. For a full explanation of every setting be sure to read the [**Configuration**]({{ "/docs/configuration/" | relative_url }}) section.

From `v4.5.0` onwards, Minimal Mistakes theme-gem comes bundled with the necessary data files for localization.
They will be picked up automatically if you have the [`jekyll-data`](https://github.com/ashmaroli/jekyll-data) plugin installed.
If you're hosting on GitHub Pages, you can copy the [`_data/ui-text.yml`][ui-text.yml] file into your repository for the localization feature to work.

You'll need to create and edit these data files to customize them:

- [`_data/ui-text.yml`][ui-text.yml] - UI text [documentation]({{ "/docs/ui-text/" | relative_url }})
- [`_data/navigation.yml`][navigation.yml] - navigation [documentation]({{ "/docs/navigation/" | relative_url }})

  [ui-text.yml]: https://github.com/mmistakes/minimal-mistakes/blob/master/_data/ui-text.yml
  [navigation.yml]: https://github.com/mmistakes/minimal-mistakes/blob/master/_data/navigation.yml

### Starting from `jekyll new`

Scaffolding out a site with the `jekyll new` command requires you to modify a few files that it creates.

Edit `_config.yml`. Then:

- Replace `<site root>/index.md` with a modified [Minimal Mistakes `index.html`](https://github.com/mmistakes/minimal-mistakes/blob/master/index.html). Be sure to enable pagination if using the [`home` layout]({{ "/docs/layouts/#home-page" | relative_url }}) by adding the necessary lines to **_config.yml**.
- Change `layout: post` in `_posts/0000-00-00-welcome-to-jekyll.markdown` to `layout: single`.
- Remove `about.md`, or at the very least change `layout: page` to `layout: single` and remove references to `icon-github.html` (or [copy to your `_includes`](https://github.com/jekyll/minima/tree/master/_includes) if using it).

### Migrating to Gem Version

If you're migrating a site already using Minimal Mistakes and haven't customized any of the theme files things upgrading will be easier for you.

Start by removing the following folders and any files within them: 

```terminal
├── _includes
├── _layouts
├── _sass
├── assets
|  ├── css
|  ├── fonts
|  └── js
```

You won't need these anymore as they're bundled with the theme gem --- unless you intend to [override them](https://jekyllrb.com/docs/themes/#overriding-theme-defaults).

**Note:** When clearing out the `assets` folder be sure to leave any files you've added and need. This includes images, CSS, or JavaScript that aren't already [bundled in the theme](https://github.com/mmistakes/minimal-mistakes/tree/master/assets). 
{: .notice--warning}

From `v4.5.0` onwards, the default language files are read-in automatically via the [`jekyll-data`](https://github.com/ashmaroli/jekyll-data) plugin if it's installed. For sites hosted with GitHub Pages, you still need to copy the [`_data/ui-text.yml`][ui-text.yml] file because the `jekyll-data` plugin [is unsupported on GitHub Pages](https://docs.github.com/en/github/working-with-github-pages/about-github-pages-and-jekyll#plugins).

If you customized any of these files leave them alone, and only remove the untouched ones. If done correctly your modified versions should [override](https://jekyllrb.com/docs/themes/#overriding-theme-defaults) the versions bundled with the theme and be used by Jekyll instead.

#### Update Gemfile

Replace `gem "github-pages` or `gem "jekyll"` with `gem "jekyll", "~> 3.5"`. You'll need the latest version of Jekyll[^update-jekyll] for Minimal Mistakes to work and load all of the theme's assets properly, this line forces Bundler to do that.

[^update-jekyll]: You could also run `bundle update jekyll` to update Jekyll.

Add the Minimal Mistakes theme gem: 

```ruby
gem "minimal-mistakes-jekyll"
```

When finished your `Gemfile` should look something like this:

```ruby
source "https://rubygems.org"

gem "jekyll", "~> 3.7"
gem "minimal-mistakes-jekyll"
```

Then run `bundle update` and add `theme: minimal-mistakes-jekyll` to your `_config.yml`.

**v4 Breaking Change:** Paths for image headers, overlays, teasers, [galleries]({{ "/docs/helpers/#gallery" | relative_url }}), and [feature rows]({{ "/docs/helpers/#feature-row" | relative_url }}) have changed and now require a full path. Instead of just `image: filename.jpg` you'll need to use the full path eg: `image: /assets/images/filename.jpg`. The preferred location is now `/assets/images/` but can be placed elsewhere or externally hosted. This applies to image references in `_config.yml` and `author.yml` as well.
{: .notice--danger}

---

That's it! If all goes well running `bundle exec jekyll serve` should spin-up your site.
