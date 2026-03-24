---
layout: splash
permalink: /
title: "Adverse Childhood Experiences (ACEs) in Electronic Health Records (EHRs)"
author_profile: false
---

<!-- 1. Load Tailwind Safely -->
<script src="https://cdn.tailwindcss.com"></script>
<script>
  tailwind.config = {
    corePlugins: { preflight: false } 
  }
</script>

<!-- 2. Load Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<!-- 3. The "Iron Shield" Overrides -->
<style>
  /* === FIX THE MENU & LOGO === */
  .masthead__inner-wrap .site-logo img {
    max-height: 24px !important; 
    width: auto !important;
  }
  .masthead__menu-item a {
    font-family: 'Inter', sans-serif !important;
    font-size: 16px !important;
    font-weight: 500 !important;
    color: #6b7280 !important;
  }
  .masthead__menu-item a:hover {
    color: #111827 !important;
  }

  /* === BREAK OUT TO FULL SCREEN === */
  .full-bleed {
    width: 100vw;
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
    background-color: #f9fafb !important; /* Exact bg-gray-50 tint */
    margin-bottom: 0 !important;
    padding-bottom: 5rem !important;
  }
  
  /* Remove Jekyll's forced padding/margins that cause the white gap */
  #main { 
    padding-top: 0 !important; 
    padding-bottom: 0 !important; 
    margin-bottom: 0 !important; 
  }

  /* === OVERRIDE JEKYLL FOOTER TO MATCH HTML DESIGN === */
  .page__footer {
    background-color: #0f172a !important; /* Slate 900 */
    color: #94a3b8 !important; /* Slate 400 */
    margin-top: 0 !important; /* Eliminates the white gap! */
    padding: 3rem 0 !important;
    border-top: none !important;
  }
  .page__footer a {
    color: #cbd5e1 !important;
    text-decoration: none !important;
  }
  .page__footer a:hover {
    color: #ffffff !important;
  }
  .page__footer-copyright {
    color: #64748b !important;
  }

  /* === PROTECT TAILWIND FROM JEKYLL === */
  .tailwind-wrap { box-sizing: border-box; }
  
  .tailwind-wrap h1, .tailwind-wrap h2, .tailwind-wrap h3, 
  .tailwind-wrap p, .tailwind-wrap a, .tailwind-wrap span, 
  .tailwind-wrap div, .tailwind-wrap strong { 
    font-family: 'Inter', sans-serif !important; 
  }
  
  /* Reset link styles BUT ignore the buttons so we don't break borders! */
  .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.grid-card) { 
    border-bottom: none !important; 
    text-decoration: none !important; 
    box-shadow: none !important; 
  }

  /* === HERO TYPOGRAPHY === */
  .hero-title {
    font-size: 48px !important;
    line-height: 48px !important;
    font-weight: 700 !important;
    color: rgb(255, 255, 255) !important;
    margin-bottom: 24px !important;
    border: none !important;
  }
  .hero-subtitle {
    font-size: 20px !important;
    line-height: 28px !important;
    font-weight: 400 !important;
    color: rgb(241, 245, 249) !important;
    margin-bottom: 32px !important;
    max-width: 720px !important; /* Forces the text to wrap like old HTML */
    margin-left: auto !important;
    margin-right: auto !important;
  }

  /* === EXACT MATCH BUTTONS === */
  .btn-primary {
    background-color: #ffffff !important;
    color: rgb(30, 41, 59) !important;
    font-size: 18px !important;
    line-height: 28px !important;
    font-weight: 600 !important;
    padding: 12px 32px !important;
    border-radius: 9999px !important;
    display: inline-flex !important;
    align-items: center !important;
    border: none !important;
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05) !important;
    transition: all 0.3s ease !important;
    text-decoration: none !important;
  }
  .btn-primary:hover {
    transform: translateY(-2px) !important;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04) !important;
  }
  .btn-primary i {
    color: #2563eb !important;
    margin-left: 8px !important;
  }

  .btn-secondary {
    background-color: rgba(15, 23, 42, 0.4) !important; 
    border: 1px solid #60a5fa !important;
    color: rgb(255, 255, 255) !important;
    font-size: 14px !important;
    line-height: 20px !important;
    font-weight: 500 !important;
    padding: 10px 20px !important;
    border-radius: 9999px !important;
    display: inline-flex !important;
    align-items: center !important;
    box-sizing: border-box !important; 
    transition: all 0.3s ease !important;
    text-decoration: none !important;
  }
  .btn-secondary:hover {
    background-color: rgba(15, 23, 42, 0.8) !important;
  }

  /* === GRID CARDS WITH PERFECT HOVER === */
  .grid-card {
    background-color: #ffffff !important;
    border-radius: 1rem !important;
    border: 1px solid #f3f4f6 !important;
    overflow: hidden !important;
    box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05) !important;
    transition: all 0.3s ease !important;
    display: flex !important;
    flex-direction: column !important;
    text-decoration: none !important;
  }
  .grid-card:hover {
    transform: translateY(-4px) !important;
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05) !important;
  }
  .grid-card img {
    transition: transform 0.5s ease !important;
  }
  .grid-card:hover img {
    transform: scale(1.05) !important;
  }
  .grid-card .card-title {
    font-size: 20px !important;
    font-weight: 700 !important;
    color: #1f2937 !important;
    margin: 0 !important;
    border: none !important;
    transition: color 0.3s ease !important;
  }
  .grid-card:hover .card-title {
    color: #2563eb !important; 
  }

  /* === CONTENT TYPOGRAPHY (EXACT MATCH) === */
  .section-title { 
    font-size: 28px !important; 
    font-weight: 700 !important; 
    color: #1e293b !important; 
    margin-bottom: 24px !important; 
    border: none !important; 
  }
  .intro-bold-text {
    font-size: 18px !important;
    line-height: 29px !important;
    font-weight: 700 !important;
    color: rgb(30, 58, 138) !important; 
    margin-bottom: 24px !important;
  }
  .intro-normal-text {
    font-size: 16px !important;
    line-height: 26px !important;
    font-weight: 400 !important;
    color: rgb(75, 85, 99) !important; 
    margin-bottom: 24px !important;
  }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

  <!-- Hero Section -->
  <header class="relative bg-slate-700 bg-opacity-50 text-white" 
      style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20home%20page%202024.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
     
    <!-- Banner Content -->
    <div class="relative z-10 max-w-5xl mx-auto px-6 py-24 md:py-32 text-center">
      <h1 class="hero-title drop-shadow-lg">
        Adverse Childhood Experiences (ACEs) <br> 
        <span style="color: #bfdbfe !important;">in Electronic Health Records</span>
      </h1>
      <p class="hero-subtitle drop-shadow-md">
        A library of indicators for ACEs in EHRs. Search, discover, and access tools, code lists, and resources to implement clinically relevant and validated indicators of ACEs in your research using de-identified electronic health records.
      </p>
       
      <div class="flex flex-col sm:flex-row justify-center items-center gap-4">
        <a href="/indicators/#download-code-lists" class="btn-primary">
          Download code lists <i class="fas fa-file-download"></i>
        </a>
      </div>

      <div class="mt-8">
        <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(24)00301-3/fulltext" target="_blank" class="btn-secondary">
          <span class="flex h-2.5 w-2.5 relative mr-3">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full opacity-75" style="background-color: #93c5fd !important;"></span>
            <span class="relative inline-flex rounded-full h-2.5 w-2.5" style="background-color: #60a5fa !important;"></span>
          </span>
          New study out in Lancet Public Health!
        </a>
      </div>
    </div>
  </header>

  <!-- Logos Section (Reduced height padding to py-3) -->
  <section class="bg-white border-b border-gray-200 py-3 shadow-sm relative z-10">
    <div class="max-w-7xl mx-auto px-6 flex flex-wrap justify-center items-center gap-8 opacity-70 grayscale hover:grayscale-0 transition duration-500">
      <a href="https://www.ucl.ac.uk/children-policy-research/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/NIHR%20CPRU%20logo%20aces%20in%20ehrs%20footer.png" alt="NIHR CPRU" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/ucl%20ich%20logo%20aces%20in%20ehrs.png" alt="UCL ICH" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.ox.ac.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/university%20of%20oxford%20logo%20aces%20in%20ehrs.png" alt="Oxford" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/NIHR%20Great%20ormond%20street%20hospital%20biomedical%20research%20centre%20logo%20aces%20in%20ehrs.png" alt="NIHR GOSH BRC" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.gosh.nhs.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/GOSH%20logo%20aces%20in%20ehrs.png" alt="GOSH" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.bristol.ac.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/University%20of%20bristol%20logo%20aces%20in%20ehrs.png" alt="Bristol" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.hdruk.ac.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/hdruk%20logo%20aces%20in%20ehrs.png" alt="HDRUK" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
      <a href="https://www.ucl.ac.uk/health-informatics/research/caliber" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/caliber%20ucl%20logo%20aces%20in%20ehrs.png" alt="Caliber UCL" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
    </div>
  </section>

  <main class="flex-grow">
    <!-- Intro Section (Constrained Width to 800px, Pulled higher to pt-8) -->
    <section class="max-w-[800px] mx-auto px-6 pt-8 pb-10 text-center">
      <h2 class="section-title">What is ACEs in EHRs?</h2>
      <p class="intro-bold-text">
        The ACEsinEHRs platform provides validated domains, indicators, and code lists to identify adverse childhood experiences (ACEs) in routinely collected de-identified electronic health records of parents and children before and after birth.
      </p>
      <p class="intro-normal-text">
        Examples of recorded ACEs include child maltreatment (e.g., child protection), exposure to domestic violence and abuse, and growing up with parental mental health problems or substance use problems (e.g., trio of vulnerabilities). This website is continuously updated and provides information on definitions, concepts, measures, and standardised tools to help users apply the developed ACE indicators to create “research-ready” datasets.
      </p>
      <a href="https://shabeer-syed.github.io/acesinehrs/research/" style="color: #1d4ed8 !important; font-weight: 600 !important; text-decoration: underline !important; text-underline-offset: 4px !important; font-size: 16px !important;">See publications here</a>
    </section>

    <!-- Grid Cards Section -->
    <section class="max-w-6xl mx-auto px-6 pb-16">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        
        <a href="https://shabeer-syed.github.io/acesinehrs/about/" class="grid-card group">
          <div class="h-48 overflow-hidden bg-gray-100 relative">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/Introduction%20aces%20small.png" alt="About" class="w-full h-full object-cover" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow bg-white z-10">
            <h3 class="card-title">About ACEs in EHRs</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/ACE-domains/" class="grid-card group">
          <div class="h-48 overflow-hidden bg-gray-100 relative">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/home%20view%20domain%20download%20small.png" alt="Domains" class="w-full h-full object-cover" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow bg-white z-10">
            <h3 class="card-title">ACE Domains</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/codelistbrowse/" class="grid-card group">
          <div class="h-48 overflow-hidden bg-gray-100 relative">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png" alt="Code Lists" class="w-full h-full object-cover" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow bg-white z-10">
            <h3 class="card-title">Browse Code Lists</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/starterguide/" class="grid-card group">
          <div class="h-48 overflow-hidden bg-gray-100 relative">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEs%20implementation%20and%20downloads.png" alt="Getting Started" class="w-full h-full object-cover" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow bg-white z-10">
            <h3 class="card-title">Starter Guide</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/theory/" class="grid-card group">
          <div class="h-48 overflow-hidden bg-gray-100 relative">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/aces%20in%20ehrs%20definitions%20theories.png" alt="Theory" class="w-full h-full object-cover" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow bg-white z-10">
            <h3 class="card-title">Theory & Definitions</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/research/" class="grid-card group">
          <div class="h-48 overflow-hidden bg-gray-100 relative">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/ACEsinEHRs%20research%20outputs%20small.png" alt="Research" class="w-full h-full object-cover" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow bg-white z-10">
            <h3 class="card-title">Research Outputs</h3>
          </div>
        </a>
      </div>
    </section>

    <!-- Notices Section -->
    <section class="max-w-4xl mx-auto px-6 pb-20 space-y-6">
       
      <!-- Notice 1: Update -->
      <div class="relative bg-white rounded-2xl p-6 border border-slate-100 flex items-start gap-4 sm:gap-5 transition duration-300 overflow-hidden group hover:shadow-md" style="box-shadow: 0 2px 10px -3px rgba(6,81,237,0.1) !important;">
        <div class="absolute left-0 top-0 bottom-0 w-1.5 rounded-l-2xl" style="background-color: #3b82f6 !important;"></div>
        <div class="flex-shrink-0 w-10 h-10 flex items-center justify-center rounded-full mt-0.5 transition-colors" style="background-color: #eff6ff !important; color: #2563eb !important;">
          <i class="fas fa-info-circle text-lg"></i>
        </div>
        <div class="flex-1">
          <p style="font-size: 15px !important; color: #475569 !important; margin: 0 !important;">
            <strong style="color: #1e293b !important; font-weight: 600 !important;">UPDATE July 2023:</strong> To derive ACEs using combined maternal and paternal data, please see the paper published in the Lancet Public Health: <br class="hidden sm:block">
            <a href="https://doi.org/10.1016/S2468-2667(23)00119-6" target="_blank" style="color: #2563eb !important; font-weight: 500 !important; text-decoration: underline !important; text-decoration-color: #bfdbfe !important; text-underline-offset: 4px !important;">"Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England"</a>.
          </p>
        </div>
      </div>

      <!-- Notice 2: Core Study -->
      <div class="relative bg-white rounded-2xl p-6 border border-slate-100 flex items-start gap-4 sm:gap-5 transition duration-300 overflow-hidden group hover:shadow-md" style="box-shadow: 0 2px 10px -3px rgba(6,81,237,0.1) !important;">
        <div class="absolute left-0 top-0 bottom-0 w-1.5 rounded-l-2xl" style="background-color: #3b82f6 !important;"></div>
        <div class="flex-shrink-0 w-10 h-10 flex items-center justify-center rounded-full mt-0.5 transition-colors" style="background-color: #eff6ff !important; color: #2563eb !important;">
          <i class="fas fa-book-medical text-lg"></i>
        </div>
        <div class="flex-1">
          <p style="font-size: 15px !important; color: #475569 !important; margin: 0 !important;">
            <strong style="color: #1e293b !important; font-weight: 600 !important;">Core Study:</strong> This library stores ACE indicators and algorithms accompanying the paper published in Lancet Digital Health: <br class="hidden sm:block">
            <a href="https://doi.org/10.1016/S2589-7500(22)00061-9" target="_blank" style="color: #2563eb !important; font-weight: 500 !important; text-decoration: underline !important; text-decoration-color: #bfdbfe !important; text-underline-offset: 4px !important;">"Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study, (2022)."</a>
          </p>
        </div>
      </div>

      <!-- Notice 3: Red Citation Warning -->
      <div class="relative bg-white rounded-2xl p-6 border border-slate-100 flex items-start gap-4 sm:gap-5 transition duration-300 overflow-hidden group hover:shadow-md" style="box-shadow: 0 2px 10px -3px rgba(239,68,68,0.1) !important;">
        <div class="absolute left-0 top-0 bottom-0 w-1.5 rounded-l-2xl" style="background-color: #ef4444 !important;"></div>
        <div class="flex-shrink-0 w-10 h-10 flex items-center justify-center rounded-full mt-0.5 transition-colors" style="background-color: #fef2f2 !important; color: #ef4444 !important;">
          <i class="fas fa-exclamation-triangle text-lg"></i>
        </div>
        <div class="flex-1">
          <p style="font-size: 15px !important; color: #334155 !important; margin: 0 !important;">
            <strong style="color: #0f172a !important; font-weight: 600 !important;">Users must cite</strong> the www.ACEsinEHRs.com library and the accompanying 
            <a href="https://doi.org/10.1016/S2589-7500(22)00061-9" target="_blank" style="color: #dc2626 !important; font-weight: 500 !important; text-decoration: underline !important; text-decoration-color: #fecaca !important; text-underline-offset: 4px !important;">Lancet Digital Health publication</a> 
            in all research outputs, presentations and reports.
          </p>
        </div>
      </div>

      <!-- Notice 4: Red Disclaimer -->
      <div class="relative bg-white rounded-2xl p-6 border border-slate-100 flex items-center gap-4 sm:gap-5 transition duration-300 overflow-hidden group hover:shadow-md" style="box-shadow: 0 2px 10px -3px rgba(239,68,68,0.1) !important;">
        <div class="absolute left-0 top-0 bottom-0 w-1.5 rounded-l-2xl" style="background-color: #ef4444 !important;"></div>
        <div class="flex-shrink-0 w-10 h-10 flex items-center justify-center rounded-full transition-colors" style="background-color: #fef2f2 !important; color: #ef4444 !important;">
          <i class="fas fa-shield-alt text-lg"></i>
        </div>
        <div class="flex-1">
          <p style="font-size: 15px !important; color: #475569 !important; margin: 0 !important;">
            <strong style="color: #1e293b !important; font-weight: 600 !important;">No EHR or patient data is stored in this library.</strong> The information is not intended for clinical use.
          </p>
        </div>
      </div>
       
    </section>
  </main>
</div>
