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
    margin-bottom: 0 !important; padding-bottom: 5rem !important;
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
  .tailwind-wrap li, .tailwind-wrap ul {
    font-family: 'Inter', sans-serif !important;
  }
  
  /* Reset link styles BUT ignore custom components */
  .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.dl-card):not(.nav-link):not(.text-blue-600) {
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
  .content-heading {
    font-size: 32px !important; font-weight: 700 !important; color: #0f172a !important;
    margin-bottom: 1.25rem !important; margin-top: 3rem !important; border-bottom: 1px solid #e2e8f0 !important; padding-bottom: 0.5rem !important;
  }
  .content-subheading {
    font-size: 22px !important; font-weight: 600 !important; color: #1e293b !important;
    margin-bottom: 1rem !important; margin-top: 2rem !important; border: none !important;
  }
  .content-text {
    font-size: 16px !important; line-height: 1.75 !important; color: #475569 !important; margin-bottom: 1.25rem !important;
  }

  /* Notice Cards */
  .notice-card {
    background-color: #ffffff !important; border-radius: 1rem !important; border: 1px solid #e2e8f0 !important;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; padding: 1.5rem !important;
    margin-bottom: 1.5rem !important; display: flex !important; align-items: flex-start !important; gap: 1rem !important;
    position: relative !important; overflow: hidden !important;
  }
  .notice-danger { border-left: 6px solid #f97316 !important; }
  .notice-info { border-left: 6px solid #3b82f6 !important; }

  /* Custom Lists */
  .custom-list { list-style: none !important; padding: 0 !important; margin: 0 0 1.5rem 0 !important; }
  .custom-list li {
    position: relative !important; padding-left: 2rem !important; margin-bottom: 1rem !important;
    font-size: 16px !important; line-height: 1.6 !important; color: #475569 !important;
  }
  .custom-list li i {
    position: absolute !important; left: 0 !important; top: 0.25rem !important; color: #3b82f6 !important; font-size: 1.1rem !important;
  }

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
  .custom-table-wrap { overflow-x: auto !important; margin-bottom: 2rem !important; border-radius: 0.75rem !important; border: 1px solid #e2e8f0 !important; box-shadow: 0 1px 3px rgba(0,0,0,0.05) !important; }
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

  /* Smooth Scrolling for anchor links */
  html { scroll-behavior: smooth; }

  /* Sidebar Active State (Optional JS handling, but basic styles here) */
  .nav-link { transition: all 0.2s ease; border-left: 2px solid transparent; }
  .nav-link:hover { color: #2563eb !important; border-left-color: #2563eb; background-color: #f8fafc; }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen bg-white">

  <!-- Hero Section -->
  <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20getting%20started%20page.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
    <div class="relative z-10 max-w-5xl mx-auto px-6 py-20 md:py-28">
      <h1 class="hero-title drop-shadow-lg text-center md:text-left">
        Getting <span style="color: #bfdbfe !important;">started</span>
      </h1>
      <p class="hero-subtitle drop-shadow-md text-center md:text-left max-w-3xl">
        A quick introduction to incorporating validated indicators, code lists and scripts for measuring intervenable and clinically relevant ACEs using EHRs.
      </p>
      <div class="mt-6 p-4 bg-slate-900 bg-opacity-50 border-l-4 border-blue-400 rounded-r-lg max-w-3xl inline-block backdrop-blur-sm">
        <p class="text-sm md:text-base text-blue-100 leading-relaxed m-0 font-medium">
          We are passionate about using EHRs to advance healthcare, social justice, and policy for families affected by adversity. However, ACEs in EHRs are not easily accessible and can be challenging to implement without guidance.
        </p>
      </div>
    </div>
  </header>

  <!-- Logos Banner -->
  <section class="bg-white border-b border-gray-200 py-6 shadow-sm relative z-10">
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

  <!-- Main Grid Layout -->
  <div class="max-w-7xl mx-auto px-6 py-12 flex flex-col lg:flex-row gap-12 w-full">
    
    <!-- LEFT SIDEBAR: Navigation -->
    <aside class="w-full lg:w-1/4 flex-shrink-0 hidden lg:block">
      <div class="sticky top-10 bg-slate-50 rounded-2xl border border-slate-200 p-6 shadow-sm">
        
        <div class="mb-6">
          <h4 class="text-xs font-bold text-slate-400 uppercase tracking-widest mb-3">Getting Started</h4>
          <ul class="list-none p-0 m-0 space-y-1">
            <li><a href="#how-does-it-work" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">How does it work?</a></li>
          </ul>
        </div>

        <div class="mb-6">
          <h4 class="text-xs font-bold text-slate-400 uppercase tracking-widest mb-3">ACEs in EHRs</h4>
          <ul class="list-none p-0 m-0 space-y-1">
            <li><a href="#domains-and-indicators" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Domains and indicators</a></li>
            <li><a href="#code-lists" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Code list</a></li>
            <li><a href="#code-list-dictionary" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Code list dictionary</a></li>
            <li><a href="#example-code-attached-to-ace-indicator" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Example</a></li>
          </ul>
        </div>

        <div class="mb-6">
          <h4 class="text-xs font-bold text-slate-400 uppercase tracking-widest mb-3">Data preparation</h4>
          <ul class="list-none p-0 m-0 space-y-1">
            <li><a href="#data-preparation-and-standardisation" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Overview & steps</a></li>
            <li><a href="#data-restructuring" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Data restructuring</a></li>
            <li><a href="#data-cleaning-and-standardisation" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Data cleaning & standardisation</a></li>
            <li><a href="#conversation-table-of-codes-requiring-prefixes" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Converting code prefixes</a></li>
            <li><a href="#create-ace-specific-master-file" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Create ACE-specific master file</a></li>
          </ul>
        </div>

        <div class="mb-6">
          <h4 class="text-xs font-bold text-slate-400 uppercase tracking-widest mb-3">Deriving variables</h4>
          <ul class="list-none p-0 m-0 space-y-1">
            <li><a href="#deriving-variables" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Introduction</a></li>
            <li><a href="#applying-algorithms" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Algorithms</a></li>
            <li><a href="#applying-algorithms-using-the-code-lists-built-in-helper-functions" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Using code list helper functions</a></li>
          </ul>
        </div>

        <div>
          <h4 class="text-xs font-bold text-slate-400 uppercase tracking-widest mb-3">Downloads</h4>
          <ul class="list-none p-0 m-0 space-y-1">
            <li><a href="#download-code-lists" class="nav-link block px-3 py-1.5 text-sm text-slate-600 font-medium rounded-r-md">Download code lists</a></li>
          </ul>
        </div>

      </div>
    </aside>

    <!-- RIGHT CONTENT AREA -->
    <div class="w-full lg:w-3/4">
      
      <div class="bg-blue-50 border border-blue-100 rounded-xl p-5 mb-10 flex items-center gap-4">
        <div class="w-10 h-10 rounded-full bg-blue-100 flex items-center justify-center text-blue-600 shrink-0">
          <i class="fas fa-info-circle text-lg"></i>
        </div>
        <p class="text-blue-900 font-medium m-0 text-lg">This page provides a guide to get you started incorporating validated indicators to identify ACEs in EHRs.</p>
      </div>

      <!-- SECTION 1 -->
      <h2 id="how-does-it-work" class="content-heading mt-0">How does it work?</h2>
      <p class="content-text font-medium text-slate-800">To use the ACE indicators, you will need:</p>
      
      <ul class="custom-list">
        <li>
          <i class="far fa-check-circle"></i>
          <strong>Access to an EHR data source for research:</strong> Obtain authorised and de-identified data of children and parents for research purposes. Most ACEs are captured in primary care. Several data sources in the UK provide linked primary care data of children and parents, including the <a href="https://cprd.com/" target="_blank" class="text-blue-600 hover:underline">Clinical Practice Research Datalink (CPRD)</a>, <a href="https://www.the-health-improvement-network.com/" target="_blank" class="text-blue-600 hover:underline">The Health Improvement Network (THIN)</a>, and <a href="https://www.qresearch.org/" target="_blank" class="text-blue-600 hover:underline">QResearch</a>. Access to CPRD requires <a href="https://cprd.com/research-applications" target="_blank" class="text-blue-600 hover:underline">protocol approval</a> via CPRD’s Research Data Governance Process. Please visit the <a href="https://www.healthdatagateway.org" target="_blank" class="text-blue-600 hover:underline">Health Data Research Innovation Gateway</a> for more information.
        </li>
        <li>
          <i class="fas fa-hospital-user"></i>
          <strong>OR: Access to your organisation's locally stored EHR data:</strong> Obtain authorised access to your service's/NHS trust's locally stored EHRs of children and parents for service-related and research purposes. Many NHS trusts provide streamlined processes to access data sources like the Clinical Record Interactive Search (<a href="https://slam.nhs.uk/clinical-record-interactive-search" target="_blank" class="text-blue-600 hover:underline">1</a>, <a href="https://www.oxfordhealth.nhs.uk/research/toolkit/cris/" target="_blank" class="text-blue-600 hover:underline">2</a>, <a href="https://www.southernhealth.nhs.uk/about-us/research/research-and-innovation/clinical-record-interactive-search" target="_blank" class="text-blue-600 hover:underline">3</a>). These local data sources often have a data structure consistent with national data sources like <a href="https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/hospital-episode-statistics" target="_blank" class="text-blue-600 hover:underline">HES-APC</a>, and used to measure ACE indicators. Contact your local data department to seek further advice.
        </li>
        <li>
          <i class="fas fa-shield-alt"></i>
          <strong>Secure Data Environment:</strong> Ensure that your work is conducted within a secure data environment (SDE) approved for working with EHRs. SDEs provide the necessary technical and governance safeguards to protect patient data and meet data security standards.
        </li>
        <li>
          <i class="fas fa-link"></i>
          <strong>Data linkage of child and parent data:</strong> Implement robust data linkage of child and parent EHRs. Providers like CPRD allow you to access already established linkages of mother-child data. For linkage of mother-child data in other EHR databases, please see methods described elsewhere (<a href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0164667" target="_blank" class="text-blue-600 hover:underline">1</a>, <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext" target="_blank" class="text-blue-600 hover:underline">2</a>, <a href="https://onlinelibrary.wiley.com/doi/full/10.1002/pds.4811" target="_blank" class="text-blue-600 hover:underline">3</a>). For paternal linkage, please see methods described <a href="https://www.thelancet.com/cms/10.1016/S2468-2667(23)00119-6/attachment/9c50602c-ebd2-445f-ae3b-de30e2a1db14/mmc1.pdf" target="_blank" class="text-blue-600 font-medium hover:underline">here</a>.
        </li>
        <li>
          <i class="fas fa-file-code"></i>
          <strong>ACE Indicators:</strong> You are in the right place. Most indicators are derived using algorithms that identify and extract information from EHRs using clinically coded healthcare information (for example, ICD-10, Read codes, SNOMED-CT). Head to the <a href="#download-code-lists" class="text-blue-600 font-medium hover:underline">download section</a> for a comprehensive list of validated ACE indicators.
        </li>
        <li>
          <i class="fas fa-database"></i>
          <strong>Data preparation and standardisation:</strong> Extract the necessary data elements from the EHRs related to ACE indicators and relevant health outcomes. Prepare the data by cleaning and structuring it in a format ready for merging.
        </li>
        <li>
          <i class="fas fa-laptop-code"></i>
          <strong>Apply algorithms for ACE indicators:</strong> Apply appropriate ACE algorithms using R, Python or any data management language to ensure you obtain validated indicators in the linked child and parent data.
        </li>
      </ul>

      <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/implement%20centered1.png" alt="Implementation workflow" class="w-full h-auto rounded-xl shadow-sm border border-slate-200 my-8">

      <!-- Danger Notice -->
      <div class="notice-card notice-danger">
        <div class="w-10 h-10 rounded-full bg-orange-100 flex items-center justify-center text-orange-600 shrink-0 mt-1">
          <i class="fas fa-exclamation-triangle text-xl"></i>
        </div>
        <div>
          <h4 class="text-lg font-bold text-slate-900 m-0 mb-2">IMPORTANT!</h4>
          <p class="text-slate-600 text-sm leading-relaxed m-0">
            Implementing the ACE indicators in more complex data sets like primary care data (GP records) requires restructuring, manipulating and combining multiple large data sets into one or multiple new files using a programming language of choice (e.g., Python, R). This section provides only brief information on data management specific to the implementation of the ACE indicators. Many data management tasks involve a <a href="https://www.jstatsoft.org/article/view/v059i10" target="_blank" class="text-blue-600 hover:underline">split-apply-combine strategy</a>. This information is intended as supplementary recommendations to users who already have skills in programming languages like R, Python, or SQL. To learn how to use R, we recommend reading <a href="https://r4ds.hadley.nz/" target="_blank" class="text-blue-600 hover:underline font-medium">"R for Data Science (2e)"</a> freely available online.
          </p>
        </div>
      </div>


      <!-- SECTION 2 -->
      <h2 id="domains-and-indicators" class="content-heading">ACE indicators</h2>
      
      <h3 class="content-subheading">Domains and indicators</h3>
      <p class="content-text">We developed two measures of ACEs for electronic health records (EHRs):</p>
      <ul class="custom-list mb-6">
        <li><i class="fas fa-layer-group"></i> <strong>Domains</strong> (i.e., grouped indicators)</li>
        <li><i class="fas fa-sitemap"></i> <strong>Indicators</strong> (i.e., grouped codes or measures)</li>
      </ul>
      
      <div class="bg-slate-50 p-6 rounded-xl border border-slate-200 mb-8 font-mono text-sm text-slate-700">
        <div class="flex flex-col space-y-2">
          <div class="flex items-center"><i class="fas fa-level-down-alt rotate-[-90deg] text-slate-400 mr-2"></i> Indicator 2</div>
          <div class="flex items-center ml-6"><i class="fas fa-level-down-alt rotate-[-90deg] text-slate-400 mr-2"></i> Indicator 1</div>
          <div class="flex items-center ml-12"><i class="fas fa-level-down-alt rotate-[-90deg] text-slate-400 mr-2"></i> Most specific indicator</div>
          <div class="flex items-center ml-18 text-blue-600"><i class="fas fa-level-down-alt rotate-[-90deg] text-blue-400 mr-2"></i> Code (alphanumerical code attached to an event description)</div>
        </div>
      </div>

      <p class="content-text">
        Indicators represent a variable of grouped codes or measures for a potential recorded ACE in mothers, fathers or children. The ACEs follow a hierarchical structure, with three levels of specificity of the underlying ACE construct. The structure ranges from the most specific ACE category (specific indicator) to broader categories (indicators 1 and 2), to the six overall ACE domains consistent with the original <a href="https://acesinehrs.com/about/" class="text-blue-600 hover:underline">ACE study</a>.
      </p>

      <a href="https://acesinehrs.com/domains/" class="block my-8 group">
        <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/domains%20and%20indicators%201.png" alt="Domains and Indicators" class="w-full h-auto rounded-xl shadow-sm border border-slate-200 transition-transform duration-300 group-hover:scale-[1.02]">
      </a>

      <!-- Danger Notice -->
      <div class="notice-card notice-danger">
        <div class="w-10 h-10 rounded-full bg-orange-100 flex items-center justify-center text-orange-600 shrink-0 mt-1">
          <i class="fas fa-exclamation-circle text-xl"></i>
        </div>
        <div>
          <h4 class="text-lg font-bold text-slate-900 m-0 mb-1">Note on sample size</h4>
          <p class="text-slate-600 text-sm leading-relaxed m-0">
            The ability to use specific indicators depends on your sample size. We recommend restricting the disaggregation of specific indicators to those present in 250 or more unique children. For many studies, it will be most appropriate to use the six ACE domains only and avoid disaggregation into specific indicators unless required to answer your research question.
          </p>
        </div>
      </div>

      <!-- Info Notice -->
      <div class="notice-card notice-info">
        <div class="w-10 h-10 rounded-full bg-blue-100 flex items-center justify-center text-blue-600 shrink-0 mt-1">
          <i class="fas fa-users text-xl"></i>
        </div>
        <div>
          <h4 class="text-lg font-bold text-slate-900 m-0 mb-1">Think-family approach</h4>
          <p class="text-slate-600 text-sm leading-relaxed m-0">
            Unless specified, indicators refer to information recorded in the child's, the mother's and the father's records. Properly studying ACEs requires a "think-family" approach - we need both children's and parents' data! Think-family means we recognise that the health and well-being of children are intricately tied to their parents' experiences and health outcomes.
          </p>
        </div>
      </div>

      <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/ehrs%20of%20aces%20indicator.png" alt="Workflow" class="w-full h-auto rounded-xl shadow-sm border border-slate-200 my-8">
      
      <!-- Flourish Embed -->
      <div class="my-8 rounded-xl overflow-hidden border border-slate-200 shadow-sm">
        <div class="flourish-embed flourish-hierarchy" data-src="visualisation/7087179"><script src="https://public.flourish.studio/resources/embed.js"></script></div>
      </div>

      <h3 id="code-lists" class="content-subheading">Code lists</h3>
      <p class="content-text">
        The ACE indicators are mapped onto codes stored in <a href="https://acesinehrs.com/domains/" class="text-blue-600 hover:underline">code lists</a>. Each data source will have different coding systems. The current ACEs indicators include ICD-9/10 codes (hospital/death records), Read codes, SNOMED-CT codes, medcodes, prodcodes, gemscripts (general practice), and codes for obtaining continuous data or coded information from speciality fields in CPRD GOLD, HES-APC, HES-A&E and HES-OP.
      </p>
      <p class="content-text">
        We have converted several original codes so the code lists contain one column of research-ready codes. This ensures efficient information integration from multiple coding systems without accidental deduplication. See code list dictionary and <a href="#conversation-table-of-codes-requiring-prefixes" class="text-blue-600 hover:underline">conversion table below</a> for more information.
      </p>

      <h3 id="code-list-dictionary" class="content-subheading">Code list dictionary</h3>
      
      <div class="custom-table-wrap">
        <table class="custom-table">
          <thead>
            <tr>
              <th style="width: 25%;">Provided variable</th>
              <th>Description</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><strong>Code</strong></td>
              <td>Data ready code. Contains CPRD GOLD medcodes and prodcodes (as used in the data provided by CPRD with added prefixes to prodcode), ICD-9/10 (removed punctuations for ICD), and OPSC-4 codes. Prefixes <code>d_</code> added to prodcodes and <code>p_</code> to OPSC-4 codes. Prefixes <a href="https://acesinehrs.com/research/#publication-list" target="_blank" class="text-blue-600 hover:underline">prevents de-duplication</a> as different systems may use the same code for different descriptions.</td>
            </tr>
            <tr>
              <td><strong>Code original</strong></td>
              <td>Original code as entered into respective system (removed punctuations for ICD)</td>
            </tr>
            <tr>
              <td><strong>Coding term</strong></td>
              <td>Original code description</td>
            </tr>
            <tr>
              <td><strong>Indicator code</strong></td>
              <td>Indicator code name</td>
            </tr>
            <tr>
              <td><strong>Indicator specific</strong></td>
              <td>Most specific indicator</td>
            </tr>
            <tr>
              <td><strong>Indicator 1</strong></td>
              <td>Main ACE indicator combining multiple codes or measures as used in validation paper</td>
            </tr>
            <tr>
              <td><strong>Indicator 2</strong></td>
              <td>Broader ACE indicator combining multiple codes or measures</td>
            </tr>
            <tr>
              <td><strong>Domain</strong></td>
              <td>ACE domain grouping all indicators together (applicable for the overall code list)</td>
            </tr>
            <tr>
              <td><strong>Severity</strong></td>
              <td>Where applicable, this variable indicates the severity classification of the code description. <em>e.g. For alcohol misuse, `mild`, `moderate`, `severe`.</em></td>
            </tr>
            <tr>
              <td><strong>Scale</strong></td>
              <td><code>1</code> = Indicates that the code and severity classifications are dependent on extra clinical information (e.g. frequency of alcohol consumption). By default, this is set to <em>`Mild`</em> for alcohol. See rule-based algorithms.</td>
            </tr>
            <tr>
              <td><strong>Reference</strong></td>
              <td><code>1</code> = code is part of family violence reference standard, <code>2</code> = code can be used as a broader measure of family violence</td>
            </tr>
            <tr>
              <td><strong>Individual</strong></td>
              <td><code>1</code> = child only, <code>2</code> = mother only, <code>3</code> = mother or child (i.e. either), <code>4</code> = only applicable to female children</td>
            </tr>
            <tr>
              <td><strong>Coding systems</strong></td>
              <td><code>GP/primary care:</code> Read, OXMIS, Prodcode, CPRD REFERRAL FHSASPEC, CPRD REFERRAL NHSSPEC. <br><code>HES-APC/secondary care/ONS:</code> ICD-10, OPCS-4, ICD-9 (ONS < year 2000), HES-APC DISDEST OR ADMISORC</td>
            </tr>
          </tbody>
        </table>
      </div>

      <h3 id="example-code-attached-to-ace-indicator" class="content-subheading">Example ACE indicator in the code list</h3>
      <div class="custom-table-wrap">
        <table class="custom-table" style="min-width: 800px;">
          <thead>
            <tr>
              <th>Code</th>
              <th>Coding term</th>
              <th>Indicator 1</th>
              <th>Indicator 2</th>
              <th>Domain</th>
              <th>Severity</th>
              <th>Indiv</th>
              <th>Coding sys</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td class="font-mono text-blue-600">912</td>
              <td>[D]Anorexia Anorexia</td>
              <td>Anorexia</td>
              <td>Eating disorders</td>
              <td>Parental mental health</td>
              <td>diagnostic</td>
              <td>2</td>
              <td>Read</td>
            </tr>
          </tbody>
        </table>
      </div>


      <!-- SECTION 3 -->
      <h2 id="data-preparation-and-standardisation" class="content-heading">Data preparation and standardisation</h2>
      <p class="content-text">
        Now, let's get the data ready for analysis! Unlike data sets such as the <a href="https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/hospital-episode-statistics" target="_blank" class="text-blue-600 hover:underline">Hospital Episode Statistics</a> where everything is nicely placed into a few files, EHRs from primary care are messier and located in multiple separate files with different structures and formats. Therefore, implementing the ACE indicators using code lists requires preparing and restructuring your data sets into a uniform format.
      </p>

      <div class="bg-white border border-slate-200 rounded-xl p-6 shadow-sm mb-8 relative overflow-hidden">
        <div class="absolute left-0 top-0 bottom-0 w-1.5 bg-blue-500"></div>
        <h4 class="text-lg font-bold text-slate-800 mb-4 ml-2">Data preparation steps:</h4>
        <div class="ml-4 space-y-2">
          <div class="flex items-start"><i class="fas fa-check text-emerald-500 mt-1 mr-3"></i> <span class="text-slate-700"><strong>Extract the raw data files</strong> using SQL (or other programming)</span></div>
          <div class="flex items-start ml-4"><i class="fas fa-arrow-right text-slate-300 mt-1 mr-3 text-sm"></i> <span class="text-slate-700"><strong>Restructure each data file</strong> (i.e. creating new data files with consistent format)</span></div>
          <div class="flex items-start ml-8"><i class="fas fa-arrow-right text-slate-300 mt-1 mr-3 text-sm"></i> <span class="text-slate-700"><strong>Data clean & standardise each file</strong> (add prefixes, remove waste etc)</span></div>
          <div class="flex items-start ml-12"><i class="fas fa-arrow-right text-slate-300 mt-1 mr-3 text-sm"></i> <span class="text-slate-700">Retrieve data & bind into a <strong>"master ACE data file"</strong></span></div>
          <div class="flex items-start ml-16"><i class="fas fa-arrow-right text-slate-300 mt-1 mr-3 text-sm"></i> <span class="text-slate-700">Merge ACEs code list with the master file</span></div>
          <div class="flex items-start ml-20"><i class="fas fa-arrow-right text-slate-300 mt-1 mr-3 text-sm"></i> <span class="text-slate-700">Apply algorithms & retain your ACE indicator</span></div>
          <div class="flex items-start ml-24"><i class="fas fa-arrow-right text-slate-300 mt-1 mr-3 text-sm"></i> <span class="text-slate-700">Merge the ACE indicator onto your selected cohort for analysis</span></div>
        </div>
      </div>

      <h3 id="data-restructuring" class="content-subheading">Data restructuring</h3>
      <ul class="custom-list">
        <li><i class="fas fa-wrench"></i> <strong>Restructuring data files and fields.</strong> Having extracted your raw files, restructure all files and variables into a consistent "long format", and rename variables into consistent names. This ensures we can easily bind all files into one combined file later.</li>
        <li><i class="fas fa-trash-alt"></i> <strong>Drop irrelevant data fields/variables</strong> to reduce file size. e.g., In the CPRD clinical file, variables like <em>"constype, sysdate, data8"</em> can easily be omitted.</li>
        <li><i class="fas fa-tag"></i> Make sure to <strong>add an extra variable</strong> to each data file to label the original data source (e.g. HES, CPRD clinical) before saving it.</li>
      </ul>

      <h3 id="data-cleaning-and-standardisation" class="content-subheading">Data cleaning and standardisation</h3>
      <p class="content-text">Most large EHR files contain errors, such as missing values, inconsistent formats, or invalid entries. Data cleaning ensures consistency across datasets.</p>
      
      <p class="text-sm font-medium text-slate-700 mb-2 mt-4">Clean and remove any punctuations or white spaces from codes:</p>
      <div class="code-container">
        <div class="code-header">
          <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
          <span class="text-xs text-slate-400 font-mono ml-2">R Script</span>
        </div>
        <pre class="code-pre"><code>aces_data$medcode &lt;- <span class="syntax-function">gsub</span>(<span class="syntax-string">"\\s+"</span>,<span class="syntax-string">""</span>,aces_data$medcode) <span class="syntax-comment">#removes white/blank spaces</span>
aces_data$medcode &lt;- <span class="syntax-function">gsub</span>(<span class="syntax-string">"\\."</span>,<span class="syntax-string">""</span>,aces_data$medcode) <span class="syntax-comment">#removes punctuations</span></code></pre>
      </div>

      <p class="text-sm font-medium text-slate-700 mb-2 mt-6">Convert data fields into consistent classes and machine-readable date formats (e.g. year-month-day):</p>
      <div class="code-container">
        <div class="code-header">
          <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
          <span class="text-xs text-slate-400 font-mono ml-2">R Script (dplyr)</span>
        </div>
        <pre class="code-pre"><code>aces_data &lt;- aces_data %&gt;% <span class="syntax-function">mutate_all</span>(as.character) %&gt;% 
 <span class="syntax-function">separate</span>(date_example_variable,<span class="syntax-function">c</span>(<span class="syntax-string">"day"</span>,<span class="syntax-string">"month"</span>,<span class="syntax-string">"year"</span>),sep=<span class="syntax-string">"-"</span>,remove=T) %&gt;% 
 <span class="syntax-function">unite</span>(new_date_variable,<span class="syntax-function">c</span>(<span class="syntax-string">"year"</span>,<span class="syntax-string">"month"</span>,<span class="syntax-string">"day"</span>),sep=<span class="syntax-string">"-"</span>,remove=T)</code></pre>
      </div>

      <h3 id="conversation-table-of-codes-requiring-prefixes" class="content-subheading">Converting code prefixes</h3>
      <p class="content-text">
        A substantial proportion of codes from different coding systems share the same alphanumeric sequence. For example, prodcodes (prescriptions) and ICD-9 codes share thousands of identical sequences that mean entirely different things. 
        <br><br>
        <code class="bg-slate-100 text-rose-600 px-2 py-1 rounded text-sm font-mono border border-slate-200">e.g. "11246" (prodcode) = Lofexidine tablets  VS.  "11246" (medcode) = At risk violence in the home</code>
      </p>
      <p class="content-text">
        To preserve uniqueness, we have converted relevant codes by adding prefixes. You will need to convert the codes in your specific data files to match the converted code lists.
      </p>

      <div class="custom-table-wrap">
        <table class="custom-table">
          <thead>
            <tr>
              <th>Data source & Coding system</th>
              <th>Prefix added</th>
              <th>Example</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>CPRD GOLD: Prodcode (Gemscript product code)</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">d_</code></td>
              <td class="font-mono text-sm text-slate-500">d_727 - Sertraline 100mg</td>
            </tr>
            <tr>
              <td>ONS Mortality ≤2000 & HES-APC ≤1998: ICD-9</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">e_</code></td>
              <td class="font-mono text-sm text-slate-500">e_5713 - Alcoholic liver damage</td>
            </tr>
            <tr>
              <td>HES-APC: OPCS-4</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">p_</code></td>
              <td class="font-mono text-sm text-slate-500">p_X66 - Cognitive behavioural therapy</td>
            </tr>
            <tr>
              <td>HES-A&E: A&E specific diagnosis system</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">aed_</code></td>
              <td class="font-mono text-sm text-slate-500">aed_144 - Poisoning (inc overdose)</td>
            </tr>
            <tr>
              <td>HES-A&E: A&E speciality field "treatment"</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">aet_</code></td>
              <td class="font-mono text-sm text-slate-500">aet_54 - Social worker intervention</td>
            </tr>
            <tr>
              <td>HES-A&E: A&E speciality field "investigations"</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">aei_</code></td>
              <td class="font-mono text-sm text-slate-500">aei_21 - Pregnancy test</td>
            </tr>
            <tr>
              <td>HES-OP: OP speciality field "treatment"</td>
              <td><code class="text-blue-600 font-bold bg-blue-50 px-1 rounded">opt_</code></td>
              <td class="font-mono text-sm text-slate-500">opt_711 - Child & Adolescent Psychiatry</td>
            </tr>
          </tbody>
        </table>
      </div>

      <h3 id="create-ace-specific-master-file" class="content-subheading">Create ACE specific "master file"</h3>
      <p class="content-text">
        Having identified your cohort and restructured the multiple files, the next step is to extract relevant data and bind it into one combined "master file" containing only ACE data.
      </p>
      <p class="content-text">
        <strong>Streaming data extraction:</strong> We recommend applying a streaming approach by iterating over each patient ID in your EHR files against your specific cohort list and ACE code lists. This processes data in chunks rather than loading massive datasets entirely into memory.
      </p>

      <div class="code-container">
        <div class="code-header">
          <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
          <span class="text-xs text-slate-400 font-mono ml-2">R Script</span>
        </div>
        <pre class="code-pre"><code><span class="syntax-comment"># Step 1: Set up the working directory</span>
<span class="syntax-function">setwd</span>(<span class="syntax-string">"path/to/ehr/files"</span>)

<span class="syntax-comment"># Step 2: Install and load required packages</span>
<span class="syntax-function">install.packages</span>(<span class="syntax-function">c</span>(<span class="syntax-string">"data.table"</span>, <span class="syntax-string">"readr"</span>,<span class="syntax-string">"tidyverse"</span>,<span class="syntax-string">"fastmatch"</span>))
<span class="syntax-keyword">library</span>(data.table)
<span class="syntax-keyword">library</span>(tidyverse)
<span class="syntax-keyword">library</span>(fastmatch)

<span class="syntax-comment"># Step 3: Read the patient ID list</span>
patient_id_list &lt;- <span class="syntax-function">read_csv</span>(<span class="syntax-string">"patient_id_list.csv"</span>)

<span class="syntax-comment"># Step 4: Stream through EHR files, match with patient ID, and save relevant data</span>
<span class="syntax-keyword">for</span> (ehr_file <span class="syntax-keyword">in</span> <span class="syntax-function">list.files</span>(pattern = <span class="syntax-string">"*.txt"</span>)) {
  output_file &lt;- <span class="syntax-function">paste0</span>(<span class="syntax-string">"output_"</span>, ehr_file)

  <span class="syntax-comment"># Create empty file & write column names</span>
  <span class="syntax-function">fwrite</span>(<span class="syntax-function">data.frame</span>(), output_file)
  <span class="syntax-function">fwrite</span>(<span class="syntax-function">names</span>(data.table::<span class="syntax-function">fread</span>(ehr_file, nrows = 0, header = TRUE, data.table = FALSE)), output_file, append = TRUE)
  
  <span class="syntax-comment"># Stream through EHR file and extract relevant data</span>
  ehr_stream &lt;- data.table::<span class="syntax-function">fread</span>(ehr_file, header = TRUE, data.table = FALSE, colClasses=<span class="syntax-string">"character"</span>, nThread=8)
  relevant_data &lt;- ehr_stream %&gt;% <span class="syntax-function">filter</span>(patient_id %fin% patient_id_list$patient_id)
  
  <span class="syntax-comment"># Append relevant data to output file</span>
  <span class="syntax-function">fwrite</span>(relevant_data, output_file, append = TRUE, quote = FALSE, row.names = FALSE, col.names=TRUE)
}</code></pre>
      </div>

      <!-- SECTION 4 -->
      <h2 id="deriving-variables" class="content-heading">Deriving variables</h2>
      
      <h3 class="content-subheading">Introduction</h3>
      <p class="content-text">
        Most indicators are ready to be used after merging the correct code list with your prepared ACE data file. However, many indicators rely on rule-based algorithms to ensure coded measures meet appropriate cut-off criteria and prevent misclassifications (e.g. age-restrictions, exclusions of accidental injuries, or maternal-child transmissions).
      </p>

      <!-- Danger Notice -->
      <div class="notice-card notice-danger">
        <div class="w-10 h-10 rounded-full bg-orange-100 flex items-center justify-center text-orange-600 shrink-0 mt-1">
          <i class="fas fa-clock text-xl"></i>
        </div>
        <div>
          <h4 class="text-lg font-bold text-slate-900 m-0 mb-1">Time restrictions</h4>
          <p class="text-slate-600 text-sm leading-relaxed m-0">
            The validated ACE indicators are time sensitive and apply any time between 2 years before birth and 10 years after birth. However, most child maltreatment and high-risk presentations of child maltreatment are limited to 2 years before to 3, or 5 years after birth. Ascertaining the correct exposure time in relation to children's birthdate is essential.
          </p>
        </div>
      </div>

      <h3 id="applying-algorithms" class="content-subheading">Algorithms</h3>
      <ul class="custom-list mb-8">
        <li><i class="fas fa-clinic-medical"></i> <strong>For GP records:</strong> We define indicators by combining information recorded in Read codes, prescriptions, referral fields and validated self-report measures (continuous variables needing re-coding).</li>
        <li><i class="fas fa-hospital"></i> <strong>For hospital and death records:</strong> We define indicators by combining codes from the ICD-9/10, OPCS-4, and HES-APC discharge/admission fields.</li>
      </ul>

      <h3 id="applying-algorithms-using-the-code-lists-built-in-helper-functions" class="content-subheading">Applying algorithms using code list helper functions</h3>
      
      <p class="content-text mb-2"><strong>1. Merge code lists & keep unique recordings.</strong></p>
      <div class="code-container">
        <div class="code-header">
          <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
        </div>
        <pre class="code-pre"><code>aces_data %&gt;% dplyr::<span class="syntax-function">distinct</span>(patid,medcode,eventdate,system,source,individual,.keep_all=T)</code></pre>
      </div>

      <p class="content-text mb-2"><strong>2. Filter against criteria using helper variables.</strong> The code lists include built-in "helper variables" (like `scale`). Here is an example filtering mental health measures that met validated cut-off criteria:</p>
      <div class="code-container">
        <div class="code-header">
          <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
        </div>
        <pre class="code-pre"><code>mmhps_depres_anx &lt;- merged_data %&gt;% <span class="syntax-function">filter</span>(Domain==<span class="syntax-string">"mMHPs"</span> & scale==<span class="syntax-string">"1"</span> & data1 &gt; cut_off)</code></pre>
      </div>

      <p class="content-text mb-2">To apply multiple <em>if-then</em> assumptions against a standalone code list, rely on control flow methods like `dplyr::case_when`:</p>
      <div class="code-container">
        <div class="code-header">
          <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
        </div>
        <pre class="code-pre"><code>data &lt;- data %&gt;%
  <span class="syntax-function">mutate</span>(Binary_Variable = <span class="syntax-function">case_when</span>(
    Code %in% code_list & Field1 &gt; 10 & Field2 == <span class="syntax-string">"Value"</span> ~ 1,
    Code %in% code_list & Field1 &lt;= 10 & Field2 != <span class="syntax-string">"Value"</span> ~ 0,
    TRUE ~ <span class="syntax-keyword">NA</span>
  ))</code></pre>
      </div>

      <p class="content-text mb-2"><strong>3. Applying multiple rule-based criteria over time.</strong> For example, depression based on symptoms/medications requiring a co-occurrence within 2 years:</p>
      <div class="code-container">
        <div class="code-header">
          <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
        </div>
        <pre class="code-pre"><code>depression_cases &lt;- ehr_data %&gt;%
  <span class="syntax-function">filter</span>(
    <span class="syntax-comment"># Check if depression symptoms or medications are present</span>
    <span class="syntax-function">any_of</span>(depression_symptoms) | <span class="syntax-function">any_of</span>(depression_medications),
    
    <span class="syntax-comment"># Check if previous codes are present within the past 2 years (365 * 2 days)</span>
    <span class="syntax-function">any_of</span>(previous_codes) & visit_date &gt;= (<span class="syntax-function">Sys.Date</span>() - 365 * 2)
  )</code></pre>
      </div>


      <!-- SECTION 5: DOWNLOADS -->
      <h2 id="download-code-lists" class="content-heading border-b-2 border-slate-800">Download code lists</h2>
      
      <p class="content-text font-medium mt-4">
        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v3.pdf" target="_blank" class="text-blue-600 hover:underline">
          <i class="fas fa-file-pdf text-rose-500 mr-2"></i> ACEsinEHRs control documentation/release information
        </a>
      </p>

      <!-- Danger Notice -->
      <div class="notice-card notice-danger mt-6">
        <div class="w-10 h-10 rounded-full bg-orange-100 flex items-center justify-center text-orange-600 shrink-0 mt-1">
          <i class="fas fa-code-branch text-xl"></i>
        </div>
        <div>
          <h4 class="text-lg font-bold text-slate-900 m-0 mb-1">Implementation Note</h4>
          <p class="text-slate-600 text-sm leading-relaxed m-0">
            The indicators use <a href="https://advanced-r-solutions.rbind.io/control-flow.html" target="_blank" class="text-blue-600 hover:underline">control flow methods</a> to implement rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions, traumatic birth injuries or maternal-child transmissions.
          </p>
        </div>
      </div>

      <h3 class="text-xl font-bold text-slate-800 mt-10 mb-4 border-none">All ACE indicators (Master Files)</h3>
      <p class="text-sm text-slate-500 mb-4">Right-click on link to save as a ".txt" file (i.e. using option "save link as")</p>

      <div class="grid grid-cols-1 gap-4 mb-10">
        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025ACEsinEHRs.txt" target="_blank" class="dl-card border-l-4 border-l-blue-500">
          <div>
            <h4 class="dl-title">All ACEs</h4>
            <p class="dl-meta">Total included codes: 23,164</p>
          </div>
          <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-blue-600 group-hover:bg-blue-50 transition-colors"><i class="fas fa-download"></i></div>
        </a>
        
        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025_medcode_prodcode_CPRD_GOLD_Aurum_ACEsinEHRs.txt" target="_blank" class="dl-card border-l-4 border-l-emerald-500">
          <div>
            <h4 class="dl-title">All ACEs GP / CPRD GOLD / AURUM only</h4>
            <p class="dl-meta">medcodes, prodcodes, measures only (20,925 codes)</p>
          </div>
          <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-emerald-600 group-hover:bg-emerald-50 transition-colors"><i class="fas fa-download"></i></div>
        </a>

        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025_ICD910_special_fields_HES_ACEsinEHRs.txt" target="_blank" class="dl-card border-l-4 border-l-purple-500">
          <div>
            <h4 class="dl-title">All ACEs Hospital only</h4>
            <p class="dl-meta">ICD, OPCS and HES-APC specific fields (2,239 codes)</p>
          </div>
          <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-purple-600 group-hover:bg-purple-50 transition-colors"><i class="fas fa-download"></i></div>
        </a>
      </div>

      <h3 class="text-xl font-bold text-slate-800 mt-10 mb-6 border-none">By ACE domain</h3>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-10">
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
            <p class="dl-meta">3,281 codes (incl. algorithms)</p>
          </div>
          <i class="fas fa-download text-slate-400"></i>
        </a>

        <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/IPV_no_algo_2025ACEsinEHRs.txt" target="_blank" class="dl-card ml-0 md:ml-4 border-l-4 border-l-slate-300">
          <div>
            <h4 class="dl-title text-sm">IPV (No Algorithms)</h4>
            <p class="dl-meta text-xs">2,044 codes (excl. requiring algo)</p>
          </div>
          <i class="fas fa-download text-slate-400 text-sm"></i>
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
            <h4 class="dl-title">Parental mental health problems</h4>
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

      <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Health%20comorbidities.txt" target="_blank" class="dl-card bg-slate-50 border-dashed border-2 mb-10">
        <div>
          <h4 class="dl-title text-slate-700">Covariates (Non-ACEs)</h4>
          <p class="dl-meta">Used to add info to risk prediction models (8,808 codes)</p>
        </div>
        <i class="fas fa-file-alt text-slate-400"></i>
      </a>

      <h3 class="text-xl font-bold text-slate-800 mt-10 mb-4 border-none">Code lists for rule-based exclusions</h3>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-10">
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
      </div>

      <!-- HDRUK Callout -->
      <div class="bg-white border border-slate-200 rounded-xl p-6 text-center shadow-sm mb-12 flex flex-col items-center">
        <h4 class="text-lg font-bold text-slate-800 mb-3 m-0">Need more code lists?</h4>
        <a href="https://www.healthdatagateway.org/" target="_blank" class="inline-block hover:opacity-80 transition-opacity">
          <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/hdruk%20small.png" alt="HDRUK Gateway" class="h-12 object-contain mx-auto">
        </a>
      </div>

      <div class="flex gap-4 border-t border-slate-200 pt-8 mt-12 pb-10">
        <a href="https://acesinehrs.com/ACE-domains/" class="inline-flex items-center text-slate-500 hover:text-blue-600 font-medium transition-colors bg-slate-50 hover:bg-blue-50 px-4 py-2 rounded-lg border border-slate-200">
          <i class="fas fa-arrow-left mr-2"></i> Domains
        </a>
      </div>

    </div>
  </div>
</div>

<script>
// Simple script to highlight the active menu item based on scroll position
document.addEventListener('DOMContentLoaded', () => {
  const links = document.querySelectorAll('.nav-link');
  const sections = Array.from(links).map(link => document.querySelector(link.getAttribute('href')));
  
  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(section => {
      if (section && window.scrollY >= (section.offsetTop - 150)) {
        current = section.getAttribute('id');
      }
    });
    
    links.forEach(link => {
      link.classList.remove('text-blue-600', 'border-blue-600', 'bg-slate-100');
      link.classList.add('text-slate-600', 'border-transparent');
      if (link.getAttribute('href') === `#${current}`) {
        link.classList.remove('text-slate-600', 'border-transparent');
        link.classList.add('text-blue-600', 'border-blue-600', 'bg-slate-100');
      }
    });
  });
});
</script>
