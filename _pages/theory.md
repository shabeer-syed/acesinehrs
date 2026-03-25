---
layout: splash
permalink: /theory/
title: "Theoretical frameworks and definitions"
description: "This page provides a comprehensive overview of the key theoretical frameworks used to understand the impact of ACEs on individuals and their development."
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
  .masthead__inner-wrap .site-logo img { max-height: 24px !important; width: auto !important; }
  .masthead__menu-item a { font-family: 'Inter', sans-serif !important; font-size: 16px !important; font-weight: 500 !important; color: #6b7280 !important; }
  .masthead__menu-item a:hover { color: #111827 !important; }

  /* === BREAK OUT TO FULL SCREEN === */
  .full-bleed {
    width: 100vw; position: relative; left: 50%; right: 50%;
    margin-left: -50vw; margin-right: -50vw;
    background-color: #ffffff !important;
    margin-bottom: 0 !important; padding-bottom: 5rem !important;
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
  .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.feature-card):not(.grid-card):not(.text-blue-600):not(.text-blue-400):not(.text-indigo-700) {
    border-bottom: none !important; text-decoration: none !important; box-shadow: none !important;
  }

  /* === HERO TYPOGRAPHY === */
  .hero-title {
    font-size: 48px !important; line-height: 1.1 !important; font-weight: 700 !important;
    color: rgb(255, 255, 255) !important; margin-bottom: 24px !important; border: none !important;
  }
  .hero-subtitle {
    font-size: 20px !important; line-height: 1.5 !important; font-weight: 400 !important;
    color: rgb(241, 245, 249) !important; margin-bottom: 0 !important;
    max-width: 820px !important; margin-left: auto !important; margin-right: auto !important;
  }

  /* === PREMIUM CONTENT STYLES === */
  .content-heading {
    font-size: 32px !important; font-weight: 700 !important; color: #0f172a !important;
    margin-bottom: 1.25rem !important; letter-spacing: -0.025em !important; border-bottom: none !important; margin-top: 2rem !important;
  }
  .content-subheading {
    font-size: 24px !important; font-weight: 600 !important; color: #1e293b !important;
    margin-bottom: 1rem !important; margin-top: 2rem !important; border: none !important;
  }
  .content-text {
    font-size: 17px !important; line-height: 1.75 !important; color: #475569 !important; margin-bottom: 1.5rem !important;
  }
  .content-text-dark {
    font-size: 17px !important; line-height: 1.75 !important; color: #cbd5e1 !important; margin-bottom: 1.5rem !important;
  }

  /* SUPERSCRIPT RESET (Prevents line-height warping) */
  sup {
    font-size: 0.75em;
    line-height: 0;
    position: relative;
    vertical-align: baseline;
    top: -0.5em;
  }

  /* Modern Info Cards */
  .feature-card {
    background: #ffffff !important; border-radius: 1rem !important; border: 1px solid #e2e8f0 !important;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; padding: 2rem !important;
    transition: transform 0.3s ease, box-shadow 0.3s ease !important;
  }
  .feature-card:hover {
    transform: translateY(-4px) !important; box-shadow: 0 12px 20px -3px rgba(0, 0, 0, 0.1) !important;
  }

  /* Clean Lists */
  .custom-list { list-style: none !important; padding: 0 !important; margin: 0 !important; }
  .custom-list li {
    position: relative !important; padding-left: 2.25rem !important; margin-bottom: 1.25rem !important;
    font-size: 16px !important; line-height: 1.6 !important; color: #475569 !important;
  }
  
  /* Dark Mode List */
  .custom-list-dark { list-style: none !important; padding: 0 !important; margin: 0 !important; }
  .custom-list-dark li {
    position: relative !important; padding-left: 2.5rem !important; margin-bottom: 1.25rem !important;
    font-size: 16px !important; line-height: 1.6 !important; color: #e2e8f0 !important;
  }
  .custom-list-dark li svg {
    position: absolute !important; left: 0 !important; top: 0.25rem !important; width: 1.5rem !important; height: 1.5rem !important; color: #60a5fa !important;
  }

  /* Modern Bottom Grid Cards */
  .grid-card {
    background-color: #ffffff !important; border-radius: 1.25rem !important; border: 1px solid #e2e8f0 !important;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1) !important;
    text-decoration: none !important; display: flex !important; flex-direction: column !important; overflow: hidden !important;
  }
  .grid-card:hover {
    transform: translateY(-6px) !important; box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1) !important; border-color: #cbd5e1 !important;
  }
  .grid-card .img-wrapper {
    background-color: #ffffff !important; padding: 2.5rem 2rem 1.5rem 2rem !important; display: flex !important; justify-content: center !important; align-items: center !important;
  }
  .grid-card img {
    transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1) !important; width: auto !important; height: 120px !important; object-fit: contain !important; margin: 0 auto !important;
  }
  .grid-card:hover img { transform: scale(1.06) !important; }
  .grid-card .content-wrapper {
    padding: 1.5rem !important; flex-grow: 1 !important; background-color: #f8fafc !important; text-align: center !important; border-top: 1px solid #f1f5f9 !important;
  }
  .grid-card .card-title {
    font-size: 19px !important; font-weight: 700 !important; color: #0f172a !important; margin: 0 0 10px 0 !important; border: none !important; transition: color 0.3s ease !important;
  }
  .grid-card:hover .card-title { color: #2563eb !important; }
  
  html { scroll-behavior: smooth; }
</style>

<!-- HIDDEN SVG DEFINITIONS FOR ARROWHEAD MARKERS -->
<svg style="width:0; height:0; position:absolute;" aria-hidden="true" focusable="false">
  <defs>
    <!-- Solid Greyish Marker for Inter-Box Flow -->
    <marker id="arrow-grey" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto">
      <path d="M 0 0 L 10 5 L 0 10 z" fill="#94a3b8" />
    </marker>
  </defs>
</svg>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

  <!-- Hero Section -->
  <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20home%20page%202023.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
    <div class="relative z-10 max-w-5xl mx-auto px-6 py-20 md:py-24 text-center">
      <h1 class="hero-title drop-shadow-lg">
        Theoretical frameworks <span style="color: #bfdbfe !important;">& definitions</span>
      </h1>
      <p class="hero-subtitle drop-shadow-md">
        Explore the foundational concepts that underpin the ACE indicators within Electronic Health Records.
      </p>
    </div>
  </header>

  <main class="flex-grow">
    
    <!-- SEO INTRO BANNER -->
    <section class="bg-blue-50 border-b border-blue-100 py-8 relative z-20 shadow-sm">
      <div class="max-w-4xl mx-auto px-6 text-center flex flex-col md:flex-row items-center justify-center gap-4">
        <div class="flex-shrink-0 w-12 h-12 rounded-full bg-blue-100 text-blue-600 flex items-center justify-center">
          <i class="fas fa-book-reader text-xl"></i>
        </div>
        <p class="text-[19px] md:text-[21px] font-medium text-blue-900 leading-relaxed m-0 border-none text-left">
          <strong>This page provides a comprehensive overview of the key theoretical frameworks used to understand the impact of ACEs on individuals and their development.</strong>
        </p>
      </div>
    </section>

    <!-- SECTION 1: Background & Core Concept (White) -->
    <section class="max-w-4xl mx-auto px-6 py-12 md:py-16">
      <h2 class="content-heading mt-0">Background</h2>
      <p class="content-text">
        Adverse childhood experiences (ACEs) are potentially traumatic, neglectful or <a href="https://www.who.int/violenceprevention/approach/definition/en/" target="_blank" class="text-blue-600 font-medium hover:underline">violent</a> experiences in childhood. Examples of ACEs range from child maltreatment and witnessing violence in the home to growing up with a parent with a mental health problem<sup><a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext" target="_blank" class="text-blue-600 font-medium hover:underline">1</a></sup>.
      </p>
      <p class="content-text">
        The concept of adversity is not new. However, the term "ACEs" was first introduced by a groundbreaking <a href="https://pubmed.ncbi.nlm.nih.gov/9635069/" target="_blank" class="text-blue-600 font-medium hover:underline">study published</a> in 1998 by the Centers for Disease Control and Prevention (CDC) and the Kaiser Permanente health care organisation in California, USA<sup><a href="https://pubmed.ncbi.nlm.nih.gov/9635069/" target="_blank" class="text-blue-600 font-medium hover:underline">2</a></sup>. Led by co-principal investigators Dr Vincent Felitti and Dr Robert Anda, the study originated from repeated clinical observations within an obesity treatment programme during the 1980s. As doctors gathered patient histories, they noticed that severe weight gain, smoking, and substance use were frequently linked to early abuse or household dysfunction<sup><a href="https://www.sciencedirect.com/science/article/pii/S074937971930100X#bib0002" target="_blank" class="text-blue-600 font-medium hover:underline">3</a></sup>.
      </p>
      <p class="content-text">
        They hypothesised that for many people, severe weight gain may be the result of an unconscious coping mechanism to manage unrecognised childhood trauma<sup><a href="https://pubmed.ncbi.nlm.nih.gov/9635069/" target="_blank" class="text-blue-600 font-medium hover:underline">2</a></sup>. This led to a study evaluating over 17,000 adult patients, where the researchers established a strong dose-response relationship between the number of ACEs and health problems in adults, including premature death.
      </p>
      <p class="content-text mb-12">
        The concept of ACEs helped bring together and measure a diverse set of preventable adverse childhood experiences that can lead to considerable long-term health problems, and can substantially pressure families, health and social care systems<sup><a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext" target="_blank" class="text-blue-600 font-medium hover:underline">1</a></sup>.
      </p>

      <!-- CDC Style Callout Box for the 10 ACEs (Redesigned matching snippet) -->
      <div class="bg-[#f8fafc] rounded-2xl border border-blue-100 overflow-hidden shadow-md">
        <div class="bg-[#2563eb] px-6 py-4">
          <h3 class="text-xl font-bold text-white m-0 border-none flex items-center tracking-wide">
            <i class="fas fa-clipboard-list mr-3 opacity-90 text-lg"></i> The Original Ten ACEs
          </h3>
        </div>
        <div class="p-6 md:p-8">
          <p class="content-text">The initial ACEs predominately referred to domains of adversity in the home environment. They are typically categorised into the following main groups:</p>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            
            <!-- Child Maltreatment Card -->
            <div class="bg-white px-5 pt-4 pb-5 rounded-xl shadow-sm border border-slate-100 border-t-4 border-t-rose-500 transition-all duration-300 hover:-translate-y-1 hover:shadow-md">
              <h4 class="text-rose-600 font-bold mb-2 flex items-center text-lg"><i class="fas fa-child mr-2 text-rose-500"></i> Child maltreatment</h4>
              <ul class="space-y-2 list-disc pl-5" style="font-size: 15px !important; color: #475569 !important;">
                <li>Psychological abuse</li>
                <li>Physical abuse</li>
                <li>Sexual abuse</li>
                <li>Physical neglect*</li>
                <li>Emotional neglect*</li>
              </ul>
            </div>

            <!-- Household Dysfunction Card -->
            <div class="bg-white px-5 pt-4 pb-5 rounded-xl shadow-sm border border-slate-100 border-t-4 border-t-emerald-500 transition-all duration-300 hover:-translate-y-1 hover:shadow-md">
              <h4 class="text-emerald-700 font-bold mb-2 flex items-center text-lg"><i class="fas fa-house-damage mr-2 text-emerald-500"></i> Household dysfunction</h4>
              <ul class="space-y-2 list-disc pl-5" style="font-size: 15px !important; color: #475569 !important;">
                <li>Substance abuse</li>
                <li>Mental illness</li>
                <li>Intimate partner violence<sup>†</sup></li>
                <li>Criminal behaviour</li>
                <li>Parental separation*</li>
              </ul>
            </div>

          </div>
          
          <!-- Redesigned Tiny Footnotes (Aggressively forced to 10px so Jekyll cannot override) -->
          <div class="mt-8 pt-4 border-t border-slate-200 space-y-2">
            <p style="font-size: 10px !important; line-height: 1.4 !important; margin: 0 !important;" class="text-slate-500 italic">
              *Not included in the initial ACE domains <sup><a href="https://pubmed.ncbi.nlm.nih.gov/9635069/" target="_blank" class="text-blue-600 hover:underline">2</a></sup>; added in later studies to form the "Ten ACEs."
            </p>
            <p style="font-size: 10px !important; line-height: 1.4 !important; margin: 0 !important;" class="text-slate-500 italic">
              <sup>†</sup>In the UK, children exposed to intimate partner violence are legally recognised as victims of domestic abuse in their own right, and this exposure is classified as a form of child abuse <sup><a href="https://www.gov.uk/government/publications/domestic-abuse-bill-2020-factsheets/statutory-definition-of-domestic-abuse-factsheet" target="_blank" class="text-blue-600 hover:underline">4</a></sup>.
            </p>
          </div>
        </div>
      </div>

      <!-- Definition of ACEs Box (Added top border accent matching bottom box) -->
      <div class="mt-10 bg-[#f8fafc] rounded-2xl border border-slate-200 border-t-[6px] border-t-blue-500 overflow-hidden shadow-md">
        <div class="bg-slate-100 px-6 py-4 border-b border-slate-200">
          <h3 class="text-xl font-bold text-slate-800 m-0 border-none flex items-center tracking-wide">
            <i class="fas fa-book-open mr-3 text-blue-600 opacity-90 text-lg"></i> Definition of ACEs
          </h3>
        </div>
        <div class="p-6 md:p-8 bg-white">
          <p class="content-text mb-6 font-medium text-slate-700">ACEs can be defined as any experience within the family environment considered to be:</p>
          <ul class="custom-list mb-6 space-y-4">
            <li>
              <i class="far fa-check-circle text-blue-500 absolute left-0 top-1 text-[1.15rem]"></i>
              <span>Frightening, violent, traumatic or neglectful (<a href="https://apps.who.int/iris/bitstream/handle/10665/42495/9241545615_eng.pdf" target="_blank" class="text-blue-600 hover:underline">see WHO violence definition</a>), with potential for immediate or longer-term harm to a child's biopsychosocial development (intentionally or unintentionally) (<a href="https://assets.publishing.service.gov.uk/media/65cb4349a7ded0000c79e4e1/Working_together_to_safeguard_children_2023_-_statutory_guidance.pdf" target="_blank" class="text-blue-600 hover:underline">see UK government definition</a>);</span>
            </li>
            <li>
              <i class="far fa-check-circle text-blue-500 absolute left-0 top-1 text-[1.15rem]"></i>
              <span>Caused by a single event or through repeated exposure;</span>
            </li>
            <li>
              <i class="far fa-check-circle text-blue-500 absolute left-0 top-1 text-[1.15rem]"></i>
              <span>Caused by external factors and not the child themselves, such as self-harm; and</span>
            </li>
            <li>
              <i class="far fa-check-circle text-blue-500 absolute left-0 top-1 text-[1.15rem]"></i>
              <span>Amenable to health or social care intervention at a family level (i.e. excluding wider factors such as socioeconomic status, community violence, school bullying etc)*.</span>
            </li>
          </ul>
          
          <!-- New Footnote section for Definition box -->
          <div class="mt-6 pt-5 border-t border-slate-200">
            <p style="font-size: 11px !important; line-height: 1.5 !important; margin: 0 0 10px 0 !important; color: #64748b !important;">
              *Refers to the ACEs included as part of the research examining ACEs using electronic health records <sup><a href="https://www.thelancet.com/journals/landig/article/PIIS2589-7500(22)00061-9/fulltext" target="_blank" style="color: #2563eb !important; text-decoration: underline !important;">1</a>, <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(23)00119-6/fulltext" target="_blank" style="color: #2563eb !important; text-decoration: underline !important;">2</a>, <a href="https://www.thelancet.com/journals/lanpub/article/piis2468-2667(24)00301-3/fulltext" target="_blank" style="color: #2563eb !important; text-decoration: underline !important;">3</a></sup>.
            </p>
            <a href="#definitions-and-inclusions" class="inline-flex items-center text-blue-600 font-semibold hover:text-blue-800 hover:underline transition-colors mt-2 text-[15px]">
              Read full inclusion criteria and rationale <i class="fas fa-arrow-down ml-2 text-sm"></i>
            </a>
          </div>
        </div>
      </div>

    </section>

    <!-- SECTION 2: Conceptual Model & Diagram (Slate 50) -->
    <section class="bg-slate-50 py-12 md:py-16 border-y border-slate-200 shadow-inner">
      <div class="max-w-5xl mx-auto px-6">
        
        <h2 class="content-heading text-center mt-0 mb-4 border-none">Theory and frameworks</h2>
        <h3 class="content-subheading text-center mt-0 mb-8 border-none text-slate-600">A conceptual model of ACEs: the biopsychosocial approach</h3>
        
        <div class="max-w-4xl mx-auto">
          <p class="content-text text-center">
            The concept of ACEs is not based on a single theory. Instead, it is best understood through an integrative biopsychosocial model that combines psychological, biological, and sociological perspectives. The goal of this model is to explain why ACEs occur, how they lead to long-term health and social problems, and why their effects vary depending on the specific type or number of adversities experienced.
          </p>
          <p class="content-text text-center">
            This model uses the socio-ecological systems theories of <a href="https://psycnet.apa.org/record/1978-06857-001" target="_blank" class="text-blue-600 font-medium hover:underline">Bronfenbrenner (1977)</a> and <a href="https://psycnet.apa.org/record/1980-12117-001" target="_blank" class="text-blue-600 font-medium hover:underline">Belsky (1980)</a> as a foundational platform. By focusing specifically on the first two ecological levels—the individual and the family environment—this approach deliberately restricts the definition of ACEs to those that are clinically measurable and intervenable at the family level, whilst acknowledging that other adversities occur in the wider community.
          </p>
          <p class="content-text text-center">
            Across these two ecological levels, the model integrates several key frameworks to predict and understand relevant ACEs. These include attachment theory (Bowlby, 1969–1982; Ainsworth et al., 1978), the <a href="https://pubmed.ncbi.nlm.nih.gov/22201156/" target="_blank" class="text-blue-600 font-medium hover:underline">cumulative stress model</a> (encompassing both the <a href="https://www.nejm.org/doi/10.1056/NEJM199801153380307" target="_blank" class="text-blue-600 font-medium hover:underline">"allostatic load"</a> and <a href="https://www.publications.aap.org/pediatrics/article-split/129/1/e232/31628/The-Lifelong-Effects-of-Early-Childhood-Adversity" target="_blank" class="text-blue-600 font-medium hover:underline">"ecobiodevelopmental"</a> frameworks), and <a href="https://psycnet.apa.org/record/1989-26231-001" target="_blank" class="text-blue-600 font-medium hover:underline">cognitive behavioural theories of emotion</a>.
          </p>
        </div>

        <!-- Image Card with smaller, forced-white button -->
        <div class="mt-10 bg-white p-4 md:p-8 rounded-2xl shadow-md border border-slate-200 text-center relative overflow-hidden group">
          <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation%20lower%20res%201.png" alt="Biopsychosocial model of ACEs formulation" class="w-full h-auto object-contain rounded-lg mx-auto transition-transform duration-500 group-hover:scale-[1.02]" style="max-width: 800px; margin: 0 auto !important;">
          <p class="text-sm text-slate-500 mt-6 mb-4 italic">The figure does not represent an exhaustive list of potential mechanisms behind ACEs.</p>
          
          <!-- Made Button smaller (px-4 py-2) and forced text white (!important) -->
          <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation.png" target="_blank" style="color: #ffffff !important;" class="inline-flex items-center justify-center px-4 py-2 bg-blue-600 hover:bg-blue-700 text-sm font-semibold rounded-full transition-all duration-300 shadow-md hover:shadow-lg hover:-translate-y-0.5">
            <i class="fas fa-search-plus mr-2"></i> View Figure in High Resolution
          </a>

        </div>
      </div>
    </section>

    <!-- SECTION 3: Ecological Levels (White) -->
    <section class="max-w-5xl mx-auto px-6 py-12 md:py-16">
      <div class="text-center mb-12">
        <h2 class="content-heading mt-0 border-none">Ecological Levels & Theoretical Mechanisms</h2>
        <p class="content-text max-w-3xl mx-auto">Below, we summarise different key theories and mechanisms hypothesised to play a role in the ACEs framework. It does not represent an exhaustive list.</p>
      </div>
      
      <div class="space-y-0">
        <!-- Society Level (Subtle Purple Tint) -->
        <div class="bg-purple-50 p-6 rounded-xl shadow-sm border border-purple-100 border-t-4 border-t-purple-400 relative z-10 transition-all duration-300 hover:-translate-y-1 hover:shadow-md">
          <h3 class="content-subheading mt-0 flex items-center">
            <div class="w-10 h-10 rounded-full bg-purple-200 text-purple-600 flex items-center justify-center mr-3"><i class="fas fa-city text-lg"></i></div>
            Society & community level
          </h3>
          <p class="content-text" style="margin-bottom: 0 !important;">Social determinants of health encompass socioeconomic conditions that shape health outcomes for individuals, families and communities. Children with ACEs are more likely to grow up in environments where raising a family and coping with everyday challenges is harder. Families may live in communities with high unemployment and a lack of local resources for families, with parents having to travel long distances to work, or family members may be more likely to suffer from health problems that make it difficult to work.</p>
        </div>

        <!-- Arrow connecting the ecological levels -->
        <div class="flex justify-center my-4 text-slate-300 text-4xl">
          <i class="fas fa-arrow-down"></i>
        </div>

        <!-- Individual & Family Level Container -->
        <div class="bg-[#f8fafc] rounded-2xl p-6 md:p-10 border border-slate-200 shadow-sm relative">
          
          <h3 class="content-subheading mt-0 mb-8 flex items-center border-none relative z-20">
            <div class="w-10 h-10 rounded-full bg-slate-200 text-slate-600 flex items-center justify-center mr-3"><i class="fas fa-users text-lg"></i></div>
            Individual & family level
          </h3>

          <!-- The Theory Boxes Grid -->
          <div class="grid grid-cols-1 lg:grid-cols-2 gap-x-8 gap-y-12 relative z-10 pt-6">
            
            <!-- Card 1: Attachment (Subtle Teal Tint) -->
            <div class="bg-teal-50 p-6 rounded-xl shadow-md border border-teal-100 border-t-4 border-t-teal-400 transition-all duration-300 hover:-translate-y-1 hover:shadow-lg relative z-20">
              
              <!-- GREY ARROW 2: Anchored to Bottom of Card 1 (Drops down into Cognitive Card) -->
              <svg class="absolute hidden lg:block pointer-events-none z-10" style="top: 100%; left: 20%; width: 40px; height: 60px; overflow: visible;" viewBox="0 0 40 60">
                <path d="M 20 0 C -10 30, -10 30, 20 60" fill="none" stroke="#94a3b8" stroke-width="3" marker-end="url(#arrow-grey)" stroke-linecap="round" />
              </svg>

              <h4 class="text-lg font-bold text-slate-800 mb-3"><i class="fas fa-link text-teal-600 mr-2"></i> Attachment and learning theory</h4>
              <p class="content-text" style="margin-bottom: 0 !important; font-size: 15px !important;">Social risk factors can negatively influence carers' ability to respond, such as being available and responsive to a child's attachment cues. Children with ACEs may be more likely to develop insecure attachments from reduced caregiving responses of emotional validation (e.g., "my pain matters") and reduced experiences of healthy parental modelling of emotion regulation. This can also mean a child loses friends and the support of adults and misses out on opportunities to grow social support networks.</p>
            </div>

            <!-- Card 2: Life Course (Subtle Amber/Yellow Tint) -->
            <div class="bg-amber-50 p-6 rounded-xl shadow-md border border-amber-100 border-t-4 border-t-amber-400 transition-all duration-300 hover:-translate-y-1 hover:shadow-lg relative z-20">
              
              <!-- GREY ARROW 1: Anchored to Left side of Card 2 (Arcs over to Card 1) -->
              <svg class="absolute hidden lg:block pointer-events-none z-10" style="top: 40px; right: 100%; width: 60px; height: 30px; overflow: visible;" viewBox="0 0 60 30">
                <path d="M 60 15 C 30 -15, 30 -15, 0 15" fill="none" stroke="#94a3b8" stroke-width="3" marker-end="url(#arrow-grey)" stroke-linecap="round" />
              </svg>

              <!-- GREY ARROW 3: Anchored to Bottom of Card 2 (Drops down into Cognitive Card) -->
              <svg class="absolute hidden lg:block pointer-events-none z-10" style="top: 100%; right: 20%; width: 40px; height: 60px; overflow: visible;" viewBox="0 0 40 60">
                <path d="M 20 0 C 50 30, 50 30, 20 60" fill="none" stroke="#94a3b8" stroke-width="3" marker-end="url(#arrow-grey)" stroke-linecap="round" />
              </svg>

              <h4 class="text-lg font-bold text-slate-800 mb-3"><i class="fas fa-road text-amber-600 mr-2"></i> Life-course approach</h4>
              <p class="content-text" style="margin-bottom: 0 !important; font-size: 15px !important;">Taken together, the model views ACEs as a complex social phenomenon and considers families as resilient and constantly striving to cope using different strategies and resources at hand. The model helps separate the <em>adverse experience</em> from the <em>adverse stress</em> response, overcoming previous limitations of reverse causality when looking at long-term outcomes. We consider ACEs recorded at the family level amenable to service intervention and relevant to EHRs.</p>
            </div>
            
            <!-- Card 3: Cognitive & Behavioural (Subtle Rose/Red Tint, Spans both columns) -->
            <div class="bg-rose-50 p-6 md:p-8 rounded-xl shadow-md border border-rose-100 border-t-4 border-t-rose-400 lg:col-span-2 transition-all duration-300 hover:-translate-y-1 hover:shadow-lg relative z-20 mt-4 lg:mt-0">
              <h4 class="text-lg font-bold text-slate-800 mb-4"><i class="fas fa-brain text-rose-600 mr-2"></i> Cognitive and behavioural theories</h4>
              
              <p class="content-text" style="font-size: 15px !important;">
                People cope with stress and perceived threats using various survival strategies—such as <strong>avoidance, escape, or fighting</strong>—to minimise negative consequences. Children who grow up in dangerous, unpredictable, or highly stressful environments are more likely to perceive the world as unsafe and doubt their ability to manage challenges. To cope, children may develop <strong>cognitive biases towards threats</strong>, suppress their emotions, and avoid situations they fear will cause distress (aligning with <a href="https://psycnet.apa.org/record/1986-15090-001" target="_blank" class="text-blue-600 hover:underline">theories on emotional processing</a>, <a href="https://pubmed.ncbi.nlm.nih.gov/10402694/" target="_blank" class="text-blue-600 hover:underline">selective attention and overestimation of threat</a>).
              </p>
              <p class="content-text" style="font-size: 15px !important;">
                While these coping mechanisms hold functional value and provide a short-term sense of safety, they can increase the long-term risk of health problems. <strong>First,</strong> these strategies overemphasise threats, creating a heightened state of alert that becomes difficult to "turn off" even in safer, normative environments where the behaviours are no longer effective. These children have a smaller window of tolerance to stress and perceived threat. <strong>Second,</strong> survival responses like avoidance, withdrawal, or reactive hostility prevent opportunities for new learning and the development of balanced cognitive appraisals (such as realising: "I'm safe", "I can cope"). As these children grow, their trauma responses and behaviour can drive peers away, stripping them of protective social networks and increasing their vulnerability. This creates a <strong>maintenance cycle of stress</strong><sup><a href="https://doi.org/10.1111/jcpp.12713" target="_blank" class="text-blue-600 hover:underline">4</a>, <a href="https://doi.org/10.1016/j.chiabu.2016.08.003" target="_blank" class="text-blue-600 hover:underline">5</a></sup>.
              </p>
              <p class="content-text" style="font-size: 15px !important;">
                For some families, these social risk factors and coping responses are <strong>carried over across generations</strong> as children become parents themselves. Whilst strategies are perceived as logical at the moment, over time, they can leave families in a cycle that perpetuates stress. As underlying stress increases, caregivers and children have fewer resources to cope and regulate responses (e.g. reduced response inhibition/executive functioning)<sup><a href="https://pubmed.ncbi.nlm.nih.gov/12212647/" target="_blank" class="text-blue-600 hover:underline">6</a></sup>, increasing the risk of more immediate coping responses to escape or re-gaining control (e.g. shouting, violence, neglect).
              </p>
              <p class="content-text" style="margin-bottom: 0 !important; font-size: 15px !important;">
                Coping responses may vary as a function of the level of need to escape distress and harm, ranging from immediate escape (e.g. violence, substance misuse, abandonment/neglect) to stronger forms of avoidance (e.g. avoiding going out, which reduces social support systems in the longer-term)<sup><a href="https://link.springer.com/article/10.1023/B:JOBA.0000007455.08539.94" target="_blank" class="text-blue-600 hover:underline">7</a></sup>.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION 4: Risk Prediction & Challenges (Slate 100) -->
    <section class="bg-slate-100 py-12 md:py-16 border-y border-slate-200">
      <div class="max-w-4xl mx-auto px-6">
        
        <!-- Updated Exact Color match #1e3a8a for prominent dark blue heading -->
        <h2 class="content-heading text-center mt-0 mb-12 border-none" style="color: #1e3a8a !important;">Adverse Childhood Experiences (ACEs) using Electronic Health Records (EHRs)</h2>

        <h3 class="content-subheading mt-0 border-none"><i class="fas fa-chart-line text-blue-500 mr-2"></i> A multistage risk prediction model to determine relevance of candidate ACEs</h3>
        <p class="content-text">
          We assessed the relevance of identified candidate ACE indicators based on their consistent risk association with a reference standard of family violence in a multistage prediction model. The reference standard (outcome) was any occurrence of child maltreatment (CM) and maternal intimate partner violence (mIPV) up to 5-years post-birth.
        </p>
        <p class="content-text">
          Consistent with our theoretical model, we predicted that the final ACE indicators would reflect a continuum of clinical relevance, ranging from a high risk of family violence (i.e. high need for intervention) to lower relevance, consistent with previously studied ACEs domains.
        </p>

        <h3 class="content-subheading mt-10 border-none"><i class="fas fa-exclamation-circle text-rose-500 mr-2"></i> Challenges in defining ACEs</h3>
        <p class="content-text">
          Since the late 1990s, the initial "ACE domains" have undergone numerous expansions across studies. Whilst this variation helped innovate and adapt indicators of ACEs to different goals, there is currently little consistency in the definition and inclusion of ACEs. The large variation of measured ACEs also means there is no agreed reference standard for developing new measures of ACEs.
        </p>
        <p class="content-text">
          Previous studies have mainly assessed the validity and relevance of ACEs based on their risk association with poorer health outcomes in adulthood. However, most studies reporting on the negative health effects of ACEs are based on cross-sectional samples of adults asked to recall experiences from childhood<sup><a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext" target="_blank" class="text-blue-600 font-medium hover:underline">1</a></sup>. Recent birth cohort studies, however, reveal that ACEs are relatively poor predictors of negative health outcomes in adulthood relative to other socioeconomic factors<sup><a href="https://jamanetwork.com/journals/jamapediatrics/article-abstract/2775420" target="_blank" class="text-blue-600 font-medium hover:underline">2</a></sup>. 
        </p>

        <div class="border-l-4 border-l-blue-400 bg-blue-50 p-5 rounded-r-lg my-6">
          <p class="text-blue-900 font-medium mb-0" style="font-size: 16px; line-height: 1.6;">
            <i class="fas fa-quote-left text-blue-300 mr-2"></i> Global studies by the World Health Organization show that traumatic stress symptoms naturally resolve on average six years after a linked traumatic event (e.g., an ACE)<sup><a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5632781/" target="_blank" class="text-blue-600 hover:underline">3</a>, <a href="https://jamanetwork.com/journals/jamapsychiatry/fullarticle/2595039" target="_blank" class="text-blue-600 hover:underline">4</a></sup>.
          </p>
        </div>

        <p class="content-text">
          These gaps create multiple challenges when attempting to develop new indicators of ACEs for electronic health records (EHRs).
        </p>

        <h3 class="content-subheading mt-10 border-none"><i class="fas fa-check-circle text-emerald-500 mr-2"></i> Establishing a consistent definition</h3>
        <p class="content-text mb-0">
          To enhance consistency in developing clinically relevant ACE indicators for different data sources, we conducted several studies<sup><a href="https://linkinghub.elsevier.com/retrieve/pii/S2589750022000619" target="_blank" class="text-blue-600 font-medium hover:underline">4</a></sup> to establish a definition of ACEs based on a set of criteria. We also developed a testable theoretical biopsychosocial model of ACEs. This model facilitates theoretically informed predictions of which ACE indicators might be more relevant than others.
        </p>
      </div>
    </section>

    <!-- SECTION 5: Definitions and Inclusions (DARK MODE - High Premium Contrast) -->
    <section id="definitions-and-inclusions" class="bg-slate-900 py-16 md:py-20 border-b border-slate-800">
      <div class="max-w-4xl mx-auto px-6">
        <h2 class="text-3xl font-bold text-white mb-10 text-center border-none">Definitions and Inclusions</h2>
        
        <div class="bg-slate-800 rounded-2xl border border-blue-500 shadow-2xl overflow-hidden relative mb-10">
          <div class="h-2 w-full bg-blue-500 absolute top-0 left-0"></div>
          <div class="p-8 md:p-10">
            <p class="content-text-dark font-semibold text-white mb-6">
              We defined ACE indicators as any experience within the family environment recorded in the child or the parent data source (e.g. health record) considered to be:
            </p>
            
            <ul class="custom-list-dark">
              <li>
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                Frightening, violent, traumatic or neglectful <a href="https://apps.who.int/iris/bitstream/handle/10665/42495/9241545615_eng.pdf" target="_blank" class="text-blue-400 hover:underline">(see WHO violence definition)</a>, with potential for immediate or longer-term harm to a child's biopsychosocial development (intentionally or unintentionally) <a href="https://assets.publishing.service.gov.uk/media/65cb4349a7ded0000c79e4e1/Working_together_to_safeguard_children_2023_-_statutory_guidance.pdf" target="_blank" class="text-blue-400 hover:underline">(see UK government definition)</a>;
              </li>
              <li>
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                Caused by a single event or through repeated exposure;
              </li>
              <li>
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                Caused by external factors and not the child themselves, such as self-harm; and
              </li>
              <li>
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                Amenable to health or social care intervention at a family level (i.e. excluding wider factors such as socioeconomic status, community violence, school bullying etc.)<sup><a href="https://jamanetwork.com/journals/jama/fullarticle/2783975" target="_blank" class="text-blue-400 hover:underline">1</a>, <a href="https://www.gov.uk/government/publications/supporting-families-programme-guidance-2022-to-2025/chapter-4-identifying-and-working-with-families" target="_blank" class="text-blue-400 hover:underline">2</a>, <a href="https://www.sciencedirect.com/science/article/abs/pii/S0749379719300315" target="_blank" class="text-blue-400 hover:underline">3</a></sup>.
              </li>
            </ul>
          </div>
        </div>

        <p class="content-text-dark">
          We made several adaptations to previously studied ACEs for feasible ascertainment in electronic health records (EHRs). We defined indicators as variables of grouped codes and measures. We aimed to develop ACE indicators that reflected clinically meaningful risk groups of adversity to identify families that may be eligible for targeted maternal-child care interventions in England (e.g. <a href="https://www.gov.uk/government/publications/supporting-families-programme-guidance-2021-to-2022" target="_blank" class="text-blue-400 font-medium hover:underline">Supporting Families programme</a>, or previously "targeted care pathway" of <a href="https://www.gov.uk/government/publications/healthy-child-programme-0-to-19-health-visitor-and-school-nurse-commissioning" target="_blank" class="text-blue-400 font-medium hover:underline">the Healthy Child Programme</a>. See also WHO for <a href="https://www.who.int/teams/social-determinants-of-health/violence-prevention/global-status-report-on-violence-against-children-2020" target="_blank" class="text-blue-400 font-medium hover:underline">intervention studies</a>).
        </p>

        <p class="content-text-dark">
          We manually grouped indicators into broader ACE domains consistent with the <a href="https://www.ajpmonline.org/article/S0749-3797(98)00017-8/fulltext" target="_blank" class="text-blue-400 font-medium hover:underline">original study</a> by <a href="https://www.cdc.gov/violenceprevention/aces/index.html" target="_blank" class="text-blue-400 font-medium hover:underline">Kaiser Permanente and CDC</a>. Due to the lack of recordings, we collapsed all types of child abuse and neglect into child maltreatment (CM). We collapsed "imprisonment of household members" and "household challenges" into Adverse family environments. We created a separate indicator, "Social service involvement" (SSI), for social care-related codes that did not contain descriptions of CM or IPV. Due to few recordings and high intercorrelations, SSI was merged with CM in the final selection process.
        </p>

        <p class="content-text-dark">
          Given the substantial under-recording of CM and IPV<sup><a href="https://www.cambridge.org/core/journals/the-british-journal-of-psychiatry/article/barriers-and-facilitators-of-disclosures-of-domestic-violence-by-mental-health-service-users-qualitative-study/7A690CCBC0322D045442549A5FA3C4CF" target="_blank" class="text-blue-400 hover:underline">1</a>, <a href="https://bjgp.org/content/67/659/e437.long" target="_blank" class="text-blue-400 hover:underline">2</a></sup>, we also added the domain “high-risk presentations of CM” (HRP-CM). HRP-CM encompassed indicators from the <a href="https://www.nice.org.uk/guidance/cg89/chapter/1-Guidance" target="_blank" class="text-blue-400 font-medium hover:underline">National Institute for Health and Care Excellence (NICE)</a> and <a href="https://www.rcgp.org.uk/clinical-and-research/resources/toolkits/child-safeguarding-toolkit.aspx" target="_blank" class="text-blue-400 font-medium hover:underline">Royal College of General Practitioners (RGCP)</a> that should raise clinical suspicion for CM.
        </p>

        <div class="mt-8 bg-slate-800 p-6 rounded-xl border-l-4 border-l-emerald-500">
          <p class="content-text-dark mb-0 italic">
            <strong>Note:</strong> ACEs can be recorded in both parents’ and children’s records. ACEs are considered based on each specific child’s time from birth. Children are, therefore, considered unexposed if no relevant recording occurs during the study period, regardless of previous exposure to children within the same family. This approach mirrors changes in stress levels as the family moves through different life stages.
          </p>
        </div>
      </div>
    </section>

    <!-- SECTION 6: Next Steps / Navigation Grid (White) -->
    <section class="max-w-4xl mx-auto px-6 py-16">
      <div class="grid grid-cols-1 sm:grid-cols-2 gap-8">
        <a href="https://acesinehrs.com/ACE-domains/" class="grid-card group">
          <div class="img-wrapper" style="padding-bottom: 0 !important;">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/home%20view%20domains.png" alt="View Domains" style="height: 180px !important;">
          </div>
          <div class="content-wrapper mt-4">
            <h3 class="card-title">Explore ACE Domains</h3>
            <p class="text-sm text-slate-500 mb-0">View comprehensive lists of selected indicators.</p>
          </div>
        </a>

        <a href="https://acesinehrs.com/codelistbrowse/" class="grid-card group">
          <div class="img-wrapper" style="padding-bottom: 0 !important;">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png" alt="Code Lists" style="height: 180px !important;">
          </div>
          <div class="content-wrapper mt-4">
            <h3 class="card-title">Browse Code Lists</h3>
            <p class="text-sm text-slate-500 mb-0">Search and access clinical code lists seamlessly.</p>
          </div>
        </a>
      </div>
      
      <div class="text-center mt-12">
        <a href="https://acesinehrs.com/" class="inline-flex items-center text-slate-500 hover:text-blue-600 font-medium transition-colors">
          <i class="fas fa-arrow-left mr-2"></i> Go back to homepage
        </a>
      </div>
    </section>

  </main>
</div>
