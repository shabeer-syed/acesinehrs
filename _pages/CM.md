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
  corePlugins: { preflight: false },
  theme: {
   extend: {
    colors: {
     brand: {
      rose: '#e11d48', // Primary CM Domain Color
      light: '#ffe4e6',
      dark: '#be123c',
     }
    }
   }
  }
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
  background-color: #f8fafc !important; /* Soft premium background */
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
 .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.pub-link):not(.text-blue-600):not(.text-rose-600) {
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
  margin-top: 0 !important; margin-bottom: 1rem !important; border: none !important; padding: 0 !important;
  letter-spacing: -0.02em !important;
 }
 .content-subheading {
  font-size: 20px !important; font-weight: 600 !important; color: #1e293b !important;
  margin-bottom: 1rem !important; margin-top: 0 !important; border: none !important;
 }
 .content-text {
  font-size: 16px !important; line-height: 1.75 !important; color: #475569 !important; margin-bottom: 1.25rem !important;
 }

 /* Premium Box Panels */
 .panel-card {
  background-color: #ffffff !important; border-radius: 1.25rem !important; border: 1px solid #e2e8f0 !important;
  box-shadow: 0 4px 6px -1px rgba(0,0,0,0.02), 0 10px 15px -3px rgba(0,0,0,0.03) !important;
  padding: 2rem !important; display: flex !important; flex-direction: column !important;
 }

 /* Code Blocks */
 .code-container {
  background: #0d1117 !important; border-radius: 0.75rem !important; overflow: hidden !important;
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1) !important;
 }
 .code-header {
  background: #161b22 !important; padding: 0.5rem 1rem !important; border-bottom: 1px solid #30363d !important;
  display: flex !important; align-items: center !important; gap: 0.5rem !important;
 }
 .code-window-dot { width: 12px !important; height: 12px !important; border-radius: 50% !important; }
 .code-pre {
  padding: 1rem 1.25rem !important; overflow-x: auto !important; margin: 0 !important;
  font-family: 'Fira Code', monospace !important; font-size: 13px !important; line-height: 1.6 !important; color: #c9d1d9 !important;
 }
 .syntax-keyword { color: #ff7b72 !important; }
 .syntax-string { color: #a5d6ff !important; }
 .syntax-function { color: #d2a8ff !important; }
 .syntax-comment { color: #8b949e !important; font-style: italic !important; }

 /* SaaS Table Styles */
 .table-wrapper {
  background: #ffffff !important; border-radius: 1.25rem !important; border: 1px solid #e2e8f0 !important;
  box-shadow: 0 4px 6px -1px rgba(0,0,0,0.02), 0 10px 15px -3px rgba(0,0,0,0.03) !important;
  overflow: hidden !important; overflow-x: auto !important;
 }
 .custom-table { width: 100% !important; border-collapse: collapse !important; text-align: left !important; }
 .custom-table th { 
  background-color: #f8fafc !important; padding: 1.25rem 1.5rem !important; font-size: 13px !important; 
  font-weight: 700 !important; color: #475569 !important; text-transform: uppercase !important; 
  letter-spacing: 0.05em !important; border-bottom: 2px solid #e2e8f0 !important; white-space: nowrap !important;
 }
 .custom-table td { 
  padding: 1.25rem 1.5rem !important; font-size: 15px !important; color: #334155 !important; 
  border-bottom: 1px solid #f1f5f9 !important; vertical-align: middle !important;
 }
 .custom-table tr:last-child td { border-bottom: none !important; }
 .custom-table tr:hover { background-color: #f8fafc !important; }

 /* Domain Pill Badge */
 .domain-badge {
  display: inline-flex !important; align-items: center !important; justify-content: center !important;
  padding: 0.25rem 0.75rem !important; border-radius: 9999px !important; font-size: 12px !important;
  font-weight: 700 !important; letter-spacing: 0.025em !important;
 }

 /* PUBLICATION LIST */
 .pub-item {
  display: flex !important; flex-direction: column !important; gap: 0.5rem !important;
  padding: 1.5rem !important; border: 1px solid #e2e8f0 !important; border-radius: 1rem !important;
  background: #ffffff !important; margin-bottom: 1rem !important; transition: all 0.3s ease !important;
 }
 .pub-item:hover { 
  border-color: #fda4af !important; 
  box-shadow: 0 10px 15px -3px rgba(225, 29, 72, 0.05) !important; 
  transform: translateY(-2px) !important;
 }
 .pub-link {
  font-size: 16px !important; font-weight: 600 !important; color: #2563eb !important; line-height: 1.5 !important;
  text-decoration: none !important; transition: color 0.2s !important; border: none !important;
 }
 .pub-link:hover { color: #1d4ed8 !important; text-decoration: underline !important; text-underline-offset: 3px !important; }

 html { scroll-behavior: smooth; }
</style>

<!-- Load Altmetric Embed Script -->
<script type="text/javascript" src="https://d1bxh8uas1mnw7.cloudfront.net/assets/embed.js" async></script>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

 <!-- ORIGINAL HERO SECTION RESTORED & THEMED -->
 <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/Child%20maltreatment%20aces%20in%20ehrs.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
  <div class="relative z-10 max-w-5xl mx-auto px-6 py-24 md:py-32 text-center md:text-left">
   <h1 class="hero-title drop-shadow-lg">
    Child <span style="color: #fda4af !important;">maltreatment</span>
   </h1>
   <p class="hero-subtitle drop-shadow-md mx-auto md:mx-0">
    This domain includes indicators of child maltreatment (CM). CM refers to any act of commission or omission by a parent or other caregiver that results in harm, potential for harm, or threat of harm to a child. Harm does not need to be intended.
   </p>
  </div>
 </header>

 <main class="flex-grow">
  
  <!-- SECTION 1: DEFINITIONS & QUICK INFOS -->
  <section class="bg-white py-16 border-b border-slate-200">
   <div class="max-w-4xl mx-auto px-6">
    
    <div class="flex items-center gap-3 mb-6">
     <div class="w-12 h-12 rounded-full bg-slate-100 text-slate-700 flex items-center justify-center shrink-0">
      <i class="fas fa-book-open text-xl"></i>
     </div>
     <h2 class="content-heading text-slate-900 !mb-0">Definition</h2>
    </div>

    <p class="content-text text-slate-700 text-lg font-medium">
     Any recorded act of commission or omission by a parent or caregiver resulting in harm, the potential for harm or threat of child harm, including neglect, psychological, physical, sexual and emotional abuse. Harm does not need to be intended <sup><a href="https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(08)61706-7/fulltext" target="_blank" class="text-blue-600 hover:underline">1</a></sup>. 
    </p>
     
    <p class="content-text text-slate-600">
     In the UK, <a href="https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf" target="_blank" class="text-blue-600 hover:underline font-medium">statutory guidelines of CM</a> include child exposure to IPV, and maternal evidence for omission or commission during pregnancy such as Neonatal Abstinence Syndrome (NAS) and Fetal Alcohol Syndrome (FAS). It includes indicators such as neglect (pre- and post-birth), child protection recordings, or out-of-home placements by social care services.
    </p>

    <p class="content-text text-slate-600 !mb-0">
     <strong class="text-slate-800">Suspected CM:</strong> Includes any maltreatment-related indicator with codes describing presentations likely to refer to CM, but without mentioning the underlying cause (e.g., harm caused by non-specified person), safeguarding procedures, or social interventions. <em class="text-rose-800">E.g., "Victim of sexual abuse", "Assault in the home".</em>
    </p>

   </div>
  </section>

  <!-- SECTION 2: ASSETS & IMPLEMENTATION -->
  <section class="bg-slate-50 pt-16 pb-12">
   <div class="max-w-5xl mx-auto px-6">
    
    <!-- Side-by-Side Cards (items-start prevents the gap stretching issue) -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12 items-start">
      
     <!-- DOWNLOAD CARD -->
     <div class="panel-card relative overflow-hidden group">
      <div class="absolute top-0 left-0 w-full h-1.5 bg-brand-rose"></div>
       
      <h3 class="content-subheading !mt-0 flex items-center">
       <i class="fas fa-cloud-download-alt text-brand-rose mr-3"></i> Code list download
      </h3>
      <p class="text-sm text-slate-500 mb-6">Access the complete set of clinical codes mapped to the CM domain.</p>
       
      <!-- Download Button Component -->
      <a href="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/codelists/CM_2025ACEsinEHRs.txt" target="_blank" class="block w-full border border-slate-200 rounded-xl p-4 hover:border-brand-rose hover:bg-rose-50 transition-colors group/btn mb-6 shadow-sm hover:shadow">
       <div class="flex items-center justify-between">
        <div>
         <h4 class="text-base font-bold text-slate-800 m-0 group-hover/btn:text-brand-rose transition-colors">Child maltreatment (.txt)</h4>
         <p class="text-xs text-slate-500 mt-1 mb-0 font-medium tracking-wide uppercase">3,852 codes included</p>
        </div>
        <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-slate-600 group-hover/btn:bg-brand-rose group-hover/btn:text-white transition-all transform group-hover/btn:scale-105">
         <i class="fas fa-arrow-down"></i>
        </div>
       </div>
      </a>

      <a href="https://github.com/shabeer-syed/acesinehrs/raw/master/assets/control_documentation/ACEsinEHRs%20Control%20documentation%20v2.pdf" target="_blank" class="inline-flex items-center text-[14px] text-blue-600 hover:text-blue-800 font-semibold group/pdf">
       <i class="fas fa-file-pdf text-rose-500 mr-2 group-hover/pdf:scale-110 transition-transform"></i> ACEsinEHRs control documentation
      </a>
     </div>

     <!-- RULES CARD (Expanded for multiple algorithms) -->
     <div class="panel-card relative overflow-hidden">
      <div class="absolute top-0 left-0 w-full h-1.5 bg-slate-800"></div>
       
      <h3 class="content-subheading !mt-0 flex items-center mb-6">
       <i class="fas fa-code-branch text-slate-700 mr-3"></i> Implementation Rules
      </h3>
      <p class="text-[14.5px] text-slate-600 mb-8 leading-relaxed">
       Certain specific indicators within this domain require rule-based algorithms to prevent misclassification.
      </p>

      <!-- Rule 1 -->
      <div class="mb-8 pb-8 border-b border-slate-100">
       <div class="bg-slate-100 border border-slate-200 rounded-lg p-2.5 mb-3 inline-flex items-center w-max">
        <span class="text-[11px] font-bold text-slate-500 uppercase tracking-wider mr-2">Applies to:</span>
        <span class="text-xs font-bold text-slate-800 bg-white px-2 py-0.5 rounded shadow-sm">CM, FGM</span>
       </div>
       <p class="text-[14px] text-slate-600 mb-4 leading-relaxed mt-0">
        Apply codes mentioning circumcision to female children only (e.g. <em>"54314 - routine or ritual circumcision"</em>). Code list includes markers for rule inclusion.
       </p>
       <div class="code-container">
        <div class="code-header">
         <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
         <span class="text-[11px] text-slate-400 font-mono ml-2">R Script</span>
        </div>
        <pre class="code-pre"><code>cm_fgm &lt;- merged_data %&gt;% 
  <span class="syntax-function">filter</span>(Domain==<span class="syntax-string">"CM"</span> & individual==<span class="syntax-string">"4"</span> & gender==<span class="syntax-string">"female"</span>)</code></pre>
       </div>
      </div>

      <!-- Rule 2 -->
      <div class="mb-8 pb-8 border-b border-slate-100">
       <div class="bg-slate-100 border border-slate-200 rounded-lg p-2.5 mb-3 inline-flex items-center w-max">
        <span class="text-[11px] font-bold text-slate-500 uppercase tracking-wider mr-2">Applies to:</span>
        <span class="text-xs font-bold text-slate-800 bg-white px-2 py-0.5 rounded shadow-sm">CM, Physical Abuse</span>
       </div>
       <p class="text-[14px] text-slate-600 mb-4 leading-relaxed mt-0">
        Restrict codes relating to shaken baby syndrome exclusively to children aged 5 years or younger at the time of the event.
       </p>
       <div class="code-container">
        <div class="code-header">
         <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
         <span class="text-[11px] text-slate-400 font-mono ml-2">R Script</span>
        </div>
        <pre class="code-pre"><code>cm_sbs &lt;- merged_data %&gt;% 
  <span class="syntax-function">filter</span>(Domain==<span class="syntax-string">"CM"</span> & code_group==<span class="syntax-string">"Shaken Baby"</span> & age_at_event &lt;= 5)</code></pre>
       </div>
      </div>

      <!-- Rule 3 -->
      <div class="mb-0">
       <div class="bg-slate-100 border border-slate-200 rounded-lg p-2.5 mb-3 inline-flex items-center w-max">
        <span class="text-[11px] font-bold text-slate-500 uppercase tracking-wider mr-2">Applies to:</span>
        <span class="text-xs font-bold text-slate-800 bg-white px-2 py-0.5 rounded shadow-sm">CM, HRP-CM</span>
       </div>
       <p class="text-[14px] text-slate-600 mb-4 leading-relaxed mt-0">
        Exclude high-risk presentations (e.g. rib fractures) if the child has a documented accidental injury code occurring on the exact same date.
       </p>
       <div class="code-container">
        <div class="code-header">
         <div class="code-window-dot bg-rose-500"></div><div class="code-window-dot bg-amber-500"></div><div class="code-window-dot bg-emerald-500"></div>
         <span class="text-[11px] text-slate-400 font-mono ml-2">R Script</span>
        </div>
        <pre class="code-pre"><code><span class="syntax-comment"># Exclude cases matching on patient ID and event date</span>
cm_hrp_filtered &lt;- cm_hrp_data %&gt;% 
  <span class="syntax-function">anti_join</span>(accidental_injuries, by = <span class="syntax-function">c</span>(<span class="syntax-string">"patid"</span>, <span class="syntax-string">"eventdate"</span>))</code></pre>
       </div>
      </div>

     </div>

    </div>

    <!-- FULL WIDTH TABLE SECTION -->
    <h3 class="content-subheading flex items-center mb-6">
     <i class="fas fa-table text-slate-400 mr-3"></i> Indicator structure & taxonomy
    </h3>
     
    <div class="table-wrapper">
     <table class="custom-table min-w-[700px]">
      <thead>
       <tr>
        <th style="width: 15%;">ACE Domain</th>
        <th style="width: 20%;">Indicator Code</th>
        <th>Indicator Name / Description</th>
       </tr>
      </thead>
      <tbody>
       <tr>
        <td><span class="domain-badge bg-brand-light text-brand-dark">CM</span></td>
        <td class="font-mono text-sm text-slate-500 font-semibold">CM1</td>
        <td class="font-medium text-slate-800">Child protection/safeguarding</td>
       </tr>
       <tr>
        <td><span class="domain-badge bg-brand-light text-brand-dark">CM</span></td>
        <td class="font-mono text-sm text-slate-500 font-semibold">CM2</td>
        <td class="font-medium text-slate-800">CM NOS, incl. physical or sexual abuse <span class="text-slate-400 font-normal ml-1">(merged)</span></td>
       </tr>
       <tr>
        <td><span class="domain-badge bg-brand-light text-brand-dark">CM</span></td>
        <td class="font-mono text-sm text-slate-500 font-semibold">CM3</td>
        <td class="font-medium text-slate-800">Neglect (incl. NAS/FASD) and emotional/psychological abuse</td>
       </tr>
       <tr>
        <td><span class="domain-badge bg-brand-light text-brand-dark">CM</span></td>
        <td class="font-mono text-sm text-slate-500 font-semibold">CM4</td>
        <td class="font-medium text-slate-800">Social service involved <span class="text-slate-500 font-normal ml-1">(incl. parental imprisonment/criminal activity)</span></td>
       </tr>
       <tr>
        <td><span class="domain-badge bg-brand-light text-brand-dark">CM</span></td>
        <td class="font-mono text-sm text-slate-500 font-semibold">CM5</td>
        <td class="font-medium text-slate-800">Child in care</td>
       </tr>
       <tr>
        <td><span class="domain-badge bg-brand-light text-brand-dark">CM</span></td>
        <td class="font-mono text-sm text-slate-500 font-semibold">CM6</td>
        <td class="font-medium text-slate-800">Suspected CM NOS <span class="text-slate-500 font-normal ml-1">(incl. neglect and social service involvements)</span></td>
       </tr>
       <tr>
        <td><span class="domain-badge bg-brand-light text-brand-dark">CM</span></td>
        <td class="font-mono text-sm text-slate-500 font-semibold">CM7</td>
        <td class="font-medium text-slate-800">Child assaulted NOS <span class="text-slate-500 font-normal ml-1">(incl. physical/sexual abuse ≤10, rib fractures ≤3†)</span></td>
       </tr>
      </tbody>
     </table>
    </div>

   </div>
  </section>

  <!-- SECTION 3: PUBLICATIONS -->
  <section class="bg-white py-16 border-t border-slate-200">
   <div class="max-w-5xl mx-auto px-6">
    
    <div class="text-center mb-10">
     <div class="inline-flex items-center justify-center w-12 h-12 rounded-full bg-slate-100 text-slate-600 mb-4">
      <i class="fas fa-graduation-cap text-xl"></i>
     </div>
     <h2 class="content-heading text-slate-900 !m-0">Related Publications</h2>
     <p class="text-slate-500 mt-2">Core research outputs associated with this specific ACE domain.</p>
    </div>

    <div class="space-y-4 max-w-4xl mx-auto">
      
     <!-- Pub 1 -->
     <div class="pub-item">
      <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext" target="_blank" class="pub-link">
       Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England.
      </a>
      <p class="text-[15px] text-slate-500 m-0">Syed S, Gilbert R, Feder G, Howe LD, Powell C, Howarth E, Deighton J, Lacey RE. <em class="text-slate-700">The Lancet Public Health</em>. 2023.</p>
     </div>
      
     <!-- Pub 2 -->
     <div class="pub-item">
      <a href="https://www.thelancet.com/journals/landig/article/PIIS2589-7500(22)00061-9/fulltext" target="_blank" class="pub-link">
       Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study.
      </a>
      <p class="text-[15px] text-slate-500 m-0">Syed S, Gonzalez-Izquierdo A, Allister J, Feder G, Li L, Gilbert R. <em class="text-slate-700">The Lancet Digital Health</em>. 2022.</p>
     </div>

     <!-- Pub 3 -->
     <div class="pub-item">
      <a href="https://www.sciencedirect.com/science/article/pii/S0140673611610878" target="_blank" class="pub-link">
       Child maltreatment: variation in trends and policies in six developed countries.
      </a>
      <p class="text-[15px] text-slate-500 m-0 flex flex-wrap gap-2 items-center">
       <span>Gilbert R, Fluke J, O'Donnell M, et al. <em class="text-slate-700">The Lancet</em>. 2012.</span>
       <a href="https://ars.els-cdn.com/content/image/1-s2.0-S0140673611610878-mmc1.pdf" target="_blank" class="inline-flex items-center px-2.5 py-1 rounded-md bg-blue-50 text-blue-600 text-xs font-semibold hover:bg-blue-100 transition-colors border-none !no-underline ml-1"><i class="fas fa-file-pdf mr-1.5"></i> View Code List</a>
      </p>
     </div>

     <!-- Pub 4 -->
     <div class="pub-item">
      <a href="https://link.springer.com/article/10.1186/1472-6963-12-65" target="_blank" class="pub-link">
       Health service use in families where children enter public care: a nested case control study using the General Practice Research Database.
      </a>
      <p class="text-[15px] text-slate-500 m-0">Simkiss DE, Spencer NJ, Stallard N, Thorogood M. <em class="text-slate-700">BMC Health Services Research</em>. 2012.</p>
     </div>

     <!-- Pub 5 -->
     <div class="pub-item">
      <a href="https://elearning.rcgp.org.uk/mod/book/view.php?id=12531" target="_blank" class="pub-link">
       Child safeguarding toolkit.
      </a>
      <p class="text-[15px] text-slate-500 m-0">Royal College of General Practitioners.</p>
     </div>
    </div>
     
    <div class="mt-12 text-center">
     <a href="https://acesinehrs.com/ACE-domains/" class="inline-flex items-center text-slate-600 hover:text-brand-rose font-semibold transition-all text-[16px] !important bg-white hover:bg-rose-50 px-6 py-3 rounded-full border border-slate-200 hover:border-rose-200 shadow-sm hover:shadow-md">
      <i class="fas fa-arrow-left mr-2"></i> Back to all ACE Domains
     </a>
    </div>

   </div>
  </section>

 </main>

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
