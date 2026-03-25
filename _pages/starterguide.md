---
layout: splash
permalink: /starterguide/
title: "Getting started"
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
  .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.dl-card):not(.step-link):not(.grid-card):not(.text-blue-600) {
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
    max-width: 820px !important; margin-left: auto !important; margin-right: auto !important;
  }

  /* === PREMIUM CONTENT STYLES === */
  .content-section {
    scroll-margin-top: 180px !important; /* CSS Fallback: Prevents external anchor links from hiding under nav */
  }
  .content-heading {
    font-size: 30px !important; font-weight: 700 !important; color: #0f172a !important;
    margin-top: 0 !important; margin-bottom: 1.5rem !important; border: none !important; padding: 0 !important;
  }
  .content-subheading {
    font-size: 20px !important; font-weight: 600 !important; color: #1e293b !important;
    margin-bottom: 1rem !important; margin-top: 2rem !important; border: none !important;
  }
  
  /* FORCE all main content paragraphs to static 16px */
  .tailwind-wrap p.content-text, 
  .tailwind-wrap .page__content p {
    font-size: 16px !important; line-height: 1.75 !important; color: #475569 !important; margin-bottom: 1.25rem !important;
  }

  /* Notice Cards - FORCE static 15px max size */
  .notice-card {
    background-color: #ffffff !important; border-radius: 0.75rem !important; border: 1px solid #e2e8f0 !important;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; padding: 1.25rem 1.5rem !important;
    margin-bottom: 1.5rem !important; display: flex !important; align-items: flex-start !important; gap: 1rem !important;
  }
  .notice-danger { border-left: 5px solid #f97316 !important; }
  .notice-info { border-left: 5px solid #3b82f6 !important; }
  
  .tailwind-wrap .notice-card h4 { 
    font-size: 16px !important; font-weight: 700 !important; color: #0f172a !important; margin: 0 0 0.25rem 0 !important; border: none !important; 
  }
  .tailwind-wrap .notice-card p, 
  .tailwind-wrap .notice-card a, 
  .tailwind-wrap .notice-card span { 
    font-size: 15px !important; line-height: 1.6 !important; color: #475569 !important; margin: 0 !important; 
  }

  /* Custom Lists - FORCE static 16px */
  .custom-list { list-style: none !important; padding: 0 !important; margin: 0 0 1.5rem 0 !important; }
  .custom-list li {
    position: relative !important; padding-left: 2rem !important; margin-bottom: 1rem !important;
    font-size: 16px !important; line-height: 1.6 !important; color: #475569 !important;
  }
  .custom-list li i {
    position: absolute !important; left: 0 !important; top: 0.25rem !important; color: #3b82f6 !important; font-size: 1.1rem !important;
  }

  /* BMJ-Style Stepper Container */
  .stepper-scroll-container {
    width: 100%; overflow-x: auto; padding-bottom: 0.5rem; scrollbar-width: thin;
  }
  .stepper-container {
    display: flex; justify-content: space-between; position: relative; min-width: 900px; padding: 0 2rem;
  }
  .stepper-line {
    position: absolute; top: 24px; left: 8%; right: 8%; height: 3px; background-color: #cbd5e1; z-index: 0;
  }
  .step-link {
    display: flex !important; flex-direction: column !important; align-items: center !important; text-align: center !important;
    width: 16% !important; z-index: 10 !important; text-decoration: none !important; group;
  }
  .step-circle {
    width: 48px !important; height: 48px !important; border-radius: 50% !important; background-color: #ffffff !important;
    border: 3px solid #cbd5e1 !important; display: flex !important; justify-content: center !important; align-items: center !important;
    color: #64748b !important; font-size: 1.1rem !important; transition: all 0.3s ease !important; margin-bottom: 0.75rem !important;
    box-shadow: 0 4px 6px -1px rgba(0,0,0,0.05) !important;
  }
  .step-link:hover .step-circle, .step-link.active .step-circle {
    border-color: #2563eb !important; background-color: #2563eb !important; color: #ffffff !important; transform: translateY(-3px) !important; box-shadow: 0 10px 15px -3px rgba(37,99,235,0.3) !important;
  }
  .step-title {
    font-size: 13px !important; font-weight: 600 !important; color: #334155 !important; line-height: 1.3 !important; margin: 0 !important; transition: color 0.3s !important;
  }
  .step-link:hover .step-title, .step-link.active .step-title { color: #2563eb !important; }

  /* Code Blocks */
  .code-container {
    background: #0d1117 !important; border-radius: 0.75rem !important; overflow: hidden !important;
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1) !important; margin-bottom: 1.5rem !important;
  }
  .code-header {
    background: #161b22 !important; padding: 0.5rem 1rem !important; border-bottom: 1px solid #30363d !important;
    display: flex !important; align-items: center !important; gap: 0.5rem !important;
  }
  .code-window-dot { width: 12px !important; height: 12px !important; border-radius: 50% !important; }
  .code-pre {
    padding: 1rem 1.25rem !important; overflow-x: auto !important; margin: 0 !important;
    font-family: 'Fira Code', monospace !important; font-size: 14px !important; line-height: 1.6 !important; color: #c9d1d9 !important;
  }
  .syntax-keyword { color: #ff7b72 !important; }
  .syntax-string { color: #a5d6ff !important; }
  .syntax-comment { color: #8b949e !important; font-style: italic !important; }
  .syntax-function { color: #d2a8ff !important; }

  /* Tables */
  .custom-table-wrap { overflow-x: auto !important; margin-bottom: 2rem !important; border-radius: 0.75rem !important; border: 1px solid #e2e8f0 !important; box-shadow: 0 1px 3px rgba(0,0,0,0.05) !important; background-color: #ffffff !important; }
  .custom-table { width: 100% !important; border-collapse: collapse !important; text-align: left !important; }
  .custom-table th { background-color: #f8fafc !important; padding: 1rem !important; font-size: 13px !important; font-weight: 600 !important; color: #334155 !important; text-transform: uppercase !important; border-bottom: 1px solid #e2e8f0 !important; }
  .custom-table td { padding: 1rem !important; font-size: 14px !important; color: #475569 !important; border-bottom: 1px solid #e2e8f0 !important; vertical-align: top !important; }
  .custom-table tr:last-child td { border-bottom: none !important; }
  .custom-table tr:hover { background-color: #f8fafc !important; }

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
  
  /* Modern Bottom Grid Cards */
  .grid-card {
    background-color: #ffffff !important; border-radius: 1.25rem !important; border: 1px solid #e2e8f0 !important;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1) !important;
    text-decoration: none !important; display: flex !important; flex-direction: column !important; overflow: hidden !important;
  }
  .grid-card:hover {
    transform: translateY(-6px) !important; box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1) !important; border-color: #cbd5e1 !important;
  }
  .grid-card .img-wrapper {
    background-color: #ffffff !important; padding: 2.5rem 2rem 1.5rem 2rem !important; display: flex !important; justify-content: center !important; align-items: center !important;
  }
  .grid-card img {
    transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1) !important; width: auto !important; height: 120px !important; object-fit: contain !important; margin: 0 auto !important;
  }
  .grid-card:hover img { transform: scale(1.06) !important; }
  .grid-card .content-wrapper {
    padding: 1.5rem !important; flex-grow: 1 !important; background-color: #f8fafc !important; text-align: center !important; border-top: 1px solid #f1f5f9 !important;
  }
  .grid-card .card-title {
    font-size: 19px !important; font-weight: 700 !important; color: #0f172a !important; margin: 0 0 10px 0 !important; border: none !important; transition: color 0.3s ease !important;
  }
  .grid-card:hover .card-title { color: #2563eb !important; }

  html { scroll-behavior: smooth; }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

  <!-- Hero Section -->
  <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20getting%20started%20page.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
    <div class="relative z-10 max-w-5xl mx-auto px-6 py-20 md:py-28 text-center md:text-left">
      <h1 class="hero-title drop-shadow-lg">
        Getting <span style="color: #bfdbfe !important;">started</span>
      </h1>
      <p class="hero-subtitle drop-shadow-md max-w-3xl">
        A quick introduction to incorporating validated indicators, code lists and scripts for measuring intervenable and clinically relevant ACEs using EHRs.
      </p>
      <div class="mt-8 p-5 bg-slate-900 bg-opacity-60 border-l-4 border-blue-400 rounded-r-xl max-w-3xl inline-block backdrop-blur-sm shadow-xl text-left">
        <p class="text-[15px] md:text-base text-blue-50 leading-relaxed m-0 font-medium">
          We are passionate about using EHRs to advance healthcare, social justice, and policy for families affected by adversity. However, ACEs in EHRs are not easily accessible and can be challenging to implement without guidance.
        </p>
      </div>
    </div>
  </header>

  <!-- BMJ-Style Horizontal Navigation Stepper (STICKY) -->
  <section class="sticky top-0 z-50 bg-white/95 backdrop-blur-md py-6 border-b border-slate-200 shadow-sm transition-all duration-300">
    <div class="max-w-5xl mx-auto px-6">
      <div class="stepper-scroll-container">
        <div class="stepper-container">
          <div class="stepper-line"></div>
          
          <a href="#prerequisites" class="step-link group nav-item">
            <div class="step-circle"><i class="fas fa-clipboard-check"></i></div>
            <p class="step-title">1. Prerequisites<br>& Governance</p>
          </a>
          
          <a href="#framework" class="step-link group nav-item">
            <div class="step-circle"><i class="fas fa-sitemap"></i></div>
            <p class="step-title">2. The ACE<br>Framework</p>
          </a>
          
          <a href="#code-lists" class="step-link group nav-item">
            <div class="step-circle"><i class="fas fa-list-ul"></i></div>
            <p class="step-title">3. Working with<br>Code Lists</p>
          </a>
          
          <a href="#data-pipeline" class="step-link group nav-item">
            <div class="step-circle"><i class="fas fa-database"></i></div>
            <p class="step-title">4. The Data<br>Pipeline</p>
          </a>
          
          <a href="#algorithms" class="step-link group nav-item">
            <div class="step-circle"><i class="fas fa-laptop-code"></i></div>
            <p class="step-title">5. Applying<br>Algorithms</p>
          </a>
          
          <a href="#downloads" class="step-link group nav-item">
            <div class="step-circle"><i class="fas fa-download"></i></div>
            <p class="step-title">6. Downloads<br>& Resources</p>
          </a>
          
        </div>
      </div>
    </div>
  </section>

  <!-- Main Content Areas (Alternating Backgrounds) -->
  
  <!-- SECTION 1: PREREQUISITES & GOVERNANCE -->
  <section id="prerequisites" class="content-section bg-slate-50 py-16 md:py-20 border-b border-slate-200">
    <div class="max-w-4xl mx-auto px-6">
      
      <!-- Reverted White Info Callout -->
      <div class="notice-card notice-info mb-10">
        <div class="w-8 h-8 rounded-full bg-blue-100 flex items-center justify-center text-blue-600 shrink-0 mt-0.5">
          <i class="fas fa-info text-sm"></i>
        </div>
        <div>
          <p class="text-[15px] !important font-medium text-slate-800 m-0">This page provides a guide to get you started incorporating validated indicators to identify ACEs in EHRs.</p>
        </div>
      </div>

      <h2 class="content-heading text-blue-900">1. Prerequisites & Governance</h2>
      <p class="content-text font-medium text-slate-800">Everything the researcher needs before touching the data. To use the ACE indicators, you will need:</p>
      
      <ul class="custom-list">
        <li>
          <i class="fas fa-database"></i>
          <strong>Data Access: Securing authorised EHR data.</strong> Obtain authorised and de-identified data of children and parents for research purposes. Most ACEs are captured in primary care. Several data sources in the UK provide linked primary care data of children and parents, including the <a href="https://cprd.com/" target="_blank" class="text-blue-600 hover:underline">Clinical Practice Research Datalink (CPRD)</a>, <a href="https://www.the-health-improvement-network.com/" target="_blank" class="text-blue-600 hover:underline">The Health Improvement Network (THIN)</a>, and <a href="https://www.qresearch.org/" target="_blank" class="text-blue-600 hover:underline">QResearch</a>. Access to CPRD requires <a href="https://cprd.com/research-applications" target="_blank" class="text-blue-600 hover:underline">protocol approval</a>. Please visit the <a href="https://www.healthdatagateway.org" target="_blank" class="text-blue-600 hover:underline">Health Data Research Innovation Gateway</a> for more information.
          <br><br>
          <em>OR: Access locally stored EHR data:</em> Many NHS trusts provide streamlined processes to access local data sources like the Clinical Record Interactive Search (<a href="https://slam.nhs.uk/clinical-record-interactive-search" target="_blank" class="text-blue-600 hover:underline">1</a>, <a href="https://www.oxfordhealth.nhs.uk/research/toolkit/cris/" target="_blank" class="text-blue-600 hover:underline">2</a>, <a href="https://www.southernhealth.nhs.uk/about-us/research/research-and-innovation/clinical-record-interactive-search" target="_blank" class="text-blue-600 hover:underline">3</a>). These often have a data structure consistent with national data sources like HES-APC.
        </li>
        <li>
          <i class="fas fa-shield-alt"></i>
          <strong>Secure Data Environments (SDE):</strong> Ensure that your work is conducted within a secure data environment approved for working with EHRs to protect privacy and meet compliance standards.
        </li>
        <li>
          <i class="fas fa-link"></i>
          <strong>Data Linkage:</strong> Implement robust linkage of child and parent records. Providers like CPRD allow you to access established mother-child linkages. For other linkage methods, please see existing methodologies (<a href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0164667" target="_blank" class="text-blue-600 hover:underline">1</a>, <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext" target="_blank" class="text-blue-600 hover:underline">2</a>, <a href="https://onlinelibrary.wiley.com/doi/full/10.1002/pds.4811" target="_blank" class="text-blue-600 hover:underline">3</a>). For paternal linkage, see methods described <a href="https://www.thelancet.com/cms/10.1016/S2468-2667(23)00119-6/attachment/9c50602c-ebd2-445f-ae3b-de30e2a1db14/mmc1.pdf" target="_blank" class="text-blue-600 font-medium hover:underline">here</a>.
        </li>
      </ul>
    </div>
  </section>

  <!-- SECTION 2: THE ACE FRAMEWORK -->
  <section id="framework" class="content-section bg-white py-16 md:py-20 border-b border-slate-200">
    <div class="max-w-4xl mx-auto px-6">
      <h2 class="content-heading text-blue-900">2. The ACE Framework</h2>
      <p class="content-text font-medium text-slate-800">Understanding the methodology underpinning the variables.</p>
      
      <h3 class="content-subheading">Domains & Indicators</h3>
      <p class="content-text">We developed two measures of ACEs for electronic health records (EHRs):</p>
      <ul class="custom-list mb-6">
        <li><i class="fas fa-layer-group"></i> <strong>Domains:</strong> Grouped, high-level indicators.</li>
        <li><i class="fas fa-sitemap"></i> <strong>Indicators:</strong> Specific grouped codes or measures.</li>
      </ul>
      
      <div class="bg-slate-50 p-6 rounded-xl border border-slate-200 mb-8 font-mono text-sm text-slate-700 shadow-sm">
        <div class="flex flex-col space-y-3">
          <div class="flex items-center font-semibold text-slate-800"><i class="fas fa-level-down-alt rotate-[-90deg] text-slate-400 mr-2"></i> Indicator 2</div>
          <div class="flex items-center ml-6 text-slate-600"><i class="fas fa-level-down-alt rotate-[-90deg] text-slate-400 mr-2"></i> Indicator 1</div>
          <div class="flex items-center ml-12 text-slate-500"><i class="fas fa-level-down-alt rotate-[-90deg] text-slate-400 mr-2"></i> Most specific indicator</div>
          <div class="flex items-center ml-18 text-blue-600 font-medium bg-blue-50 px-2 py-1 rounded inline-block w-max"><i class="fas fa-level-down-alt rotate-[-90deg] text-blue-400 mr-2"></i> Code (alphanumerical code attached to event)</div>
        </div>
      </div>

      <!-- Info Notice -->
      <div class="notice-card notice-info">
        <div class="w-8 h-8 rounded-full bg-blue-100 flex items-center justify-center text-blue-600 shrink-0 mt-0.5">
          <i class="fas fa-users text-sm"></i>
        </div>
        <div>
          <h4>The "Think-Family" Approach</h4>
          <p>Unless specified, indicators refer to information recorded in the child's, the mother's and the father's records. Properly studying ACEs requires a "think-family" approach. We recognise that the health and well-being of children are intricately tied to their parents' experiences and health outcomes.</p>
        </div>
      </div>

      <!-- Danger Notice -->
      <div class="notice-card notice-danger">
        <div class="w-8 h-8 rounded-full bg-orange-100 flex items-center justify-center text-orange-600 shrink-0 mt-0.5">
          <i class="fas fa-exclamation-circle text-sm"></i>
        </div>
        <div>
          <h4>Sample Size Guidelines</h4>
          <p>The ability to use specific indicators depends on your sample size. We recommend restricting the disaggregation of specific indicators to those present in 250 or more unique children. For many studies, it will be most appropriate to use the six broad ACE domains only.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- SECTION 3: WORKING WITH CODE LISTS -->
  <section id="code-lists" class="content-section bg-slate-50 py-16 md:py-20 border-b border-slate-200">
    <div class="max-w-4xl mx-auto px-6">
      <h2 class="content-heading text-blue-900">3. Working with Code Lists</h2>
      <p class="content-text font-medium text-slate-800">The translation layer between the framework and the raw data.</p>
      <p class="content-text">
        The ACE indicators are mapped onto codes stored in <a href="https://acesinehrs.com/domains/" class="text-blue-600 hover:underline">code lists</a>. The current ACEs indicators include ICD-9/10 codes (hospital/death records), Read codes, SNOMED-CT codes, medcodes, prodcodes, gemscripts, and specific field codes for HES datasets.
      </p>

      <h3 class="content-subheading">Code List Dictionary</h3>
      <div class="custom-table-wrap">
        <table class="custom-table">
          <thead>
            <tr>
              <th style="width: 25%;">Variable</th>
              <th>Explanation</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><strong>Code</strong></td>
              <td>Data ready code. Contains added prefixes to prevent de-duplication across different systems.</td>
            </tr>
            <tr>
              <td><strong>Code original</strong></td>
              <td>Original code exactly as entered into the respective system.</td>
            </tr>
            <tr>
              <td><strong>Indicator code</strong></td>
              <td>Name of the specific indicator the code maps to.</td>
            </tr>
            <tr>
              <td><strong>Severity</strong></td>
              <td>Severity classification of the code description (e.g. for alcohol misuse: <em>`mild`, `moderate`, `severe`</em>).</td>
            </tr>
            <tr>
              <td><strong>Scale</strong></td>
              <td><code>1</code> = Code/severity are dependent on extra clinical information (helper functions required).</td>
            </tr>
            <tr>
              <td><strong>Reference</strong></td>
              <td><code>1</code> = part of family violence reference standard, <code>2</code> = broader measure.</td>
            </tr>
            <tr>
              <td><strong>Individual</strong></td>
              <td><code>1</code> = child only, <code>2</code> = mother only, <code>3</code> = mother or child, <code>4</code> = female children only.</td>
            </tr>
          </tbody>
        </table>
      </div>

      <h3 class="content-subheading">Prefix Conversion Table</h3>
      <p class="content-text">
        A substantial proportion of codes share the same alphanumeric sequence (e.g., "11246" is a medication in prodcode, but a diagnosis in medcode). To prevent accidental deduplication, we added prefixes to the master lists. You will need to convert your raw data codes to match:
      </p>
      <div class="custom-table-wrap mb-0">
        <table class="custom-table">
          <thead>
            <tr>
              <th>Data source & Coding system</th>
              <th>Prefix</th>
              <th>Example</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>CPRD GOLD: Prodcode</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">d_</code></td>
              <td class="font-mono text-sm text-slate-500">d_727 - Sertraline</td>
            </tr>
            <tr>
              <td>ONS Mortality ≤2000 & HES-APC ≤1998</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">e_</code></td>
              <td class="font-mono text-sm text-slate-500">e_5713 - Alcoholic liver damage</td>
            </tr>
            <tr>
              <td>HES-APC: OPCS-4</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">p_</code></td>
              <td class="font-mono text-sm text-slate-500">p_X66 - CBT Therapy</td>
            </tr>
            <tr>
              <td>HES-A&E: Specific diagnosis system</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">aed_</code></td>
              <td class="font-mono text-sm text-slate-500">aed_144 - Poisoning</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <!-- SECTION 4: THE DATA PIPELINE -->
  <section id="data-pipeline" class="content-section bg-white py-16 md:py-20 border-b border-slate-200">
    <div class="max-w-4xl mx-auto px-6">
      <h2 class="content-heading text-blue-900">4. The Data Pipeline (Preparation)</h2>
      <p class="content-text font-medium text-slate-800">Getting the messy raw data ready for analysis.</p>

      <ul class="custom-list">
        <li><i class="fas fa-wrench"></i> <strong>Extraction & Restructuring:</strong> Extract your raw files via SQL. Restructure all files and variables into a consistent "long format". Drop irrelevant data fields to reduce memory weight.</li>
        <li><i class="fas fa-broom"></i> <strong>Cleaning & Standardization:</strong> Remove white space/punctuation from codes and standardize date formats.</li>
      </ul>

      <p class="text-sm font-medium text-slate-700 mb-2 mt-4">Example: Cleaning codes and standardizing dates (R)</p>
      <div class="code-container">
        <div class="code-header">
          <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
        </div>
        <pre class="code-pre"><code>aces_data$medcode &lt;- <span class="syntax-function">gsub</span>(<span class="syntax-string">"\\s+"</span>,<span class="syntax-string">""</span>,aces_data$medcode) <span class="syntax-comment"># remove space</span>
aces_data$medcode &lt;- <span class="syntax-function">gsub</span>(<span class="syntax-string">"\\."</span>,<span class="syntax-string">""</span>,aces_data$medcode) <span class="syntax-comment"># remove punctuation</span>

aces_data &lt;- aces_data %&gt;% <span class="syntax-function">mutate_all</span>(as.character) %&gt;% 
 <span class="syntax-function">separate</span>(date_var,<span class="syntax-function">c</span>(<span class="syntax-string">"day"</span>,<span class="syntax-string">"month"</span>,<span class="syntax-string">"year"</span>),sep=<span class="syntax-string">"-"</span>) %&gt;% 
 <span class="syntax-function">unite</span>(new_date,<span class="syntax-function">c</span>(<span class="syntax-string">"year"</span>,<span class="syntax-string">"month"</span>,<span class="syntax-string">"day"</span>),sep=<span class="syntax-string">"-"</span>)</code></pre>
      </div>

      <p class="content-text mt-8">
        <strong>Creating the Master File (Streaming Approach):</strong> We recommend a streaming approach to bind patient data into one manageable file. This iterates over patient IDs in chunks rather than crashing your memory.
      </p>

      <div class="code-container mb-0">
        <div class="code-header">
          <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
        </div>
        <pre class="code-pre"><code><span class="syntax-comment"># Stream through EHR files and save relevant patient data</span>
<span class="syntax-keyword">for</span> (ehr_file <span class="syntax-keyword">in</span> <span class="syntax-function">list.files</span>(pattern = <span class="syntax-string">"*.txt"</span>)) {
  output_file &lt;- <span class="syntax-function">paste0</span>(<span class="syntax-string">"output_"</span>, ehr_file)

  <span class="syntax-comment"># Create empty file & write column names</span>
  <span class="syntax-function">fwrite</span>(<span class="syntax-function">data.frame</span>(), output_file)
  <span class="syntax-function">fwrite</span>(<span class="syntax-function">names</span>(data.table::<span class="syntax-function">fread</span>(ehr_file, nrows = 0, header = T)), output_file, append = T)
  
  <span class="syntax-comment"># Read in chunks, filter against cohort list</span>
  ehr_stream &lt;- data.table::<span class="syntax-function">fread</span>(ehr_file, header = T, colClasses=<span class="syntax-string">"character"</span>, nThread=8)
  relevant_data &lt;- ehr_stream %&gt;% <span class="syntax-function">filter</span>(patient_id %fin% patient_id_list$patient_id)
  
  <span class="syntax-function">fwrite</span>(relevant_data, output_file, append = T)
}</code></pre>
      </div>
    </div>
  </section>

  <!-- SECTION 5: APPLYING ALGORITHMS -->
  <section id="algorithms" class="content-section bg-slate-50 py-16 md:py-20 border-b border-slate-200">
    <div class="max-w-4xl mx-auto px-6">
      <h2 class="content-heading text-blue-900">5. Applying Algorithms</h2>
      <p class="content-text font-medium text-slate-800">Refining the data to ensure accuracy.</p>
      
      <!-- Danger Notice -->
      <div class="notice-card notice-danger">
        <div class="w-8 h-8 rounded-full bg-orange-100 flex items-center justify-center text-orange-600 shrink-0 mt-0.5">
          <i class="fas fa-clock text-sm"></i>
        </div>
        <div>
          <h4>Time Restrictions</h4>
          <p>The validated ACE indicators are time sensitive and generally apply anytime between 2 years before birth and 10 years after birth. However, most child maltreatment algorithms are strictly limited to 2 years before birth up to 5 years after birth. Ascertaining correct exposure times is essential.</p>
        </div>
      </div>

      <p class="content-text">
        <strong>Helper Functions & Rule-Based Criteria:</strong> Some codes require extra clinical information or co-occurrence rules. Use control flow logic to define these parameters.
      </p>

      <p class="text-sm font-medium text-slate-700 mb-2 mt-4">Example: Depression requiring symptom/medication AND a diagnosis within 2 years</p>
      <div class="code-container mb-0">
        <div class="code-header">
          <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
        </div>
        <pre class="code-pre"><code>depression_cases &lt;- ehr_data %&gt;%
  <span class="syntax-function">filter</span>(
    <span class="syntax-comment"># Has symptoms or medications</span>
    <span class="syntax-function">any_of</span>(depression_symptoms) | <span class="syntax-function">any_of</span>(depression_medications),
    
    <span class="syntax-comment"># AND co-occurs with a previous code within 2 years (365*2 days)</span>
    <span class="syntax-function">any_of</span>(previous_codes) & visit_date &gt;= (<span class="syntax-function">Sys.Date</span>() - 365 * 2)
  )</code></pre>
      </div>
    </div>
  </section>

  <!-- SECTION 6: DOWNLOADS -->
  <section id="downloads" class="content-section bg-white py-16 md:py-20 border-b border-slate-200">
    <div class="max-w-4xl mx-auto px-6">
      <h2 class="content-heading text-blue-900">6. Downloads & Resources</h2>
      <p class="content-text font-medium text-slate-800">The actual files researchers need to execute the work.</p>
      
      <p class="content-text mt-4">
        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v3.pdf" target="_blank" class="text-blue-600 hover:underline font-semibold">
          <i class="fas fa-file-pdf text-rose-500 mr-2"></i> ACEsinEHRs control documentation & release information
        </a>
      </p>

      <!-- Danger Notice -->
      <div class="notice-card notice-danger mt-6">
        <div class="w-8 h-8 rounded-full bg-orange-100 flex items-center justify-center text-orange-600 shrink-0 mt-0.5">
          <i class="fas fa-code-branch text-sm"></i>
        </div>
        <div>
          <h4>Implementation Note</h4>
          <p>
            The indicators use <a href="https://advanced-r-solutions.rbind.io/control-flow.html" target="_blank" class="text-blue-600 hover:underline">control flow methods</a> to implement rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions, traumatic birth injuries or maternal-child transmissions.
          </p>
        </div>
      </div>

      <h3 class="text-xl font-bold text-slate-800 mt-10 mb-4 border-none">Master Code Lists</h3>
      <p class="text-sm text-slate-500 mb-4">Right-click on link to save as a ".txt" file.</p>

      <div class="grid grid-cols-1 gap-4 mb-10">
        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025ACEsinEHRs.txt" target="_blank" class="dl-card border-l-4 border-l-blue-500">
          <div>
            <h4 class="dl-title">All ACEs Complete Bundle</h4>
            <p class="dl-meta">Total included codes: 23,164</p>
          </div>
          <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-blue-600 group-hover:bg-blue-50 transition-colors"><i class="fas fa-download"></i></div>
        </a>
        
        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025_medcode_prodcode_CPRD_GOLD_Aurum_ACEsinEHRs.txt" target="_blank" class="dl-card border-l-4 border-l-emerald-500">
          <div>
            <h4 class="dl-title">Primary Care GP Bundle (CPRD / AURUM)</h4>
            <p class="dl-meta">medcodes, prodcodes, measures only (20,925 codes)</p>
          </div>
          <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-emerald-600 group-hover:bg-emerald-50 transition-colors"><i class="fas fa-download"></i></div>
        </a>

        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025_ICD910_special_fields_HES_ACEsinEHRs.txt" target="_blank" class="dl-card border-l-4 border-l-purple-500">
          <div>
            <h4 class="dl-title">Hospital Records Bundle</h4>
            <p class="dl-meta">ICD, OPCS and HES-APC specific fields (2,239 codes)</p>
          </div>
          <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-purple-600 group-hover:bg-purple-50 transition-colors"><i class="fas fa-download"></i></div>
        </a>
      </div>

      <h3 class="text-xl font-bold text-slate-800 mt-10 mb-6 border-none">Domain-Specific Lists</h3>
      <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mb-10">
        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/CM_2025ACEsinEHRs.txt" target="_blank" class="dl-card">
          <div>
            <h4 class="dl-title">Child maltreatment</h4>
            <p class="dl-meta">3,852 codes</p>
          </div>
          <i class="fas fa-download text-slate-400"></i>
        </a>

        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/IPV_2025ACEsinEHRs.txt" target="_blank" class="dl-card">
          <div>
            <h4 class="dl-title">Intimate partner violence</h4>
            <p class="dl-meta">3,281 codes</p>
          </div>
          <i class="fas fa-download text-slate-400"></i>
        </a>

        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/HRPCM_2025ACEsinEHRs.txt" target="_blank" class="dl-card">
          <div>
            <h4 class="dl-title">High-risk presentation of CM</h4>
            <p class="dl-meta">1,774 codes</p>
          </div>
          <i class="fas fa-download text-slate-400"></i>
        </a>

        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/AFE_2025ACEsinEHRs.txt" target="_blank" class="dl-card">
          <div>
            <h4 class="dl-title">Adverse family environment</h4>
            <p class="dl-meta">2,308 codes</p>
          </div>
          <i class="fas fa-download text-slate-400"></i>
        </a>

        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/MHP_2025ACEsinEHRs.txt" target="_blank" class="dl-card">
          <div>
            <h4 class="dl-title">Parental mental health</h4>
            <p class="dl-meta">9,063 codes</p>
          </div>
          <i class="fas fa-download text-slate-400"></i>
        </a>

        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/SM_2025ACEsinEHRs.txt" target="_blank" class="dl-card">
          <div>
            <h4 class="dl-title">Parental substance misuse</h4>
            <p class="dl-meta">2,886 codes</p>
          </div>
          <i class="fas fa-download text-slate-400"></i>
        </a>
      </div>

      <h3 class="text-xl font-bold text-slate-800 mt-10 mb-4 border-none">Exclusion & Context Code Lists</h3>
      <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mb-0">
        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/Accident_excl_2025ACEsinEHRs.txt" target="_blank" class="dl-card bg-rose-50 border-rose-100 hover:border-rose-300">
          <div>
            <h4 class="dl-title text-rose-800">Accidents</h4>
            <p class="dl-meta text-rose-600">3,356 codes</p>
          </div>
          <i class="fas fa-ban text-rose-400"></i>
        </a>
        <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Osteoporosis%20Bone%20disease.txt" target="_blank" class="dl-card bg-rose-50 border-rose-100 hover:border-rose-300">
          <div>
            <h4 class="dl-title text-rose-800">Osteoporosis - Bone disease</h4>
            <p class="dl-meta text-rose-600">406 codes</p>
          </div>
          <i class="fas fa-ban text-rose-400"></i>
        </a>
        <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Birth%20injury%20or%20complication.txt" target="_blank" class="dl-card bg-rose-50 border-rose-100 hover:border-rose-300">
          <div>
            <h4 class="dl-title text-rose-800">Birth injuries/complications</h4>
            <p class="dl-meta text-rose-600">238 codes</p>
          </div>
          <i class="fas fa-ban text-rose-400"></i>
        </a>
        <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Mother-to-child%20transmission.txt" target="_blank" class="dl-card bg-rose-50 border-rose-100 hover:border-rose-300">
          <div>
            <h4 class="dl-title text-rose-800">Mother-to-child-transmissions</h4>
            <p class="dl-meta text-rose-600">15 codes</p>
          </div>
          <i class="fas fa-ban text-rose-400"></i>
        </a>
        
        <!-- Non-ACE covariates mapped alongside exclusions -->
        <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Health%20comorbidities.txt" target="_blank" class="dl-card bg-slate-50 border-slate-200 hover:border-slate-300 sm:col-span-2 border-dashed border-2">
          <div>
            <h4 class="dl-title text-slate-700">Covariates (Non-ACEs)</h4>
            <p class="dl-meta">Used to add context/info to risk prediction models (8,808 codes)</p>
          </div>
          <i class="fas fa-file-alt text-slate-400"></i>
        </a>
      </div>
    </div>
  </section>

  <!-- SECTION 7: Next Steps / Navigation Grid -->
  <section class="bg-slate-50 py-16 border-t border-slate-200">
    <div class="max-w-4xl mx-auto px-6">
      <div class="grid grid-cols-1 sm:grid-cols-2 gap-8 mb-12">
        <a href="https://acesinehrs.com/ACE-domains/" class="grid-card group">
          <div class="img-wrapper" style="padding-bottom: 0 !important;">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/home%20view%20domains.png" alt="View Domains" style="height: 180px !important;">
          </div>
          <div class="content-wrapper mt-4">
            <h3 class="card-title">Explore ACE Domains</h3>
            <p class="text-sm text-slate-500 mb-0" style="font-size: 14px !important;">View comprehensive lists of selected indicators.</p>
          </div>
        </a>

        <a href="https://acesinehrs.com/codelistbrowse/" class="grid-card group">
          <div class="img-wrapper" style="padding-bottom: 0 !important;">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png" alt="Code Lists" style="height: 180px !important;">
          </div>
          <div class="content-wrapper mt-4">
            <h3 class="card-title">Browse Code Lists</h3>
            <p class="text-sm text-slate-500 mb-0" style="font-size: 14px !important;">Search and access clinical code lists seamlessly.</p>
          </div>
        </a>
      </div>
      
      <div class="text-center pb-4">
        <a href="https://acesinehrs.com/" class="inline-flex items-center text-blue-600 hover:text-blue-800 font-medium transition-colors text-[16px] !important" style="font-size: 16px !important;">
          <i class="fas fa-arrow-left mr-2"></i> Go back to homepage
        </a>
      </div>
    </div>
  </section>

</div>

<script>
// Advanced script to perfectly handle sticky nav highlighting and scroll offsets
document.addEventListener('DOMContentLoaded', () => {
  const navItems = document.querySelectorAll('.nav-item');
  const stickyHeader = document.querySelector('.sticky');
  const sections = document.querySelectorAll('.content-section');
  
  // 1. Perfect Smooth Scroll Offset on Click
  navItems.forEach(step => {
    step.addEventListener('click', function(e) {
      e.preventDefault();
      
      const targetId = this.getAttribute('href');
      const targetSection = document.querySelector(targetId);
      
      if (targetSection && stickyHeader) {
        // Calculate exact height of the sticky menu + 30px breathing room
        const headerOffset = stickyHeader.offsetHeight + 30; 
        const elementPosition = targetSection.getBoundingClientRect().top;
        const offsetPosition = elementPosition + window.pageYOffset - headerOffset;
  
        window.scrollTo({
          top: offsetPosition,
          behavior: "smooth"
        });
      }
    });
  });

  // 2. Highlight active step dynamically on scroll
  window.addEventListener('scroll', () => {
    let current = '';
    // Determine the hit-zone offset dynamically based on sticky header height
    const hitZoneOffset = stickyHeader ? stickyHeader.offsetHeight + 40 : 180;
    
    sections.forEach(section => {
      const sectionTop = section.offsetTop;
      if (pageYOffset >= (sectionTop - hitZoneOffset)) {
        current = section.getAttribute('id');
      }
    });

    navItems.forEach(item => {
      item.classList.remove('active');
      if (item.getAttribute('href') === `#${current}`) {
        item.classList.add('active');
      }
    });
  });
});
</script>
