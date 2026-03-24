---
layout: splash
permalink: /theory/
title: "Theoretical frameworks and definitions"
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
  width: 100vw; position: relative; left: 50%; right: 50%; margin-left: -50vw; margin-right: -50vw;
  background-color: #ffffff !important; margin-bottom: 0 !important; padding-bottom: 5rem !important;
 }
  
 #main { padding-top: 0 !important; padding-bottom: 0 !important; margin-bottom: 0 !important; }

 /* === OVERRIDE JEKYLL FOOTER === */
 .page__footer { background-color: #0f172a !important; color: #94a3b8 !important; margin-top: 0 !important; padding: 3rem 0 !important; border-top: none !important; }
 .page__footer a { color: #cbd5e1 !important; text-decoration: none !important; }
 .page__footer a:hover { color: #ffffff !important; }
 .page__footer-copyright { color: #64748b !important; }

 /* === PROTECT TAILWIND FROM JEKYLL === */
 .tailwind-wrap { box-sizing: border-box; }
 .tailwind-wrap h1, .tailwind-wrap h2, .tailwind-wrap h3, .tailwind-wrap h4, .tailwind-wrap p, .tailwind-wrap a, .tailwind-wrap span, .tailwind-wrap div, .tailwind-wrap li, .tailwind-wrap ul { font-family: 'Inter', sans-serif !important; }
  
 /* Reset link styles BUT ignore custom components */
 .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.feature-card):not(.grid-card):not(.text-blue-600) { border-bottom: none !important; text-decoration: none !important; box-shadow: none !important; }

 /* === HERO TYPOGRAPHY === */
 .hero-title { font-size: 48px !important; line-height: 1.1 !important; font-weight: 700 !important; color: rgb(255, 255, 255) !important; margin-bottom: 24px !important; border: none !important; }
 .hero-subtitle { font-size: 20px !important; line-height: 1.5 !important; font-weight: 400 !important; color: rgb(241, 245, 249) !important; margin-bottom: 0 !important; max-width: 820px !important; margin-left: auto !important; margin-right: auto !important; }

 /* === PREMIUM CONTENT STYLES === */
 .content-heading { font-size: 32px !important; font-weight: 700 !important; color: #0f172a !important; margin-bottom: 1.25rem !important; letter-spacing: -0.025em !important; border-bottom: none !important; margin-top: 2rem !important; }
 .content-subheading { font-size: 24px !important; font-weight: 600 !important; color: #1e293b !important; margin-bottom: 1rem !important; margin-top: 2rem !important; border: none !important; }
 .content-text { font-size: 17px !important; line-height: 1.75 !important; color: #475569 !important; margin-bottom: 1.5rem !important; }
 
 /* Modern Info Cards */
 .feature-card { background: #ffffff !important; border-radius: 1rem !important; border: 1px solid #e2e8f0 !important; box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; padding: 2rem !important; transition: transform 0.3s ease, box-shadow 0.3s ease !important; }
 .feature-card:hover { transform: translateY(-4px) !important; box-shadow: 0 12px 20px -3px rgba(0, 0, 0, 0.1) !important; }

 /* Clean Lists */
 .custom-list { list-style: none !important; padding: 0 !important; margin: 0 !important; }
 .custom-list li { position: relative !important; padding-left: 2.5rem !important; margin-bottom: 1.25rem !important; font-size: 16px !important; line-height: 1.6 !important; color: #334155 !important; }
 .custom-list li svg { position: absolute !important; left: 0 !important; top: 0.25rem !important; width: 1.5rem !important; height: 1.5rem !important; }

 /* Modern Bottom Grid Cards */
 .grid-card { background-color: #ffffff !important; border-radius: 1.25rem !important; border: 1px solid #e2e8f0 !important; box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05) !important; transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1) !important; text-decoration: none !important; display: flex !important; flex-direction: column !important; overflow: hidden !important; }
 .grid-card:hover { transform: translateY(-6px) !important; box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1) !important; border-color: #cbd5e1 !important; }
 .grid-card .img-wrapper { background-color: #ffffff !important; padding: 2.5rem 2rem 1.5rem 2rem !important; display: flex !important; justify-content: center !important; align-items: center !important; }
 .grid-card img { transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1) !important; width: auto !important; height: 120px !important; object-fit: contain !important; margin: 0 auto !important; }
 .grid-card:hover img { transform: scale(1.06) !important; }
 .grid-card .content-wrapper { padding: 1.5rem !important; flex-grow: 1 !important; background-color: #f8fafc !important; text-align: center !important; border-top: 1px solid #f1f5f9 !important; }
 .grid-card .card-title { font-size: 19px !important; font-weight: 700 !important; color: #0f172a !important; margin: 0 0 10px 0 !important; border: none !important; transition: color 0.3s ease !important; }
 .grid-card:hover .card-title { color: #2563eb !important; }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

 <!-- Hero Section -->
 <header class="relative bg-slate-800 bg-opacity-70 text-white" 
  style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20home%20page%202023.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
  <div class="relative z-10 max-w-5xl mx-auto px-6 py-20 md:py-24 text-center">
   <h1 class="hero-title drop-shadow-lg">
    Theoretical frameworks <span style="color: #bfdbfe !important;">& definitions</span>
   </h1>
   <p class="hero-subtitle drop-shadow-md">
    Find out more about the different theoretical frameworks and definitions that underpin the ACE indicators within Electronic Health Records.
   </p>
  </div>
 </header>

 <main class="flex-grow">
  
  <!-- SECTION 1: Background & Core Concept -->
  <section class="max-w-4xl mx-auto px-6 py-12 md:py-16">
   <h2 class="content-heading mt-0">Background</h2>
   <p class="content-text">
    Adverse childhood experiences (ACEs) are potentially traumatic, neglectful or <a href="https://www.who.int/violenceprevention/approach/definition/en/" target="_blank" class="text-blue-600 font-medium hover:underline">violent</a> experiences in childhood. Examples of ACEs range from child maltreatment and witnessing violence in the home to growing up with a parent with a mental health problem <a href="https://www.cdc.gov/violenceprevention/aces/fastfact.html" target="_blank" class="text-blue-600 font-medium hover:underline">(1)</a>.
   </p>
   <p class="content-text">
    The concept of adversity is not new. However, the term "ACEs" was first introduced by a groundbreaking <a href="https://pubmed.ncbi.nlm.nih.gov/9635069/" target="_blank" class="text-blue-600 font-medium hover:underline">study published in 1998</a> by the Centers for Disease Control and the Kaiser Permanente health care organization in USA, California. The concept of ACEs helped bring together and measure a diverse set of preventable adverse childhood experiences that can lead to considerable long-term health problems, and can substantially pressure families, health and social care systems <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext" target="_blank" class="text-blue-600 font-medium hover:underline">(3)</a>. 
   </p>
   
   <!-- CDC Style Callout Box for the 10 ACEs -->
   <div class="mt-10 mb-8 bg-blue-50 rounded-2xl border border-blue-100 overflow-hidden shadow-sm">
    <div class="bg-blue-600 px-6 py-4">
     <h3 class="text-xl font-bold text-white m-0 border-none flex items-center">
      <i class="fas fa-clipboard-list mr-3 opacity-80"></i> The Original "Ten ACEs" Domains
     </h3>
    </div>
    <div class="p-6 md:p-8">
     <p class="text-slate-700 mb-6">The initial ACEs predominately referred to domains of adversity in the home environment. They are typically categorised into three main groups:</p>
     
     <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <div class="bg-white p-5 rounded-xl shadow-sm border border-slate-100">
       <h4 class="text-blue-800 font-bold mb-3 flex items-center"><i class="fas fa-child mr-2 text-blue-500"></i> Abuse</h4>
       <ul class="text-sm text-slate-600 space-y-2 list-disc pl-4">
        <li>Psychological abuse</li>
        <li>Physical abuse</li>
        <li>Sexual abuse</li>
       </ul>
      </div>
      <div class="bg-white p-5 rounded-xl shadow-sm border border-slate-100">
       <h4 class="text-emerald-800 font-bold mb-3 flex items-center"><i class="fas fa-house-damage mr-2 text-emerald-500"></i> Dysfunction</h4>
       <ul class="text-sm text-slate-600 space-y-2 list-disc pl-4">
        <li>Substance abuse</li>
        <li>Mental illness</li>
        <li>Domestic violence</li>
        <li>Criminal behaviour</li>
        <li>Parental separation</li>
       </ul>
      </div>
      <div class="bg-white p-5 rounded-xl shadow-sm border border-slate-100">
       <h4 class="text-rose-800 font-bold mb-3 flex items-center"><i class="fas fa-user-times mr-2 text-rose-500"></i> Neglect</h4>
       <ul class="text-sm text-slate-600 space-y-2 list-disc pl-4">
        <li>Physical neglect</li>
        <li>Emotional neglect</li>
       </ul>
      </div>
     </div>
    </div>
   </div>
   <p class="content-text italic text-slate-500">This page provides a comprehensive overview of the key theoretical frameworks used to understand the impact of these ACEs on individuals and their development.</p>
  </section>

  <!-- SECTION 2: Conceptual Model & Diagram -->
  <section class="bg-slate-50 py-12 md:py-16 border-y border-slate-200">
   <div class="max-w-5xl mx-auto px-6">
    <h2 class="content-heading text-center mt-0 mb-6">A conceptual model of ACEs: the biopsychosocial approach</h2>
    
    <div class="max-w-4xl mx-auto">
     <p class="content-text text-center">
      We developed a "testable" conceptual, integrative biopsychosocial model to help better understand ACEs and generate theoretically informed predictions of which ACE indicators might be more relevant than others. In this model, we integrate theories from the socio-ecological system theory by <a href="https://psycnet.apa.org/record/1978-06857-001" target="_blank" class="text-blue-600 font-medium hover:underline">Bronfenbrenner (1977)</a> and <a href="https://psycnet.apa.org/record/1980-12117-001" target="_blank" class="text-blue-600 font-medium hover:underline">Belsky (1980)</a> as a platform to map other theories relevant to ACEs within two ecological levels (the individual and the family environment). By focusing on the first two ecological levels, we restricted ACEs to clinically measurable and intervenable indicators at a family level.
     </p>
     <p class="content-text text-center">
      Across these two "ecological" levels, we make predictions of relevant ACEs based on attachment theory (Bowlby, 1969–82; Ainsworth et al., 1978), the <a href="https://pubmed.ncbi.nlm.nih.gov/22201156/" target="_blank" class="text-blue-600 font-medium hover:underline">cumulative stress model</a> (includes the <a href="https://www.nejm.org/doi/10.1056/NEJM199801153380307" target="_blank" class="text-blue-600 font-medium hover:underline">"allostatic load" model</a> and the <a href="https://www.publications.aap.org/pediatrics/article-split/129/1/e232/31628/The-Lifelong-Effects-of-Early-Childhood-Adversity" target="_blank" class="text-blue-600 font-medium hover:underline">"ecobiodevelopmental" framework</a>), and <a href="https://psycnet.apa.org/record/1989-26231-001" target="_blank" class="text-blue-600 font-medium hover:underline">cognitive behavioural theories of emotions</a>.
     </p>
    </div>

    <!-- Image Card -->
    <div class="mt-10 bg-white p-4 md:p-8 rounded-2xl shadow-md border border-slate-100 text-center">
     <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation%20lower%20res%201.png" alt="Biopsychosocial model of ACEs formulation" class="w-full h-auto object-contain rounded-lg mx-auto" style="max-width: 800px; margin: 0 auto !important;">
     <p class="text-sm text-slate-500 mt-6 mb-2 italic">The figure does not represent an exhaustive list of potential mechanisms behind ACEs.</p>
     <a href="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation.png" target="_blank" class="inline-flex items-center justify-center px-4 py-2 bg-slate-100 hover:bg-slate-200 text-slate-700 text-sm font-medium rounded-lg transition-colors">
      <i class="fas fa-search-plus mr-2"></i> Download figure in high resolution
     </a>
    </div>

   </div>
  </section>

  <!-- SECTION 3: Ecological Levels (Cards) -->
  <section class="max-w-5xl mx-auto px-6 py-12 md:py-16">
   <div class="text-center mb-12">
    <h2 class="content-heading mt-0 border-none">Ecological Levels & Theoretical Mechanisms</h2>
    <p class="content-text max-w-3xl mx-auto">Below, we summarise different key theories and mechanisms hypothesised to play a role in ACEs. It does not represent an exhaustive list.</p>
   </div>

   <div class="space-y-8">
    
    <!-- Society Level -->
    <div class="feature-card border-l-4 border-l-blue-500">
     <h3 class="content-subheading mt-0 flex items-center">
      <div class="w-10 h-10 rounded-full bg-blue-100 text-blue-600 flex items-center justify-center mr-3"><i class="fas fa-city text-lg"></i></div>
      Society & community level
     </h3>
     <p class="content-text mb-0">Social determinants of health encompass socioeconomic conditions that shape health outcomes for individuals, families and communities. Children with ACEs are more likely to grow up in environments where raising a family and coping with everyday challenges is harder. Families may live in communities with high unemployment and a lack of local resources for families, with parents having to travel long distances to work, or family members may be more likely to suffer from health problems that make it difficult to work.</p>
    </div>

    <!-- Individual & Family Level Container -->
    <div class="bg-slate-50 rounded-2xl p-6 md:p-8 border border-slate-100">
     <h3 class="content-subheading mt-0 mb-6 flex items-center">
      <div class="w-10 h-10 rounded-full bg-emerald-100 text-emerald-600 flex items-center justify-center mr-3"><i class="fas fa-users text-lg"></i></div>
      Individual & family level
     </h3>
     
     <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
      <!-- Attachment -->
      <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-200">
       <h4 class="text-lg font-bold text-slate-800 mb-3"><i class="fas fa-link text-emerald-500 mr-2"></i> Attachment and learning theory</h4>
       <p class="text-slate-600 text-sm leading-relaxed mb-0">Social risk factors can negatively influence carers' ability to respond, such as being available and responsive to a child's attachment cues. Children with ACEs may be more likely to develop insecure attachments from reduced caregiving responses of emotional validation (e.g., "my pain matters") and reduced experiences of healthy parental modelling of emotion regulation. This can also mean a child loses friends and the support of adults and misses out on opportunities to grow social support networks.</p>
      </div>

      <!-- Life Course -->
      <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-200">
       <h4 class="text-lg font-bold text-slate-800 mb-3"><i class="fas fa-road text-emerald-500 mr-2"></i> Life-course approach</h4>
       <p class="text-slate-600 text-sm leading-relaxed mb-0">Taken together, the model views ACEs as a complex social phenomenon and considers families as resilient and constantly striving to cope using different strategies and resources at hand. The model helps separate the <em>adverse experience</em> from the <em>adverse stress</em> response, overcoming previous limitations of reverse causality when looking at long-term outcomes. We consider ACEs recorded at the family level amenable to service intervention and relevant to EHRs.</p>
      </div>
      
      <!-- Cognitive & Behavioural (Full Width inside grid) -->
      <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-200 lg:col-span-2">
       <h4 class="text-lg font-bold text-slate-800 mb-3"><i class="fas fa-brain text-emerald-500 mr-2"></i> Cognitive and behavioural theories</h4>
       <p class="text-slate-600 text-sm leading-relaxed mb-4">People cope with stress and perceived threats using different preventative strategies (e.g. avoidance, escape, fight) to minimise negative consequences. Children who grew up in environments with increased levels of stress and unpredictability can be more likely to perceive the world as less safe and feel less confident they can manage. To cope, children may develop cognitive biases toward threats, learn to suppress emotions, and avoid situations they fear will cause further distress (e.g. see <a href="https://psycnet.apa.org/record/1986-15090-001" target="_blank" class="text-blue-600 hover:underline">theories on emotional processing</a>, <a href="https://pubmed.ncbi.nlm.nih.gov/10402694/" target="_blank" class="text-blue-600 hover:underline">selective attention and overestimation of threat</a>). Over time, however, this interaction prevents new learning of balanced threat appraisals (e.g. "I can cope"), creating a maintenance cycle of stress.</p>
       
       <p class="text-slate-600 text-sm leading-relaxed mb-4">For some families, these social risk factors and coping responses are carried over across generations as children become parents themselves. Whilst strategies are perceived as logical at the moment, over time, they can leave families in a cycle that perpetuates stress. As underlying stress increases, caregivers and children have fewer resources to cope and regulate responses (e.g. reduced response inhibition/executive functioning) <a href="https://pubmed.ncbi.nlm.nih.gov/12212647/" target="_blank" class="text-blue-600 hover:underline">(6)</a>, increasing the risk of more immediate coping responses to escape or re-gaining control (e.g. shouting, violence, neglect).</p>
       
       <p class="text-slate-600 text-sm leading-relaxed mb-0">Coping responses may vary as a function of the level of need to escape distress and harm, ranging from immediate escape (e.g. violence, substance misuse, abandonment/neglect) to stronger forms of avoidance (e.g. avoiding going out, which reduces social support systems in the longer-term) <a href="https://link.springer.com/article/10.1023/B:JOBA.0000007455.08539.94" target="_blank" class="text-blue-600 hover:underline">(7)</a>.</p>
      </div>
     </div>
    </div>

   </div>
  </section>

  <!-- SECTION 4: Risk Prediction & Challenges -->
  <section class="max-w-4xl mx-auto px-6 py-12">
   <h3 class="content-subheading mt-0 border-none">A multistage risk prediction model to determine relevance of candidate ACEs</h3>
   <p class="content-text">
    We assessed the relevance of identified candidate ACE indicators based on their consistent risk association with a reference standard of family violence in a multistage prediction model. The reference standard (outcome) was any occurrence of child maltreatment (CM) and maternal intimate partner violence (mIPV) up to 5-years post-birth.
   </p>
   <p class="content-text">
    Consistent with our theoretical model, we predicted that the final ACE indicators would reflect a continuum of clinical relevance, ranging from a high risk of family violence (i.e. high need for intervention) to lower relevance, consistent with previously studied ACEs domains.
   </p>

   <h3 class="content-subheading mt-10 border-none">Challenges in defining ACEs</h3>
   <p class="content-text">
    Since the late 1990s, the initial "ACE domains" have undergone numerous expansions across studies. Whilst this variation helped innovate and adapt indicators of ACEs to different goals, there is currently little consistency in the definition and inclusion of ACEs. The large variation of measured ACEs also means there is no agreed reference standard for developing new measures of ACEs. 
   </p>
   <p class="content-text">
    Previous studies have mainly assessed the validity and relevance of ACEs based on their risk association with poorer health outcomes in adulthood. However, most studies reporting on the negative health effects of ACEs are based on cross-sectional samples of adults asked to recall experiences from childhood <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext" target="_blank" class="text-blue-600 font-medium hover:underline">(1)</a>. Recent birth cohort studies, however, reveal that ACEs are relatively poor predictors of negative health outcomes in adulthood relative to other socioeconomic factors <a href="https://jamanetwork.com/journals/jamapediatrics/article-abstract/2775420" target="_blank" class="text-blue-600 font-medium hover:underline">(2)</a>. Global studies by the World Health Organization show that traumatic stress symptoms naturally resolve on average six years after a linked traumatic event (e.g., an ACE) <a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5632781/" target="_blank" class="text-blue-600 font-medium hover:underline">(3)</a>, <a href="https://jamanetwork.com/journals/jamapsychiatry/fullarticle/2595039" target="_blank" class="text-blue-600 font-medium hover:underline">(4)</a>. These gaps create multiple challenges when attempting to develop new indicators of ACEs for electronic health records (EHRs).
   </p>

   <h3 class="content-subheading mt-10 border-none">Establishing a consistent definition</h3>
   <p class="content-text">
    To enhance consistency in developing clinically relevant ACE indicators for different data sources, we conducted several studies <a href="https://linkinghub.elsevier.com/retrieve/pii/S2589750022000619" target="_blank" class="text-blue-600 font-medium hover:underline">(4)</a> to establish a definition of ACEs based on a set of criteria. We also developed a testable theoretical biopsychosocial model of ACEs. This model facilitates theoretically informed predictions of which ACE indicators might be more relevant than others.
   </p>
  </section>

  <!-- SECTION 5: Definitions and Inclusions (Checklist Style) -->
  <section class="bg-slate-50 py-12 md:py-16 border-y border-slate-200">
   <div class="max-w-4xl mx-auto px-6">
    <h2 class="content-heading mt-0 text-center mb-10">Definitions and inclusions</h2>
    
    <div class="bg-white rounded-2xl border border-blue-100 shadow-md overflow-hidden relative mb-10">
     <div class="h-2 w-full bg-blue-500 absolute top-0 left-0"></div>
     <div class="p-8 md:p-10">
      <p class="content-text font-semibold text-slate-800 mb-6">
       We defined ACE indicators as any experience within the family environment recorded in the child or the parent data source (e.g. health record) considered to be:
      </p>
      
      <ul class="custom-list">
       <li>
        <svg class="text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        Frightening, violent, traumatic or neglectful <a href="https://apps.who.int/iris/bitstream/handle/10665/42495/9241545615_eng.pdf" target="_blank" class="text-blue-600 hover:underline">(see WHO violence definition)</a>, with potential for immediate or longer-term harm to a child's biopsychosocial development (intentionally or unintentionally) <a href="https://assets.publishing.service.gov.uk/media/65cb4349a7ded0000c79e4e1/Working_together_to_safeguard_children_2023_-_statutory_guidance.pdf" target="_blank" class="text-blue-600 hover:underline">(see UK government definition)</a>;
       </li>
       <li>
        <svg class="text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        Caused by a single event or through repeated exposure;
       </li>
       <li>
        <svg class="text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        Caused by external factors and not the child themselves, such as self-harm; and
       </li>
       <li>
        <svg class="text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        Amenable to health or social care intervention at a family level (i.e. excluding wider factors such as socioeconomic status, community violence, school bullying etc; see <a href="https://jamanetwork.com/journals/jama/fullarticle/2783975" target="_blank" class="text-blue-600 hover:underline">1</a>, <a href="https://www.gov.uk/government/publications/supporting-families-programme-guidance-2022-to-2025/chapter-4-identifying-and-working-with-families" target="_blank" class="text-blue-600 hover:underline">2</a>, <a href="https://www.sciencedirect.com/science/article/abs/pii/S0749379719300315" target="_blank" class="text-blue-600 hover:underline">3</a>).
       </li>
      </ul>
     </div>
    </div>

    <p class="content-text">
     We made several adaptations to previously studied ACEs for feasible ascertainment in electronic health records (EHRs). We defined indicators as variables of grouped codes and measures. We aimed to develop ACE indicators that reflected clinically meaningful risk groups of adversity to identify families that may be eligible for targeted maternal-child care interventions in England (e.g. <a href="https://www.gov.uk/government/publications/supporting-families-programme-guidance-2021-to-2022" target="_blank" class="text-blue-600 font-medium hover:underline">Supporting Families programme</a>, or previously "targeted care pathway" of <a href="https://www.gov.uk/government/publications/healthy-child-programme-0-to-19-health-visitor-and-school-nurse-commissioning" target="_blank" class="text-blue-600 font-medium hover:underline">the Healthy Child Programme</a>. See also WHO for <a href="https://www.who.int/teams/social-determinants-of-health/violence-prevention/global-status-report-on-violence-against-children-2020" target="_blank" class="text-blue-600 font-medium hover:underline">intervention studies</a>).
    </p>

    <p class="content-text">
     We manually grouped indicators into broader ACE domains consistent with the <a href="https://www.ajpmonline.org/article/S0749-3797(98)00017-8/fulltext" target="_blank" class="text-blue-600 font-medium hover:underline">original study</a> by <a href="https://www.cdc.gov/violenceprevention/aces/index.html" target="_blank" class="text-blue-600 font-medium hover:underline">Kaiser Permanente and CDC</a>. Due to the lack of recordings, we collapsed all types of child abuse and neglect into child maltreatment (CM). We collapsed "imprisonment of household members" and "household challenges" into Adverse family environments. We created a separate indicator, "Social service involvement" (SSI), for social care-related codes that did not contain descriptions of CM or IPV. Due to few recordings and high intercorrelations, SSI was merged with CM in the final selection process.
    </p>

    <p class="content-text">
     Given the substantial under-recording of CM and IPV (e.g. see <a href="https://www.cambridge.org/core/journals/the-british-journal-of-psychiatry/article/barriers-and-facilitators-of-disclosures-of-domestic-violence-by-mental-health-service-users-qualitative-study/7A690CCBC0322D045442549A5FA3C4CF" target="_blank" class="text-blue-600 hover:underline">1</a>, <a href="https://bjgp.org/content/67/659/e437.long" target="_blank" class="text-blue-600 hover:underline">2</a>), we also added the domain “high-risk presentations of CM” (HRP-CM). HRP-CM encompassed indicators from the <a href="https://www.nice.org.uk/guidance/cg89/chapter/1-Guidance" target="_blank" class="text-blue-600 font-medium hover:underline">National Institute for Health and Care Excellence (NICE)</a> and <a href="https://www.rcgp.org.uk/clinical-and-research/resources/toolkits/child-safeguarding-toolkit.aspx" target="_blank" class="text-blue-600 font-medium hover:underline">Royal College of General Practitioners (RGCP)</a> that should raise clinical suspicion for CM.
    </p>

    <p class="content-text font-medium text-slate-800">
     ACEs can be recorded in both parents’ and children’s records. ACEs are considered based on each specific child’s time from birth. Children are, therefore, considered unexposed if no relevant recording occurs during the study period, regardless of previous exposure to children within the same family. This approach mirrors changes in stress levels as the family moves through different life stages.
    </p>
   </div>
  </section>

  <!-- SECTION 6: Next Steps / Navigation Grid -->
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
