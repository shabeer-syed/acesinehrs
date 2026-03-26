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
 .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.feature-card):not(.scholar-link):not(.text-blue-600):not(.text-blue-400):not(.notice-card):not(.gs-title) { 
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
 
 /* Notice Warning Cards */
 .notice-card {
  background-color: #ffffff !important;
  border-radius: 1.25rem !important;
  border: 1px solid #f3f4f6 !important;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.04) !important;
  transition: all 0.3s ease !important;
  text-decoration: none !important;
  position: relative !important;
  overflow: hidden !important;
  display: flex !important;
 }
 .notice-card:hover {
  transform: translateY(-4px) !important;
  box-shadow: 0 12px 20px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05) !important;
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
 The ACEsinEHRs platform provides validated domains, indicators, and code lists to identify adverse childhood experiences (ACEs) in routinely collected non-identifiable electronic healthcare records of parents and children before and after birth.
 </p>
 </div>
 </header>

 <main class="flex-grow">
  
 <!-- Section 1: Introduction & Infographic -->
 <section class="max-w-6xl mx-auto px-6 py-12 md:py-16">
 <div class="grid grid-cols-1 md:grid-cols-2 gap-8 lg:gap-12 items-center">
 <div>
  <h2 class="content-heading">Adverse childhood experiences</h2>
  <p class="content-text">
  Adverse childhood experiences (ACEs) are potentially traumatic, violent, or neglectful events in childhood that can have a profound impact on a child’s health and development <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext" target="_blank" class="text-blue-600 font-medium hover:underline">(1)</a>. 
  </p>
  <p class="content-text">
  Examples of recorded ACEs include child maltreatment (e.g., child protection interventions), exposure to domestic violence, and growing up with a parent experiencing mental health or substance use problems (often referred to as the 'trio of vulnerabilities') <a href="https://www.cdc.gov/violenceprevention/aces/fastfact.html" target="_blank" class="text-blue-600 font-medium hover:underline">(2)</a>.
  </p>
  
  <h2 class="content-heading mt-10">ACEs in EHRs</h2>
  <p class="content-text">
  Electronic health records (EHRs) contain a wealth of routinely collected information about patients, including their medical, medication, and social histories. ACEsinEHRs is a platform that provides clinically relevant and validated indicators to identify these experiences within EHRs. 
  </p>
  <p class="content-text">
  These indicators are based on several rigorous studies <span class="text-slate-500">(3, 4, 5)</span> and inspired by the landmark Adverse Childhood Experiences (ACE) Study, which established that exposure to ACEs is strongly associated with a wide range of adverse health outcomes.
  </p>
 </div>
  
 <!-- Clickable Infographic -->
 <div class="flex justify-center md:justify-end">
  <a href="https://acesinehrs.com/theory/" class="block bg-slate-50 p-6 rounded-3xl border border-slate-100 shadow-sm w-full max-w-md transition-all duration-300 hover:-translate-y-2 hover:shadow-xl hover:border-blue-200 group relative">
  <!-- Hover Icon -->
  <div class="absolute top-5 right-5 text-blue-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
   <i class="fas fa-external-link-alt text-lg"></i>
  </div>
  <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/aces%20in%20ehrs%20definitions%20theories.png" alt="ACEs Infographic" class="w-full h-auto object-contain rounded-xl mix-blend-multiply transition-transform duration-300 group-hover:scale-[1.02]" style="margin: 0 !important;">
  </a>
 </div>
 </div>
 </section>

 <!-- Section 2: Mission & Achievements -->
 <section class="bg-slate-50 py-12 md:py-16 border-y border-slate-200">
 <div class="max-w-6xl mx-auto px-6">
  
 <div class="max-w-3xl mx-auto text-center mb-10">
  <h2 class="content-heading">Mission statement and aims</h2>
  <p class="content-text">
  EHRs are routinely collected and readily available. However, there are significant challenges in using them to inform practice and policy. EHRs are often stored across disparate databases, organisations, and coding systems, resulting in a complex web of data requiring specialist management skills. Prior to this platform, there was no validated set of indicators for identifying ACEs in EHRs using both parent and child data.
  </p>
 </div>

 <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 mb-8">
  
  <!-- Mission Card -->
  <div class="feature-card h-full">
  <div class="flex items-center mb-6">
  <div class="w-12 h-12 rounded-full bg-blue-100 flex items-center justify-center text-blue-600 mr-4 shrink-0">
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
  <div class="feature-card h-full relative overflow-hidden">
  <div class="absolute -right-10 -top-10 w-40 h-40 bg-blue-50 rounded-full opacity-50 pointer-events-none"></div>
   
  <div class="flex items-center mb-6 relative z-10">
  <div class="w-12 h-12 rounded-full bg-emerald-100 flex items-center justify-center text-emerald-600 mr-4 shrink-0">
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

 <!-- WHO & Open Source Callout -->
 <div class="bg-white rounded-xl p-6 md:p-8 border border-slate-200 shadow-sm max-w-4xl mx-auto mt-8 flex items-start gap-5">
  <i class="fas fa-globe-europe text-3xl text-blue-500 mt-1 shrink-0"></i>
  <div>
  <p class="content-text text-sm md:text-base !mb-3">
  <strong>All platform activity is publicly logged.</strong> All code for data management and analysis is shared under open licenses.
  </p>
  <p class="content-text text-sm md:text-base !mb-0">
  We follow WHO's Minsk Declaration and view ACEs through a "life-course" and a "trauma-informed" lens. This approach acknowledges that risk is not static and depends on the interaction of multiple unmeasured promotive, protective, and risk factors throughout generations and people's lives.
  </p>
  </div>
 </div>

 </div>
 </section>

 <!-- Section 3: Impact & Real-World Results -->
 <section class="bg-slate-900 text-white py-12 md:py-16">
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
  <div class="scholar-feed max-h-[300px] overflow-y-auto pr-3 space-y-5 text-slate-800">
   
   <!-- Li 2026 -->
   <div class="group">
    <a href="https://scholar.google.com/scholar?q=The+Role+of+Artificial+Intelligence+for+Intimate+Partner+Violence+Prevention%3A+A+Systematic+Review" target="_blank" class="gs-title block text-blue-700 hover:text-blue-800 border-none !no-underline group-hover:underline">
     <h4 class="font-semibold text-[15px] leading-snug mb-1 m-0">The Role of Artificial Intelligence for Intimate Partner Violence Prevention: A Systematic Review</h4>
    </a>
    <p class="text-emerald-700 text-xs font-medium mb-1.5 mt-0">Li et al. - <span class="text-slate-500 font-normal">2026</span></p>
    <p class="text-slate-600 text-[14px] leading-relaxed line-clamp-2 m-0">Intimate partner violence (IPV), encompassing physical, sexual, emotional and economic abuse, remains a pervasive global health concern. Traditional prevention efforts...</p>
   </div>

   <!-- Lee 2025 -->
   <div class="group">
    <a href="https://scholar.google.com/scholar?q=Artificial+intelligence+in+applied+family+research+involving+families+with+young+children%3A+A+scoping+review" target="_blank" class="gs-title block text-blue-700 hover:text-blue-800 border-none !no-underline group-hover:underline">
     <h4 class="font-semibold text-[15px] leading-snug mb-1 m-0">Artificial intelligence in applied family research involving families with young children: A scoping review</h4>
    </a>
    <p class="text-emerald-700 text-xs font-medium mb-1.5 mt-0">Lee et al. - <span class="text-slate-500 font-normal">2025</span></p>
    <p class="text-slate-600 text-[14px] leading-relaxed line-clamp-2 m-0">This scoping review systematically examined the applied family science literature involving families raising young children to understand how relevant studies have applied...</p>
   </div>

   <!-- Syed 2025 -->
   <div class="group">
    <a href="https://scholar.google.com/scholar?q=Adverse+childhood+experiences+in+firstborns+and+mental+health+risk+and+health-care+use+in+siblings" target="_blank" class="gs-title block text-blue-700 hover:text-blue-800 border-none !no-underline group-hover:underline">
     <h4 class="font-semibold text-[15px] leading-snug mb-1 m-0">Adverse childhood experiences in firstborns and mental health risk and health-care use in siblings: a population-based birth cohort study</h4>
    </a>
    <p class="text-emerald-700 text-xs font-medium mb-1.5 mt-0">Syed et al. - <span class="text-slate-500 font-normal">2025</span></p>
    <p class="text-slate-600 text-[14px] leading-relaxed line-clamp-2 m-0">Adverse childhood experiences (ACEs) often affect multiple children within families, yet studies tend to focus on the health outcomes of individual children...</p>
   </div>

   <!-- Baird 2025 -->
   <div class="group">
    <a href="https://scholar.google.com/scholar?q=Applying+analytics+to+sociodemographic+disparities+in+mental+health" target="_blank" class="gs-title block text-blue-700 hover:text-blue-800 border-none !no-underline group-hover:underline">
     <h4 class="font-semibold text-[15px] leading-snug mb-1 m-0">Applying analytics to sociodemographic disparities in mental health</h4>
    </a>
    <p class="text-emerald-700 text-xs font-medium mb-1.5 mt-0">Baird & Xia - <span class="text-slate-500 font-normal">2025</span></p>
    <p class="text-slate-600 text-[14px] leading-relaxed line-clamp-2 m-0">Mental health services and treatment are unfortunately subject to sociodemographic disparities. To address this issue, recent studies have begun to apply analytics methods...</p>
   </div>

   <!-- Crowley 2025 -->
   <div class="group">
    <a href="https://scholar.google.com/scholar?q=Machine+learning+for+prediction+of+childhood+mental+health+problems+in+social+care" target="_blank" class="gs-title block text-blue-700 hover:text-blue-800 border-none !no-underline group-hover:underline">
     <h4 class="font-semibold text-[15px] leading-snug mb-1 m-0">Machine learning for prediction of childhood mental health problems in social care</h4>
    </a>
    <p class="text-emerald-700 text-xs font-medium mb-1.5 mt-0">Crowley et al. - <span class="text-slate-500 font-normal">2025</span></p>
    <p class="text-slate-600 text-[14px] leading-relaxed line-clamp-2 m-0">Rates of childhood mental health problems are increasing in the UK. Early identification of childhood mental health problems is challenging but critical to children's...</p>
   </div>

   <!-- Joshi 2025 -->
   <div class="group">
    <a href="https://scholar.google.com/scholar?q=Examining+the+rollout+of+the+Triple+P+system+parenting+program+in+Manitoba+on+rates+of+child+maltreatment" target="_blank" class="gs-title block text-blue-700 hover:text-blue-800 border-none !no-underline group-hover:underline">
     <h4 class="font-semibold text-[15px] leading-snug mb-1 m-0">Examining the rollout of the Triple P system parenting program in Manitoba on rates of child maltreatment</h4>
    </a>
    <p class="text-emerald-700 text-xs font-medium mb-1.5 mt-0">Joshi et al. - <span class="text-slate-500 font-normal">2025</span></p>
    <p class="text-slate-600 text-[14px] leading-relaxed line-clamp-2 m-0">Triple P is a multilevel parenting program aimed at promoting children's emotional, social, and behavioural competence and preventing behavioural problems...</p>
   </div>

   <!-- Schoenaker 2024 -->
   <div class="group">
    <a href="https://scholar.google.com/scholar?q=Preconception+indicators+and+associations+with+health+outcomes+reported+in+UK+routine+primary+care+data%3A+a+systematic+review" target="_blank" class="gs-title block text-blue-700 hover:text-blue-800 border-none !no-underline group-hover:underline">
     <h4 class="font-semibold text-[15px] leading-snug mb-1 m-0">Preconception indicators and associations with health outcomes reported in UK routine primary care data: a systematic review</h4>
    </a>
    <p class="text-emerald-700 text-xs font-medium mb-1.5 mt-0">Schoenaker et al. - <span class="text-slate-500 font-normal">2024</span></p>
    <p class="text-slate-600 text-[14px] leading-relaxed line-clamp-2 m-0">Routine primary care data may be a valuable resource for preconception health research and informing provision of preconception care. Aim: To review how primary...</p>
   </div>

   <!-- Danese 2024 -->
   <div class="group">
    <a href="https://scholar.google.com/scholar?q=Revisiting+the+use+of+adverse+childhood+experience+screening+in+healthcare+settings" target="_blank" class="gs-title block text-blue-700 hover:text-blue-800 border-none !no-underline group-hover:underline">
     <h4 class="font-semibold text-[15px] leading-snug mb-1 m-0">Revisiting the use of adverse childhood experience screening in healthcare settings</h4>
    </a>
    <p class="text-emerald-700 text-xs font-medium mb-1.5 mt-0">Danese et al. - <span class="text-slate-500 font-normal">2024</span></p>
    <p class="text-slate-600 text-[14px] leading-relaxed line-clamp-2 m-0">Adverse childhood experiences (ACEs) are key modifiable risk factors for mental illness. The potential to detect and mitigate ACEs to improve population mental health...</p>
   </div>

   <!-- Lam 2024 -->
   <div class="group">
    <a href="https://scholar.google.com/scholar?q=The+association+between+adverse+childhood+experiences+and+mental+health%2C+behaviour%2C+and+educational+performance+in+adolescence" target="_blank" class="gs-title block text-blue-700 hover:text-blue-800 border-none !no-underline group-hover:underline">
     <h4 class="font-semibold text-[15px] leading-snug mb-1 m-0">The association between adverse childhood experiences and mental health, behaviour, and educational performance in adolescence</h4>
    </a>
    <p class="text-emerald-700 text-xs font-medium mb-1.5 mt-0">Lam et al. - <span class="text-slate-500 font-normal">2024</span></p>
    <p class="text-slate-600 text-[14px] leading-relaxed line-clamp-2 m-0">Adverse childhood experiences (ACEs) are thought to have negative effects on mental health and well-being in adolescence. The definition of ACEs varies between studies...</p>
   </div>

   <!-- Ungar 2024 -->
   <div class="group">
    <a href="https://scholar.google.com/scholar?q=Access+without+borders%3A+a+scoping+review+to+identify+solutions+to+creating+portable+identity%2C+education+and+health+records+for+refugee+children" target="_blank" class="gs-title block text-blue-700 hover:text-blue-800 border-none !no-underline group-hover:underline">
     <h4 class="font-semibold text-[15px] leading-snug mb-1 m-0">Access without borders: a scoping review to identify solutions to creating portable identity, education and health records for refugee children</h4>
    </a>
    <p class="text-emerald-700 text-xs font-medium mb-1.5 mt-0">Ungar & Seymour - <span class="text-slate-500 font-normal">2024</span></p>
    <p class="text-slate-600 text-[14px] leading-relaxed line-clamp-2 m-0">The focus of this scoping review is to identify studies, reports, and other relevant sources from the peer-reviewed and grey literature that reports on refugee children's access...</p>
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

 <!-- Section 4: Advantages & Data Linkage (White Background) -->
 <section class="max-w-6xl mx-auto px-6 py-12 md:py-16">
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

 <!-- Responsive UCL Iframe Player with Light Grey Frame -->
 <div class="relative w-full rounded-2xl overflow-hidden shadow-sm border-2 border-slate-100 bg-slate-50" style="padding-top: 63.33%;">
  <iframe class="absolute top-0 left-0 w-full h-full rounded-xl" src="https://mediacentral.ucl.ac.uk//Player?autostart=n&fullscreen=y&width=0&height=0&videoId=CFGDc8DB&quality=hi&captions=y&chapterId=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
 </div>

 </div>
 </section>

 <!-- Section 5: Limitations (Light Grey Background for contrast) -->
 <section class="bg-slate-50 py-12 md:py-16 border-y border-slate-200">
 <div class="max-w-4xl mx-auto px-6">
  <div class="bg-white rounded-2xl border border-rose-100 shadow-md overflow-hidden relative">
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
 </div>
 </section>

 <!-- Section 6: Team & Contributors (White Background) -->
 <section class="max-w-4xl mx-auto px-6 py-12 md:py-16">
 <h2 class="content-heading text-center">Team & Contributors</h2>
 <p class="content-text text-center mb-8">This project was developed by a range of researchers and clinical experts:</p>
  
 <div class="bg-slate-50 rounded-2xl p-8 border border-slate-100 shadow-sm mb-8">
 <div class="grid grid-cols-1 sm:grid-cols-2 gap-x-8 gap-y-4 text-slate-800 font-medium text-sm">
  <div>Dr Shabeer Syed <span class="font-normal text-slate-500">(s.syed.16@ucl.ac.uk) <sup>1,2</sup></span></div>
  <div>Dr Arturo Gonzalez-Izquierdo <sup>1, 3</sup></div>
  <div>Dr Linda Wijlaars <sup>1, 3</sup></div>
  <div>Dr Janice Allister <sup>5</sup></div>
  <div>Dr Leah Li <sup>1</sup></div>
  <div>Dr Matthew Jay <sup>1</sup></div>
  <div>Prof Gene Feder <sup>4</sup></div>
  <div>Dr Louise Johns</div>
  <div>Dr Richard F Howard <sup>6, 7</sup></div>
  <div>Prof Ruth Gilbert <span class="font-normal text-slate-500">(r.gilbert@ucl.ac.uk) <sup>1,3</sup></span></div>
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

 <!-- Section 7: Feedback & Contributions (Dark Banner) -->
 <section class="bg-slate-900 py-12 md:py-16">
 <div class="max-w-3xl mx-auto px-6 text-center">
  <h3 class="text-2xl font-bold text-white mb-4 border-none">Feedback & Contributions</h3>
  <p class="text-slate-300 mb-4">We are continuously working to make this platform and the ACE indicators easier to access and implement. This website is open source and hosted via Github.</p>
  <p class="text-slate-300 font-medium">If you would like to contribute or provide feedback, please get in touch at <a href="mailto:s.syed.16@ucl.ac.uk" class="text-blue-400 hover:text-blue-300 hover:underline">s.syed.16@ucl.ac.uk</a></p>
 </div>
 </section>

 <!-- Section 8: Acknowledgements (Light Grey Background) -->
 <section class="bg-slate-50 py-12 md:py-16 border-t border-slate-200">
 <div class="max-w-5xl mx-auto px-6">
  
 <div class="mb-10">
  <h3 class="text-2xl font-bold text-slate-900 mb-8 border-none text-center">Acknowledgements</h3>
  
  <!-- Banner of Logos -->
  <div class="flex flex-wrap justify-center items-center gap-8 opacity-70 grayscale hover:grayscale-0 transition duration-500 mb-10">
  <a href="https://www.ucl.ac.uk/children-policy-research/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/NIHR%20CPRU%20logo%20aces%20in%20ehrs%20footer.png" alt="NIHR CPRU" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
  <a href="https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/ucl%20ich%20logo%20aces%20in%20ehrs.png" alt="UCL ICH" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
  <a href="https://www.ox.ac.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/university%20of%20oxford%20logo%20aces%20in%20ehrs.png" alt="Oxford" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
  <a href="https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/NIHR%20Great%20ormond%20street%20hospital%20biomedical%20research%20centre%20logo%20aces%20in%20ehrs.png" alt="NIHR GOSH BRC" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
  <a href="https://www.gosh.nhs.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/GOSH%20logo%20aces%20in%20ehrs.png" alt="GOSH" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
  <a href="https://www.bristol.ac.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/University%20of%20bristol%20logo%20aces%20in%20ehrs.png" alt="Bristol" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
  <a href="https://www.hdruk.ac.uk/" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/hdruk%20logo%20aces%20in%20ehrs.png" alt="HDRUK" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
  <a href="https://www.ucl.ac.uk/health-informatics/research/caliber" target="_blank"><img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/caliber%20ucl%20logo%20aces%20in%20ehrs.png" alt="Caliber UCL" class="h-10 object-contain hover:scale-105 transition-transform" style="margin: 0 !important;"></a>
  </div>

  <!-- Acknowledgements Fine Print -->
  <div class="text-xs text-slate-500 leading-relaxed space-y-4 max-w-4xl mx-auto">
  <p><strong class="text-slate-700">Study Support:</strong> This webpage accompanies a study that uses patients' data collected by the NHS as part of their care <span class="text-blue-600 font-semibold">#DataSavesLives</span>. We are extremely grateful to the generosity of the patients and their families, along with the participating GP practices and NHS staff, for their ongoing contribution to mental health and family violence research.</p>
  <p>The ACEs studies (protocols: 19_162R, 21_000587) were approved by the MHRA (UK) Independent Scientific Advisory Committee, under Section 251 (NHS Social Care Act 2006). The studies were carried out as part of the CALIBER© resource. CALIBER, led by the UCL Institute of Health Informatics, is a research resource providing validated electronic health record phenotyping algorithms and tools for national structured data sources.</p>
  <p>The ACEs studies are based on data from the CPRD obtained under licence from the UK Medicines and Healthcare products Regulatory Agency. The interpretation and conclusions contained in this study are those of the author/s alone. HES, and ONS are under copyright © (2020), re-used with the permission of The Health & Social Care Information Centre. All rights reserved.</p>
  <p>The research was supported in part by the NIHR Great Ormond Street Hospital Biomedical Research Centre. This research benefits from and contributes to the NIHR Children and Families Policy Research Unit, but was not commissioned by the National Institute for Health Research (NIHR) Policy Research Programme. The views expressed are those of the author(s) and not necessarily those of the NHS, the National Institute for Health Research, the Department of Health and Social Care or its arm's length bodies, and other Government Departments.</p>
  </div>
 </div>

 <!-- Mandatory Citation Warning (Matched to Home Page) -->
 <div class="mt-12 max-w-4xl mx-auto">
  <a href="https://doi.org/10.1016/S2589-7500(22)00061-9" target="_blank" class="notice-card p-6 items-start gap-4 sm:gap-5">
  <div class="absolute left-0 top-0 bottom-0 w-1.5" style="background-color: #ef4444 !important; border-top-left-radius: 1.25rem; border-bottom-left-radius: 1.25rem;"></div>
  <div class="flex-shrink-0 w-10 h-10 flex items-center justify-center rounded-full mt-0.5" style="background-color: #fef2f2 !important; color: #ef4444 !important;">
   <i class="fas fa-exclamation-triangle text-lg"></i>
  </div>
  <div class="flex-1">
   <p style="font-size: 15px !important; color: #334155 !important; margin: 0 !important;">
   <strong style="color: #0f172a !important; font-weight: 600 !important;">Users must cite</strong> the www.ACEsinEHRs.com library and the accompanying 
   <span style="color: #dc2626 !important; font-weight: 500 !important; text-decoration: underline !important; text-decoration-color: #fecaca !important; text-underline-offset: 4px !important;">Lancet Digital Health publication</span> 
   in all research outputs, presentations and reports.
   </p>
  </div>
  </a>
 </div>
  
 </div>
 </section>

 </main>
</div>
