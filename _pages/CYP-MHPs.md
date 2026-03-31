---
layout: splash
title: "Child & Adolescent Mental Health Problems (Outcomes)"
permalink: /CYP-MHPs/
author_profile: false
---
<!-- 1. Load Tailwind Safely -->
<script src="https://cdn.tailwindcss.com"></script>
<script>
 tailwind.config = {
  corePlugins: { preflight: false },
  theme: {
   extend: {
    colors: {
     brand: {
      emerald: '#059669', // Primary MHPs Color
      light: '#d1fae5',
      dark: '#047857',
     }
    }
   }
  }
 }
</script>

<!-- 2. Load Fonts, Icons & DataTables CSS -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<link rel="stylesheet" href="https://cdn.datatables.net/1.13.6/css/jquery.dataTables.min.css">

<!-- 3. The "Iron Shield" Overrides & Custom Styles -->
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
 .tailwind-wrap li, .tailwind-wrap ul, .tailwind-wrap td, .tailwind-wrap th,
 .tailwind-wrap details, .tailwind-wrap summary, .tailwind-wrap strong, .tailwind-wrap em {
  font-family: 'Inter', sans-serif !important;
 }
  
 /* Reset link styles BUT ignore custom components */
 .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.pub-link):not(.text-blue-600):not(.text-emerald-600):not(.text-emerald-700):not(.data-source-link):not(.domain-nav-link):not(.notice-card) {
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

 /* === DOMAIN TIMELINE NAVIGATION === */
 .hide-scrollbar::-webkit-scrollbar { display: none; }
 .hide-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
 .domain-nav-link { text-decoration: none !important; border: none !important; }

 /* === SIDEBAR & SECTIONS === */
 .nav-dot {
  width: 24px !important; height: 24px !important; border-radius: 50% !important;
  background-color: #f1f5f9 !important; border: 2px solid #cbd5e1 !important;
  display: flex !important; align-items: center !important; justify-content: center !important;
  font-size: 11px !important; font-weight: 700 !important; color: #64748b !important;
  position: absolute !important; left: -12px !important; top: 0 !important;
  transition: all 0.3s ease !important;
 }
 .nav-item:hover .nav-dot { border-color: #059669 !important; color: #059669 !important; background-color: #d1fae5 !important; }
 
 .section-header {
  display: flex !important; align-items: center !important;
  font-size: 24px !important; font-weight: 700 !important; color: #0f172a !important;
  margin-bottom: 1.5rem !important; border-bottom: 1px solid #e2e8f0 !important; padding-bottom: 0.75rem !important;
 }
 .section-number {
  width: 32px !important; height: 32px !important; border-radius: 50% !important;
  border: 1px solid #cbd5e1 !important; display: flex !important; align-items: center !important;
  justify-content: center !important; font-size: 14px !important; color: #64748b !important; margin-right: 0.75rem !important;
 }

 /* === EXPANDABLE BOXES === */
 details > summary { list-style: none !important; outline: none !important; }
 details > summary::-webkit-details-marker { display: none !important; }
 .expandable-box {
  background: #ffffff !important; border: 1px solid #e2e8f0 !important; border-radius: 0.75rem !important;
  overflow: hidden !important; margin-bottom: 1rem !important; box-shadow: 0 1px 2px rgba(0,0,0,0.02) !important;
  transition: box-shadow 0.3s ease !important;
 }
 .expandable-box:hover { box-shadow: 0 4px 6px -1px rgba(0,0,0,0.05) !important; border-color: #cbd5e1 !important; }
 .expandable-summary {
  padding: 1rem 1.25rem !important; background-color: #f8fafc !important; cursor: pointer !important;
  display: flex !important; justify-content: space-between !important; align-items: center !important;
  font-weight: 600 !important; color: #1e293b !important; font-size: 16px !important;
 }
 .expandable-box[open] > .expandable-summary { border-bottom: 1px solid #e2e8f0 !important; background-color: #ffffff !important; }
 .expandable-icon { transition: transform 0.3s ease !important; color: #94a3b8 !important; }
 .expandable-box[open] > .expandable-summary .expandable-icon { transform: rotate(180deg) !important; color: #059669 !important; }
 .expandable-content { padding: 1.25rem !important; background: #ffffff !important; }

 /* Content Typography */
 .content-text { font-size: 16px !important; line-height: 1.75 !important; color: #475569 !important; margin-bottom: 1.25rem !important; }
 .hdr-pill {
  display: inline-flex !important; align-items: center !important; padding: 0.2rem 0.6rem !important;
  border-radius: 0.375rem !important; font-size: 12px !important; font-weight: 600 !important;
  background-color: #dcfce7 !important; color: #166534 !important; border: 1px solid #bbf7d0 !important;
  white-space: nowrap !important;
 }
 .data-source-link {
  display: inline-flex !important; align-items: center !important; padding: 0.2rem 0.6rem !important;
  border-radius: 0.375rem !important; font-size: 12px !important; font-weight: 600 !important;
  background-color: #f1f5f9 !important; color: #334155 !important; border: 1px solid #e2e8f0 !important;
  text-decoration: none !important; transition: all 0.2s ease !important; white-space: nowrap !important;
 }
 .data-source-link:hover { background-color: #e2e8f0 !important; border-color: #cbd5e1 !important; color: #0f172a !important; }

 /* Code Blocks */
 .code-container { background: #0d1117 !important; border-radius: 0.5rem !important; overflow: hidden !important; border: 1px solid #30363d !important; }
 .code-header { background: #161b22 !important; padding: 0.5rem 1rem !important; border-bottom: 1px solid #30363d !important; display: flex !important; align-items: center !important; gap: 0.5rem !important; }
 .code-window-dot { width: 10px !important; height: 10px !important; border-radius: 50% !important; }
 .code-pre { padding: 1rem !important; overflow-x: auto !important; margin: 0 !important; font-family: 'Fira Code', monospace !important; font-size: 13px !important; line-height: 1.6 !important; color: #c9d1d9 !important; }
 .syntax-keyword { color: #ff7b72 !important; }
 .syntax-string { color: #a5d6ff !important; }
 .syntax-function { color: #d2a8ff !important; }
 .syntax-comment { color: #8b949e !important; font-style: italic !important; }

 /* Custom Tables */
 .custom-table { width: 100% !important; border-collapse: collapse !important; text-align: left !important; }
 .custom-table th { background-color: #f8fafc !important; padding: 1rem !important; font-size: 13px !important; font-weight: 700 !important; color: #475569 !important; border-bottom: 2px solid #e2e8f0 !important; white-space: nowrap !important; }
 .custom-table td { padding: 0.75rem 1rem !important; font-size: 14px !important; color: #334155 !important; border-bottom: 1px solid #f1f5f9 !important; }
 .domain-badge { display: inline-flex !important; align-items: center !important; justify-content: center !important; padding: 0.25rem 0.5rem !important; border-radius: 0.25rem !important; font-size: 12px !important; font-weight: 700 !important; background: #e0f2fe !important; color: #0369a1 !important; }

 /* NOTICE CARDS */
 .notice-card {
  background-color: #ffffff !important; border-radius: 0.75rem !important; border: 1px solid #f3f4f6 !important;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.04) !important; transition: all 0.3s ease !important;
  position: relative !important; overflow: hidden !important; display: flex !important;
 }
 .notice-card:hover { transform: translateY(-2px) !important; box-shadow: 0 12px 20px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05) !important; }

 /* PUBLICATION LIST */
 .pub-item { display: flex !important; flex-direction: column !important; gap: 0.5rem !important; padding: 1.25rem !important; border: 1px solid #e2e8f0 !important; border-radius: 0.75rem !important; background: #ffffff !important; margin-bottom: 1rem !important; transition: all 0.3s ease !important; }
 .pub-item:hover { border-color: #34d399 !important; box-shadow: 0 4px 6px -1px rgba(5, 150, 105, 0.05) !important; transform: translateY(-2px) !important; }
 .pub-link { font-size: 15px !important; font-weight: 600 !important; color: #2563eb !important; line-height: 1.5 !important; text-decoration: none !important; }
 .pub-link:hover { color: #1d4ed8 !important; text-decoration: underline !important; text-underline-offset: 3px !important; }

 html { scroll-behavior: smooth; }
</style>

<!-- Load Altmetric Embed Script -->
<script type="text/javascript" src="https://d1bxh8uas1mnw7.cloudfront.net/assets/embed.js" async></script>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

 <!-- HERO SECTION -->
 <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/parental%20mental%20health%20problems%20aces%20in%20ehrs.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
  <div class="relative z-10 max-w-6xl mx-auto px-6 py-20 md:py-28 text-center md:text-left">
   <div class="inline-flex items-center px-3 py-1 mb-4 border border-emerald-400 text-emerald-300 rounded-full text-xs font-bold uppercase tracking-wider">
    <i class="fas fa-child mr-2"></i> Child & Adolescent Outcome
   </div>
   <h1 class="hero-title drop-shadow-lg">
    Mental health problems <br><span style="color: #6ee7b7 !important;">in children & adolescents</span>
   </h1>
   <p class="hero-subtitle drop-shadow-md mx-auto md:mx-0">
    This outcome page contains clinical code lists and classification algorithms used to identify mental health problems and substance misuse indicators in children and adolescents (up to 18 years) within EHRs.
   </p>
  </div>
 </header>

 <!-- DOMAIN TIMELINE NAVIGATION -->
 <div class="bg-slate-50 border-b border-slate-200 shadow-sm relative z-20">
  <div class="max-w-6xl mx-auto px-6 overflow-hidden">
   <div class="overflow-x-auto hide-scrollbar py-4">
    <div class="relative flex items-center gap-3 w-max min-w-full">
     
     <div class="absolute top-1/2 left-4 right-4 h-[2px] bg-slate-200 -translate-y-1/2 z-0"></div>
     
     <a href="https://acesinehrs.com/indicators/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-white border border-slate-300 text-slate-600 hover:text-slate-900 hover:border-slate-400 text-[13px] font-semibold px-4 py-2 rounded-full transition-all duration-200">
      All indicators
     </a>
     
     <a href="https://acesinehrs.com/CM/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-white border border-slate-300 text-slate-600 hover:text-slate-900 hover:border-slate-400 text-[13px] font-semibold px-4 py-2 rounded-full transition-all duration-200">
      Child maltreatment
     </a>

     <a href="https://acesinehrs.com/MHPs/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-white border border-slate-300 text-slate-600 hover:text-slate-900 hover:border-slate-400 text-[13px] font-semibold px-4 py-2 rounded-full transition-all duration-200">
      Parental mental health problems
     </a>

     <!-- CYP MHPs Highlighted Nav -->
     <a href="https://acesinehrs.com/CYP-MHPs/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-emerald-700 border-2 border-emerald-700 text-white text-[13px] font-semibold px-4 py-2 rounded-full shadow-md">
      Outcomes: CYP Mental Health Problems
     </a>

    </div>
   </div>
  </div>
 </div>

 <main class="flex-grow max-w-6xl mx-auto px-6 py-12 w-full">
  
  <div class="flex flex-col md:flex-row gap-10 relative">
   
   <!-- LEFT SIDEBAR -->
   <div class="hidden md:block w-56 flex-shrink-0 sticky top-10 h-max self-start pt-2">
    <ul class="relative border-l border-slate-200 ml-3 space-y-8 m-0 p-0 list-none">
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">1</div>
      <a href="#overview" class="text-sm font-semibold text-slate-600 hover:text-brand-emerald transition-colors border-none hover:bg-transparent">Overview</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">2</div>
      <a href="#definition" class="text-sm font-semibold text-slate-600 hover:text-brand-emerald transition-colors border-none hover:bg-transparent">Definition & Rules</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">3</div>
      <a href="#codelists" class="text-sm font-semibold text-slate-600 hover:text-brand-emerald transition-colors border-none hover:bg-transparent">Clinical Codelist</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">4</div>
      <a href="#implementation" class="text-sm font-semibold text-slate-600 hover:text-brand-emerald transition-colors border-none hover:bg-transparent">Implementation Algorithms</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">5</div>
      <a href="#publications" class="text-sm font-semibold text-slate-600 hover:text-brand-emerald transition-colors border-none hover:bg-transparent">Mandatory Citation</a>
     </li>
    </ul>
   </div>

   <!-- MAIN CONTENT AREA -->
   <div class="flex-1 space-y-16">

    <!-- CITATION WARNING NOTICE -->
    <a href="https://doi.org/10.1016/S2468-2667(24)00301-3" target="_blank" class="notice-card p-6 items-start gap-4 sm:gap-5 mb-8">
     <div class="absolute left-0 top-0 bottom-0 w-1.5" style="background-color: #ef4444 !important; border-top-left-radius: 0.75rem; border-bottom-left-radius: 0.75rem;"></div>
     <div class="flex-shrink-0 w-10 h-10 flex items-center justify-center rounded-full mt-0.5" style="background-color: #fef2f2 !important; color: #ef4444 !important;">
      <i class="fas fa-exclamation-triangle text-lg"></i>
     </div>
     <div class="flex-1">
      <p style="font-size: 15px !important; color: #334155 !important; margin: 0 !important;">
       <strong style="color: #0f172a !important; font-weight: 600 !important;">Mandatory Citation:</strong> Users must cite the publication 
       <span style="color: #dc2626 !important; font-weight: 500 !important; text-decoration: underline !important; text-decoration-color: #fecaca !important; text-underline-offset: 4px !important;">"The Lancet Public Health (2025)"</span> 
       when utilising this CYP Mental Health Problems code list in any research outputs.
      </p>
     </div>
    </a>

    <!-- 1. OVERVIEW -->
    <section id="overview" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">1</span> Overview
     </h2>
     
     <div class="bg-white border border-slate-200 rounded-xl overflow-hidden shadow-sm text-[13.5px]">
      
      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Phenotype Category</div>
       <div class="py-2.5 px-4 md:col-span-3 flex items-center">
        <span class="hdr-pill !bg-emerald-100 !text-emerald-800 !border-emerald-200">Mental health & substance misuse outcomes</span>
       </div>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Sex</div>
       <div class="py-2.5 px-4 md:col-span-3 flex flex-wrap items-center gap-2">
        <span class="hdr-pill !bg-slate-100 !text-slate-700 !border-slate-200">Both</span>
       </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Age Range</div>
       <div class="py-2.5 px-4 md:col-span-3 flex flex-wrap items-center gap-2">
        <span class="hdr-pill !bg-sky-100 !text-sky-800 !border-sky-200">Child / Adolescent (0 to 18 years)</span>
       </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Coding System</div>
       <div class="py-2.5 px-4 md:col-span-3 flex flex-wrap gap-2">
        <span class="hdr-pill !bg-emerald-50 !text-emerald-700 !border-emerald-200">READ</span>
        <span class="hdr-pill !bg-emerald-50 !text-emerald-700 !border-emerald-200">SNOMED CT</span>
        <span class="hdr-pill !bg-emerald-50 !text-emerald-700 !border-emerald-200">ICD-10</span>
        <span class="hdr-pill !bg-emerald-50 !text-emerald-700 !border-emerald-200">HES-AE specialty</span>
        <span class="hdr-pill !bg-emerald-50 !text-emerald-700 !border-emerald-200">CPRD prescriptions</span>
       </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Data Sources</div>
       <div class="py-2.5 px-4 md:col-span-3 flex flex-wrap gap-2">
        <a href="https://healthdatagateway.org/en/dataset/692" target="_blank" class="data-source-link">CPRD Aurum <i class="fas fa-external-link-alt ml-1.5 text-[10px] opacity-70"></i></a>
        <a href="https://healthdatagateway.org/en/dataset/875" target="_blank" class="data-source-link">HES-APC <i class="fas fa-external-link-alt ml-1.5 text-[10px] opacity-70"></i></a>
        <a href="https://healthdatagateway.org/dataset/662" target="_blank" class="data-source-link">HES-AE <i class="fas fa-external-link-alt ml-1.5 text-[10px] opacity-70"></i></a>
        <a href="https://healthdatagateway.org/en/dataset/856" target="_blank" class="data-source-link">HES-OP <i class="fas fa-external-link-alt ml-1.5 text-[10px] opacity-70"></i></a>
       </div>
      </div>

     </div>
    </section>

    <!-- 2. DEFINITION -->
    <section id="definition" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">2</span> Definition & Rules
     </h2>
     
     <div class="content-text text-slate-800 font-medium bg-slate-50 border-l-4 border-brand-emerald p-4 rounded-r-lg mb-6">
      This outcome encompasses mental health problems and substance misuse specifically evaluated in children and adolescents, incorporating strict age minimums and validated algorithm rules.
     </div>

     <p class="content-text">
      <strong>Indicators are not mutually exclusive.</strong> A child could be counted in multiple indicators, but only once per indicator and only once for any overarching mental health problem. In the published study, the disaggregation of specific mental health problems was restricted to indicators present in 100 or more children.
     </p>

     <p class="content-text">
      Mental health indicators are defined by multiple rule-based algorithms. These include the requirement to meet a higher cut-off score on validated self-report instruments, or the presence of symptoms combined with an intervention or referral. Medications, interventions, and psychiatric symptoms were combined into appropriate disorder clusters using validated algorithms.
     </p>
    </section>

    <!-- 3. CLINICAL CODELIST -->
    <section id="codelists" class="scroll-mt-10">
     <h2 class="section-header justify-between">
      <div class="flex items-center"><span class="section-number">3</span> Clinical Codelist & Taxonomy</div>
     </h2>
     
     <div class="flex flex-col sm:flex-row gap-3 mb-6">
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/CYP_mental_health_problems_2025_ACEsinEHR.txt" target="_blank" class="inline-flex items-center px-4 py-2 bg-emerald-50 border border-emerald-200 rounded-lg text-[13px] font-semibold text-emerald-800 hover:bg-emerald-100 shadow-sm transition-all hover:-translate-y-0.5">
       <i class="fas fa-file-download text-emerald-600 mr-2 text-lg"></i> Download CYP MHP Codelist
      </a>
     </div>

     <p class="content-text mb-4">
      The taxonomy funnels down from the broad domain (MHP/SM) to specific sub-indicators. Expand the categories below to view the specific indicator classifications.
     </p>

     <!-- NESTED TAXONOMY: Common Mental Health Problems -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       <div><span class="domain-badge mr-2">MHP</span> Common mental health problems</div>
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      <div class="expandable-content p-4 bg-slate-50">
       
       <details class="expandable-box ml-2 mb-2 group shadow-none border-slate-200">
        <summary class="expandable-summary !bg-white py-2 px-4 text-[14px]">
         Depression
         <i class="fas fa-chevron-down expandable-icon text-xs"></i>
        </summary>
        <div class="expandable-content p-0">
         <table class="custom-table w-full text-xs">
          <tr><td class="w-full">Depression</td></tr>
          <tr><td class="w-full">Suicidal ideation</td></tr>
          <tr><td class="w-full">Antidepressant</td></tr>
         </table>
        </div>
       </details>

       <details class="expandable-box ml-2 mb-2 group shadow-none border-slate-200">
        <summary class="expandable-summary !bg-white py-2 px-4 text-[14px]">
         Anxiety disorder NOS (incl. anxiolytics)
         <i class="fas fa-chevron-down expandable-icon text-xs"></i>
        </summary>
        <div class="expandable-content p-0">
         <table class="custom-table w-full text-xs">
          <tr><td class="w-full">Generalised anxiety disorder</td></tr>
          <tr><td class="w-full">Anxiety disorder</td></tr>
          <tr><td class="w-full">Anxiolytic</td></tr>
          <tr><td class="w-full">Somatic symptom and related disorders</td></tr>
          <tr><td class="w-full">Obsessive-compulsive disorders</td></tr>
          <tr><td class="w-full">Panic disorder (incl. agoraphobia, health anx)</td></tr>
          <tr><td class="w-full">Dissociative disorder</td></tr>
          <tr><td class="w-full">PTSD/Acute stress</td></tr>
          <tr><td class="w-full">Gender dysphoria</td></tr>
         </table>
        </div>
       </details>

       <details class="expandable-box ml-2 mb-2 group shadow-none border-slate-200">
        <summary class="expandable-summary !bg-white py-2 px-4 text-[14px]">
         Self-harm or suicide attempts
         <i class="fas fa-chevron-down expandable-icon text-xs"></i>
        </summary>
        <div class="expandable-content p-0">
         <table class="custom-table w-full text-xs">
          <tr><td class="w-full">Self-harm or suicide attempts</td></tr>
          <tr><td class="w-full">Suicide attempt</td></tr>
          <tr><td class="w-full">Self-harm or suicide</td></tr>
         </table>
        </div>
       </details>

       <details class="expandable-box ml-2 mb-2 group shadow-none border-slate-200">
        <summary class="expandable-summary !bg-white py-2 px-4 text-[14px]">
         Mental health problems NOS
         <i class="fas fa-chevron-down expandable-icon text-xs"></i>
        </summary>
        <div class="expandable-content p-0">
         <table class="custom-table w-full text-xs">
          <tr><td class="w-full">Childhood emotional disorder, unspecified</td></tr>
          <tr><td class="w-full">Mental health problem NOS</td></tr>
          <tr><td class="w-full">Puerperal mental disorder NOS</td></tr>
          <tr><td class="w-full">Seen by/referral to mental health professional</td></tr>
         </table>
        </div>
       </details>

       <details class="expandable-box ml-2 mb-0 group shadow-none border-slate-200">
        <summary class="expandable-summary !bg-white py-2 px-4 text-[14px]">
         Sleep-wake disorders
         <i class="fas fa-chevron-down expandable-icon text-xs"></i>
        </summary>
        <div class="expandable-content p-0">
         <table class="custom-table w-full text-xs">
          <tr><td class="w-full">Sleep-wake disorder</td></tr>
         </table>
        </div>
       </details>

      </div>
     </details>

     <!-- NESTED TAXONOMY: Severe mental illness -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       <div><span class="domain-badge mr-2">MHP</span> Severe mental illness</div>
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      <div class="expandable-content p-4 bg-slate-50">

       <details class="expandable-box ml-2 mb-2 group shadow-none border-slate-200">
        <summary class="expandable-summary !bg-white py-2 px-4 text-[14px]">
         Psychosis & Bipolar
         <i class="fas fa-chevron-down expandable-icon text-xs"></i>
        </summary>
        <div class="expandable-content p-0">
         <table class="custom-table w-full text-xs">
          <tr><td class="w-full">Psychosis incl. sections</td></tr>
          <tr><td class="w-full">Bipolar</td></tr>
          <tr><td class="w-full">Antipsychotic medication NOS</td></tr>
          <tr><td class="w-full">Antipsychotics (first generation)</td></tr>
          <tr><td class="w-full">Antipsychotics (second generation)</td></tr>
          <tr><td class="w-full">Forensic psychiatric admission/discharge</td></tr>
         </table>
        </div>
       </details>

       <details class="expandable-box ml-2 mb-2 group shadow-none border-slate-200">
        <summary class="expandable-summary !bg-white py-2 px-4 text-[14px]">
         Personality disorders
         <i class="fas fa-chevron-down expandable-icon text-xs"></i>
        </summary>
        <div class="expandable-content p-0">
         <table class="custom-table w-full text-xs">
          <tr><td class="w-full">Personality disorder</td></tr>
          <tr><td class="w-full">Paraphilic disorder</td></tr>
         </table>
        </div>
       </details>

       <details class="expandable-box ml-2 mb-0 group shadow-none border-slate-200">
        <summary class="expandable-summary !bg-white py-2 px-4 text-[14px]">
         Eating disorders
         <i class="fas fa-chevron-down expandable-icon text-xs"></i>
        </summary>
        <div class="expandable-content p-0">
         <table class="custom-table w-full text-xs">
          <tr><td class="w-full">Eating disorder</td></tr>
          <tr><td class="w-full">Anorexia nervosa</td></tr>
          <tr><td class="w-full">Bulimia</td></tr>
         </table>
        </div>
       </details>

      </div>
     </details>

     <!-- NESTED TAXONOMY: Neurodevelopmental disorders -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       <div><span class="domain-badge mr-2">MHP</span> Neurodevelopmental disorders</div>
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      <div class="expandable-content p-0">
       <table class="custom-table w-full text-xs border-t-0">
        <tr><td class="w-full border-b border-slate-100">Neurodevelopmental conditions and conduct disorders</td></tr>
        <tr><td class="w-full border-b border-slate-100">ADHD (incl. conduct disorder)</td></tr>
        <tr><td class="w-full border-none">Autism spectrum disorder</td></tr>
       </table>
      </div>
     </details>

     <!-- NESTED TAXONOMY: Substance Misuse -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       <div><span class="domain-badge !bg-purple-100 !text-purple-800 mr-2">SM</span> Substance Misuse</div>
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      <div class="expandable-content p-4 bg-slate-50">
       
       <details class="expandable-box ml-2 mb-2 group shadow-none border-slate-200">
        <summary class="expandable-summary !bg-white py-2 px-4 text-[14px]">
         Drug Misuse
         <i class="fas fa-chevron-down expandable-icon text-xs"></i>
        </summary>
        <div class="expandable-content p-0">
         <table class="custom-table w-full text-xs">
          <tr><td class="w-full">Drug misuse, severe (likely dependence levels)</td></tr>
          <tr><td class="w-full">Drugs used for opioid dependence, multipurpose</td></tr>
          <tr><td class="w-full">Drug misuse, moderate (all other)</td></tr>
          <tr><td class="w-full">Personal history of psychoactive substance abuse</td></tr>
          <tr><td class="w-full">Poisoning by addictive drugs incl. benzodiazepines</td></tr>
         </table>
        </div>
       </details>

       <details class="expandable-box ml-2 mb-0 group shadow-none border-slate-200">
        <summary class="expandable-summary !bg-white py-2 px-4 text-[14px]">
         Alcohol Misuse
         <i class="fas fa-chevron-down expandable-icon text-xs"></i>
        </summary>
        <div class="expandable-content p-0">
         <table class="custom-table w-full text-xs">
          <tr><td class="w-full">Alcohol misuse, severe (incl. units per week)</td></tr>
          <tr><td class="w-full">Drugs used for alcohol dependence, specific</td></tr>
         </table>
        </div>
       </details>

      </div>
     </details>

    </section>

    <!-- 4. IMPLEMENTATION RULES -->
    <section id="implementation" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">4</span> Implementation Algorithms
     </h2>
     <p class="content-text mb-6">
      Specific conditions apply to coding CYP mental health problems to avoid misclassification (e.g., differentiating normal developmental behaviour from clinical psychopathology).
     </p>

     <!-- Expandable Rule 1 -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       <div class="flex items-center">
        <span class="bg-blue-100 text-blue-800 border border-blue-200 text-[10px] uppercase font-bold px-2 py-0.5 rounded mr-3">Algorithm 1</span>
        Minimum Age Restrictions
       </div>
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      <div class="expandable-content border-t border-slate-100 bg-slate-50">
       <p class="text-[14px] text-slate-700 leading-relaxed mb-4 mt-0">
        To minimise misclassification, the following minimum age restrictions must be applied to the records before considering them valid indicators for a child:
       </p>
       <ul class="list-disc ml-6 text-[14px] text-slate-700 mb-4 space-y-1">
        <li><strong>Self-harm:</strong> $\ge$ 7 years</li>
        <li><strong>Psychosis:</strong> $\ge$ 10 years</li>
        <li><strong>Personality disorders:</strong> $\ge$ 12 years</li>
        <li><strong>Substance use:</strong> $\ge$ 12 years</li>
       </ul>
       <div class="code-container">
        <div class="code-header">
         <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
         <span class="text-[11px] text-slate-400 font-mono ml-2">R Script / Logic</span>
        </div>
        <pre class="code-pre"><code><span class="syntax-comment"># Apply age restrictions to raw outcome records</span>
cyp_outcomes_filtered &lt;- raw_data %&gt;%
  <span class="syntax-function">filter</span>(
    !(indicator == <span class="syntax-string">"Self-harm"</span> & age_at_event &lt; <span class="syntax-keyword">7</span>),
    !(indicator == <span class="syntax-string">"Psychosis"</span> & age_at_event &lt; <span class="syntax-keyword">10</span>),
    !(indicator == <span class="syntax-string">"Personality disorder"</span> & age_at_event &lt; <span class="syntax-keyword">12</span>),
    !(indicator == <span class="syntax-string">"Substance misuse"</span> & age_at_event &lt; <span class="syntax-keyword">12</span>)
  )</code></pre>
       </div>
      </div>
     </details>

     <!-- Expandable Rule 2 -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       <div class="flex items-center">
        <span class="bg-blue-100 text-blue-800 border border-blue-200 text-[10px] uppercase font-bold px-2 py-0.5 rounded mr-3">Algorithm 2</span>
        Neurodevelopmental Conditions Rule
       </div>
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      <div class="expandable-content border-t border-slate-100 bg-slate-50">
       <p class="text-[14px] text-slate-700 leading-relaxed mb-4 mt-0">
        Recorded neurodevelopmental conditions (such as ADHD, Autism spectrum disorder) are <strong>only retained</strong> when they are also associated with a mental health-related referral or intervention. A neurodevelopmental code alone does not meet the criteria for a mental health problem in this framework.
       </p>
       <div class="code-container">
        <div class="code-header">
         <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
         <span class="text-[11px] text-slate-400 font-mono ml-2">R Script / Logic</span>
        </div>
        <pre class="code-pre"><code><span class="syntax-comment"># Retain neurodevelopmental codes ONLY if associated with intervention</span>
cyp_neurodev_validated &lt;- dataset %&gt;% 
  <span class="syntax-function">mutate</span>(
    is_valid_nd = <span class="syntax-function">ifelse</span>(
      indicator == <span class="syntax-string">"Neurodevelopmental disorders"</span> & has_mh_intervention == <span class="syntax-keyword">TRUE</span>,
      <span class="syntax-keyword">TRUE</span>, <span class="syntax-keyword">FALSE</span>
    )
  )</code></pre>
       </div>
      </div>
     </details>

     <!-- Expandable Rule 3 -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       <div class="flex items-center">
        <span class="bg-blue-100 text-blue-800 border border-blue-200 text-[10px] uppercase font-bold px-2 py-0.5 rounded mr-3">Algorithm 3</span>
        Symptoms & Validated Questionnaires
       </div>
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      <div class="expandable-content border-t border-slate-100 bg-slate-50">
       <p class="text-[14px] text-slate-700 leading-relaxed mb-4 mt-0">
        Mental health indicators require meeting a higher cut-off score on a validated self-report instrument, or the presence of specific symptoms combined with a relevant intervention/referral. Medications, interventions, and psychiatric symptoms were combined into appropriate disorder clusters (e.g., Depression, Anxiety). 
        <br><br>
        Please see the control documentation (<a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v3.pdf" target="_blank" class="text-emerald-700 font-semibold hover:underline">ACEsinEHRs Control documentation v3.pdf</a>) and the specific pages for the ACEs domain <a href="https://acesinehrs.com/MHPs/" target="_blank" class="text-emerald-700 font-semibold hover:underline">parental MHPs</a> and <a href="https://acesinehrs.com/SM/" target="_blank" class="text-emerald-700 font-semibold hover:underline">SM</a> for more information.
       </p>
      </div>
     </details>

    </section>

    <!-- 5. PUBLICATIONS -->
    <section id="publications" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">5</span> Publications & Citation
     </h2>
     <p class="content-text mb-6">Users of the CYP Mental Health Outcomes dataset and algorithms <strong>must cite the following publication</strong>:</p>

     <div class="space-y-4">
      
      <!-- MANDATORY CITATION -->
      <div class="pub-item border-l-4 !border-l-blue-500">
       <div class="text-xs font-bold text-blue-600 uppercase tracking-wide mb-1">Core Study Citation</div>
       <a href="https://doi.org/10.1016/S2468-2667(24)00301-3" target="_blank" class="pub-link">
        Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England.
       </a>
       <p class="text-[14px] text-slate-500 m-0">Syed S, Gilbert R, Feder G, Howe LD, Powell C, Howarth E, Deighton J, Lacey RE. <em class="text-slate-700">The Lancet Public Health</em>. 2024.</p>
      </div>

     </div>

     <div class="mt-12 pt-8 border-t border-slate-200">
      <a href="https://acesinehrs.com/ACE-domains/" class="inline-flex items-center text-slate-500 hover:text-brand-emerald font-medium transition-colors text-sm">
       <i class="fas fa-arrow-left mr-2"></i> Back to all Domains & Outcomes
      </a>
     </div>
    </section>

   </div>
  </div>
 </main>

 <!-- Logos Banner -->
 <section class="bg-slate-50 border-t border-slate-200 py-10 shadow-inner mt-auto">
  <div class="max-w-6xl mx-auto px-6 flex flex-wrap justify-center items-center gap-8 opacity-70 grayscale hover:grayscale-0 transition duration-500">
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

<script src="https://code.jquery.com/jquery-3.7.0.min.js"></script>
<script>
 // Smooth scroll for inner nav
 $(document).ready(function() {
  $('a[href^="#"]').on('click', function(e) {
   e.preventDefault();
   var target = this.hash;
   $('html, body').animate({
    scrollTop: $(target).offset().top - 40
   }, 500);
  });
 });
</script>
