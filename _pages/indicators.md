---
layout: splash
title: "All ACE domains & indicators"
permalink: /indicators/
author_profile: false
---
<!-- 1. Load Tailwind
 Safely -->
<script src="https://cdn.tailwindcss.com"></script>
<script>
 tailwind.config = {
  corePlugins: { preflight: false },
  theme: {
   extend: {
    colors: {
     brand: {
      slate: '#475569', // Primary Overview Color
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
 .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.pub-link):not(.data-source-link):not(.domain-nav-link):not(.download-card) {
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
 .nav-item:hover .nav-dot { border-color: #475569 !important; color: #475569 !important; background-color: #f1f5f9 !important; }
 
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
 .expandable-box[open] .expandable-icon { transform: rotate(180deg) !important; color: #475569 !important; }
 .expandable-content { padding: 1.25rem !important; background: #ffffff !important; }

 /* Content Typography */
 .content-text { font-size: 16px !important; line-height: 1.75 !important; color: #475569 !important; margin-bottom: 1.25rem !important; }
 
 /* === CUSTOM COMPACT TABLES === */
 .custom-table-compact { width: 100% !important; border-collapse: collapse !important; text-align: left !important; }
 .custom-table-compact th { background-color: #f8fafc !important; padding: 0.5rem 1rem !important; font-size: 12px !important; font-weight: 700 !important; color: #475569 !important; border-bottom: 2px solid #e2e8f0 !important; white-space: nowrap !important; }
 .custom-table-compact td { padding: 0.4rem 1rem !important; font-size: 13px !important; color: #334155 !important; border-bottom: 1px solid #f1f5f9 !important; }
 .domain-badge { display: inline-flex !important; align-items: center !important; justify-content: center !important; padding: 0.15rem 0.4rem !important; border-radius: 0.25rem !important; font-size: 11px !important; font-weight: 700 !important; }

 /* === DATATABLES OVERRIDES FOR TAILWIND/HDR UK LOOK === */
 .dataTables_wrapper .dataTables_filter input {
  border: 1px solid #cbd5e1 !important; border-radius: 0.375rem !important;
  padding: 0.35rem 0.75rem !important; margin-left: 0.5rem !important; outline: none !important;
  font-family: 'Inter', sans-serif !important; font-size: 13px !important; color: #334155 !important;
 }
 .dataTables_wrapper .dataTables_filter input:focus { border-color: #475569 !important; box-shadow: 0 0 0 1px #475569 !important; }
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

 /* Download Cards */
 .download-card { display: flex !important; align-items: center !important; gap: 1rem !important; padding: 1rem 1.25rem !important; border: 1px solid #e2e8f0 !important; border-radius: 0.75rem !important; background: #ffffff !important; transition: all 0.2s ease !important; text-decoration: none !important; }
 .download-card:hover { border-color: #cbd5e1 !important; box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; transform: translateY(-2px) !important; }
 .dl-icon-wrapper { width: 2.5rem !important; height: 2.5rem !important; border-radius: 0.5rem !important; display: flex !important; align-items: center !important; justify-content: center !important; font-size: 1.25rem !important; flex-shrink: 0 !important; }
 .dl-content { display: flex !important; flex-direction: column !important; }
 .dl-title { font-size: 14px !important; font-weight: 600 !important; color: #1e293b !important; line-height: 1.2 !important; margin-bottom: 0.25rem !important; border: none !important; }
 .dl-meta { font-size: 12px !important; color: #64748b !important; font-family: 'Fira Code', monospace !important; }

 html { scroll-behavior: smooth; }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

 <!-- HERO SECTION -->
 <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20home%20page%202023.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
  <div class="relative z-10 max-w-6xl mx-auto px-6 py-20 md:py-28 text-center md:text-left">
   <h1 class="hero-title drop-shadow-lg">
    All ACE <span style="color: #cbd5e1 !important;">domains & indicators</span>
   </h1>
   <p class="hero-subtitle drop-shadow-md mx-auto md:mx-0">
    View definitions of domains and indicators. Explore the master taxonomy and access comprehensive code list downloads for your research.
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
     
     <!-- Domain Nodes (ALL INDICATORS IS ACTIVE) -->
     <a href="https://acesinehrs.com/indicators/" class="domain-nav-link relative z-10 shrink-0 inline-flex items-center justify-center bg-slate-800 border-2 border-slate-800 text-white text-[13px] font-semibold px-4 py-2 rounded-full shadow-md">
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
      <a href="#master-list" class="text-sm font-semibold text-slate-600 hover:text-slate-900 transition-colors border-none hover:bg-transparent">Master Indicator List</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">2</div>
      <a href="#notices" class="text-sm font-semibold text-slate-600 hover:text-slate-900 transition-colors border-none hover:bg-transparent">Important Notices</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">3</div>
      <a href="#all-aces-downloads" class="text-sm font-semibold text-slate-600 hover:text-slate-900 transition-colors border-none hover:bg-transparent">All ACEs Code Lists</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">4</div>
      <a href="#domain-downloads" class="text-sm font-semibold text-slate-600 hover:text-slate-900 transition-colors border-none hover:bg-transparent">Domain Code Lists</a>
     </li>
     <li class="relative pl-6 nav-item">
      <div class="nav-dot">5</div>
      <a href="#exclusions" class="text-sm font-semibold text-slate-600 hover:text-slate-900 transition-colors border-none hover:bg-transparent">Exclusion Rules</a>
     </li>

    </ul>
   </div>

   <!-- MAIN CONTENT AREA -->
   <div class="flex-1 space-y-16">

    <!-- 1. MASTER INDICATOR LIST -->
    <section id="master-list" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">1</span> Master Indicator List
     </h2>
     
     <!-- EXPANDABLE COMPACT TABLE BOX -->
     <details class="expandable-box group">
      <summary class="expandable-summary">
       Comprehensive Taxonomy View
       <i class="fas fa-chevron-down expandable-icon"></i>
      </summary>
      
      <div class="expandable-content p-0">
       <div class="p-4">
        <div class="overflow-x-auto">
         <table id="masterTaxonomyTable" class="custom-table-compact w-full">
          <thead>
           <tr>
            <th style="width: 15%;">ACE Domain</th>
            <th style="width: 15%;">Indicator Code</th>
            <th style="width: 70%;">Indicator Name</th>
           </tr>
          </thead>
          <tbody>
           
           <!-- CM ROWS -->
           <tr class="bg-rose-50/40"><td data-sort="1"><span class="domain-badge bg-rose-100 text-rose-800">CM</span></td><td class="font-mono font-semibold">CM00</td><td class="font-semibold text-slate-800">Child maltreatment (CM)</td></tr>
           <tr><td data-sort="1"><span class="domain-badge bg-rose-100 text-rose-800">CM</span></td><td class="font-mono">CM1</td><td class="font-medium">Child protection/safeguarding</td></tr>
           <tr><td data-sort="1"><span class="domain-badge bg-rose-100 text-rose-800">CM</span></td><td class="font-mono">CM2</td><td class="font-medium">CM NOS, incl. physical or sexual abuse (merged)</td></tr>
           <tr><td data-sort="1"><span class="domain-badge bg-rose-100 text-rose-800">CM</span></td><td class="font-mono">CM3</td><td class="font-medium">Neglect (incl. NAS/FASD) and emotional/psychological abuse</td></tr>
           <tr><td data-sort="1"><span class="domain-badge bg-rose-100 text-rose-800">CM</span></td><td class="font-mono">CM4</td><td class="font-medium">Social service involved (incl. parental imprisonment/criminal activity)</td></tr>
           <tr><td data-sort="1"><span class="domain-badge bg-rose-100 text-rose-800">CM</span></td><td class="font-mono">CM5</td><td class="font-medium">Child in care</td></tr>
           <tr><td data-sort="1"><span class="domain-badge bg-rose-100 text-rose-800">CM</span></td><td class="font-mono">CM6</td><td class="font-medium">Suspected CM NOS (incl. neglect and social service involvements)</td></tr>
           <tr><td data-sort="1"><span class="domain-badge bg-rose-100 text-rose-800">CM</span></td><td class="font-mono">CM7</td><td class="font-medium">Child assaulted NOS (incl. physical/sexual abuse ≤10, rib fractures ≤3†)</td></tr>

           <!-- IPV ROWS -->
           <tr class="bg-amber-50/40"><td data-sort="2"><span class="domain-badge bg-amber-100 text-amber-800">IPV</span></td><td class="font-mono font-semibold">IPV00</td><td class="font-semibold text-slate-800">Intimate partner violence (IPV)</td></tr>
           <tr><td data-sort="2"><span class="domain-badge bg-amber-100 text-amber-800">IPV</span></td><td class="font-mono">IPV1</td><td class="font-medium">IPV, NOS (incl. physical/sexual abuse)</td></tr>
           <tr><td data-sort="2"><span class="domain-badge bg-amber-100 text-amber-800">IPV</span></td><td class="font-mono">IPV2</td><td class="font-medium">Mother assaulted + child protection recording or pregnant incident†</td></tr>
           <tr><td data-sort="2"><span class="domain-badge bg-amber-100 text-amber-800">IPV</span></td><td class="font-mono">IPV3</td><td class="font-medium">Suspected IPV NOS</td></tr>
           <tr><td data-sort="2"><span class="domain-badge bg-amber-100 text-amber-800">IPV</span></td><td class="font-mono">IPV4</td><td class="font-medium">Suspected IPV, physical or sexual abuse</td></tr>
           <tr><td data-sort="2"><span class="domain-badge bg-amber-100 text-amber-800">IPV</span></td><td class="font-mono">IPV5</td><td class="font-medium">Mother assaulted NOS (hospital admission only)</td></tr>
           <tr><td data-sort="2"><span class="domain-badge bg-amber-100 text-amber-800">IPV</span></td><td class="font-mono">IPV6</td><td class="font-medium">Mother assaulted + high-risk presentations (algorithm)†</td></tr>

           <!-- HRP-CM ROWS -->
           <tr class="bg-purple-50/40"><td data-sort="3"><span class="domain-badge bg-purple-100 text-purple-800">HRP-CM</span></td><td class="font-mono font-semibold">HRPCM00</td><td class="font-semibold text-slate-800">High-risk presentations of CM (HRP-CM)</td></tr>
           <tr><td data-sort="3"><span class="domain-badge bg-purple-100 text-purple-800">HRP-CM</span></td><td class="font-mono">HRPCM1</td><td class="font-medium">Bruising & contusions ≤3†</td></tr>
           <tr><td data-sort="3"><span class="domain-badge bg-purple-100 text-purple-800">HRP-CM</span></td><td class="font-mono">HRPCM2</td><td class="font-medium">Superficial injuries of head, neck or multiple body parts ≤3†</td></tr>
           <tr><td data-sort="3"><span class="domain-badge bg-purple-100 text-purple-800">HRP-CM</span></td><td class="font-mono">HRPCM3</td><td class="font-medium">Thermal injuries - head, face or neck ≤3†</td></tr>
           <tr><td data-sort="3"><span class="domain-badge bg-purple-100 text-purple-800">HRP-CM</span></td><td class="font-mono">HRPCM4</td><td class="font-medium">Thermal injuries - trunk, back or trachea ≤3†</td></tr>
           <tr><td data-sort="3"><span class="domain-badge bg-purple-100 text-purple-800">HRP-CM</span></td><td class="font-mono">HRPCM5</td><td class="font-medium">Skull fractures or intracranial crush injury ≤3†</td></tr>
           <tr><td data-sort="3"><span class="domain-badge bg-purple-100 text-purple-800">HRP-CM</span></td><td class="font-mono">HRPCM6</td><td class="font-medium">Child harm by undetermined intent - rare injuries & life-threatening events (retinal haemorrhages, drownings, SUDI, firearm etc.) ≤10†</td></tr>
           <tr><td data-sort="3"><span class="domain-badge bg-purple-100 text-purple-800">HRP-CM</span></td><td class="font-mono">HRPCM7</td><td class="font-medium">Child harm by undetermined intent - exposure to unspecified factor≤10†</td></tr>
           <tr><td data-sort="3"><span class="domain-badge bg-purple-100 text-purple-800">HRP-CM</span></td><td class="font-mono">HRPCM8</td><td class="font-medium">Failure to thrive (excessive thirst, suspected malnutrition) ≤10†</td></tr>
           <tr><td data-sort="3"><span class="domain-badge bg-purple-100 text-purple-800">HRP-CM</span></td><td class="font-mono">HRPCM9</td><td class="font-medium">Non-attendance of child appointment (≥3 appts. within 2-years) ≤10†</td></tr>

           <!-- SM ROWS -->
           <tr class="bg-emerald-50/40"><td data-sort="4"><span class="domain-badge bg-emerald-100 text-emerald-800">SM</span></td><td class="font-mono font-semibold">SM00</td><td class="font-semibold text-slate-800">Parental substance misuse (SM)</td></tr>
           <tr><td data-sort="4"><span class="domain-badge bg-emerald-100 text-emerald-800">SM</span></td><td class="font-mono">SM1</td><td class="font-medium">Drug misuse, severe (dependence levels)</td></tr>
           <tr><td data-sort="4"><span class="domain-badge bg-emerald-100 text-emerald-800">SM</span></td><td class="font-mono">SM2</td><td class="font-medium">Drug misuse, moderate (all other)</td></tr>
           <tr><td data-sort="4"><span class="domain-badge bg-emerald-100 text-emerald-800">SM</span></td><td class="font-mono">SM3</td><td class="font-medium">Drug prescription for opioid dependence, multipurpose usage</td></tr>
           <tr><td data-sort="4"><span class="domain-badge bg-emerald-100 text-emerald-800">SM</span></td><td class="font-mono">SM4</td><td class="font-medium">Family substance misuse (i.e. unspecified family member)</td></tr>
           <tr><td data-sort="4"><span class="domain-badge bg-emerald-100 text-emerald-800">SM</span></td><td class="font-mono">SM5</td><td class="font-medium">Alcohol misuse, severe (incl. self-report measures/≥35 alcohol units per week103)†</td></tr>

           <!-- AFE ROWS -->
           <tr class="bg-blue-50/40"><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono font-semibold">AFE00</td><td class="font-semibold text-slate-800">Adverse family environments (AFE)</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE1</td><td class="font-medium">High-risk antenatal presentation, social-risk specific</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE2</td><td class="font-medium">High-risk antenatal presentation, psychosocial NOS</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE3</td><td class="font-medium">Unwanted/concealed pregnancy incl. attempted abortion of the current child</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE4</td><td class="font-medium">Psychosocial health problem with lower-level intervention</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE5</td><td class="font-medium">Health visitor increasing concern</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE6</td><td class="font-medium">Family disruptions and parental conflicts NOS</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE7</td><td class="font-medium">Parental separations</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE8</td><td class="font-medium">Parent with legal problems</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE9</td><td class="font-medium">Family is cause for concern (incl. maternal FGM, current rec. historic event)</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE10</td><td class="font-medium">Problems related to negative childhood events</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE11</td><td class="font-medium">Mother assaulted NOS (GP record only)</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE12</td><td class="font-medium">Housing problems, effects of deprivation and refugee (excl. homelessness)</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE13</td><td class="font-medium">Homelessness (child/mother)</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE14</td><td class="font-medium">Vulnerable family NOS (incl. CPA)</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE15</td><td class="font-medium">Family/parental support referral</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE16</td><td class="font-medium">Problems related to psychosocial circumstances</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE17</td><td class="font-medium">Learning or intellectual disability</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE18</td><td class="font-medium">Increased concerns of parental capacity</td></tr>
           <tr><td data-sort="5"><span class="domain-badge bg-blue-100 text-blue-800">AFE</span></td><td class="font-mono">AFE19</td><td class="font-medium">Parental problems with daily living/limited capacity to work (incl. financial concerns)</td></tr>

           <!-- MHPs ROWS -->
           <tr class="bg-teal-50/40"><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono font-semibold">MHP00</td><td class="font-semibold text-slate-800">Parental mental health problems (MHPs)</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP</td><td class="font-medium">Common mental health problems</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP1</td><td class="font-medium">Depression incl. antidepressants†</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP2</td><td class="font-medium">Self-harm or suicide attempts</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP3</td><td class="font-medium">Anxiety disorder NOS incl. anxiolytics†</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP4</td><td class="font-medium">Panic disorder (incl. agoraphobia, health anxiety)</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP5</td><td class="font-medium">Obsessive-compulsive disorders</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP6</td><td class="font-medium">PTSD incl. acute stress disorder</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP7</td><td class="font-medium">Sleep-wake disorders</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP8</td><td class="font-medium">Mental health problems NOS</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP9</td><td class="font-medium">Referred/seen by a mental health professional (≥tier 3 profession)</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP10</td><td class="font-medium">Puerperal mental health problem NOS</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP11</td><td class="font-medium">Anorexia nervosa</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP12</td><td class="font-medium">Eating disorders NOS (incl. Bulimia)</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP13</td><td class="font-medium">Psychosis incl. mental health sections NOS</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP14</td><td class="font-medium">Antipsychotics (1st-2nd gen & NOS)</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP15</td><td class="font-medium">Bipolar disorders</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP16</td><td class="font-medium">Personality disorders (e.g. BPD)</td></tr>
           <tr><td data-sort="6"><span class="domain-badge bg-teal-100 text-teal-800">MHPs</span></td><td class="font-mono">MHP17</td><td class="font-medium">Neurodevelopmental conditions and conduct disorders</td></tr>

          </tbody>
         </table>
        </div>
       </div>
      </div>
     </details>
    </section>

    <!-- 2. NOTICES -->
    <section id="notices" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">2</span> Important Notices
     </h2>

     <div class="space-y-4">
      <!-- Info Notice -->
      <div class="bg-blue-50 border border-blue-200 rounded-xl p-4 flex gap-4 shadow-sm">
       <div class="w-10 h-10 rounded-full bg-white flex shrink-0 items-center justify-center text-blue-600 shadow-sm">
        <i class="fas fa-users text-lg"></i>
       </div>
       <div>
        <h4 class="text-blue-900 font-bold text-[15px] m-0 border-none mb-1">Think-family approach</h4>
        <p class="text-[14px] text-blue-800 m-0 leading-relaxed">
         Unless specified, indicators refer to information recorded in the child, mother and father.
        </p>
       </div>
      </div>

      <!-- Danger Notice -->
      <div class="bg-rose-50 border border-rose-200 rounded-xl p-4 flex gap-4 shadow-sm">
       <div class="w-10 h-10 rounded-full bg-white flex shrink-0 items-center justify-center text-rose-600 shadow-sm">
        <i class="fas fa-exclamation-triangle text-lg"></i>
       </div>
       <div>
        <h4 class="text-rose-900 font-bold text-[15px] m-0 border-none mb-1">Implementation Rules Required</h4>
        <p class="text-[14px] text-rose-800 m-0 leading-relaxed">
         The indicators use <a href="https://advanced-r-solutions.rbind.io/control-flow.html" target="_blank" class="font-semibold underline hover:text-rose-900">control flow methods</a> to implement rule-based algorithms. These must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth.
        </p>
       </div>
      </div>
     </div>
    </section>

    <!-- 3. ALL ACEs DOWNLOADS -->
    <section id="all-aces-downloads" class="scroll-mt-10">
     <div class="flex justify-between items-end mb-4 border-b border-slate-200 pb-3">
      <h2 class="text-2xl font-bold text-slate-900 m-0 border-none flex items-center">
       <span class="section-number">3</span> All ACEs Code Lists
      </h2>
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v3.pdf" target="_blank" class="text-sm font-semibold text-blue-600 hover:text-blue-800 hover:underline">
       <i class="fas fa-file-pdf mr-1"></i> Control Documentation v3
      </a>
     </div>
     
     <p class="text-sm text-slate-500 mb-6 font-medium">Right-click on a link to save as a ".txt" file (i.e. using option "save link as"). Total included ACE codes: 23,164</p>

     <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025ACEsinEHRs.txt" target="_blank" class="download-card border-slate-300">
       <div class="dl-icon-wrapper bg-slate-100 text-slate-600"><i class="fas fa-file-alt"></i></div>
       <div class="dl-content">
        <span class="dl-title">All ACEs Master List</span>
        <span class="dl-meta">23,164 codes</span>
       </div>
      </a>
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025_medcode_prodcode_CPRD_GOLD_Aurum_ACEsinEHRs.txt" target="_blank" class="download-card border-slate-300">
       <div class="dl-icon-wrapper bg-slate-100 text-slate-600"><i class="fas fa-laptop-medical"></i></div>
       <div class="dl-content">
        <span class="dl-title">GP/CPRD GOLD/AURUM Only</span>
        <span class="dl-meta">20,925 codes</span>
       </div>
      </a>
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/ACEs_2025_ICD910_special_fields_HES_ACEsinEHRs.txt" target="_blank" class="download-card border-slate-300 md:col-span-2 lg:col-span-1">
       <div class="dl-icon-wrapper bg-slate-100 text-slate-600"><i class="fas fa-hospital"></i></div>
       <div class="dl-content">
        <span class="dl-title">Hospital Only (ICD/HES)</span>
        <span class="dl-meta">2,239 codes</span>
       </div>
      </a>
     </div>
    </section>

    <!-- 4. DOMAIN DOWNLOADS -->
    <section id="domain-downloads" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">4</span> Domain Code Lists
     </h2>
     
     <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
      
      <!-- CM -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/CM_2025ACEsinEHRs.txt" target="_blank" class="download-card border-rose-200 hover:border-rose-400">
       <div class="dl-icon-wrapper bg-rose-50 text-rose-600"><i class="fas fa-child"></i></div>
       <div class="dl-content">
        <span class="dl-title group-hover:text-rose-700">Child Maltreatment (CM)</span>
        <span class="dl-meta">3,852 codes</span>
       </div>
      </a>

      <!-- HRP-CM -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/HRPCM_2025ACEsinEHRs.txt" target="_blank" class="download-card border-purple-200 hover:border-purple-400">
       <div class="dl-icon-wrapper bg-purple-50 text-purple-600"><i class="fas fa-exclamation-circle"></i></div>
       <div class="dl-content">
        <span class="dl-title group-hover:text-purple-700">High-risk Presentation of CM</span>
        <span class="dl-meta">1,774 codes</span>
       </div>
      </a>

      <!-- IPV (Algorithms Included) -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/IPV_2025ACEsinEHRs.txt" target="_blank" class="download-card border-indigo-200 hover:border-indigo-400">
       <div class="dl-icon-wrapper bg-indigo-50 text-indigo-600"><i class="fas fa-user-injured"></i></div>
       <div class="dl-content">
        <span class="dl-title group-hover:text-indigo-700">Intimate Partner Violence</span>
        <span class="dl-meta">3,281 codes (incl. algorithms)</span>
       </div>
      </a>

      <!-- IPV (No Algorithms) -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/IPV_no_algo_2025ACEsinEHRs.txt" target="_blank" class="download-card border-indigo-100 hover:border-indigo-300">
       <div class="dl-icon-wrapper bg-slate-50 text-indigo-400"><i class="fas fa-file-code"></i></div>
       <div class="dl-content">
        <span class="dl-title text-slate-600">IPV (Base List Only)</span>
        <span class="dl-meta">2,044 codes (excl. algorithms)</span>
       </div>
      </a>

      <!-- SM -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/SM_2025ACEsinEHRs.txt" target="_blank" class="download-card border-amber-200 hover:border-amber-400">
       <div class="dl-icon-wrapper bg-amber-50 text-amber-600"><i class="fas fa-wine-glass-alt"></i></div>
       <div class="dl-content">
        <span class="dl-title group-hover:text-amber-700">Parental Substance Misuse</span>
        <span class="dl-meta">2,886 codes</span>
       </div>
      </a>

      <!-- AFE -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/AFE_2025ACEsinEHRs.txt" target="_blank" class="download-card border-blue-200 hover:border-blue-400">
       <div class="dl-icon-wrapper bg-blue-50 text-blue-600"><i class="fas fa-home"></i></div>
       <div class="dl-content">
        <span class="dl-title group-hover:text-blue-700">Adverse Family Environments</span>
        <span class="dl-meta">2,308 codes</span>
       </div>
      </a>

      <!-- MHPs -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/MHP_2025ACEsinEHRs.txt" target="_blank" class="download-card border-emerald-200 hover:border-emerald-400 md:col-span-2 lg:col-span-1">
       <div class="dl-icon-wrapper bg-emerald-50 text-emerald-600"><i class="fas fa-brain"></i></div>
       <div class="dl-content">
        <span class="dl-title group-hover:text-emerald-700">Parental Mental Health Problems</span>
        <span class="dl-meta">9,063 codes</span>
       </div>
      </a>

      <!-- Covariates -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Health%20comorbidities.txt" target="_blank" class="download-card border-slate-300 hover:border-slate-500 md:col-span-2 lg:col-span-1 bg-slate-50">
       <div class="dl-icon-wrapper bg-white text-slate-700 shadow-sm"><i class="fas fa-plus-circle"></i></div>
       <div class="dl-content">
        <span class="dl-title text-slate-800">Covariates (Non-ACEs)</span>
        <span class="dl-meta">8,808 codes (Health comorbidities)</span>
       </div>
      </a>

     </div>
    </section>

    <!-- 5. EXCLUSION RULES -->
    <section id="exclusions" class="scroll-mt-10">
     <h2 class="section-header">
      <span class="section-number">5</span> Exclusion Rules Code Lists
     </h2>
     
     <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/Accident_excl_2025ACEsinEHRs.txt" target="_blank" class="download-card border-slate-200 hover:border-rose-300">
       <div class="dl-icon-wrapper bg-slate-50 text-slate-500"><i class="fas fa-car-crash"></i></div>
       <div class="dl-content">
        <span class="dl-title">Accidents</span>
        <span class="dl-meta">3,356 codes</span>
       </div>
      </a>
      
      <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Osteoporosis%20Bone%20disease.txt" target="_blank" class="download-card border-slate-200 hover:border-rose-300">
       <div class="dl-icon-wrapper bg-slate-50 text-slate-500"><i class="fas fa-bone"></i></div>
       <div class="dl-content">
        <span class="dl-title">Osteoporosis / Bone Disease</span>
        <span class="dl-meta">406 codes</span>
       </div>
      </a>

      <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Birth%20injury%20or%20complication.txt" target="_blank" class="download-card border-slate-200 hover:border-rose-300">
       <div class="dl-icon-wrapper bg-slate-50 text-slate-500"><i class="fas fa-baby"></i></div>
       <div class="dl-content">
        <span class="dl-title">Birth Injuries/Complications</span>
        <span class="dl-meta">238 codes</span>
       </div>
      </a>

      <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Mother-to-child%20transmission.txt" target="_blank" class="download-card border-slate-200 hover:border-rose-300">
       <div class="dl-icon-wrapper bg-slate-50 text-slate-500"><i class="fas fa-virus"></i></div>
       <div class="dl-content">
        <span class="dl-title">Mother-to-Child Transmissions</span>
        <span class="dl-meta">15 codes</span>
       </div>
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
  $('#masterTaxonomyTable').DataTable({
   "pageLength": 15,
   "lengthMenu":[10, 15, 25, 50, 100],
   "order": [[0, "asc"]], // Defaults to Domain column sorting based on data-sort
   "dom": '<"flex flex-col sm:flex-row justify-between items-start sm:items-center mb-4 gap-3"lf>rt<"flex flex-col sm:flex-row justify-between items-center mt-4 gap-3"ip>',
   "language": {
    "search": "",
    "searchPlaceholder": "Search indicators or codes...",
    "lengthMenu": "_MENU_ entries per page"
   }
  });
 });
</script>
