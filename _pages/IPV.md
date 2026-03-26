---
layout: splash
title: "Intimate partner violence"
permalink: /IPV/
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
      indigo: '#4f46e5', // Primary IPV Domain Color
      light: '#e0e7ff',
      dark: '#3730a3',
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
 .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.pub-link):not(.text-blue-600):not(.text-indigo-600):not(.data-source-link):not(.domain-nav-link) {
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
 .nav-item:hover .nav-dot { border-color: #4f46e5 !important; color: #4f46e5 !important; background-color: #e0e7ff !important; }
 
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
 .expandable-box[open] .expandable-icon { transform: rotate(180deg) !important; color: #4f46e5 !important; }
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
 .domain-badge { display: inline-flex !important; align-items: center !important; justify-content: center !important; padding: 0.25rem 0.5rem !important; border-radius: 0.25rem !important; font-size: 12px !important; font-weight: 700 !important; background: #e0e7ff !important; color: #3730a3 !important; }

 /* === DATATABLES OVERRIDES FOR TAILWIND/HDR UK LOOK === */
 .dataTables_wrapper .dataTables_filter input {
  border: 1px solid #cbd5e1 !important; border-radius: 0.375rem !important;
  padding: 0.35rem 0.75rem !important; margin-left: 0.5rem !important; outline: none !important;
  font-family: 'Inter', sans-serif !important; font-size: 13px !important; color: #334155 !important;
 }
 .dataTables_wrapper .dataTables_filter input:focus { border-color: #4f46e5 !important; box-shadow: 0 0 0 1px #4f46e5 !important; }
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
 .pub-item:hover { border-color: #818cf8 !important; box-shadow: 0 4px 6px -1px rgba(79, 70, 229, 0.05) !important; transform: translateY(-2px) !important; }
 .pub-link { font-size: 15px !important; font-weight: 600 !important; color: #2563eb !important; line-height: 1.5 !important; text-decoration: none !important; }
 .pub-link:hover { color: #1d4ed8 !important; text-decoration: underline !important; text-underline-offset: 3px !important; }

 html { scroll-behavior: smooth; }
</style>

<!-- Load Altmetric Embed Script -->
<script type="text/javascript" src="https://d1bxh8uas1mnw7.cloudfront.net/assets/embed.js" async></script>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

 <!-- HERO SECTION -->
 <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/Intimate%20partner%20violence%20aces%20in%20ehrs.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
  <div class="relative z-10 max-w-6xl mx-auto px-6 py-20 md:py-28 text-center md:text-left">
   <h1 class="hero-title drop-shadow-lg">
    Intimate partner <span style="color: #a5b4fc !important;">violence</span>
   </h1>
   <p class="hero-subtitle drop-shadow-md mx-auto md:mx-0">
    This domain includes indicators of intimate partner violence (IPV). The WHO defines IPV as any behaviour within an intimate relationship that causes physical, psychological or sexual harm to those in the relationship. IPV indicators are restricted to parents aged ≥16.
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

     <a href="https://acesinehrs.com/IPV/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-slate-800 border-2 border-slate-800 text-white text-[13px] font-semibold px-4 py-2 rounded-full shadow-md">
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

     <a href="https://acesinehrs.com/AFE/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-white border border-slate-300 text-slate-600 hover:text-slate-900 hover:border-slate-400 text-[13px] font-semibold px-4 py-2 rounded-full transition-all duration-200">
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
      <a href="#overview" class="text-sm font-semibold text-slate-600 hover:text-brand-indigo transition-colors border-none hover:bg-transparent">Overview</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">2</div>
      <a href="#definition" class="text-sm font-semibold text-slate-600 hover:text-brand-indigo transition-colors border-none hover:bg-transparent">Definition</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">3</div>
      <a href="#codelists" class="text-sm font-semibold text-slate-600 hover:text-brand-indigo transition-colors border-none hover:bg-transparent">Clinical Codelist</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">4</div>
      <a href="#implementation" class="text-sm font-semibold text-slate-600 hover:text-brand-indigo transition-colors border-none hover:bg-transparent">Implementation</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">5</div>
      <a href="#publications" class="text-sm font-semibold text-slate-600 hover:text-brand-indigo transition-colors border-none hover:bg-transparent">Publications</a>
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
        <span class="hdr-pill !bg-indigo-100 !text-indigo-800 !border-indigo-200">Intimate partner violence</span>
       </div>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Sex</div>
       <div class="py-2.5 px-4 md:col-span-3 flex items-center">
        <span class="hdr-pill !bg-slate-100 !text-slate-700 !border-slate-200">Both</span>
       </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Age Range</div>
       <div class="py-2.5 px-4 md:col-span-3 flex items-center">
        <span class="hdr-pill !bg-slate-100 !text-slate-700 !border-slate-200">16+ years (Parent), Any (Child exposure)</span>
       </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Individual</div>
       <div class="py-2.5 px-4 md:col-span-3 flex items-center gap-2">
        <span class="hdr-pill !bg-slate-100 !text-slate-700 !border-slate-200">Parent</span>
        <span class="hdr-pill !bg-slate-100 !text-slate-700 !border-slate-200">Child</span>
       </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4 border-b border-slate-100">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Coding System</div>
       <div class="py-2.5 px-4 md:col-span-3 flex flex-wrap gap-2">
        <span class="hdr-pill !bg-indigo-50 !text-indigo-700 !border-indigo-200">READ</span>
        <span class="hdr-pill !bg-indigo-50 !text-indigo-700 !border-indigo-200">SNOMED CT</span>
        <span class="hdr-pill !bg-indigo-50 !text-indigo-700 !border-indigo-200">ICD-10</span>
        <span class="hdr-pill !bg-indigo-50 !text-indigo-700 !border-indigo-200">ICD-9</span>
        <span class="hdr-pill !bg-indigo-50 !text-indigo-700 !border-indigo-200">HES-APC</span>
        <span class="hdr-pill !bg-indigo-50 !text-indigo-700 !border-indigo-200">HES-AE</span>
       </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4">
       <div class="bg-slate-50 py-2.5 px-4 text-slate-500 font-semibold md:border-r border-slate-100 flex items-center">Data Sources</div>
       <div class="py-2.5 px-4 md:col-span-3 flex flex-wrap gap-2">
        <a href="https://healthdatagateway.org/en/dataset/692" target="_blank" class="data-source-link">CPRD Aurum <i class="fas fa-external-link-alt ml-1.5 text-[10px] opacity-70"></i></a>
        <a href="https://healthdatagateway.org/en/dataset/694" target="_blank" class="data-source-link">CPRD GOLD <i class="fas fa-external-link-alt ml-1.5 text-[10px] opacity-70"></i></a>
        <a href="https://healthdatagateway.org/en/dataset/875" target="_blank" class="data-source-link">HES-APC <i class="fas fa-external-link-alt ml-1.5 text-[10px] opacity-70"></i></a>
        <a href="https://healthdatagateway.org/dataset/662" target="_blank" class="data-source-link">HES-AE <i class="fas fa-external-link-alt ml-1.5 text-[10px] opacity-70"></i></a>
       </div>
      </div>

     </div>
    </section>

    <!-- 2. DEFINITION -->
    <section id="definition" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">2</span> Definition
     </h2>
     
     <div class="content-text text-slate-800 font-medium bg-slate-50 border-l-4 border-brand-indigo p-4 rounded-r-lg mb-6">
      The <a href="https://www.sciencedirect.com/science/article/abs/pii/S0140673602111330" target="_blank" class="text-indigo-600 font-bold hover:underline">WHO</a> defines IPV as any behaviour within an intimate relationship that causes physical, psychological or sexual harm to adults who are, or have been, intimate partners or family members.
     </div>

     <p class="content-text">
      We restricted IPV indicators to parents aged ≥16 and their corresponding children to prevent misclassification of child maltreatment by the parents of younger parents.
     </p>

     <p class="content-text">
      <strong>Suspected IPV:</strong> Includes suspected indicators with coding terms mentioning historic IPV or maltreatment by an unspecified person. For instance, the "suspected IPV, NOS" indicator contains codes mentioning <em>"[X]Maltreatment, by acquaintance or friend"</em>, <em>"Risk of non-accidental injury"</em>, and <em>"Assault in the home"</em>.
     </p>
    </section>

    <!-- 3. CLINICAL CODELIST -->
    <section id="codelists" class="scroll-mt-10">
     <h2 class="section-header justify-between">
      <div class="flex items-center"><span class="section-number">3</span> Clinical Codelist</div>
     </h2>
     
     <div class="flex flex-col sm:flex-row gap-3 mb-6">
      <!-- File 1 -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/IPV_no_algo_2025ACEsinEHRs.txt" target="_blank" class="inline-flex items-center px-4 py-2 bg-white border border-slate-300 rounded-lg text-[13px] font-semibold text-slate-700 hover:bg-slate-50 hover:border-indigo-400 hover:text-indigo-700 shadow-sm transition-all hover:-translate-y-0.5">
       <i class="fas fa-file-download text-brand-indigo mr-2 text-lg"></i> Download IPV Codelist (2044 codes - excluding algo)
      </a>
      <!-- File 2 -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/IPV_2025ACEsinEHRs.txt" target="_blank" class="inline-flex items-center px-4 py-2 bg-indigo-50 border border-indigo-200 rounded-lg text-[13px] font-semibold text-indigo-800 hover:bg-indigo-100 shadow-sm transition-all hover:-translate-y-0.5">
       <i class="fas fa-file-code text-indigo-600 mr-2 text-lg"></i> Download IPV Codelist (3281 codes - incl. algo)
      </a>
     </div>

     <p class="content-text mb-6">
      See the <a href="https://github.com/shabeer-syed/acesinehrs/raw/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v2.pdf" target="_blank" class="text-indigo-600 font-medium hover:underline"><i class="fas fa-file-pdf mr-1 text-indigo-500"></i>ACEsinEHRs Control documentation</a> for code processing rules and release information.
     </p>

     <!-- Expandable Taxonomy Box -->
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
          <th style="width: 15%;">Indicator Code</th>
          <th style="width: 55%;">Indicator Name</th>
          <th style="width: 15%;">No. Codes</th>
         </tr>
        </thead>
        <tbody>
         <tr>
          <td><span class="domain-badge">IPV</span></td>
          <td class="font-mono text-xs font-semibold">IPV1</td>
          <td class="font-medium text-slate-800">IPV, NOS (incl. physical/sexual abuse)</td>
          <td class="font-mono text-xs text-slate-500">67</td>
         </tr>
         <tr>
          <td><span class="domain-badge">IPV</span></td>
          <td class="font-mono text-xs font-semibold">IPV2</td>
          <td class="font-medium text-slate-800">Mother assaulted + child protection recording or pregnant incident†</td>
          <td class="font-mono text-xs text-slate-500">554</td>
         </tr>
         <tr>
          <td><span class="domain-badge">IPV</span></td>
          <td class="font-mono text-xs font-semibold">IPV3</td>
          <td class="font-medium text-slate-800">Suspected IPV NOS</td>
          <td class="font-mono text-xs text-slate-500">33</td>
         </tr>
         <tr>
          <td><span class="domain-badge">IPV</span></td>
          <td class="font-mono text-xs font-semibold">IPV4</td>
          <td class="font-medium text-slate-800">Suspected IPV, physical or sexual abuse</td>
          <td class="font-mono text-xs text-slate-500">45</td>
         </tr>
         <tr>
          <td><span class="domain-badge">IPV</span></td>
          <td class="font-mono text-xs font-semibold">IPV5</td>
          <td class="font-medium text-slate-800">Mother assaulted NOS (hospital admission only)</td>
          <td class="font-mono text-xs text-slate-500">119</td>
         </tr>
         <tr>
          <td><span class="domain-badge">IPV</span></td>
          <td class="font-mono text-xs font-semibold">IPV6</td>
          <td class="font-medium text-slate-800">Mother assaulted + high-risk presentations (algorithm)†</td>
          <td class="font-mono text-xs text-slate-500">236</td>
         </tr>
        </tbody>
       </table>
      </div>
     </details>

    </section>

    <!-- 4. IMPLEMENTATION RULES -->
    <section id="implementation" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">4</span> Implementation
     </h2>
     <p class="content-text mb-6">
      Certain specific indicators within this domain require rule-based algorithms to prevent misclassification.
     </p>

     <!-- Expandable Rule 1 -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       <div class="flex items-center">
        <span class="bg-indigo-100 text-indigo-800 border border-indigo-200 text-[10px] uppercase font-bold px-2 py-0.5 rounded mr-3">Algorithm 1</span>
        Susp. IPV: Assault NOS & High-Risk (30/100 days)
       </div>
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      <div class="expandable-content border-t border-slate-100 bg-slate-50">
       <p class="text-[14px] text-slate-700 leading-relaxed mb-4 mt-0">
        Include as IPV if assault recording co-occurs with any <strong>"high-risk presentation recording"</strong> 30 days before the assault or in 100-days post the assault recording. High-risk recordings are a composite variable of recordings related to parental conflicts, health visitors being sent to the home, nurse partnership referrals, superficial head injuries and bruises. We developed the composite variable using results from our systematic review. In the current study, the algorithm showed PPVs ranging from 18%-30% of definitive IPV (derivation cohort).
       </p>
       <div class="code-container">
        <div class="code-header">
         <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
         <span class="text-[11px] text-slate-400 font-mono ml-2">R Script / Logic</span>
        </div>
        <pre class="code-pre"><code><span class="syntax-comment"># Logic flag for IPV high-risk presentation algorithm</span>
ipv_algo_high_risk &lt;- merged_data %&gt;%
  <span class="syntax-function">filter</span>(indicator == <span class="syntax-string">"Assault NOS"</span>) %&gt;%
  <span class="syntax-function">mutate</span>(
    is_ipv = <span class="syntax-function">ifelse</span>(
      (days_to_high_risk &gt;= -<span class="syntax-keyword">30</span> & days_to_high_risk &lt;= <span class="syntax-keyword">100</span>), 
      <span class="syntax-keyword">TRUE</span>, <span class="syntax-keyword">FALSE</span>
    )
  )</code></pre>
       </div>
      </div>
     </details>

     <!-- Expandable Rule 2 -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       <div class="flex items-center">
        <span class="bg-indigo-100 text-indigo-800 border border-indigo-200 text-[10px] uppercase font-bold px-2 py-0.5 rounded mr-3">Algorithm 2</span>
        Definitive IPV: Assault & Safeguarding/Pregnancy (45 days)
       </div>
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      <div class="expandable-content border-t border-slate-100 bg-slate-50">
       <p class="text-[14px] text-slate-700 leading-relaxed mb-4 mt-0">
        Include as IPV if assault recording co-occurs with any recordings of a safeguarding referral, child protection recording, definitive CM indicator, or <strong>"pregnant state, incidental"</strong> (marked in codelist) within 45 days of the assault. UK guidelines state 45 days is the maximum timeframe for an initial outcome following a children’s social care assessment from the date of received safeguarding referral (see point 82, <a href="https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf" target="_blank" class="text-indigo-600 hover:underline">working together to safeguard children</a>).
       </p>
       <div class="code-container">
        <div class="code-header">
         <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
         <span class="text-[11px] text-slate-400 font-mono ml-2">R Script / Logic</span>
        </div>
        <pre class="code-pre"><code><span class="syntax-comment"># Logic flag for IPV 45-day safeguarding/pregnancy algorithm</span>
ipv_algo_45_days &lt;- merged_data %&gt;%
  <span class="syntax-function">filter</span>(indicator == <span class="syntax-string">"Assault NOS"</span>) %&gt;%
  <span class="syntax-function">mutate</span>(
    is_ipv = <span class="syntax-function">ifelse</span>(
      (safeguarding_or_preg == <span class="syntax-keyword">TRUE</span> & <span class="syntax-function">abs</span>(days_between) &lt;= <span class="syntax-keyword">45</span>), 
      <span class="syntax-keyword">TRUE</span>, <span class="syntax-keyword">FALSE</span>
    )
  )</code></pre>
       </div>
      </div>
     </details>

    </section>

    <!-- 5. PUBLICATIONS -->
    <section id="publications" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">5</span> Publications
     </h2>
     <p class="content-text mb-6">Core research outputs associated with the Intimate partner violence domain.</p>

     <div class="space-y-4">
      
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

     </div>

     <div class="mt-12 pt-8 border-t border-slate-200">
      <a href="https://acesinehrs.com/ACE-domains/" class="inline-flex items-center text-slate-500 hover:text-brand-indigo font-medium transition-colors text-sm">
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
