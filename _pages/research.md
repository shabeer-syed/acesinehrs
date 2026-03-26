---
layout: splash
permalink: /research/
title: "Research & Outputs"
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
 .tailwind-wrap li, .tailwind-wrap ul {
  font-family: 'Inter', sans-serif !important;
 }
  
 /* Reset link styles BUT ignore custom components */
 .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.pub-link):not(.text-blue-600):not(.scholar-link):not(.gs-title) {
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
  font-size: 30px !important; font-weight: 700 !important; color: #0f172a !important;
  margin-top: 0 !important; margin-bottom: 1.5rem !important; border: none !important; padding: 0 !important;
 }
  
 /* FORCE all main content paragraphs to static 16px */
 .content-text {
  font-size: 16px !important; line-height: 1.75 !important; color: #475569 !important; margin-bottom: 1.25rem !important;
 }

 /* FEATURED RESEARCH CARDS */
 .research-card {
  background-color: #ffffff !important; 
  border-radius: 1.25rem !important; 
  border: 1px solid #bfdbfe !important; 
  box-shadow: 0 4px 6px -1px rgba(37, 99, 235, 0.05), 0 2px 4px -1px rgba(37, 99, 235, 0.03) !important;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1) !important;
  display: flex !important; flex-direction: column !important; overflow: hidden !important; height: 100% !important;
 }
 .research-card:hover {
  transform: translateY(-6px) !important; 
  border-color: #60a5fa !important; 
  box-shadow: 0 20px 25px -5px rgba(37, 99, 235, 0.1), 0 0 0 3px rgba(191, 219, 254, 0.4) !important;
 }
 .research-card .img-wrapper {
  width: 100% !important; height: 200px !important; overflow: hidden !important; background-color: #f1f5f9 !important;
  border-bottom: 1px solid #e2e8f0 !important;
 }
 .research-card img {
  width: 100% !important; height: 100% !important; object-fit: cover !important; transition: transform 0.5s ease !important; margin: 0 !important;
 }
 .research-card:hover img { transform: scale(1.05) !important; }
 .research-card .content-wrapper {
  padding: 1.5rem !important; display: flex !important; flex-direction: column !important; flex-grow: 1 !important; background-color: #ffffff !important;
 }
 .research-card .card-title {
  font-size: 18px !important; font-weight: 700 !important; color: #0f172a !important; margin: 0 0 0.75rem 0 !important; line-height: 1.4 !important; border: none !important;
 }
 .research-card .card-excerpt {
  font-size: 14.5px !important; line-height: 1.6 !important; color: #475569 !important; margin: 0 0 1.5rem 0 !important; flex-grow: 1 !important;
 }
 .btn-card {
  align-self: flex-start !important; background-color: #475569 !important; color: #ffffff !important; font-size: 13px !important; font-weight: 600 !important;
  padding: 8px 16px !important; border-radius: 6px !important; text-decoration: none !important; transition: all 0.3s ease !important; border: none !important;
 }
 .research-card:hover .btn-card { 
  background-color: #2563eb !important; 
  box-shadow: 0 4px 6px -1px rgba(37, 99, 235, 0.2) !important;
 }

 /* PUBLICATION LIST */
 .pub-item {
  display: flex !important; flex-direction: column !important; gap: 1rem !important;
  padding: 1.5rem 0 !important; border-bottom: 1px solid #e2e8f0 !important;
 }
 @media (min-width: 640px) {
  .pub-item { flex-direction: row !important; justify-content: space-between !important; align-items: flex-start !important; }
 }
 .pub-item:last-child { border-bottom: none !important; }
 .pub-link {
  font-size: 16px !important; font-weight: 600 !important; color: #2563eb !important; line-height: 1.5 !important;
  text-decoration: none !important; transition: color 0.2s !important; border: none !important; display: block !important;
 }
 .pub-link:hover { color: #1d4ed8 !important; text-decoration: underline !important; text-underline-offset: 3px !important; }

 /* WIDGET STYLES */
 .scholar-feed::-webkit-scrollbar { width: 6px; }
 .scholar-feed::-webkit-scrollbar-track { background: #f1f5f9; border-radius: 4px; }
 .scholar-feed::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 4px; }
 .scholar-feed::-webkit-scrollbar-thumb:hover { background: #94a3b8; }

 html { scroll-behavior: smooth; }
</style>

<!-- Load Altmetric Embed Script ONCE for the whole page -->
<script type="text/javascript" src="https://d1bxh8uas1mnw7.cloudfront.net/assets/embed.js" async></script>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

 <!-- Hero Section -->
 <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20home%20page%202023.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
  <div class="relative z-10 max-w-5xl mx-auto px-6 py-20 md:py-28 text-center md:text-left">
   <h1 class="hero-title drop-shadow-lg">
    Research <span style="color: #bfdbfe !important;">& Outputs</span>
   </h1>
    
   <!-- mx-auto for mobile centering, md:mx-0 for left align on desktop -->
   <p class="hero-subtitle drop-shadow-md mx-auto md:mx-0">
    Explore peer-reviewed publications, academic presentations, and research outputs generated using the ACEs in EHRs framework.
   </p>
    
   <div class="mt-8 flex flex-col md:flex-row items-center md:justify-start gap-4">
    <!-- Upgraded Button Styling for better contrast -->
    <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext" target="_blank" class="inline-flex items-center px-5 py-2.5 bg-slate-800 bg-opacity-60 hover:bg-opacity-80 border border-blue-400 rounded-full text-white text-sm font-medium transition-all backdrop-blur-md shadow-md">
     <span class="flex h-2.5 w-2.5 relative mr-3">
      <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-blue-300 opacity-75"></span>
      <span class="relative inline-flex rounded-full h-2.5 w-2.5 bg-blue-400"></span>
     </span>
     New study out in Lancet Public Health!
    </a>
   </div>
  </div>
 </header>

 <!-- SECTION 1: Featured Outputs -->
 <section class="bg-slate-50 py-16 border-b border-slate-200 shadow-inner">
  <div class="max-w-6xl mx-auto px-6">
    
   <div class="text-center mb-12">
    <p class="content-text font-medium text-slate-600">
     <a href="#publication-list" class="text-blue-600 hover:underline">Selected publications</a> and outputs using the ACEs in EHRs library.
    </p>
   </div>

   <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
     
    <!-- Feature Card 1 -->
    <a href="/research-aces-firstborns-siblings/" class="research-card group">
     <div class="img-wrapper">
      <img src="https://www.ucl.ac.uk/news/sites/news/files/styles/large_image/public/boy_shadows-fotor-2025020410261.png?itok=JKqj-dAX" alt="Firstborns and siblings">
     </div>
     <div class="content-wrapper">
      <h3 class="card-title">Adverse childhood experiences in firstborns and mental health risk and health-care use in siblings</h3>
      <p class="card-excerpt">Children are nearly three-quarters (71%) more likely to develop mental health problems between the ages of five and 18, if the firstborn child in their family experienced adversity during their first....</p>
      <span class="btn-card">Learn more</span>
     </div>
    </a>

    <!-- Feature Card 2 -->
    <a href="/research-acamh-ipv/" class="research-card group">
     <div class="img-wrapper">
      <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/acamh%20seminar%20ipv%20and%20aces%202023%20thumbnail.jpg" alt="ACAMH Seminar">
     </div>
     <div class="content-wrapper">
      <h3 class="card-title">ACAMH Seminar - Interrelationships between parental mental health, intimate partner violence and child mental health</h3>
      <p class="card-excerpt">Watch our recent ACAMH presentation of our publication exploring clinically relevant family adversity indicators of IPV aimed at improving responses to affected families presenting to healthcare...</p>
      <span class="btn-card">Learn more</span>
     </div>
    </a>

    <!-- Feature Card 3 (UPDATED TITLE) -->
    <a href="/research-aces-ipv/" class="research-card group">
     <div class="img-wrapper">
      <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/Syed%202023%20Family%20adversity%20and%20IPV%20and%20lancet%20public%20health.png" alt="Family adversity and health characteristics">
     </div>
     <div class="content-wrapper">
      <h3 class="card-title">Family adversity and health characteristics associated with intimate partner violence in children and parents</h3>
      <p class="card-excerpt">Intimate partner violence (IPV) is a significant public health issue that affects millions of women worldwide. One in three women experiences IPV, translating to over 800 million women globally...</p>
      <span class="btn-card">Learn more</span>
     </div>
    </a>

    <!-- Feature Card 4 (Validation Study) -->
    <a href="/research-acesinehrs-validation/" class="research-card group">
     <div class="img-wrapper">
      <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20getting%20started%20page.jpg" alt="Validation Study">
     </div>
     <div class="content-wrapper">
      <h3 class="card-title">Identifying adverse childhood experiences with electronic health records of linked mothers and children in England</h3>
      <p class="card-excerpt">A multistage development and validation study establishing clinically relevant ACE indicators in routine healthcare data. A total of 63 distinct ACE indicators were developed and validated for use in routine EHRs...</p>
      <span class="btn-card">Learn more</span>
     </div>
    </a>

    <!-- Feature Card 5 (Review) -->
    <a href="/research-review-ipv-cm/" class="research-card group">
     <div class="img-wrapper">
      <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/aces%20in%20ehrs%20research%20review%20CM%20IPV.png" alt="State of the art review">
     </div>
     <div class="content-wrapper">
      <h3 class="card-title">State of the art review: indicators of child maltreatment and intimate partner violence</h3>
      <p class="card-excerpt">Intimate partner violence (IPV) and child maltreatment (CM) are forms of family violence that often go unnoticed by services, despite recommendations to improve monitoring efforts by the World Health Organization (WHO)..</p>
      <span class="btn-card">Learn more</span>
     </div>
    </a>

   </div>
  </div>
 </section>

 <!-- SECTION 2: Impact & Real-World Results -->
 <section class="bg-slate-900 text-white py-16 md:py-20 border-b border-slate-800">
  <div class="max-w-6xl mx-auto px-6 grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
    
   <!-- Left Column: Impact Text -->
   <div class="lg:col-span-5">
    <h2 class="text-3xl font-bold mb-6 text-white border-none leading-tight">
     Real-World Impact:<br><span class="text-blue-400">From Research to Results</span>
    </h2>
     
    <div class="flex gap-4 mb-8">
     <div class="bg-slate-800 border border-slate-700 rounded-lg p-4 flex-1 text-center">
      <div class="text-2xl font-bold text-white">100+</div>
      <div class="text-[11px] text-slate-400 uppercase tracking-wide mt-1">Weekly Global Visits</div>
     </div>
     <div class="bg-slate-800 border border-slate-700 rounded-lg p-4 flex-1 text-center">
      <div class="text-2xl font-bold text-emerald-400">40+</div>
      <div class="text-[11px] text-slate-400 uppercase tracking-wide mt-1">Peer-Reviewed Citations</div>
     </div>
    </div>

    <p class="text-slate-300 text-[15px] leading-relaxed mb-6">
     The ACEsinEHRs open-access platform shares essential coding algorithms, tutorials, and theoretical frameworks that have been widely adopted by researchers globally.
    </p>
     
    <div class="space-y-4 text-sm text-slate-300">
     <div class="flex items-start">
      <i class="fas fa-check-circle text-blue-400 mt-1 mr-3 text-[15px]"></i>
      <div style="line-height: 1.6;">
       <strong class="text-white">Advancing predictive algorithms:</strong> Our code lists have facilitated the creation of the first externally validated algorithms for identifying child maltreatment in routine care, and developed machine learning models predicting childhood mental health issues.
      </div>
     </div>
     <div class="flex items-start">
      <i class="fas fa-check-circle text-blue-400 mt-1 mr-3 text-[15px]"></i>
      <div style="line-height: 1.6;">
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

     <!-- Scrollable Feed (UPDATED CITATIONS) -->
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
     <div class="mt-6 flex flex-col sm:flex-row gap-3 pt-5 border-t border-slate-100">
      <a href="https://scholar.google.co.uk/scholar?cites=17825954885314129992&as_sdt=2005&sciodt=0,5&hl=en" target="_blank" class="scholar-link flex-1 bg-slate-50 hover:bg-slate-100 border border-slate-200 text-slate-700 text-[13px] font-semibold py-3 px-4 rounded-lg flex items-center justify-center transition-colors">
       View Core Study 1 Citations <i class="fas fa-external-link-alt ml-2 text-[11px]"></i>
      </a>
      <a href="https://scholar.google.co.uk/scholar?cites=15768036519941313473&as_sdt=2005&sciodt=0,5&hl=en" target="_blank" class="scholar-link flex-1 bg-blue-50 hover:bg-blue-100 border border-blue-100 text-blue-700 text-[13px] font-semibold py-3 px-4 rounded-lg flex items-center justify-center transition-colors">
       View Core Study 2 Citations <i class="fas fa-external-link-alt ml-2 text-[11px]"></i>
      </a>
     </div>

    </div>
   </div>
  </div>
 </section>

 <!-- SECTION 3: Publication List -->
 <section id="publication-list" class="bg-white py-16 md:py-24">
  <div class="max-w-4xl mx-auto px-6">
    
   <div class="flex items-center gap-4 mb-10 pb-4 border-b-2 border-slate-100">
    <div class="w-12 h-12 rounded-full bg-blue-50 text-blue-600 flex items-center justify-center shrink-0">
     <i class="fas fa-file-alt text-xl"></i>
    </div>
    <h2 class="content-heading !m-0 !border-none !pb-0 text-slate-800">Publication list</h2>
   </div>

   <div class="space-y-2">
     
    <!-- Pub Item -->
    <div class="pub-item group">
     <a href="https://doi.org/10.1016/S2468-2667(24)00301-3" target="_blank" class="pub-link pr-4">
      Adverse childhood experiences in firstborns and mental health risk and health-care use in siblings: a population-based birth cohort study of half a million children in England
     </a>
     <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end mt-2 sm:mt-0">
      <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="173795607"></div>
     </div>
    </div>

    <!-- Pub Item -->
    <div class="pub-item group">
     <a href="https://doi.org/10.1016/S2468-2667(23)00119-6" target="_blank" class="pub-link pr-4">
      Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England
     </a>
     <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end mt-2 sm:mt-0">
      <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="150725211"></div>
     </div>
    </div>

    <!-- Pub Item (No Altmetric) -->
    <div class="pub-item group">
     <a href="https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2801832" target="_blank" class="pub-link pr-4">
      Association of interparental violence and maternal depression with depression among adolescents at the population and individual level
     </a>
     <div class="shrink-0 min-w-[60px]"></div>
    </div>

    <!-- Pub Item -->
    <div class="pub-item group">
     <a href="https://doi.org/10.1016/S2589-7500(22)00061-9" target="_blank" class="pub-link pr-4">
      Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study
     </a>
     <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end mt-2 sm:mt-0">
      <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="128460919"></div>
     </div>
    </div>

    <!-- Pub Item -->
    <div class="pub-item group">
     <a href="https://doi.org/10.1038/s41598-023-34011-3" target="_blank" class="pub-link pr-4">
      An external validation of coding for childhood maltreatment in routinely collected primary and secondary care data
     </a>
     <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end mt-2 sm:mt-0">
      <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="148625842"></div>
     </div>
    </div>

    <!-- Pub Item -->
    <div class="pub-item group">
     <a href="http://dx.doi.org/10.1136/archdischild-2020-319027" target="_blank" class="pub-link pr-4">
      Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis
     </a>
     <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end mt-2 sm:mt-0">
      <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="88250923"></div>
     </div>
    </div>

    <!-- Pub Item (No Altmetric) -->
    <div class="pub-item group">
     <a href="https://journals.sagepub.com/doi/full/10.1177/10775595221079308" target="_blank" class="pub-link pr-4">
      Leveraging administrative data to better understand and address child maltreatment: a scoping review of data linkage studies
     </a>
     <div class="shrink-0 min-w-[60px]"></div>
    </div>

    <!-- Pub Item (No Altmetric) -->
    <div class="pub-item group">
     <a href="https://jamanetwork.com/journals/jamanetworkopen/article-abstract/2807932" target="_blank" class="pub-link pr-4">
      Association of pregnancy-specific alcohol policies with infant morbidities and maltreatment
     </a>
     <div class="shrink-0 min-w-[60px]"></div>
    </div>

    <!-- Pub Item (No Altmetric) -->
    <div class="pub-item group">
     <a href="https://link.springer.com/article/10.1186/s12916-021-02119-w" target="_blank" class="pub-link pr-4">
      The risk of COVID-19 in survivors of domestic violence and abuse
     </a>
     <div class="shrink-0 min-w-[60px]"></div>
    </div>

    <!-- Pub Item (No Altmetric) -->
    <div class="pub-item group">
     <a href="https://journals.sagepub.com/doi/abs/10.1177/15248380221090977" target="_blank" class="pub-link pr-4">
      The measurement of intimate partner violence using International Classification of Diseases diagnostic codes: a systematic review
     </a>
     <div class="shrink-0 min-w-[60px]"></div>
    </div>

    <!-- Pub Item -->
    <div class="pub-item group">
     <a href="https://doi.org/10.1093/pubmed/fdaa115" target="_blank" class="pub-link pr-4">
      Are children who are home from school at an increased risk of child maltreatment?
     </a>
     <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end mt-2 sm:mt-0">
      <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="86946201"></div>
     </div>
    </div>

    <!-- Pub Item -->
    <div class="pub-item group">
     <a href="http://dx.doi.org/10.1136/bmjopen-2019-036564" target="_blank" class="pub-link pr-4">
      Association between health indicators of maternal adversity and the rate of infant entry to local authority care in England: a longitudinal ecological study
     </a>
     <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end mt-2 sm:mt-0">
      <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="88240312"></div>
     </div>
    </div>

    <!-- Pub Item -->
    <div class="pub-item group">
     <a href="https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(17)31045-0/fulltext" target="_blank" class="pub-link pr-4">
      Causes of death up to 10 years after admissions to hospitals for self-inflicted, drug-related or alcohol-related, or violent injury during adolescence: a retrospective, nationwide, cohort study
     </a>
     <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end mt-2 sm:mt-0">
      <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="20533675"></div>
     </div>
    </div>

    <!-- Pub Item -->
    <div class="pub-item group">
     <a href="https://bmjopen.bmj.com/content/5/2/e006079" target="_blank" class="pub-link pr-4">
      Violence, self-harm and drug or alcohol misuse in adolescents admitted to hospitals in England for injury: a retrospective cohort study
     </a>
     <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end mt-2 sm:mt-0">
      <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="3443408"></div>
     </div>
    </div>

    <!-- Pub Item -->
    <div class="pub-item group">
     <a href="https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.1001931" target="_blank" class="pub-link pr-4">
      10-y Risks of Death and Emergency Re-admission in Adolescents Hospitalised with Violent, Drug- or Alcohol-Related, or Self-Inflicted Injury: A Population-Based Cohort Study
     </a>
     <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end mt-2 sm:mt-0">
      <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="4934607"></div>
     </div>
    </div>

   </div>
    
   <!-- Hidden Author Tag for SEO Indexing -->
   <span class="hidden">Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate</span>

  </div>
 </section>

 <!-- Logos Banner (Footer Equivalent) -->
 <section class="bg-slate-50 border-t border-slate-200 py-8 shadow-inner">
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
