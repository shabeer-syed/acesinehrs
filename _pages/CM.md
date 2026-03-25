---
layout: splash
title: "Child maltreatment"
permalink: /CM/
author_profile: false
---
<!-- 1. Load Tailwind Safely -->
<script src="https://cdn.tailwindcss.com"></script>
<script>
  tailwind.config = {
    corePlugins: { preflight: false }
  }
</script>

<!-- 2. Load Fonts & Icons -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<!-- 3. The "Iron Shield" Overrides -->
<style>
  /* === FIX THE MENU & LOGO === */
  .masthead__inner-wrap .site-logo img { max-height: 24px !important; width: auto !important; }
  .masthead__menu-item a { font-family: 'Inter', sans-serif !important; font-size: 16px !important; font-weight: 500 !important; color: #6b7280 !important; }
  .masthead__menu-item a:hover { color: #111827 !important; }

  /* === BREAK OUT TO FULL SCREEN === */
  .full-bleed {
    width: 100vw; position: relative; left: 50%; right: 50%;
    margin-left: -50vw; margin-right: -50vw;
    background-color: #ffffff !important;
    margin-bottom: 0 !important; padding-bottom: 0 !important;
  }
  #main { padding-top: 0 !important; padding-bottom: 0 !important; margin-bottom: 0 !important; }

  /* === OVERRIDE JEKYLL FOOTER === */
  .page__footer {
    background-color: #0f172a !important; color: #94a3b8 !important;
    margin-top: 0 !important; padding: 3rem 0 !important; border-top: none !important;
  }
  .page__footer a { color: #cbd5e1 !important; text-decoration: none !important; }
  .page__footer a:hover { color: #ffffff !important; }
  .page__footer-copyright { color: #64748b !important; }

  /* === PROTECT TAILWIND FROM JEKYLL === */
  .tailwind-wrap { box-sizing: border-box; }
  .tailwind-wrap h1, .tailwind-wrap h2, .tailwind-wrap h3, .tailwind-wrap h4,
  .tailwind-wrap p, .tailwind-wrap a, .tailwind-wrap span, .tailwind-wrap div,
  .tailwind-wrap li, .tailwind-wrap ul, .tailwind-wrap td, .tailwind-wrap th {
    font-family: 'Inter', sans-serif !important;
  }
  
  /* Reset link styles BUT ignore custom components */
  .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.dl-card):not(.pub-link):not(.text-blue-600) {
    border-bottom: none !important; text-decoration: none !important; box-shadow: none !important;
  }

  /* === HERO TYPOGRAPHY === */
  .hero-title {
    font-size: 48px !important; line-height: 1.1 !important; font-weight: 700 !important;
    color: rgb(255, 255, 255) !important; margin-bottom: 24px !important; border: none !important;
  }
  .hero-subtitle {
    font-size: 20px !important; line-height: 1.6 !important; font-weight: 400 !important;
    color: rgb(241, 245, 249) !important; margin-bottom: 0 !important;
    max-width: 820px !important;
  }

  /* === PREMIUM CONTENT STYLES === */
  .content-heading {
    font-size: 28px !important; font-weight: 700 !important; color: #0f172a !important;
    margin-top: 0 !important; margin-bottom: 1.5rem !important; border: none !important; padding: 0 !important;
  }
  .content-subheading {
    font-size: 20px !important; font-weight: 600 !important; color: #1e293b !important;
    margin-bottom: 1rem !important; margin-top: 2rem !important; border: none !important;
  }
  
  /* FORCE all main content paragraphs to static 16px */
  .content-text {
    font-size: 16px !important; line-height: 1.75 !important; color: #475569 !important; margin-bottom: 1.25rem !important;
  }

  /* Notice Cards - FORCE static 15px max size */
  .notice-card {
    background-color: #ffffff !important; border-radius: 0.75rem !important; border: 1px solid #e2e8f0 !important;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; padding: 1.25rem 1.5rem !important;
    margin-bottom: 1.5rem !important; display: flex !important; align-items: flex-start !important; gap: 1rem !important;
  }
  .notice-info { border-left: 5px solid #3b82f6 !important; }
  
  /* Download Cards */
  .dl-card {
    display: flex !important; align-items: center !important; justify-content: space-between !important;
    background-color: #ffffff !important; border: 1px solid #e2e8f0 !important; border-radius: 0.75rem !important;
    padding: 1.25rem !important; transition: all 0.2s ease !important; text-decoration: none !important;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05) !important; margin-bottom: 1rem !important;
  }
  .dl-card:hover {
    border-color: #93c5fd !important; box-shadow: 0 10px 15px -3px rgba(0,0,0,0.05) !important; transform: translateY(-2px) !important;
  }
  .dl-title { font-size: 16px !important; font-weight: 600 !important; color: #0f172a !important; margin: 0 !important; transition: color 0.2s !important; }
  .dl-card:hover .dl-title { color: #2563eb !important; }
  .dl-meta { font-size: 13px !important; color: #64748b !important; margin-top: 0.25rem !important; }

  /* Tables */
  .custom-table-wrap { overflow-x: auto !important; margin-bottom: 2rem !important; border-radius: 0.75rem !important; border: 1px solid #e2e8f0 !important; box-shadow: 0 1px 3px rgba(0,0,0,0.05) !important; background-color: #ffffff !important; }
  .custom-table { width: 100% !important; border-collapse: collapse !important; text-align: left !important; }
  .custom-table th { background-color: #f8fafc !important; padding: 1rem !important; font-size: 13px !important; font-weight: 600 !important; color: #334155 !important; text-transform: uppercase !important; border-bottom: 1px solid #e2e8f0 !important; }
  .custom-table td { padding: 1rem !important; font-size: 14px !important; color: #475569 !important; border-bottom: 1px solid #e2e8f0 !important; vertical-align: middle !important; }
  .custom-table tr:last-child td { border-bottom: none !important; }

  /* Code Blocks */
  .code-container {
    background: #0d1117 !important; border-radius: 0.5rem !important; overflow: hidden !important;
  }
  .code-pre {
    padding: 1rem !important; overflow-x: auto !important; margin: 0 !important;
    font-family: 'Fira Code', monospace !important; font-size: 13px !important; line-height: 1.6 !important; color: #c9d1d9 !important;
  }
  .syntax-keyword { color: #ff7b72 !important; }
  .syntax-string { color: #a5d6ff !important; }

  /* PUBLICATION LIST */
  .pub-item {
    display: flex !important; flex-direction: column !important; gap: 0.5rem !important;
    padding: 1.25rem 0 !important; border-bottom: 1px solid #e2e8f0 !important;
  }
  .pub-item:last-child { border-bottom: none !important; }
  .pub-link {
    font-size: 15px !important; font-weight: 600 !important; color: #2563eb !important; line-height: 1.5 !important;
    text-decoration: none !important; transition: color 0.2s !important; border: none !important; display: block !important;
  }
  .pub-link:hover { color: #1d4ed8 !important; text-decoration: underline !important; text-underline-offset: 3px !important; }

  /* FLOURISH CONTAINER OVERRIDES */
  .flourish-container-wrap {
    background: #ffffff !important; border-radius: 1rem !important; border: 1px solid #e2e8f0 !important;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; padding: 1.5rem !important; overflow: hidden !important;
  }

  html { scroll-behavior: smooth; }
</style>

<!-- Load Altmetric Embed Script -->
<script type="text/javascript" src="https://d1bxh8uas1mnw7.cloudfront.net/assets/embed.js" async></script>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

  <!-- Hero Section -->
  <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/Child%20maltreatment%20aces%20in%20ehrs.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
    <div class="relative z-10 max-w-5xl mx-auto px-6 py-24 md:py-32 text-center md:text-left">
      <h1 class="hero-title drop-shadow-lg">
        Child <span style="color: #bfdbfe !important;">maltreatment</span>
      </h1>
      <p class="hero-subtitle drop-shadow-md mx-auto md:mx-0">
        This domain includes indicators of child maltreatment (CM). CM refers to any act of commission or omission by a parent or other caregiver that results in harm, potential for harm, or threat of harm to a child. Harm does not need to be intended.
      </p>
    </div>
  </header>

  <!-- Main Content Areas -->
  
  <!-- SECTION 1: DEFINITIONS -->
  <section class="bg-white py-16 border-b border-slate-200">
    <div class="max-w-4xl mx-auto px-6">
      <div class="flex items-center gap-3 mb-6">
        <div class="w-10 h-10 rounded-full bg-rose-50 text-rose-600 flex items-center justify-center shrink-0">
          <i class="fas fa-book-open text-lg"></i>
        </div>
        <h2 class="content-heading text-slate-900 !mb-0">Definition</h2>
      </div>

      <p class="content-text text-slate-700">
        Any recorded act of commission or omission by a parent or caregiver resulting in harm, the potential for harm or threat of child harm, including neglect, psychological, physical, sexual and emotional abuse. Harm does not need to be intended <sup><a href="https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(08)61706-7/fulltext" target="_blank" class="text-blue-600 hover:underline">1</a></sup>. 
      </p>
      
      <p class="content-text text-slate-700">
        In the UK, <a href="https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf" target="_blank" class="text-blue-600 hover:underline font-medium">statutory guidelines of CM</a> include child exposure to IPV, and maternal evidence for omission or commission during pregnancy such as Neonatal Abstinence Syndrome (NAS) and Fetal Alcohol Syndrome (FAS). It includes indicators such as neglect (pre- and post-birth), child protection recordings, or out-of-home placements by social care services (see <a href="https://acesinehrs.com/codelistbrowse/" class="text-blue-600 hover:underline">code list browser</a>).
      </p>

      <div class="notice-card notice-info mt-8 bg-blue-50/50">
        <div class="w-8 h-8 rounded-full bg-blue-100 flex items-center justify-center text-blue-600 shrink-0 mt-0.5">
          <i class="fas fa-search text-sm"></i>
        </div>
        <div>
          <h4 class="text-[16px] !important text-blue-900">Suspected CM</h4>
          <p class="text-[15px] !important text-slate-700">
            Suspected CM includes any maltreatment-related indicator with codes or measures describing presentations likely to refer to CM, but without mentioning the underlying cause (e.g., harm caused by non-specified person), safeguarding procedures, or child social service interventions. For instance, the "suspected CM, NOS" indicator contains codes mentioning <em>"Victim of sexual abuse"</em>, <em>"Multi-professional risk assessment done"</em>, and <em>"Assault in the home"</em>.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- SECTION 2: INDICATOR LIST & DOWNLOADS -->
  <section class="bg-slate-50 py-16 border-b border-slate-200 shadow-inner">
    <div class="max-w-5xl mx-auto px-6">
      
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
        
        <!-- Left Column: Downloads & Implementation -->
        <div class="lg:col-span-5 flex flex-col">
          
          <h3 class="content-subheading !mt-0">Code list download</h3>
          <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/CM_2025ACEsinEHRs.txt" target="_blank" class="dl-card border-l-4 border-l-rose-500 mb-4">
            <div>
              <h4 class="dl-title">Child maltreatment</h4>
              <p class="dl-meta">3,852 codes</p>
            </div>
            <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-rose-600 group-hover:bg-rose-50 transition-colors"><i class="fas fa-download"></i></div>
          </a>
          
          <a href="https://github.com/shabeer-syed/acesinehrs/raw/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v2.pdf" target="_blank" class="text-sm text-blue-600 hover:underline font-medium mb-10 flex items-center">
            <i class="fas fa-file-pdf text-slate-400 mr-2"></i> ACEsinEHRs control documentation
          </a>

          <h3 class="content-subheading !mt-0">Implementation Rules</h3>
          <p class="content-text text-sm text-slate-600 mb-4">Certain specific indicators within this domain require rule-based algorithms to prevent misclassification.</p>
          
          <div class="custom-table-wrap !mb-0">
            <table class="custom-table">
              <thead>
                <tr>
                  <th style="width: 30%;">Indicator</th>
                  <th>Rule / Algorithm</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td><strong class="text-slate-800">CM, FGM</strong></td>
                  <td class="text-[13px]">
                    <p class="mb-3">Apply codes mentioning circumcision to female children only (e.g. <em>"54314 - routine or ritual circumcision"</em>). Code list includes markers for rule inclusion.</p>
                    <div class="code-container">
                      <pre class="code-pre"><code>cm_fgm &lt;- merged_data %&gt;% 
  <span class="syntax-function">filter</span>(Domain==<span class="syntax-string">"CM"</span> & individual==<span class="syntax-string">"4"</span> & gender==<span class="syntax-string">"female"</span>)</code></pre>
                    </div>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>

        </div>

        <!-- Right Column: Flourish Embed -->
        <div class="lg:col-span-7">
          <h3 class="content-subheading !mt-0">Indicator list</h3>
          <div class="flourish-container-wrap">
            <div class="flourish-embed flourish-table" data-src="visualisation/9799589">
              <script src="https://public.flourish.studio/resources/embed.js"></script>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- SECTION 3: PUBLICATIONS -->
  <section class="bg-white py-16">
    <div class="max-w-4xl mx-auto px-6">
      <div class="flex items-center gap-3 mb-8 pb-4 border-b-2 border-slate-100">
        <div class="w-10 h-10 rounded-full bg-slate-100 text-slate-600 flex items-center justify-center shrink-0">
          <i class="fas fa-graduation-cap text-lg"></i>
        </div>
        <h2 class="content-heading !m-0 !border-none !pb-0 text-slate-800">Related Publications</h2>
      </div>

      <div class="space-y-1">
        <!-- Pub 1 -->
        <div class="pub-item">
          <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext" target="_blank" class="pub-link">
            Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England.
          </a>
          <p class="text-sm text-slate-500 m-0">Syed S, Gilbert R, Feder G, Howe LD, Powell C, Howarth E, Deighton J, Lacey RE. <em>The Lancet Public Health</em>. 2023.</p>
        </div>
        
        <!-- Pub 2 -->
        <div class="pub-item">
          <a href="https://www.thelancet.com/journals/landig/article/PIIS2589-7500(22)00061-9/fulltext" target="_blank" class="pub-link">
            Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study.
          </a>
          <p class="text-sm text-slate-500 m-0">Syed S, Gonzalez-Izquierdo A, Allister J, Feder G, Li L, Gilbert R. <em>The Lancet Digital Health</em>. 2022.</p>
        </div>

        <!-- Pub 3 -->
        <div class="pub-item">
          <a href="https://www.sciencedirect.com/science/article/pii/S0140673611610878" target="_blank" class="pub-link">
            Child maltreatment: variation in trends and policies in six developed countries.
          </a>
          <p class="text-sm text-slate-500 m-0">Gilbert R, Fluke J, O'Donnell M, et al. <em>The Lancet</em>. 2012. <a href="https://ars.els-cdn.com/content/image/1-s2.0-S0140673611610878-mmc1.pdf" target="_blank" class="text-blue-500 hover:underline">View Code List</a></p>
        </div>

        <!-- Pub 4 -->
        <div class="pub-item">
          <a href="https://link.springer.com/article/10.1186/1472-6963-12-65" target="_blank" class="pub-link">
            Health service use in families where children enter public care: a nested case control study using the General Practice Research Database.
          </a>
          <p class="text-sm text-slate-500 m-0">Simkiss DE, Spencer NJ, Stallard N, Thorogood M. <em>BMC Health Services Research</em>. 2012.</p>
        </div>

        <!-- Pub 5 -->
        <div class="pub-item border-none">
          <a href="https://elearning.rcgp.org.uk/mod/book/view.php?id=12531" target="_blank" class="pub-link">
            Child safeguarding toolkit.
          </a>
          <p class="text-sm text-slate-500 m-0">Royal College of General Practitioners.</p>
        </div>
      </div>
      
      <div class="mt-10 pt-8 border-t border-slate-200 text-center">
        <a href="https://acesinehrs.com/ACE-domains/" class="inline-flex items-center text-slate-500 hover:text-blue-600 font-medium transition-colors text-[16px] !important bg-slate-50 hover:bg-blue-50 px-5 py-2.5 rounded-lg border border-slate-200">
          <i class="fas fa-arrow-left mr-2"></i> All ACE Domains
        </a>
      </div>

    </div>
  </section>

  <!-- Hidden Author Tag for SEO Indexing -->
  <span class="hidden">Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate</span>

  <!-- Logos Banner (Footer Equivalent) -->
  <section class="bg-slate-50 border-t border-slate-200 py-10 shadow-inner mt-auto">
    <div class="max-w-7xl mx-auto px-6 flex flex-wrap justify-center items-center gap-8 opacity-70 grayscale hover:grayscale-0 transition duration-500">
      <a href="https://www.ucl.ac.uk/children-policy-research/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/NIHR%20CPRU%20logo%20aces%20in%20ehrs%20footer.png" alt="NIHR CPRU" class="h-8 md:h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/ucl%20ich%20logo%20aces%20in%20ehrs.png" alt="UCL ICH" class="h-8 md:h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.ox.ac.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/university%20of%20oxford%20logo%20aces%20in%20ehrs.png" alt="Oxford" class="h-8 md:h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/NIHR%20Great%20ormond%20street%20hospital%20biomedical%20research%20centre%20logo%20aces%20in%20ehrs.png" alt="NIHR GOSH BRC" class="h-8 md:h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.gosh.nhs.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/GOSH%20logo%20aces%20in%20ehrs.png" alt="GOSH" class="h-8 md:h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.bristol.ac.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/University%20of%20bristol%20logo%20aces%20in%20ehrs.png" alt="Bristol" class="h-8 md:h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.hdruk.ac.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/hdruk%20logo%20aces%20in%20ehrs.png" alt="HDRUK" class="h-8 md:h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.ucl.ac.uk/health-informatics/research/caliber" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/caliber%20ucl%20logo%20aces%20in%20ehrs.png" alt="Caliber UCL" class="h-8 md:h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
    </div>
  </section>

</div>
