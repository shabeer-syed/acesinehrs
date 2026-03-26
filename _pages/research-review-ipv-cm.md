---
layout: splash
title: "Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records"
permalink: /research-review-ipv-cm/
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
 <header class="relative bg-[#0f172a] text-white pt-12 pb-24 md:pt-16 md:pb-32" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/aces%20in%20ehrs%20research%20review%20CM%20IPV.png'); background-size: cover; background-position: center; background-blend-mode: multiply;">
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
    Predictive value of indicators for identifying child maltreatment and intimate partner violence
   </h1>
   <p class="text-slate-300 text-lg md:text-xl mb-8 leading-relaxed font-light max-w-3xl drop-shadow">
    A systematic review and meta-analysis evaluating the accuracy of coded electronic health records for family violence.
   </p>
   
   <div class="flex flex-wrap items-center gap-6 text-sm text-slate-300 font-medium">
    <span class="flex items-center"><i class="far fa-calendar-alt mr-2 text-blue-400"></i> January 2021</span>
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
      <h3 class="text-slate-900 font-bold text-lg m-0 border-none">Published in Archives of Disease in Childhood</h3>
      <p class="text-slate-500 text-[14.5px] m-0 mt-1 leading-snug">Read the full peer-reviewed systematic review assessing the validity of coded indicators.</p>
     </div>
    </div>
    <a href="http://dx.doi.org/10.1136/archdischild-2020-319027" target="_blank" class="shrink-0 w-full md:w-auto text-center inline-flex items-center justify-center px-6 py-3.5 bg-blue-600 hover:bg-blue-700 text-white font-semibold rounded-xl shadow-md hover:shadow-lg transition-all btn-custom text-[15px]">
     View Publication <i class="fas fa-external-link-alt ml-2 text-sm opacity-80"></i>
    </a>
   </div>

   <!-- Article Body -->
   <div class="bg-white rounded-2xl p-8 md:p-12 shadow-sm border border-slate-200">
    
    <p class="article-text">
     Intimate partner violence (IPV) and child maltreatment (CM) represent forms of family violence that often go undetected by support services, despite World Health Organization (WHO) recommendations to improve monitoring efforts. CM and IPV refer to any act that causes biopsychosocial harm to a child, a future child, or a partner. In the UK, statutory definitions of CM also include conditions resulting from prenatal neglect, such as fetal alcohol syndrome (FAS) and neonatal abstinence syndrome (NAS).
    </p>

    <p class="article-text">
     Assessing health records manually for detailed information on family violence is time-consuming and resource-intensive. Consequently, clinical services and researchers are increasingly utilising routinely coded electronic health records (EHRs) to assess family violence. Coded EHRs offer the potential for longitudinal population-based assessments, automated early warning systems, and the identification of high-risk populations at a relatively low cost. 
    </p>

    <p class="article-text">
     However, the validity of these coded indicators has remained uncertain due to reported quality issues and a lack of external validation. To address this, a comprehensive systematic review and meta-analysis was conducted to estimate the positive predictive values (PPVs) of coded indicators for different forms of family violence based on independent reference standards.
    </p>

    <h2 class="text-2xl font-bold text-slate-900 mb-5 mt-10 border-b border-slate-100 pb-3">Key findings</h2>

    <p class="article-text">
     The researchers searched 18 electronic databases and 20 selected journals, adhering to PRISMA-DTA and MOOSE guidelines. The final meta-analysis included 65 cross-sectional and 23 longitudinal studies, encompassing 20 distinct clinical indicators and evaluating 3,875,183 individuals across 11 different countries.
    </p>

    <ul class="list-disc pl-6 mb-8 text-[17px] text-slate-700 space-y-3">
     <li><strong>High predictive value:</strong> The pooled PPV for general child maltreatment (0-18 years) was 87.8%, and for IPV among women (12-50 years) was 86.1%.</li>
     <li><strong>Prenatal neglect indicators:</strong> The pooled PPV of primary diagnoses for neonatal abstinence syndrome (NAS) was 80.9%, while fetal alcohol syndrome (FAS) was 39.3%.</li>
     <li><strong>Variation in physical injury indicators:</strong> Specific CM indicators showed variation; the PPV for rib fractures was notably high at 88.3%, whereas multiple burn injuries in children under 5 years yielded a PPV of 19.6%.</li>
     <li><strong>Injury-related IPV:</strong> General injury-related presentations of IPV provided relatively lower predictive values compared to explicit diagnostic codes.</li>
     <li><strong>Coding accuracy:</strong> The proportion of misclassifications (false positives) resulting strictly from coding errors averaged 2.1%. However, in assault-coded cases among women, 28.0% lacked recorded perpetrator information in the underlying medical charts.</li>
    </ul>

    <!-- Expert Quote -->
    <h3 class="author-heading">Lead author Dr Shabeer Syed (UCL Great Ormond Street Institute of Child Health), said:</h3>
    <div class="quote-text">
     <p class="mb-0">“Our analysis demonstrates the utility of using routinely coded medical data to evaluate services for at-risk groups. The consistently high positive predictive values for explicit child maltreatment and IPV indicators in electronic health records suggest significant potential for the early identification and support of vulnerable individuals.”</p>
    </div>

    <h2 class="text-2xl font-bold text-slate-900 mb-5 mt-10 border-b border-slate-100 pb-3">Clinical implications</h2>

    <p class="article-text">
     The findings indicate that utilising EHRs to identify family violence can facilitate improved, targeted care for at-risk individuals. 
    </p>

    <ul class="list-disc pl-6 mb-8 text-[17px] text-slate-700 space-y-3">
     <li>Coded indicators of family violence have the potential to be integrated into computerized clinical decision support systems, helping to automatically flag potential at-risk cases to clinicians.</li>
     <li>Linking the EHRs of family members enables a "think-family" approach, aiding practitioners in identifying vulnerable children through maternal records, or vice versa.</li>
     <li>Coded physical injury patterns may serve as a broader measure to identify high-risk groups requiring secondary assessment.</li>
    </ul>

    <!-- Study Limitations Box -->
    <div class="mt-12 bg-slate-50 border border-slate-200 rounded-xl p-6 md:p-8">
     <h2 class="text-xl font-bold text-slate-900 mb-4 border-none flex items-center">
      <i class="fas fa-info-circle text-slate-400 mr-3"></i> Study limitations
     </h2>
     <ul class="list-disc pl-6 text-[15px] text-slate-600 space-y-3 m-0">
      <li>Predictive estimates varied considerably depending on the specific indicator and outcome, revealing substantial heterogeneity across studies.</li>
      <li>The complexity of definitively identifying CM and IPV in clinical practice means potential missed diagnoses or misclassifications remain a factor in EHR data.</li>
      <li>While automated EHR systems offer benefits for family violence identification, careful consideration of potential unintended consequences—such as stigma, legal repercussions, compromised patient trust, and reduced help-seeking behaviour—is required prior to implementation.</li>
     </ul>
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
