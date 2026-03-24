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
    corePlugins: { preflight: false } // Protects the rest of your site
  }
</script>

<!-- 2. Load Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<!-- 3. The "Iron Shield" Overrides -->
<style>
  /* === FIX THE MENU & LOGO === */
  .masthead__inner-wrap .site-logo img,
  .masthead__inner-wrap .site-title img {
    max-height: 22px !important; /* Makes the logo exactly the size you had in HTML */
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
  }
  
  /* Remove Jekyll's default spacing */
  #main { padding-top: 0 !important; }

  /* === PROTECT TAILWIND FROM JEKYLL === */
  .tailwind-wrap * { font-family: 'Inter', sans-serif !important; box-sizing: border-box; }
  
  /* Reset all link interference */
  #main .tailwind-wrap a { 
    border-bottom: none !important; 
    text-decoration: none !important; 
    box-shadow: none !important; 
  }
  #main .tailwind-wrap a:hover { 
    text-decoration: none !important; 
  }

  /* Lock in Header Fonts so Jekyll doesn't change them */
  .tailwind-wrap h1 { font-size: 2.5rem !important; line-height: 1.2 !important; font-weight: 700 !important; color: white !important; margin-bottom: 1.5rem !important; border: none !important; }
  @media (min-width: 768px) { .tailwind-wrap h1 { font-size: 3rem !important; } }
  .tailwind-wrap h2 { font-size: 1.875rem !important; font-weight: 700 !important; color: #1e293b !important; margin-bottom: 1.5rem !important; border: none !important; }
  .tailwind-wrap h3 { font-size: 1.25rem !important; font-weight: 700 !important; color: #1f2937 !important; margin: 0 !important; border: none !important; }
  .tailwind-wrap p { font-size: 1.125rem !important; line-height: 1.75 !important; margin-bottom: 1.5rem !important; }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

  <!-- Hero Section -->
  <header class="relative bg-slate-700 bg-opacity-50 text-white" 
      style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20home%20page%202024.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
     
    <!-- Banner Content -->
    <div class="relative z-10 max-w-5xl mx-auto px-6 py-24 md:py-32 text-center">
      <h1 class="tracking-tight drop-shadow-lg text-white">
        Adverse Childhood Experiences (ACEs) <br> 
        <span style="color: #bfdbfe !important;">in Electronic Health Records</span>
      </h1>
      <p class="max-w-3xl mx-auto leading-relaxed drop-shadow-md" style="color: #f1f5f9 !important;">
        A library of indicators for ACEs in EHRs. Search, discover, and access tools, code lists, and resources to implement clinically relevant and validated indicators of ACEs in your research using de-identified electronic health records.
      </p>
       
      <div class="flex flex-col sm:flex-row justify-center items-center gap-4">
        <a href="/indicators/#download-code-lists" class="inline-flex items-center justify-center px-8 py-4 bg-white rounded-full transition duration-300 transform hover:-translate-y-1" style="color: #1e293b !important; font-weight: 600 !important; font-size: 1.125rem !important; box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05) !important;">
          Download code lists <i class="fas fa-file-download ml-2" style="color: #2563eb !important;"></i>
        </a>
      </div>

      <div class="mt-8">
        <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(24)00301-3/fulltext" target="_blank" class="inline-flex items-center px-5 py-2.5 rounded-full transition duration-300 backdrop-blur-sm" style="background-color: rgba(15, 23, 42, 0.6) !important; border: 1px solid #60a5fa !important; color: #ffffff !important; font-size: 0.875rem !important; font-weight: 500 !important;">
          <span class="flex h-2.5 w-2.5 relative mr-3">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full opacity-75" style="background-color: #93c5fd !important;"></span>
            <span class="relative inline-flex rounded-full h-2.5 w-2.5" style="background-color: #60a5fa !important;"></span>
          </span>
          New study out in Lancet Public Health!
        </a>
      </div>
    </div>
  </header>

  <!-- Logos Section -->
  <section class="bg-white border-b border-gray-200 py-8 shadow-sm relative z-10">
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
    <!-- Intro Section -->
    <section class="max-w-4xl mx-auto px-6 py-16 text-center">
      <h2>What is ACEs in EHRs?</h2>
      <p>
        <strong style="color: #1e3a8a !important; font-weight: 600 !important;">The ACEsinEHRs platform provides validated domains, indicators, and code lists to identify adverse childhood experiences (ACEs) in routinely collected de-identified electronic health records of parents and children before and after birth.</strong>
      </p>
      <p style="color: #4b5563 !important;">
        Examples of recorded ACEs include child maltreatment (e.g., child protection), exposure to domestic violence and abuse, and growing up with parental mental health problems or substance use problems (e.g., trio of vulnerabilities). This website is continuously updated and provides information on definitions, concepts, measures, and standardised tools to help users apply the developed ACE indicators to create “research-ready” datasets.
      </p>
      <a href="https://shabeer-syed.github.io/acesinehrs/research/" style="color: #1d4ed8 !important; font-weight: 600 !important; text-decoration: underline !important; text-underline-offset: 4px !important;">See publications here</a>
    </section>

    <!-- Grid Cards Section -->
    <section class="max-w-6xl mx-auto px-6 pb-16">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <a href="https://shabeer-syed.github.io/acesinehrs/about/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden transition duration-300 transform hover:-translate-y-1 hover:shadow-xl">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/Introduction%20aces%20small.png" alt="About" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="group-hover:text-blue-600 transition">About ACEs in EHRs</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/ACE-domains/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden transition duration-300 transform hover:-translate-y-1 hover:shadow-xl">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/home%20view%20domain%20download%20small.png" alt="Domains" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="group-hover:text-blue-600 transition">ACE Domains</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/codelistbrowse/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden transition duration-300 transform hover:-translate-y-1 hover:shadow-xl">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png" alt="Code Lists" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="group-hover:text-blue-600 transition">Browse Code Lists</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/starterguide/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden transition duration-300 transform hover:-translate-y-1 hover:shadow-xl">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEs%20implementation%20and%20downloads.png" alt="Getting Started" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="group-hover:text-blue-600 transition">Starter Guide</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/theory/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden transition duration-300 transform hover:-translate-y-1 hover:shadow-xl">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/aces%20in%20ehrs%20definitions%20theories.png" alt="Theory" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="group-hover:text-blue-600 transition">Theory & Definitions</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/research/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden transition duration-300 transform hover:-translate-y-1 hover:shadow-xl">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/ACEsinEHRs%20research%20outputs%20small.png" alt="Research" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" style="margin: 0 !important;">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="group-hover:text-blue-600 transition">Research Outputs</h3>
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
