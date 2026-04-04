---
layout: splash
permalink: /CYP-MHPs/
title: "CYP mental health problems"
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
    background-color: #f8fafc !important; /* Soft slate background for the whole page */
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
  .tailwind-wrap a:not(.btn-secondary):not(.btn-primary):not(.text-blue-600) {
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

  /* FLOURISH CONTAINER OVERRIDES */
  .flourish-container-wrap {
    background: #ffffff !important;
    border-radius: 1rem !important;
    border: 1px solid #e2e8f0 !important;
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.05), 0 4px 6px -2px rgba(0, 0, 0, 0.025) !important;
    padding: 1.5rem !important;
    overflow: hidden !important;
  }

  html { scroll-behavior: smooth; }
</style>

<!-- 4. The HTML Content -->
<div class="full-bleed tailwind-wrap text-gray-800 antialiased flex flex-col min-h-screen">

  <!-- Hero Section -->
  <header class="relative bg-slate-800 bg-opacity-70 text-white" style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20home%20page%202023.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
    <div class="relative z-10 max-w-7xl mx-auto px-6 py-20 md:py-24 text-center md:text-left">
      <h1 class="hero-title drop-shadow-lg">
        CYP <span style="color: #bfdbfe !important;">Mental Health Problems</span>
      </h1>
      <p class="hero-subtitle drop-shadow-md mx-auto md:mx-0">
        Search, filter, and access clinical code lists for Child and Young Person mental health conditions seamlessly cross-mapped across multiple healthcare coding systems.
      </p>
    </div>
  </header>

  <!-- Main Content Areas -->
  <main class="flex-grow py-12 md:py-16">
    <div class="max-w-7xl mx-auto px-6">
      
      <!-- Action Bar: Legend & Download Button -->
      <div class="bg-white rounded-xl border border-slate-200 shadow-sm p-5 md:p-6 mb-8 flex flex-col lg:flex-row lg:items-center justify-between gap-6">
        
        <!-- Rebuilt HTML Legend -->
        <div class="flex-1">
          <h3 class="text-sm font-bold text-slate-400 uppercase tracking-wider mb-3 m-0 border-none">Domain Abbreviation</h3>
          <div class="flex flex-wrap gap-2.5">
            <!-- CYP-MHPs -->
            <div class="inline-flex items-center px-3 py-1.5 rounded-md bg-indigo-50 border border-indigo-100 text-indigo-800 text-sm font-medium">
              <span class="bg-indigo-500 text-white px-2 py-0.5 rounded text-xs font-bold mr-2">CYP-MHPs</span> Child & Young Person Mental Health Problems
            </div>
          </div>
        </div>

        <!-- Download Button (Forced White Text) -->
        <div class="flex-shrink-0">
          <a href="https://acesinehrs.com/starterguide/#downloads" style="color: #ffffff !important;" class="inline-flex items-center px-6 py-3 bg-blue-600 hover:bg-blue-700 text-[15px] font-semibold rounded-lg shadow-md hover:shadow-lg hover:-translate-y-0.5 transition-all duration-300">
            <i class="fas fa-file-download mr-2" style="color: #ffffff !important;"></i> Download code lists
          </a>
        </div>
      </div>

      <!-- Flourish Embed Container -->
      <div class="flourish-container-wrap">
        <div class="flourish-embed flourish-chart" data-src="visualisation/28374670">
            <script src="https://public.flourish.studio/resources/embed.js"></script>
            <noscript><img src="https://public.flourish.studio/visualisation/28374670/thumbnail" width="100%" alt="visualization" /></noscript>
        </div>
      </div>

    </div>
  </main>

  <!-- Navigation / Footer area -->
  <section class="bg-white border-t border-slate-200 py-12">
    <div class="max-w-7xl mx-auto px-6 text-center">
      <a href="https://acesinehrs.com/" class="inline-flex items-center text-slate-500 hover:text-blue-600 font-medium transition-colors text-[16px] !important bg-slate-50 hover:bg-blue-50 px-5 py-2.5 rounded-lg border border-slate-200">
        <i class="fas fa-arrow-left mr-2"></i> Go back to homepage
      </a>
    </div>
  </section>

</div>
