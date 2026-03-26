---
layout: splash
title: "Identifying adverse childhood experiences with electronic health records of linked mothers and children in England"
permalink: /research-acesinehrs-validation/
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
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
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
 .tailwind-wrap li, .tailwind-wrap ul, .tailwind-wrap blockquote {
  font-family: 'Inter', sans-serif !important;
 }
  
 /* Reset link styles BUT ignore custom components */
 .tailwind-wrap a:not(.btn-custom) {
  border-bottom: none !important; text-decoration: none !important; box-shadow: none !important;
 }

 /* Typography specific to Article */
 .article-text {
  font-size: 17px !important; 
  line-height: 1.8 !important; 
  color: #334155 !important; 
  margin-bottom: 1.5rem !important;
 }
 .author-heading {
  font-size: 20px !important;
  font-weight: 700 !important;
  color: #1e3a8a !important; /* Dark navy blue */
  margin-top: 2.5rem !important;
  margin-bottom: 1rem !important;
  line-height: 1.4 !important;
  border: none !important;
 }
 .quote-text {
  font-size: 17px !important;
  line-height: 1.8 !important;
  color: #475569 !important;
  margin-bottom: 1.25rem !important;
  padding-left: 1rem !important;
  border-left: 3px solid #cbd5e1 !important;
 }

 html { scroll-behavior: smooth; }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen bg-slate-50">

 <!-- Article Hero Section -->
 <header class="relative bg-[#0f172a] text-white pt-12 pb-24 md:pt-16 md:pb-32" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20getting%20started%20page.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
  <div class="max-w-4xl mx-auto px-6 relative z-10">
   
   <!-- Back Button -->
   <a href="/research/" class="inline-flex items-center text-slate-300 hover:text-white transition-colors text-[14px] font-semibold mb-8 btn-custom">
    <div class="w-8 h-8 rounded-full bg-slate-800/50 border border-slate-600 flex items-center justify-center mr-3 hover:bg-slate-700 transition-colors">
     <i class="fas fa-arrow-left"></i>
    </div>
    Back to Research & Outputs
   </a>

   <!-- Title & Meta -->
   <h1 class="text-3xl md:text-4xl lg:text-[42px] font-bold leading-[1.2] mb-5 text-white border-none drop-shadow-md">
    Identifying adverse childhood experiences with electronic health records of linked mothers and children
   </h1>
   <p class="text-slate-300 text-lg md:text-xl mb-8 leading-relaxed font-light max-w-3xl drop-shadow">
    A multistage development and validation study establishing clinically relevant ACE indicators in routine healthcare data.
   </p>
   
   <div class="flex flex-wrap items-center gap-6 text-sm text-slate-300 font-medium">
    <span class="flex items-center"><i class="far fa-calendar-alt mr-2 text-blue-400"></i> July 2022</span>
    <span class="flex items-center"><i class="far fa-clock mr-2 text-blue-400"></i> 4 min read</span>
   </div>
  </div>
 </header>

 <!-- Main Content Area -->
 <main class="flex-grow pb-20 relative">
  <div class="max-w-4xl mx-auto px-6">
   
   <!-- Floating Publication Highlight Box -->
   <div class="bg-white rounded-2xl p-6 md:p-8 shadow-xl border border-slate-100 flex flex-col md:flex-row items-start md:items-center justify-between gap-6 -mt-12 md:-mt-16 relative z-20 mb-12">
    <div class="flex items-start gap-4">
     <div class="w-12 h-12 rounded-full bg-blue-50 text-blue-600 flex items-center justify-center shrink-0 mt-1">
      <i class="fas fa-book-medical text-xl"></i>
     </div>
     <div>
      <h3 class="text-slate-900 font-bold text-lg m-0 border-none">Published in The Lancet Digital Health</h3>
      <p class="text-slate-500 text-[14.5px] m-0 mt-1 leading-snug">Read the foundational study detailing the development of the ACEs in EHRs library framework.</p>
     </div>
    </div>
    <a href="https://doi.org/10.1016/S2589-7500(22)00061-9" target="_blank" class="shrink-0 w-full md:w-auto text-center inline-flex items-center justify-center px-6 py-3.5 bg-blue-600 hover:bg-blue-700 text-white font-semibold rounded-xl shadow-md hover:shadow-lg transition-all btn-custom text-[15px]">
     View Publication <i class="fas fa-external-link-alt ml-2 text-sm opacity-80"></i>
    </a>
   </div>

   <!-- Article Body -->
   <div class="bg-white rounded-2xl p-8 md:p-12 shadow-sm border border-slate-200">
    
    <p class="article-text">
     Adverse childhood experiences (ACEs) are potentially traumatic or neglectful events that can impact children's health and development. Identifying and measuring ACEs is a key step for early intervention and reducing long-term health risks. However, the lack of validated indicators in routine electronic health records (EHRs) poses a challenge for policy makers and service providers aiming to identify vulnerable families.
    </p>

    <p class="article-text">
     To address this gap, researchers utilised a population-based birth cohort in England, linking the primary and secondary care EHRs of mothers and their children. Candidate ACE indicators were systematically identified, and a multistage prediction framework was employed to develop clinically relevant indicators for measuring family adversity.
    </p>

    <h2 class="text-2xl font-bold text-slate-900 mb-5 mt-10 border-b border-slate-100 pb-3">Key findings</h2>

    <p class="article-text">
     Following review by an expert panel, the study successfully translated a comprehensive list of candidate codes into grouped ACE domains.
    </p>

    <ul class="list-disc pl-6 mb-8 text-[17px] text-slate-700 space-y-3">
     <li><strong>Identified indicators:</strong> A total of 63 distinct ACE indicators were developed and validated for use in routine EHRs.</li>
     <li><strong>Six distinct domains:</strong> These indicators represent six core domains: maternal mental health problems, maternal substance misuse, adverse family environments, child maltreatment, maternal intimate partner violence (IPV), and high-risk presentations of child maltreatment.</li>
     <li><strong>High prevalence rate:</strong> The prevalence of any ACE recorded in primary and secondary care during the two years before and after birth was 39.1%.</li>
     <li><strong>Predictive performance:</strong> Validation estimates demonstrated that the developed algorithms have good predictive performance for accurately identifying instances of child maltreatment or maternal IPV.</li>
    </ul>

    <h2 class="text-2xl font-bold text-slate-900 mb-5 mt-10 border-b border-slate-100 pb-3">Clinical implications</h2>

    <p class="article-text">
     The ACE domains established in this study align with the clinically meaningful presentations of vulnerable families seeking routine healthcare. The findings underscore the potential of using linked maternal and child EHRs to actively identify ACEs, aiding resource prioritisation and the development of trauma-informed care plans.
    </p>

    <p class="article-text">
     Because a significant proportion of ACEs are recorded in the period immediately preceding and following birth, the study highlights the importance of early primary care responses and the necessity of adopting "think-family" approaches in general practice. However, researchers note that routine implementation requires careful pilot testing to address ethical considerations and potential unintended harms.
    </p>

    <!-- Expert Quote -->
    <h3 class="author-heading">Lead author Dr Shabeer Syed (UCL Great Ormond Street Institute of Child Health), said:</h3>
    <div class="quote-text">
     <p class="mb-0">“This study represents a significant step in developing clinically relevant ACE indicators in EHRs. It offers practical insights for policymakers, service providers, and researchers working towards early intervention to support children and families exposed to adversity.”</p>
    </div>

   </div>

   <!-- Bottom Back Button -->
   <div class="mt-10 text-center">
    <a href="/research/" class="inline-flex items-center px-6 py-3 bg-white border border-slate-300 text-slate-700 font-semibold rounded-full hover:bg-slate-50 hover:text-blue-600 transition-all shadow-sm btn-custom">
     <i class="fas fa-arrow-left mr-2"></i> Return to Research & Outputs
    </a>
   </div>

  </div>
 </main>

 <!-- Logos Banner -->
 <section class="bg-white border-t border-slate-200 py-10 shadow-sm mt-auto">
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
