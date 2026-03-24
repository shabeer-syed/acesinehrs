---
layout: splash
permalink: /about/
title: "About ACEs in EHRs"
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
  background-color: #ffffff !important; 
  margin-bottom: 0 !important;
  padding-bottom: 5rem !important;
 }
  
 /* Remove Jekyll's forced padding/margins */
 #main { 
  padding-top: 0 !important; 
  padding-bottom: 0 !important; 
  margin-bottom: 0 !important; 
 }

 /* === OVERRIDE JEKYLL FOOTER TO MATCH HTML DESIGN === */
 .page__footer {
  background-color: #0f172a !important; /* Slate 900 */
  color: #94a3b8 !important; /* Slate 400 */
  margin-top: 0 !important; 
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
 .tailwind-wrap div, .tailwind-wrap li, .tailwind-wrap ul { 
  font-family: 'Inter', sans-serif !important; 
 }
  
 /* Reset link styles BUT ignore buttons/cards */
 .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.feature-card):not(.scholar-link) { 
  border-bottom: none !important; 
  text-decoration: none !important; 
  box-shadow: none !important; 
 }

 /* === HERO TYPOGRAPHY === */
 .hero-title {
  font-size: 48px !important;
  line-height: 1.1 !important;
  font-weight: 700 !important;
  color: rgb(255, 255, 255) !important;
  margin-bottom: 24px !important;
  border: none !important;
 }
 .hero-subtitle {
  font-size: 20px !important;
  line-height: 1.5 !important;
  font-weight: 400 !important;
  color: rgb(241, 245, 249) !important;
  margin-bottom: 0 !important;
  max-width: 820px !important; 
  margin-left: auto !important;
  margin-right: auto !important;
 }

 /* === PREMIUM CONTENT STYLES === */
 .content-heading {
  font-size: 32px !important;
  font-weight: 700 !important;
  color: #0f172a !important; /* Slate 900 */
  margin-bottom: 1rem !important; 
  letter-spacing: -0.025em !important;
  border-bottom: none !important;
 }
 .content-text {
  font-size: 17px !important;
  line-height: 1.7 !important;
  color: #475569 !important; /* Slate 600 */
  margin-bottom: 1.25rem !important; 
 }
 
 /* Modern Info Cards */
 .feature-card {
  background: #ffffff !important;
  border-radius: 1.25rem !important;
  border: 1px solid #e2e8f0 !important;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -1px rgba(0, 0, 0, 0.03) !important;
  padding: 2rem !important; 
  transition: transform 0.3s ease, box-shadow 0.3s ease !important;
 }
 .feature-card:hover {
  transform: translateY(-4px) !important;
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04) !important;
 }

 /* Clean Lists */
 .custom-list {
  list-style: none !important;
  padding: 0 !important;
  margin: 0 !important;
 }
 .custom-list li {
  position: relative !important;
  padding-left: 2.5rem !important;
  margin-bottom: 1.25rem !important;
  font-size: 16px !important;
  line-height: 1.6 !important;
  color: #334155 !important;
 }
 .custom-list li svg {
  position: absolute !important;
  left: 0 !important;
  top: 0.25rem !important;
  width: 1.25rem !important;
  height: 1.25rem !important;
 }

 /* Scholar Feed Scrollbar */
 .scholar-feed::-webkit-scrollbar {
  width: 6px;
 }
 .scholar-feed::-webkit-scrollbar-track {
  background: #f1f5f9; 
  border-radius: 4px;
 }
 .scholar-feed::-webkit-scrollbar-thumb {
  background: #cbd5e1; 
  border-radius: 4px;
 }
 .scholar-feed::-webkit-scrollbar-thumb:hover {
  background: #94a3b8; 
 }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

 <!-- Hero Section -->
 <header class="relative bg-slate-800 bg-opacity-60 text-white" 
   style="background-image: url('https://images.unsplash.com/photo-1511895426328-dc8714191300?q=80&w=2070&auto=format&fit=crop'); background-size: cover; background-position: center; background-blend-mode: multiply;">
   
  <!-- Banner Content -->
  <div class="relative z-10 max-w-5xl mx-auto px-6 py-20 md:py-24 text-center">
   <h1 class="hero-title drop-shadow-lg">
    About ACEs <span style="color: #bfdbfe !important;">in EHRs</span>
   </h1>
   <p class="hero-subtitle drop-shadow-md">
    The ACEsinEHRs platform provides validated domains, indicators, and code lists to identify adverse childhood experiences (ACEs) in routinely collected, non-identifiable electronic healthcare records of parents and children before and after birth.
   </p>
  </div>
 </header>

 <main class="flex-grow">
  
  <!-- Section 1: Introduction & Infographic -->
  <section class="max-w-6xl mx-auto px-6 py-10 md:py-16">
   <div class="grid grid-cols-1 md:grid-cols-2 gap-8 lg:gap-12 items-center">
    <div>
     <h2 class="content-heading">Adverse childhood experiences</h2>
     <p class="content-text">
      Adverse childhood experiences (ACEs) are potentially traumatic, violent, or neglectful events in childhood that can have a profound impact on a child’s health and development <a href="#" class="text-blue-600 hover:underline">(1)</a>. 
     </p>
     <p class="content-text">
      Examples of recorded ACEs include child maltreatment (e.g., child protection interventions), exposure to domestic violence, and growing up with a parent experiencing mental health or substance use problems (often referred to as the 'trio of vulnerabilities') <a href="#" class="text-blue-600 hover:underline">(2)</a>.
     </p>
     
     <h2 class="content-heading mt-10">ACEs in EHRs</h2>
     <p class="content-text">
      Electronic health records (EHRs) contain a wealth of routinely collected information about patients, including their medical, medication, and social histories. ACEsinEHRs is a platform that provides clinically relevant and validated indicators to identify these experiences within EHRs. 
     </p>
     <p class="content-text">
      These indicators are based on several rigorous studies <a href="#" class="text-blue-600 hover:underline">(3, 4, 5)</a> and inspired by the landmark Adverse Childhood Experiences (ACE) Study, which established that exposure to ACEs is strongly associated with a wide range of adverse health outcomes.
     </p>
    </div>
    
    <!-- Infographic -->
    <div class="flex justify-center md:justify-end">
     <div class="bg-slate-50 p-6 rounded-3xl border border-slate-100 shadow-sm w-full max-w-md">
      <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/aces%20in%20ehrs%20definitions%20theories.png" alt="ACEs Infographic" class="w-full h-auto object-contain rounded-xl mix-blend-multiply" style="margin: 0 !important;">
     </div>
    </div>
   </div>
  </section>

  <!-- Section 2: Mission & Achievements -->
  <section class="bg-slate-50 py-10 md:py-16 border-y border-slate-200">
   <div class="max-w-6xl mx-auto px-6">
    
    <div class="max-w-3xl mx-auto text-center mb-10">
     <h2 class="content-heading">Mission statement and aims</h2>
     <p class="content-text">
      EHRs are routinely collected and readily available. However, there are significant challenges in using them to inform practice and policy. EHRs are often stored across disparate databases, organisations, and coding systems, resulting in a complex web of data requiring specialist management skills. Prior to this platform, there was no validated set of indicators for identifying ACEs in EHRs using both parent and child data.
     </p>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
     
     <!-- Mission Card -->
     <div class="feature-card">
      <div class="flex items-center mb-6">
       <div class="w-12 h-12 rounded-full bg-blue-100 flex items-center justify-center text-blue-600 mr-4">
        <i class="fas fa-bullseye text-xl"></i>
       </div>
       <h3 class="text-2xl font-bold text-slate-900 m-0 border-none">Our Mission</h3>
      </div>
      <ul class="custom-list">
       <li>
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        To improve the health of families and young people by utilising electronic health records (EHRs) to identify and measure ACEs.
       </li>
       <li>
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        To advocate for early support and family-centred services for families affected by ACEs.
       </li>
       <li>
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        To collaborate with researchers, professionals, and policymakers to promote trauma-informed care and public health policies.
       </li>
       <li>
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        To enhance the methodological standards, accessibility, and utility of data-driven, 'think-family' approaches.
       </li>
       <li>
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        To continuously develop the ACEsinEHRs platform to improve resources for the wider clinical and research community.
       </li>
      </ul>
     </div>

     <!-- Achievements Card -->
     <div class="feature-card relative overflow-hidden">
      <!-- Decorative background element -->
      <div class="absolute -right-10 -top-10 w-40 h-40 bg-blue-50 rounded-full opacity-50 pointer-events-none"></div>
      
      <div class="flex items-center mb-6 relative z-10">
       <div class="w-12 h-12 rounded-full bg-emerald-100 flex items-center justify-center text-emerald-600 mr-4">
        <i class="fas fa-trophy text-xl"></i>
       </div>
       <h3 class="text-2xl font-bold text-slate-900 m-0 border-none">Key Achievements</h3>
      </div>
      <ul class="custom-list relative z-10">
       <li>
        <svg class="text-emerald-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>
        Developed common data standards and comprehensive coding systems for tracking ACEs in EHRs.
       </li>
       <li>
        <svg class="text-emerald-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>
        Created sophisticated data management tools and resources, making ACE indicators readily accessible and usable for external researchers.
       </li>
       <li>
        <svg class="text-emerald-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>
        Pioneered methodologies for reliably linking and studying EHR data across multiple family members.
       </li>
      </ul>
     </div>

    </div>
   </div>
  </section>

  <!-- Section 3: Advantages & Data Linkage -->
  <section class="max-w-6xl mx-auto px-6 py-10 md:py-16">
   <div class="grid grid-cols-1 lg:grid-cols-2 gap-10 lg:gap-12 items-center">
    
    <!-- Text Content -->
    <div>
     <h2 class="content-heading">Advantages of EHRs</h2>
     <p class="content-text">
      ACEs are preventable. However, many are exceptionally difficult to identify during childhood. Most traditional studies rely on adults' retrospective self-reports many years after the event, which are prone to memory biases. This "time gap" means data is collected too late to prevent the immediate harmful effects.
     </p>
     <p class="content-text">
      Conversely, EHRs provide prospectively recorded data from hospitals, GPs, and other health systems as events naturally happen during routine care. This information becomes available shortly after a healthcare presentation and poses far less burden on patients than completing complex research surveys. 
     </p>
     <p class="content-text font-semibold text-slate-800">
      Crucially, in the UK, mothers' and children's EHRs can be securely linked across services. This unique capability allows researchers to seamlessly measure ACEs before pregnancy, throughout childhood, and intergenerationally.
     </p>
    </div>

    <!-- REAL WORKING HTML5 VIDEO PLAYER -->
    <div class="relative rounded-2xl overflow-hidden shadow-lg border border-slate-200">
     <video controls class="w-full h-auto" poster="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/Data%20linkage%20video%20thumbnail.jpg">
      <source src="YOUR_VIDEO_URL_HERE.mp4" type="video/mp4">
      Your browser does not support the video tag.
     </video>
    </div>

   </div>
  </section>

  <!-- NEW SECTION: Impact & Real-World Results (BMJ-Inspired) -->
  <section class="bg-slate-900 text-white py-16 md:py-20 my-8">
   <div class="max-w-6xl mx-auto px-6 grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
    
    <!-- Left Column: Impact Text -->
    <div class="lg:col-span-5">
     <h2 class="text-3xl font-bold mb-6 text-white border-none leading-tight">
      Real-World Impact:<br><span class="text-blue-400">From Research to Results</span>
     </h2>
     
     <div class="flex gap-4 mb-8">
      <div class="bg-slate-800 border border-slate-700 rounded-lg p-4 flex-1 text-center">
       <div class="text-2xl font-bold text-white">100+</div>
       <div class="text-xs text-slate-400 uppercase tracking-wide mt-1">Weekly Global Visits</div>
      </div>
      <div class="bg-slate-800 border border-slate-700 rounded-lg p-4 flex-1 text-center">
       <div class="text-2xl font-bold text-emerald-400">40+</div>
       <div class="text-xs text-slate-400 uppercase tracking-wide mt-1">Peer-Reviewed Citations</div>
      </div>
     </div>

     <p class="text-slate-300 text-base leading-relaxed mb-6">
      The ACEsinEHRs open-access platform shares essential coding algorithms, tutorials, and theoretical frameworks that have been widely adopted by researchers globally.
     </p>
     
     <div class="space-y-4 text-sm text-slate-300">
      <div class="flex items-start">
       <i class="fas fa-check-circle text-blue-400 mt-1 mr-3 text-base"></i>
       <div>
        <strong class="text-white">Advancing predictive algorithms:</strong> Our code lists have facilitated the creation of the first externally validated algorithms for identifying child maltreatment in routine care, and developed machine learning models predicting childhood mental health issues.
       </div>
      </div>
      <div class="flex items-start">
       <i class="fas fa-check-circle text-blue-400 mt-1 mr-3 text-base"></i>
       <div>
        <strong class="text-white">Informing population health:</strong> Our family-linkage methodologies actively support evaluating health visiting models for ACE mitigation, optimising ACE screening protocols, and integrating healthcare responses to intimate partner violence.
       </div>
      </div>
     </div>
    </div>

    <!-- Right Column: Simulated Google Scholar Widget -->
    <div class="lg:col-span-7">
     <div class="bg-white rounded-2xl p-6 md:p-8 shadow-2xl relative overflow-hidden">
      
      <!-- Widget Header -->
      <div class="flex items-center justify-between border-b border-slate-200 pb-4 mb-4">
       <div class="flex items-center text-slate-900">
        <i class="fas fa-graduation-cap text-blue-600 text-2xl mr-3"></i>
        <h3 class="text-lg font-bold m-0 border-none">Latest Citing Research</h3>
       </div>
       <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c7/Google_Scholar_logo.svg/512px-Google_Scholar_logo.svg.png" alt="Google Scholar" class="h-6">
      </div>

      <!-- Scrollable Feed -->
      <div class="scholar-feed max-h-[300px] overflow-y-auto pr-3 space-y-4">
       
       <!-- Citation Item -->
       <div class="group">
        <h4 class="text-blue-700 font-semibold text-base leading-snug mb-1 group-hover:underline cursor-pointer">Developing machine models predicting childhood mental health issues</h4>
        <p class="text-emerald-700 text-xs font-medium mb-1">Crowley et al. - <span class="text-slate-500 font-normal">2025</span></p>
        <p class="text-slate-500 text-sm leading-relaxed line-clamp-2">Utilising ACEsinEHRs indicators to train predictive models identifying risk factors for adolescent psychiatric presentations.</p>
       </div>

       <!-- Citation Item -->
       <div class="group">
        <h4 class="text-blue-700 font-semibold text-base leading-snug mb-1 group-hover:underline cursor-pointer">Analysing maternal vulnerabilities in the family court system</h4>
        <p class="text-emerald-700 text-xs font-medium mb-1">Ireland et al. - <span class="text-slate-500 font-normal">2024</span></p>
        <p class="text-slate-500 text-sm leading-relaxed line-clamp-2">A data-driven think-family approach investigating the intersection of domestic adversity and legal interventions.</p>
       </div>

       <!-- Citation Item -->
       <div class="group">
        <h4 class="text-blue-700 font-semibold text-base leading-snug mb-1 group-hover:underline cursor-pointer">Optimising ACE screening in clinical practice</h4>
        <p class="text-emerald-700 text-xs font-medium mb-1">Danese et al. - <span class="text-slate-500 font-normal">2024</span></p>
        <p class="text-slate-500 text-sm leading-relaxed line-clamp-2">Evaluating routine care screening protocols against validated electronic health record phenotyping algorithms.</p>
       </div>

       <!-- Citation Item -->
       <div class="group">
        <h4 class="text-blue-700 font-semibold text-base leading-snug mb-1 group-hover:underline cursor-pointer">Integrating healthcare responses to intimate partner violence</h4>
        <p class="text-emerald-700 text-xs font-medium mb-1">Fanslow - <span class="text-slate-500 font-normal">2023</span></p>
        <p class="text-slate-500 text-sm leading-relaxed line-clamp-2">Policy integration leveraging linked maternal and child health records to inform population-level interventions.</p>
       </div>

       <!-- Citation Item -->
       <div class="group">
        <h4 class="text-blue-700 font-semibold text-base leading-snug mb-1 group-hover:underline cursor-pointer">Externally validating algorithms for identifying child maltreatment</h4>
        <p class="text-emerald-700 text-xs font-medium mb-1">John et al. - <span class="text-slate-500 font-normal">2023</span></p>
        <p class="text-slate-500 text-sm leading-relaxed line-clamp-2">The first external validation of coding algorithms designed to reliably identify safeguarding interventions in routine care.</p>
       </div>
       
       <!-- Citation Item -->
       <div class="group">
        <h4 class="text-blue-700 font-semibold text-base leading-snug mb-1 group-hover:underline cursor-pointer">Evaluating health visiting models for ACE mitigation</h4>
        <p class="text-emerald-700 text-xs font-medium mb-1">Woodman et al. - <span class="text-slate-500 font-normal">2022</span></p>
        <p class="text-slate-500 text-sm leading-relaxed line-clamp-2">Utilising standard data classifications to assess the efficacy of early-years public health visiting interventions.</p>
       </div>

      </div>

      <!-- Action Buttons -->
      <div class="mt-6 flex flex-col sm:flex-row gap-3 pt-4 border-t border-slate-100">
       <a href="https://scholar.google.co.uk/scholar?cites=17825954885314129992&as_sdt=2005&sciodt=0,5&hl=en" target="_blank" class="scholar-link flex-1 bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-semibold py-3 px-4 rounded-lg flex items-center justify-center transition-colors">
        View Core Study 1 Citations <i class="fas fa-external-link-alt ml-2"></i>
       </a>
       <a href="https://scholar.google.co.uk/scholar?cites=15768036519941313473&as_sdt=2005&sciodt=0,5&hl=en" target="_blank" class="scholar-link flex-1 bg-blue-50 hover:bg-blue-100 text-blue-700 text-xs font-semibold py-3 px-4 rounded-lg flex items-center justify-center transition-colors">
        View Core Study 2 Citations <i class="fas fa-external-link-alt ml-2"></i>
       </a>
      </div>

     </div>
    </div>
   </div>
  </section>

  <!-- Section 4: Limitations (Warning Style) -->
  <section class="max-w-4xl mx-auto px-6 pb-12 pt-8">
   <div class="bg-white rounded-2xl border border-rose-100 shadow-md overflow-hidden relative">
    <!-- Red top accent line -->
    <div class="h-2 w-full bg-rose-500 absolute top-0 left-0"></div>
    
    <div class="p-8 md:p-10">
     <div class="flex items-center mb-8">
      <div class="w-12 h-12 rounded-full bg-rose-100 flex items-center justify-center text-rose-600 mr-4">
       <i class="fas fa-exclamation-triangle text-xl"></i>
      </div>
      <h2 class="text-2xl font-bold text-slate-900 m-0 border-none">Limitations of ACEs in EHRs</h2>
     </div>
     
     <p class="content-text font-medium text-slate-800 mb-6">When utilising this library, it is essential to note:</p>
     
     <ul class="custom-list">
      <li>
       <svg class="text-rose-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path></svg>
       There are methodological challenges in accurately linking children’s EHRs to their fathers’ EHRs (a long-standing limitation of anonymised secondary and primary care data). Consequently, current ACE research using EHRs has primarily been based on linked maternal and child data.
      </li>
      <li>
       <svg class="text-rose-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path></svg>
       The platform only identifies experiences recorded in semi-structured, coded non-identifiable data. Serious concerns recorded solely in free-text clinical notes will not be captured by these coded indicators.
      </li>
      <li>
       <svg class="text-rose-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path></svg>
       The indicators do not represent an exhaustive list of all possible adversities experienced by children.
      </li>
      <li>
       <svg class="text-rose-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path></svg>
       <strong>Cannot make inferences about an individual.</strong> This means that indicators cannot be used to guide individual-level clinical decision-making, including screening, diagnosing, or labelling children or families to be at risk of harm.
      </li>
      <li>
       <svg class="text-rose-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path></svg>
       Do not assume children with ACEs will inevitably develop poorer health outcomes. Most children with ACEs <strong>do not</strong> develop poorer health outcomes and show profound resilience.
      </li>
      <li>
       <svg class="text-rose-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path></svg>
       These records do not account for mitigating protective factors and wider systemic contexts.
      </li>
     </ul>
    </div>
   </div>
  </section>

  <!-- Section 5: Team & Contributors -->
  <section class="max-w-4xl mx-auto px-6 pb-16">
   <h2 class="content-heading text-center">Team & Contributors</h2>
   <p class="content-text text-center mb-8">This project was developed by a diverse range of researchers and clinical experts:</p>
   
   <div class="bg-slate-50 rounded-2xl p-8 border border-slate-100 shadow-sm mb-8">
    <div class="grid grid-cols-1 sm:grid-cols-2 gap-x-8 gap-y-4 text-slate-700 font-medium text-sm">
     <div>Dr Shabeer Syed <sup>1, 2</sup></div>
     <div>Dr Arturo Gonzalez-Izquierdo <sup>1, 3</sup></div>
     <div>Dr Linda Wijlaars <sup>1, 3</sup></div>
     <div>Dr Janice Allister <sup>5</sup></div>
     <div>Dr Leah Li <sup>1</sup></div>
     <div>Dr Matthew Jay <sup>1</sup></div>
     <div>Prof Gene Feder <sup>4</sup></div>
     <div>Dr Louise Johns</div>
     <div>Dr Richard F Howard <sup>6, 7</sup></div>
     <div>Prof Ruth Gilbert <sup>1, 3</sup></div>
     <div>Dr Rebecca E Lacey</div>
     <div>Prof Laura D Howe</div>
     <div>Prof Jessica Deighton</div>
     <div>Dr Rachel Ashwick</div>
     <div>Mr Muhammad Qummer ul Arfeen <sup>3</sup></div>
    </div>
   </div>

   <!-- Affiliations Footnotes -->
   <div class="text-xs text-slate-500 leading-relaxed border-t border-slate-200 pt-6">
    <p class="mb-2"><strong>1.</strong> UCL Great Ormond Street Institute of Child Health, Population, Policy and Practice, Faculty of Population Health Sciences London WC1N 1EH.</p>
    <p class="mb-2"><strong>2.</strong> Oxford Institute of Clinical Psychology Training and Research, University of Oxford, Oxford, UK.</p>
    <p class="mb-2"><strong>3.</strong> Institute of Health Informatics and Health Data Research UK, University College London.</p>
    <p class="mb-2"><strong>4.</strong> Bristol Medical School, Bristol Population Health Science Institute Centre for Academic Primary Care, University of Bristol.</p>
    <p class="mb-2"><strong>5.</strong> General Practitioner, NHS.</p>
    <p class="mb-2"><strong>6.</strong> Paediatric Pain Research Group, University College London Great Ormond Street, Institute of Child Health, London WC1N 1EH.</p>
    <p class="mb-0"><strong>7.</strong> Department of Anaesthesia & Pain Medicine, Great Ormond Street Hospital for Children NHS Foundation Trust.</p>
   </div>
  </section>

 </main>
</div>
