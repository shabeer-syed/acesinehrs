---
layout: splash
title: "Adverse childhood experiences in firstborns and mental health risk and health-care use in siblings"
permalink: /research-aces-firstborns-siblings/
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
  color: #1e3a8a !important; /* Dark navy blue from Anna Freud site */
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
 <header class="relative bg-[#1e293b] text-white pt-12 pb-24 md:pt-16 md:pb-32" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20getting%20started%20page.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
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
    Adverse childhood experiences in firstborns and mental health risk and health-care use in siblings
   </h1>
   <p class="text-slate-300 text-lg md:text-xl mb-8 leading-relaxed font-light max-w-3xl drop-shadow">
    A population-based birth cohort study of half a million children in England
   </p>
   
   <div class="flex flex-wrap items-center gap-6 text-sm text-slate-300 font-medium">
    <span class="flex items-center"><i class="far fa-calendar-alt mr-2 text-blue-400"></i> 4 February 2025</span>
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
      <h3 class="text-slate-900 font-bold text-lg m-0 border-none">Published in The Lancet Public Health</h3>
      <p class="text-slate-500 text-[14.5px] m-0 mt-1 leading-snug">Read the full peer-reviewed, first-of-its-kind study funded by the National Institute for Health and Care Research.</p>
     </div>
    </div>
    <a href="https://doi.org/10.1016/S2468-2667(24)00301-3" target="_blank" class="shrink-0 w-full md:w-auto text-center inline-flex items-center justify-center px-6 py-3.5 bg-blue-600 hover:bg-blue-700 text-white font-semibold rounded-xl shadow-md hover:shadow-lg transition-all btn-custom text-[15px]">
     View Publication <i class="fas fa-external-link-alt ml-2 text-sm opacity-80"></i>
    </a>
   </div>

   <!-- Article Body -->
   <div class="bg-white rounded-2xl p-8 md:p-12 shadow-sm border border-slate-200">
    
    <h2 class="text-2xl font-bold text-slate-900 mb-6 border-b border-slate-100 pb-3">Key findings</h2>

    <p class="article-text">
     Children are nearly three-quarters (71%) more likely to develop mental health problems between the ages of five and 18, if the firstborn child in their family experienced adversity during their first 1,000 days, finds a new study led by UCL researchers.
    </p>

    <p class="article-text">
     The first-of-its-kind study, published in <em>The Lancet Public Health</em> and funded by the National Institute for Health and Care Research Policy Research Programme, found that mothers whose firstborns had experienced adverse childhood experiences had a 71% increased risk of having children (aged five - 18) with mental health problems, compared to mothers whose firstborn did not experience adversity.
    </p>

    <p class="article-text font-medium text-slate-800">
     This translates to 12 additional children with mental health problems for every 100 mothers whose firstborn experienced adversity.
    </p>

    <p class="article-text">
     These findings underscore the pervasive risk that early adversity can have on multiple children in the family, and the importance of early identification and sustained support for vulnerable families beyond the first 1,000 days of a child's life.
    </p>

    <p class="article-text">
     As part of the study, researchers analysed linked GP and hospital health records from 333,048 first-time mothers and their 534,904 children (firstborns and siblings) born in England between 2002 and 2018. They focused on six different forms of adverse childhood experiences in the firstborn child recorded during their first 1,000 days of life (from conception up until the age of two).
    </p>

    <p class="article-text">
     These included: child maltreatment, intimate partner violence, maternal substance misuse, maternal mental health problems, adverse family environments (e.g. homelessness), and high-risk presentations of child maltreatment (e.g. unexplained child injuries).
    </p>

    <ul class="list-disc pl-6 mb-8 text-[17px] text-slate-700 space-y-3">
     <li>Over a third (37.1%) of firstborn children had at least one recorded adverse childhood experience.</li>
     <li>The most common adverse childhood experiences were living with maternal mental health problems (21.6%), followed by adverse family environments (14.5%) such as parental criminality and housing instability.</li>
     <li>Approximately one in five (19.8%) mothers had at least one child with a recorded mental health problem between the ages of five and 18.</li>
    </ul>

    <p class="article-text">
     Mothers whose firstborns experienced adverse childhood experiences had significantly more children with mental health problems (average of 30 per 100 mothers) compared to mothers whose firstborns did not (average of 17 per 100 mothers).
    </p>

    <p class="article-text">
     The risk of mental health problems was consistent across all siblings, regardless of birth order (firstborn vs thirdborn), in families where the firstborn experienced adverse childhood experiences. Furthermore, children in families where the firstborn experienced adversity also had <strong>50% more emergency hospital admissions</strong> for any reason and double the amount of mental health-related healthcare contacts.
    </p>

    <!-- Expert Quotes Section (Anna Freud Style) -->
    
    <h3 class="author-heading">Lead author Dr Shabeer Syed (UCL Great Ormond Street Institute of Child Health), said:</h3>
    <div class="quote-text">
     <p class="mb-3">“Whilst previous research has focused on the impact of adverse childhood experiences on individual children, our study reveals a cascading health risk that extends beyond the individual, impacting on the health of siblings as well.</p>
     <p class="mb-0">“This likely stems from the continuation of adverse childhood experiences within the family. When a child or parent presents with mental health concerns, violence or other forms of adversity, it's essential to ask about the wider family context.”</p>
    </div>

    <h3 class="author-heading">Professor Jessica Deighton (UCL Psychology & Language Sciences, and Anna Freud), said:</h3>
    <div class="quote-text">
     <p class="mb-3">“With escalating rates of children and young people in contact with mental health services, early and effective prevention strategies are the key to improving wellbeing. These findings indicate that, when we encounter children facing significant challenges like domestic abuse or poverty, we must expand our focus to the whole family, including siblings. This would help to ensure all children and young people within families dealing with adversity receive appropriate care as early as possible.</p>
     <p class="mb-0">“To achieve this, we want to see increased funding for prevention schemes and harness community assets – such as GPs and local organisations – which are crucial for helping to identify and meet the needs of vulnerable young people. There should also be, in partnership with diverse groups of children and young people, the development of a comprehensive, cross-government mental health prevention strategy.”</p>
    </div>

    <p class="article-text mt-8">
     As a result of their findings, the team are also calling for further research into the impact of early health visiting and primary care support.
    </p>

    <h3 class="author-heading">Senior author, Professor Ruth Gilbert (UCL Great Ormond Street Institute of Child Health), said:</h3>
    <div class="quote-text">
     <p class="mb-3">“Prevention of childhood mental health problems through intensive support in early life for parents and their first and subsequent children could potentially benefit multiple family members.</p>
     <p class="mb-0">“Research is needed to assess whether early community support from health visitors, GPs and practical parenting support for families whose first or subsequent children are affected by adverse childhood experiences reduces mental health problems later in childhood.”</p>
    </div>

    <h3 class="author-heading">Co-author, Professor Gene Feder (University of Bristol Centre for Academic Primary Care), said:</h3>
    <div class="quote-text">
     <p class="mb-3">“General practice teams have a key role in identifying first-born children experiencing adverse childhood experiences and in supporting first-time parents to help reduce the impact of adverse childhood experiences on the whole family, including subsequent children.</p>
     <p class="mb-0">“We need further evidence for effective interventions to reduce that impact, particularly on mental health.”</p>
    </div>

    <!-- Study Limitations Box -->
    <div class="mt-12 bg-slate-50 border border-slate-200 rounded-xl p-6 md:p-8">
     <h2 class="text-xl font-bold text-slate-900 mb-4 border-none flex items-center">
      <i class="fas fa-info-circle text-slate-400 mr-3"></i> Study limitations
     </h2>
     <ul class="list-disc pl-6 text-[15px] text-slate-600 space-y-3 m-0">
      <li>The researchers could not investigate adverse childhood experiences related to fathers’ mental health or substance use as healthcare data from fathers could not be linked to their children.</li>
      <li>The study found that adverse childhood experiences in firstborns were associated with mental health outcomes in the first and subsequent children, but this does not necessarily mean that adverse childhood experiences directly cause mental health problems.</li>
      <li>Additionally, electronic health-care records underestimate intimate partner violence and child maltreatment due to non-disclosure and/or detection and under-recording by clinicians.</li>
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
