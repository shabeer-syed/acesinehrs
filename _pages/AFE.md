---
layout: splash
title: "Adverse family environments"
permalink: /AFE/
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
      blue: '#0284c7', // Primary AFE Domain Color
      light: '#e0f2fe',
      dark: '#0369a1',
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
 .tailwind-wrap details, .tailwind-wrap summary {
  font-family: 'Inter', sans-serif !important;
 }
  
 /* Reset link styles BUT ignore custom components */
 .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.pub-link):not(.text-blue-600):not(.text-blue-700):not(.data-source-link):not(.domain-nav-link) {
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

 /* === HDR UK STYLE SIDEBAR & SECTIONS === */
 .nav-dot {
  width: 24px !important; height: 24px !important; border-radius: 50% !important;
  background-color: #f1f5f9 !important; border: 2px solid #cbd5e1 !important;
  display: flex !important; align-items: center !important; justify-content: center !important;
  font-size: 11px !important; font-weight: 700 !important; color: #64748b !important;
  position: absolute !important; left: -12px !important; top: 0 !important;
  transition: all 0.3s ease !important;
 }
 .nav-item:hover .nav-dot { border-color: #0284c7 !important; color: #0284c7 !important; background-color: #e0f2fe !important; }
 
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

 /* === HDR UK STYLE EXPANDABLE BOXES === */
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
 .expandable-box[open] .expandable-summary { border-bottom: 1px solid #e2e8f0 !important; background-color: #ffffff !important; }
 .expandable-icon { transition: transform 0.3s ease !important; color: #94a3b8 !important; }
 .expandable-box[open] .expandable-icon { transform: rotate(180deg) !important; color: #0284c7 !important; }
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
 .custom-table td { padding: 1rem !important; font-size: 14px !important; color: #334155 !important; border-bottom: 1px solid #f1f5f9 !important; }
 .domain-badge { display: inline-flex !important; align-items: center !important; justify-content: center !important; padding: 0.25rem 0.5rem !important; border-radius: 0.25rem !important; font-size: 12px !important; font-weight: 700 !important; background: #e0f2fe !important; color: #0369a1 !important; }

 /* === DATATABLES OVERRIDES FOR TAILWIND/HDR UK LOOK === */
 .dataTables_wrapper .dataTables_filter input {
  border: 1px solid #cbd5e1 !important; border-radius: 0.375rem !important;
  padding: 0.35rem 0.75rem !important; margin-left: 0.5rem !important; outline: none !important;
  font-family: 'Inter', sans-serif !important; font-size: 13px !important; color: #334155 !important;
 }
 .dataTables_wrapper .dataTables_filter input:focus { border-color: #0284c7 !important; box-shadow: 0 0 0 1px #0284c7 !important; }
 .dataTables_wrapper .dataTables_length select {
  border: 1px solid #cbd5e1 !important; border-radius: 0.375rem !important;
  padding: 0.25rem 1.5rem 0.25rem 0.5rem !important; outline: none !important; font-size: 13px !important; color: #334155 !important;
 }
 .dataTables_wrapper .dataTables_paginate .paginate_button {
  padding: 0.25rem 0.75rem !important; margin-left: 0.25rem !important; border-radius: 0.375rem !important;
  border: 1px solid #e2e8f0 !important; background: #f8fafc !important; font-size: 13px !important; color: #475569 !important;
 }
 .dataTables_wrapper .dataTables_paginate .paginate_button.current {
  background: #e2e8f0 !important; border-color: #cbd5e1 !important; color: #0f172a !important; font-weight: 600 !important;
 }
 .dataTables_wrapper .dataTables_paginate .paginate_button:hover { background: #e2e8f0 !important; color: #0f172a !important; border-color: #cbd5e1 !important; }
 table.dataTable.no-footer { border-bottom: 1px solid #e2e8f0 !important; }

 /* PUBLICATION LIST */
 .pub-item { display: flex !important; flex-direction: column !important; gap: 0.5rem !important; padding: 1.25rem !important; border: 1px solid #e2e8f0 !important; border-radius: 0.75rem !important; background: #ffffff !important; margin-bottom: 1rem !important; transition: all 0.3s ease !important; }
 .pub-item:hover { border-color: #7dd3fc !important; box-shadow: 0 4px 6px -1px rgba(2, 132, 199, 0.05) !important; transform: translateY(-2px) !important; }
 .pub-link { font-size: 15px !important; font-weight: 600 !important; color: #2563eb !important; line-height: 1.5 !important; text-decoration: none !important; }
 .pub-link:hover { color: #1d4ed8 !important; text-decoration: underline !important; text-underline-offset: 3px !important; }

 html { scroll-behavior: smooth; }
</style>

<!-- Load Altmetric Embed Script -->
<script type="text/javascript" src="https://d1bxh8uas1mnw7.cloudfront.net/assets/embed.js" async></script>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

 <!-- HERO SECTION -->
 <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/Adverse%20family%20environment%20aces%20in%20ehrs.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
  <div class="relative z-10 max-w-6xl mx-auto px-6 py-20 md:py-28 text-center md:text-left">
   <h1 class="hero-title drop-shadow-lg">
    Adverse family <span style="color: #7dd3fc !important;">environments</span>
   </h1>
   <p class="hero-subtitle drop-shadow-md mx-auto md:mx-0">
    This domain includes indicators of adverse family environments (AFE), aligning with the original ACE domain "household challenges". We define an AFE as any clinically intervenable psychosocial risk factor or experience recorded in the child or the parent.
   </p>
  </div>
 </header>

 <!-- DOMAIN TIMELINE NAVIGATION -->
 <div class="bg-slate-50 border-b border-slate-200 shadow-sm relative z-20">
  <div class="max-w-6xl mx-auto px-6 overflow-hidden">
   <div class="overflow-x-auto hide-scrollbar py-4">
    <div class="relative flex items-center gap-3 w-max min-w-full">
     
     <!-- The Connecting Line -->
     <div class="absolute top-1/2 left-4 right-4 h-[2px] bg-slate-200 -translate-y-1/2 z-0"></div>
     
     <!-- Domain Nodes -->
     <a href="https://acesinehrs.com/indicators/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-white border border-slate-300 text-slate-600 hover:text-slate-900 hover:border-slate-400 text-[13px] font-semibold px-4 py-2 rounded-full transition-all duration-200">
      All indicators
     </a>
     
     <a href="https://acesinehrs.com/CM/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-white border border-slate-300 text-slate-600 hover:text-slate-900 hover:border-slate-400 text-[13px] font-semibold px-4 py-2 rounded-full transition-all duration-200">
      Child maltreatment
     </a>

     <a href="https://acesinehrs.com/IPV/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-white border border-slate-300 text-slate-600 hover:text-slate-900 hover:border-slate-400 text-[13px] font-semibold px-4 py-2 rounded-full transition-all duration-200">
      Intimate partner violence
     </a>

     <a href="https://acesinehrs.com/HRPCM/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-white border border-slate-300 text-slate-600 hover:text-slate-900 hover:border-slate-400 text-[13px] font-semibold px-4 py-2 rounded-full transition-all duration-200">
      High-risk presentation of child maltreatment
     </a>

     <a href="https://acesinehrs.com/MHPs/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-white border border-slate-300 text-slate-600 hover:text-slate-900 hover:border-slate-400 text-[13px] font-semibold px-4 py-2 rounded-full transition-all duration-200">
      Parental mental health problems
     </a>

     <a href="https://acesinehrs.com/SM/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-white border border-slate-300 text-slate-600 hover:text-slate-900 hover:border-slate-400 text-[13px] font-semibold px-4 py-2 rounded-full transition-all duration-200">
      Parental substance misuse
     </a>

     <a href="https://acesinehrs.com/AFE/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-slate-800 border-2 border-slate-800 text-white text-[13px] font-semibold px-4 py-2 rounded-full shadow-md">
      Adverse family environments
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
      <a href="#overview" class="text-sm font-semibold text-slate-600 hover:text-brand-blue transition-colors border-none hover:bg-transparent">Overview</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">2</div>
      <a href="#definition" class="text-sm font-semibold text-slate-600 hover:text-brand-blue transition-colors border-none hover:bg-transparent">Definition</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">3</div>
      <a href="#codelists" class="text-sm font-semibold text-slate-600 hover:text-brand-blue transition-colors border-none hover:bg-transparent">Clinical Codelist</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">4</div>
      <a href="#implementation" class="text-sm font-semibold text-slate-600 hover:text-brand-blue transition-colors border-none hover:bg-transparent">Implementation</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">5</div>
      <a href="#publications" class="text-sm font-semibold text-slate-600 hover:text-brand-blue transition-colors border-none hover:bg-transparent">Publications</a>
     </li>

    </ul>
   </div>

   <!-- MAIN CONTENT AREA -->
   <div class="flex-1 space-y-16">

    <!-- 1. OVERVIEW -->
    <section id="overview" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">1</span> Overview
     </h2>
     
     <div class="bg-white border border-slate-200 rounded-xl overflow-hidden shadow-sm text-[13.5px]">
      
      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Domain / Phenotype</div>
       <div class="py-2.5 px-4 md:col-span-3 flex items-center">
        <span class="hdr-pill !bg-blue-100 !text-blue-800 !border-blue-200">Adverse family environments (AFE)</span>
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
        <span class="hdr-pill !bg-slate-100 !text-slate-700 !border-slate-200">Child (0-18y)</span>
        <span class="hdr-pill !bg-slate-100 !text-slate-700 !border-slate-200">Parent (Adults)</span>
       </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Individual</div>
       <div class="py-2.5 px-4 md:col-span-3 flex flex-wrap items-center gap-2">
        <span class="hdr-pill !bg-slate-100 !text-slate-700 !border-slate-200">Parent</span>
        <span class="hdr-pill !bg-slate-100 !text-slate-700 !border-slate-200">Child</span>
       </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Coding System</div>
       <div class="py-2.5 px-4 md:col-span-3 flex flex-wrap gap-2">
        <span class="hdr-pill !bg-blue-50 !text-blue-700 !border-blue-200">READ</span>
        <span class="hdr-pill !bg-blue-50 !text-blue-700 !border-blue-200">SNOMED CT</span>
        <span class="hdr-pill !bg-blue-50 !text-blue-700 !border-blue-200">ICD-10</span>
        <span class="hdr-pill !bg-blue-50 !text-blue-700 !border-blue-200">HES-AE speciality field</span>
        <span class="hdr-pill !bg-blue-50 !text-blue-700 !border-blue-200">HES-OP speciality field</span>
       </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Data Sources</div>
       <div class="py-2.5 px-4 md:col-span-3 flex flex-wrap gap-2">
        <a href="https://healthdatagateway.org/en/dataset/692" target="_blank" class="data-source-link">CPRD Aurum <i class="fas fa-external-link-alt ml-1.5 text-[10px] opacity-70"></i></a>
        <a href="https://healthdatagateway.org/en/dataset/694" target="_blank" class="data-source-link">CPRD GOLD <i class="fas fa-external-link-alt ml-1.5 text-[10px] opacity-70"></i></a>
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
      <span class="section-number">2</span> Definition
     </h2>
     
     <div class="content-text text-slate-800 font-medium bg-slate-50 border-l-4 border-brand-blue p-4 rounded-r-lg mb-6">
      The term "adverse family environments" refers to any clinically intervenable psychosocial risk factor or experience recorded in the child or the parent that met the <a href="https://acesinehrs.com/definitions" target="_blank" class="text-blue-700 font-bold hover:underline">pre-defined inclusion criteria</a>.
     </div>

     <p class="content-text">
      The AFE domain broadly aligns with the original ACE domain titled <em>"household challenges"</em> from the CDC-Kaiser ACE Study, supplemented with clinically relevant definitions to select indicators consistent with the <a href="https://www.gov.uk/government/publications/supporting-families-programme-guidance-2022-to-2025/chapter-4-identifying-and-working-with-families#identifying-and-evidencing-family-need" target="_blank" class="text-blue-600 font-medium hover:underline">UK guidance for identifying families in need</a>, and the <a href="https://jamanetwork.com/journals/jama/fullarticle/2783975" target="_blank" class="text-blue-600 font-medium hover:underline">US Preventive Services Task Force for social risk domains</a>.
     </p>

     <p class="content-text">
      The AFE domain includes indicators from multiple social risk domains covering clinical concerns relating to housing instability (e.g., homelessness), “criminal behaviours in the household”, food insecurity, education and financial strains, transportation difficulties, utility needs, and aspects of interpersonal safety that are not already addressed by other ACE domains.
     </p>

     <p class="content-text">
      This domain also incorporates <a href="https://bjgp.org/content/bjgp/62/600/e478.full.pdf" target="_blank" class="text-blue-600 font-medium hover:underline">Royal College of General Practitioners</a> recommended indicators for recordings that should raise a cause for concern (e.g., coded observations include various concerns in parent or child such as: <em>"life crisis", "concerned about appearance", "history of other physical trauma", "anger or aggressive behaviours", etc.</em>).
     </p>
    </section>

    <!-- 3. CLINICAL CODELIST -->
    <section id="codelists" class="scroll-mt-10">
     <h2 class="section-header justify-between">
      <div class="flex items-center"><span class="section-number">3</span> Clinical Codelist</div>
     </h2>
     
     <div class="flex flex-col sm:flex-row gap-3 mb-6">
      <!-- Download Button -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/AFE_2025ACEsinEHRs.txt" target="_blank" class="inline-flex items-center px-4 py-2 bg-blue-50 border border-blue-200 rounded-lg text-[13px] font-semibold text-blue-800 hover:bg-blue-100 shadow-sm transition-all hover:-translate-y-0.5" title="Right-click on link to save as a '.txt' file">
       <i class="fas fa-file-download text-blue-600 mr-2 text-lg"></i> Download AFE Codelist (2193 codes)
      </a>
     </div>

     <p class="content-text mb-6">
      See the <a href="https://github.com/shabeer-syed/acesinehrs/raw/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v2.pdf" target="_blank" class="text-blue-700 font-medium hover:underline"><i class="fas fa-file-pdf mr-1 text-blue-600"></i>ACEsinEHRs Control documentation</a> for code processing rules and release information.
     </p>

     <!-- Expandable Taxonomy Box (N Codes Excluded) -->
     <details class="expandable-box group mb-4">
      <summary class="expandable-summary">
       Indicator Structure & Taxonomy
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      <div class="expandable-content p-0 overflow-x-auto">
       <table class="custom-table min-w-full">
        <thead>
         <tr>
          <th style="width: 15%;">Domain</th>
          <th style="width: 20%;">Indicator Code</th>
          <th style="width: 65%;">Indicator Name</th>
         </tr>
        </thead>
        <tbody>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE1</td>
          <td class="font-medium text-slate-800">High-risk antenatal presentation, social-risk specific</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE2</td>
          <td class="font-medium text-slate-800">High-risk antenatal presentation, psychosocial NOS</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE3</td>
          <td class="font-medium text-slate-800">Unwanted/concealed pregnancy incl. attempted abortion of the current child</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE4</td>
          <td class="font-medium text-slate-800">Psychosocial health problem with lower-level intervention</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE5</td>
          <td class="font-medium text-slate-800">Health visitor increasing concern</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE6</td>
          <td class="font-medium text-slate-800">Family disruptions and parental conflicts NOS</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE7</td>
          <td class="font-medium text-slate-800">Parental separations</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE8</td>
          <td class="font-medium text-slate-800">Parent with legal problems</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE9</td>
          <td class="font-medium text-slate-800">Family is cause for concern (incl. maternal FGM, current rec. historic event)</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE10</td>
          <td class="font-medium text-slate-800">Problems related to negative childhood events</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE11</td>
          <td class="font-medium text-slate-800">Parent assaulted NOS (GP record only)</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE12</td>
          <td class="font-medium text-slate-800">Housing problems, effects of deprivation and refugee (excl. homelessness)</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE13</td>
          <td class="font-medium text-slate-800">Homelessness (child/parent)</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE14</td>
          <td class="font-medium text-slate-800">Vulnerable family NOS (incl. CPA)</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE15</td>
          <td class="font-medium text-slate-800">Family/parental support referral</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE16</td>
          <td class="font-medium text-slate-800">Problems related to psychosocial circumstances</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE17</td>
          <td class="font-medium text-slate-800">Learning or intellectual disability</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE18</td>
          <td class="font-medium text-slate-800">Parent lack capacity, increased concerns</td>
         </tr>
         <tr>
          <td><span class="domain-badge">AFE</span></td>
          <td class="font-mono text-xs font-semibold">AFE19</td>
          <td class="font-medium text-slate-800">Parental problems with daily living/limited capacity to work (incl. financial concerns)</td>
         </tr>
        </tbody>
       </table>
      </div>
     </details>
     
     <!-- Browse & Search Interactive Box -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       Browse & Search Clinical Codelist (Preview)
       <i class="fas fa-search text-slate-400 group-hover:text-brand-blue transition-colors ml-2 mr-auto text-sm"></i>
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      
      <div class="expandable-content p-0">
       <div class="bg-[#a3a3a3] px-5 py-3.5 text-white text-sm font-semibold flex justify-between items-center tracking-wide">
        <span>Adverse family environments | ALL CODING SYSTEMS</span>
       </div>

       <div class="p-5 bg-white">
        <div class="overflow-x-auto">
         <table id="codeSearchTable" class="custom-table w-full">
          <thead>
           <tr>
            <th style="width: 20%;">Code</th>
            <th style="width: 45%;">Description</th>
            <th style="width: 20%;">Coding System</th>
            <th style="width: 15%;">Indicator</th>
           </tr>
          </thead>
          <tbody>
           <!-- Sample codes for structure representation -->
           <tr><td class="font-mono">SN160824009</td><td>Housing problems</td><td>SNOMED CT</td><td><span class="hdr-pill !bg-slate-100 !border-slate-200 !text-slate-700">AFE12</span></td></tr>
           <tr><td class="font-mono">Z59.0</td><td>Homelessness</td><td>ICD-10</td><td><span class="hdr-pill !bg-slate-100 !border-slate-200 !text-slate-700">AFE13</span></td></tr>
           <tr><td class="font-mono">1L10.</td><td>Problems related to family circumstances</td><td>READ</td><td><span class="hdr-pill !bg-slate-100 !border-slate-200 !text-slate-700">AFE6</span></td></tr>
          </tbody>
         </table>
        </div>
       </div>
      </div>
     </details>
    </section>

    <!-- 4. IMPLEMENTATION RULES -->
    <section id="implementation" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">4</span> Implementation
     </h2>
     
     <!-- Compact Placeholder for Empty Implementation -->
     <div class="bg-slate-50 border border-slate-200 rounded-xl p-4 flex flex-col sm:flex-row items-start sm:items-center gap-4 shadow-sm mb-6">
      <div class="w-10 h-10 bg-white border border-slate-200 rounded-full flex shrink-0 items-center justify-center shadow-sm">
       <i class="fas fa-code-branch text-blue-500 text-base"></i>
      </div>
      <div>
       <h3 class="text-slate-800 font-semibold text-[15px] m-0 border-none">Standard Mapping Applied</h3>
       <p class="text-[14px] text-slate-500 mt-0.5 mb-0">
        No complex rule-based algorithms are currently required for the Adverse family environments domain beyond standard clinical code mapping.
       </p>
      </div>
     </div>

    </section>

    <!-- 5. PUBLICATIONS & REFERENCES -->
    <section id="publications" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">5</span> Publications
     </h2>
     
     <p class="content-text mb-6">Core research outputs associated with the Adverse family environments domain.</p>

     <div class="space-y-4 mb-10">
      <!-- Pub 1 -->
      <div class="pub-item">
       <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext" target="_blank" class="pub-link">
        Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England.
       </a>
       <p class="text-[14px] text-slate-500 m-0">Syed S, Gilbert R, Feder G, Howe LD, Powell C, Howarth E, Deighton J, Lacey RE. <em class="text-slate-700">The Lancet Public Health</em>. 2023.</p>
      </div>

      <!-- Pub 2 -->
      <div class="pub-item">
       <a href="https://www.thelancet.com/journals/landig/article/PIIS2589-7500(22)00061-9/fulltext" target="_blank" class="pub-link">
        Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study.
       </a>
       <p class="text-[14px] text-slate-500 m-0">Syed S, Gonzalez-Izquierdo A, Allister J, Feder G, Li L, Gilbert R. <em class="text-slate-700">The Lancet Digital Health</em>. 2022.</p>
      </div>

      <!-- Pub 3 -->
      <div class="pub-item">
       <a href="https://adc.bmj.com/content/106/1/44.full" target="_blank" class="pub-link">
        Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis.
       </a>
       <p class="text-[14px] text-slate-500 m-0">Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. <em class="text-slate-700">Archives of Disease in Childhood</em>. 2021.</p>
      </div>

      <!-- Pub 4 -->
      <div class="pub-item">
       <a href="https://onlinelibrary.wiley.com/doi/full/10.1111/cch.12134" target="_blank" class="pub-link">
        Notifications for child safeguarding from an acute hospital in response to presentations to healthcare by parents.
       </a>
       <p class="text-[14px] text-slate-500 m-0">Gonzalez‐Izquierdo A, Ward A, Smith P, Walford C, Begent J, Ioannou Y, Gilbert R. <em class="text-slate-700">Child: Care, Health and Development</em>. 2015.</p>
      </div>
     </div>

     <!-- Relevant References Sub-section -->
     <h3 class="text-[18px] font-bold text-slate-800 mb-4 border-none flex items-center">
      <i class="fas fa-bookmark text-blue-500 mr-2 text-sm"></i> Relevant References
     </h3>
     <div class="space-y-4">
      <div class="bg-slate-50 border border-slate-200 rounded-lg p-4">
       <a href="https://bmjopen.bmj.com/content/bmjopen/3/12/e003894.full.pdf" target="_blank" class="text-[14px] font-semibold text-blue-600 hover:text-blue-800 hover:underline leading-snug block mb-1">
        Responses to concerns about child maltreatment: a qualitative study of GPs in England.
       </a>
       <p class="text-[13px] text-slate-500 m-0">Woodman J, Gilbert R, Allister J, Glaser D, Brandon M. <em class="text-slate-700">BMJ Open</em>. 2013.</p>
      </div>
      
      <div class="bg-slate-50 border border-slate-200 rounded-lg p-4">
       <a href="https://bjgp.org/content/bjgp/62/600/e478.full.pdf" target="_blank" class="text-[14px] font-semibold text-blue-600 hover:text-blue-800 hover:underline leading-snug block mb-1">
        A simple approach to improve recording of concerns about child maltreatment in primary care records: developing a quality improvement intervention.
       </a>
       <p class="text-[13px] text-slate-500 m-0">Woodman J, Allister J, Rafi I, de Lusignan S, Belsey J, Petersen I, Gilbert R. <em class="text-slate-700">British Journal of General Practice</em>. 2012.</p>
      </div>

      <div class="bg-slate-50 border border-slate-200 rounded-lg p-4">
       <a href="https://jamanetwork.com/journals/jama/fullarticle/2783975" target="_blank" class="text-[14px] font-semibold text-blue-600 hover:text-blue-800 hover:underline leading-snug block mb-1">
        Screening and interventions for social risk factors: technical brief to support the US Preventive Services Task Force.
       </a>
       <p class="text-[13px] text-slate-500 m-0">Eder M, Henninger M, Durbin S, Iacocca MO, Martin A, Gottlieb LM, Lin JS. <em class="text-slate-700">JAMA</em>. 2021.</p>
      </div>
     </div>

     <div class="mt-12 pt-8 border-t border-slate-200">
      <a href="https://acesinehrs.com/ACE-domains/" class="inline-flex items-center text-slate-500 hover:text-brand-blue font-medium transition-colors text-sm">
       <i class="fas fa-arrow-left mr-2"></i> Back to all ACE Domains
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

<!-- DataTables Initialization Script -->
<script src="https://code.jquery.com/jquery-3.7.0.min.js"></script>
<script src="https://cdn.datatables.net/1.13.6/js/jquery.dataTables.min.js"></script>
<script>
 $(document).ready(function() {
  $('#codeSearchTable').DataTable({
   "pageLength": 10,
   "lengthMenu":[5, 10, 25, 50],
   "dom": '<"flex flex-col sm:flex-row justify-between items-start sm:items-center mb-4 gap-3"lf>rt<"flex flex-col sm:flex-row justify-between items-center mt-4 gap-3"ip>',
   "language": {
    "search": "",
    "searchPlaceholder": "Search codes or keywords...",
    "lengthMenu": "_MENU_ entries per page"
   }
  });
 });
</script>
