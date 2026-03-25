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
  .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.pub-link):not(.text-blue-600) {
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
    background-color: #ffffff !important; border-radius: 1.25rem !important; border: 1px solid #e2e8f0 !important;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1) !important;
    display: flex !important; flex-direction: column !important; overflow: hidden !important; height: 100% !important;
  }
  .research-card:hover {
    transform: translateY(-6px) !important; box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1) !important; border-color: #cbd5e1 !important;
  }
  .research-card .img-wrapper {
    width: 100% !important; height: 200px !important; overflow: hidden !important; background-color: #f1f5f9 !important;
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
    padding: 8px 16px !important; border-radius: 6px !important; text-decoration: none !important; transition: background-color 0.2s !important; border: none !important;
  }
  .research-card:hover .btn-card { background-color: #2563eb !important; }

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
      <!-- Added md:mx-0 to perfectly align left on desktop -->
      <p class="hero-subtitle drop-shadow-md mx-auto md:mx-0">
        Explore peer-reviewed publications, academic presentations, and research outputs generated using the ACEs in EHRs framework.
      </p>
      
      <div class="mt-8 flex flex-col md:flex-row items-center md:justify-start gap-4">
        <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext" target="_blank" class="inline-flex items-center px-5 py-2.5 bg-slate-900 bg-opacity-60 hover:bg-opacity-80 border border-slate-700 rounded-full text-blue-200 text-sm font-medium transition-all backdrop-blur-md">
          <span class="flex h-2.5 w-2.5 relative mr-3">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-blue-400 opacity-75"></span>
            <span class="relative inline-flex rounded-full h-2.5 w-2.5 bg-blue-500"></span>
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

        <!-- Feature Card 3 -->
        <a href="/research-aces-ipv/" class="research-card group">
          <div class="img-wrapper">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/Syed%202023%20Family%20adversity%20and%20IPV%20and%20lancet%20public%20health.png" alt="Clinical characteristics">
          </div>
          <div class="content-wrapper">
            <h3 class="card-title">Clinical characteristics of families affected by intimate partner violence</h3>
            <p class="card-excerpt">Intimate partner violence (IPV) is a violation against human rights that affects millions of women worldwide. One in three women experiences IPV, translating to over 800 million women globally...</p>
            <span class="btn-card">Learn more</span>
          </div>
        </a>

        <!-- Feature Card 4 -->
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

  <!-- SECTION 2: Publication List -->
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
          <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end">
            <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="173795607"></div>
          </div>
        </div>

        <!-- Pub Item -->
        <div class="pub-item group">
          <a href="https://doi.org/10.1016/S2468-2667(23)00119-6" target="_blank" class="pub-link pr-4">
            Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England
          </a>
          <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end">
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
          <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end">
            <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="128460919"></div>
          </div>
        </div>

        <!-- Pub Item -->
        <div class="pub-item group">
          <a href="https://doi.org/10.1038/s41598-023-34011-3" target="_blank" class="pub-link pr-4">
            An external validation of coding for childhood maltreatment in routinely collected primary and secondary care data
          </a>
          <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end">
            <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="148625842"></div>
          </div>
        </div>

        <!-- Pub Item -->
        <div class="pub-item group">
          <a href="http://dx.doi.org/10.1136/archdischild-2020-319027" target="_blank" class="pub-link pr-4">
            Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis
          </a>
          <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end">
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
          <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end">
            <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="86946201"></div>
          </div>
        </div>

        <!-- Pub Item -->
        <div class="pub-item group">
          <a href="http://dx.doi.org/10.1136/bmjopen-2019-036564" target="_blank" class="pub-link pr-4">
            Association between health indicators of maternal adversity and the rate of infant entry to local authority care in England: a longitudinal ecological study
          </a>
          <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end">
            <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="88240312"></div>
          </div>
        </div>

        <!-- Pub Item -->
        <div class="pub-item group">
          <a href="https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(17)31045-0/fulltext" target="_blank" class="pub-link pr-4">
            Causes of death up to 10 years after admissions to hospitals for self-inflicted, drug-related or alcohol-related, or violent injury during adolescence: a retrospective, nationwide, cohort study
          </a>
          <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end">
            <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="20533675"></div>
          </div>
        </div>

        <!-- Pub Item -->
        <div class="pub-item group">
          <a href="https://bmjopen.bmj.com/content/5/2/e006079" target="_blank" class="pub-link pr-4">
            Violence, self-harm and drug or alcohol misuse in adolescents admitted to hospitals in England for injury: a retrospective cohort study
          </a>
          <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end">
            <div class="altmetric-embed" data-badge-type="donut" data-altmetric-id="3443408"></div>
          </div>
        </div>

        <!-- Pub Item -->
        <div class="pub-item group">
          <a href="https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.1001931" target="_blank" class="pub-link pr-4">
            10-y Risks of Death and Emergency Re-admission in Adolescents Hospitalised with Violent, Drug- or Alcohol-Related, or Self-Inflicted Injury: A Population-Based Cohort Study
          </a>
          <div class="shrink-0 flex items-center opacity-90 group-hover:opacity-100 transition-opacity min-w-[60px] justify-end">
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
