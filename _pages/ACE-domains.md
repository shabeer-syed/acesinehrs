---
layout: splash
title: "All ACE domains & indicators"
permalink: /ACE-domains/
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
  .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.domain-card):not(.text-blue-600) {
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
    margin-top: 0 !important; margin-bottom: 2.5rem !important; border: none !important; padding: 0 !important;
  }
  
  /* DOMAIN CARDS */
  .domain-card {
    display: flex !important; align-items: center !important; gap: 1.25rem !important;
    background-color: #ffffff !important; border-radius: 1.25rem !important; border: 1px solid #e2e8f0 !important;
    padding: 1.25rem !important; transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1) !important;
    text-decoration: none !important; box-shadow: 0 2px 4px rgba(0,0,0,0.02) !important;
  }
  .domain-card:hover {
    transform: translateY(-4px) !important; box-shadow: 0 12px 20px -3px rgba(0, 0, 0, 0.08) !important; border-color: #cbd5e1 !important;
  }
  
  .img-circle {
    width: 100px !important; height: 100px !important; flex-shrink: 0 !important;
    border-radius: 50% !important; overflow: hidden !important; border: 3px solid #f8fafc !important;
    box-shadow: inset 0 2px 4px rgba(0,0,0,0.1) !important; background-color: #ffffff !important;
  }
  @media (min-width: 640px) {
    .img-circle { width: 120px !important; height: 120px !important; }
  }
  .domain-card img {
    width: 100% !important; height: 100% !important; object-fit: cover !important; 
    transition: transform 0.5s ease !important; margin: 0 !important; mix-blend-mode: multiply;
  }
  .domain-card:hover img { transform: scale(1.08) !important; }
  
  .card-content { display: flex !important; flex-direction: column !important; justify-content: center !important; }
  .card-title {
    font-size: 18px !important; font-weight: 700 !important; color: #1e293b !important; 
    margin: 0 0 0.5rem 0 !important; line-height: 1.3 !important; border: none !important; transition: color 0.2s !important;
  }
  .domain-card:hover .card-title { color: #2563eb !important; }
  
  .card-desc {
    font-size: 14px !important; line-height: 1.5 !important; color: #64748b !important; margin: 0 !important;
  }

  html { scroll-behavior: smooth; }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

  <!-- Hero Section -->
  <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20home%20page%202023.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
    <div class="relative z-10 max-w-5xl mx-auto px-6 py-20 md:py-28 text-center md:text-left">
      <h1 class="hero-title drop-shadow-lg">
        All ACE domains <span style="color: #bfdbfe !important;">& indicators</span>
      </h1>
      <p class="hero-subtitle drop-shadow-md mx-auto md:mx-0">
        Browse and access comprehensive lists of validated ACE indicators, organized by clinical domain, complete with definitions and relevance rankings.
      </p>
      
      <div class="mt-8 flex flex-col sm:flex-row items-center justify-center md:justify-start gap-4">
        
        <!-- Primary CTA 1 -->
        <a href="https://acesinehrs.com/starterguide/" class="inline-flex items-center px-6 py-3 bg-white text-slate-900 text-base font-bold rounded-full shadow-lg hover:shadow-xl hover:-translate-y-0.5 transition-all duration-300">
          Need help getting started? <i class="fas fa-arrow-right ml-2 text-blue-600"></i>
        </a>

        <!-- Primary CTA 2 -->
        <a href="https://acesinehrs.com/theory/" class="inline-flex items-center px-6 py-3 bg-white text-slate-900 text-base font-bold rounded-full shadow-lg hover:shadow-xl hover:-translate-y-0.5 transition-all duration-300">
          Theories & frameworks of ACEs? <i class="fas fa-arrow-right ml-2 text-blue-600"></i>
        </a>

      </div>
    </div>
  </header>

  <!-- Main Content Areas -->
  <main class="flex-grow bg-slate-50 py-16 md:py-24 border-b border-slate-200 shadow-inner">
    <div class="max-w-5xl mx-auto px-6">
      
      <h2 class="content-heading text-center md:text-left border-b-2 border-slate-200 pb-4 inline-block mx-auto md:mx-0">
        All ACE domains & indicators: definitions and code lists
      </h2>

      <!-- Domain Cards Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mt-8">
        
        <!-- Card 1: All Indicators -->
        <a href="https://shabeer-syed.github.io/acesinehrs/indicators/" class="domain-card group">
          <div class="img-circle">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/home%20view%20indicators.png" alt="All ACE Indicators">
          </div>
          <div class="card-content">
            <h3 class="card-title">View all ACE indicators</h3>
            <p class="card-desc">Lists all selected and excluded indicators, with relevance rankings.</p>
          </div>
        </a>

        <!-- Card 2: Child Maltreatment -->
        <a href="https://shabeer-syed.github.io/acesinehrs/CM/" class="domain-card group">
          <div class="img-circle">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/child%20maltreatment.png" alt="Child Maltreatment">
          </div>
          <div class="card-content">
            <h3 class="card-title">Child maltreatment</h3>
            <p class="card-desc">Lists all selected indicators.</p>
          </div>
        </a>

        <!-- Card 3: Intimate Partner Violence -->
        <a href="https://shabeer-syed.github.io/acesinehrs/IPV/" class="domain-card group">
          <div class="img-circle">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/Intimate%20partner%20violence.png" alt="Intimate Partner Violence">
          </div>
          <div class="card-content">
            <h3 class="card-title">Intimate partner violence</h3>
            <p class="card-desc">Lists all selected indicators.</p>
          </div>
        </a>

        <!-- Card 4: Parental Mental Health -->
        <a href="https://shabeer-syed.github.io/acesinehrs/MHPs/" class="domain-card group">
          <div class="img-circle">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/parental%20mental%20health%20problems.png" alt="Parental Mental Health Problems">
          </div>
          <div class="card-content">
            <h3 class="card-title">Parental mental health problems</h3>
            <p class="card-desc">Lists all selected indicators.</p>
          </div>
        </a>

        <!-- Card 5: Parental Substance Misuse -->
        <a href="https://shabeer-syed.github.io/acesinehrs/SM/" class="domain-card group">
          <div class="img-circle">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/Parental%20substance%20misuse.png" alt="Parental Substance Misuse">
          </div>
          <div class="card-content">
            <h3 class="card-title">Parental substance misuse</h3>
            <p class="card-desc">Lists all selected indicators.</p>
          </div>
        </a>

        <!-- Card 6: Adverse Family Environments -->
        <a href="https://shabeer-syed.github.io/acesinehrs/AFE/" class="domain-card group">
          <div class="img-circle">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/adverse%20family%20environments.png" alt="Adverse Family Environments">
          </div>
          <div class="card-content">
            <h3 class="card-title">Adverse family environments</h3>
            <p class="card-desc">Lists all selected indicators.</p>
          </div>
        </a>

        <!-- Card 7: High-Risk Presentation -->
        <a href="https://shabeer-syed.github.io/acesinehrs/HRPCM/" class="domain-card group">
          <div class="img-circle">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/high-risk%20presentattion%20of%20child%20maltreatment.png" alt="High-risk Presentation of Child Maltreatment">
          </div>
          <div class="card-content">
            <h3 class="card-title">High-risk presentation of child maltreatment</h3>
            <p class="card-desc">Lists all selected indicators.</p>
          </div>
        </a>

      </div>

      <!-- Hidden Author Tag for SEO Indexing -->
      <span class="hidden">Dr Shabeer Syed, Clinical Psychologist & Senior Research Associate</span>

    </div>
  </main>

  <!-- Logos Banner (Footer Equivalent) -->
  <section class="bg-white border-t border-slate-200 py-10 shadow-sm relative z-10">
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
