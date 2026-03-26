---
layout: splash
title: "ACAMH Seminar - Interrelationships between parental mental health, intimate partner violence and child mental health"
permalink: /research-acamh-ipv/
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
 .tailwind-wrap a:not(.btn-custom):not(.resource-card) {
  border-bottom: none !important; text-decoration: none !important; box-shadow: none !important;
 }

 /* Typography specific to Article */
 .article-text {
  font-size: 17px !important; 
  line-height: 1.8 !important; 
  color: #334155 !important; 
  margin-bottom: 1.5rem !important;
 }
 
 /* Resource Cards for Links */
 .resource-card {
  display: flex !important; align-items: center !important; gap: 1rem !important;
  padding: 1rem 1.25rem !important; border: 1px solid #e2e8f0 !important;
  border-radius: 0.75rem !important; background: #f8fafc !important;
  transition: all 0.2s ease !important; text-decoration: none !important;
 }
 .resource-card:hover {
  border-color: #bfdbfe !important; background: #ffffff !important;
  box-shadow: 0 4px 6px -1px rgba(37, 99, 235, 0.05) !important; transform: translateY(-2px) !important;
 }
 .resource-card .rc-icon {
  width: 2.5rem !important; height: 2.5rem !important; border-radius: 0.5rem !important;
  display: flex !important; align-items: center !important; justify-content: center !important;
  font-size: 1.25rem !important; flex-shrink: 0 !important; background: #eff6ff !important; color: #2563eb !important;
 }
 .resource-card .rc-title {
  font-size: 15px !important; font-weight: 600 !important; color: #1e293b !important; line-height: 1.3 !important; border: none !important;
 }

 html { scroll-behavior: smooth; }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen bg-slate-50">

 <!-- Article Hero Section -->
 <header class="relative bg-[#1e293b] text-white pt-12 pb-32 md:pt-16 md:pb-40" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/ACAMHS%20ACEsinEHRs%20Seminar%20presentation.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
  <div class="max-w-5xl mx-auto px-6 relative z-10">
   
   <!-- Back Button -->
   <a href="/research/" class="inline-flex items-center text-slate-300 hover:text-white transition-colors text-[14px] font-semibold mb-8 btn-custom">
    <div class="w-8 h-8 rounded-full bg-slate-800/50 border border-slate-600 flex items-center justify-center mr-3 hover:bg-slate-700 transition-colors">
     <i class="fas fa-arrow-left"></i>
    </div>
    Back to Research & Outputs
   </a>

   <!-- Title & Meta -->
   <h1 class="text-3xl md:text-4xl lg:text-[42px] font-bold leading-[1.2] mb-5 text-white border-none drop-shadow-md">
    ACAMH Seminar - Interrelationships between parental mental health, intimate partner violence and child mental health
   </h1>
   <p class="text-slate-300 text-lg md:text-xl mb-8 leading-relaxed font-light max-w-3xl drop-shadow">
    Clinical implications for practice and improving responses to affected families presenting to healthcare.
   </p>
   
   <div class="flex flex-wrap items-center gap-6 text-sm text-slate-300 font-medium">
    <span class="flex items-center"><i class="fas fa-video mr-2 text-blue-400"></i> Recorded Webinar</span>
    <span class="flex items-center"><i class="far fa-calendar-alt mr-2 text-blue-400"></i> June 2023</span>
   </div>
  </div>
 </header>

 <!-- Main Content Area -->
 <main class="flex-grow pb-20 relative">
  <div class="max-w-4xl mx-auto px-6">
   
   <!-- Restored Original Video Dimensions (Floats over hero cleanly) -->
   <div class="relative z-20 -mt-16 md:-mt-20 mb-12 flex justify-center px-2">
    <iframe title="vimeo-player" src="https://player.vimeo.com/video/840480281?h=0ea3958d16" width="640" height="360" frameborder="0" allowfullscreen class="rounded-xl shadow-2xl border border-slate-200 bg-black max-w-full"></iframe>
   </div>

   <!-- Article Body -->
   <div class="bg-white rounded-2xl p-8 md:p-12 shadow-sm border border-slate-200">
    
    <h2 class="text-2xl font-bold text-slate-900 mb-6 border-b border-slate-100 pb-3">About the seminar</h2>

    <p class="article-text">
     This free webinar is open to all, and is organised by ACAMH’s Adverse Childhood Experiences (ACEs) Special Interest Group Monthly seminars.
    </p>

    <p class="article-text">
     This webinar <strong>‘Interrelationships between parental mental health, intimate partner violence and child mental health – implications for practice’</strong> is led by Prof Gene Feder, Dr Shabeer Syed, and Dr Claire Powell on behalf of the NIHR Children and Families Policy Research Unit.
    </p>

    <h2 class="text-xl font-bold text-slate-900 mb-5 mt-10">Event resources</h2>
    
    <!-- Modern Grid for Links -->
    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mb-6">
     
     <a href="https://www.acamh.org/event/pmi-violence/" target="_blank" class="resource-card group">
      <div class="rc-icon"><i class="fas fa-play-circle"></i></div>
      <div class="rc-title group-hover:text-blue-600">Link to ACAMH event</div>
     </a>

     <a href="https://www.acamh.org/app/uploads/2023/06/Shabeer-Syed-ACAMH-ACE-Seminar-presentation-Shabeer-Syed-27.06.2023.pdf" target="_blank" class="resource-card group">
      <div class="rc-icon"><i class="fas fa-file-pdf"></i></div>
      <div class="rc-title group-hover:text-blue-600">Presentation slides</div>
     </a>

     <a href="https://doi.org/10.1016/S2468-2667(23)00119-6" target="_blank" class="resource-card group sm:col-span-2">
      <div class="rc-icon bg-emerald-50 text-emerald-600"><i class="fas fa-book-medical"></i></div>
      <div class="rc-title group-hover:text-emerald-600">Research publication (The Lancet Public Health)</div>
     </a>

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
