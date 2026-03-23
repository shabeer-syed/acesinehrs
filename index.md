---
layout: none
permalink: /
title: "Adverse Childhood Experiences (ACEs) in Electronic Health Records (EHRs)"
---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Adverse Childhood Experiences (ACEs) in Electronic Health Records (EHRs)</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    body { font-family: 'Inter', sans-serif; }
  </style>
</head>
<body class="bg-gray-50 text-gray-800 antialiased flex flex-col min-h-screen">

  <!-- Top Navigation Bar -->
  <nav class="bg-white border-b border-gray-200 w-full z-50 relative shadow-sm">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 py-4 flex justify-between items-center">
      
      <!-- Site Brand/Logo -->
      <a href="/" class="flex-shrink-0 flex items-center mr-6">
        <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/logos/acesinehrs-logo.png" alt="ACEs in EHRs Logo" class="h-5 sm:h-6 object-contain hover:opacity-80 transition duration-300">
      </a>
      
      <!-- Main Links (Desktop) - Font size increased to text-base (16px) -->
      <div class="hidden lg:flex items-center justify-end flex-grow gap-5 xl:gap-8 mr-6 text-base font-medium text-gray-500">
        <a href="https://shabeer-syed.github.io/acesinehrs/about/" class="hover:text-gray-900 transition">About</a>
        <a href="https://shabeer-syed.github.io/acesinehrs/starterguide/" class="hover:text-gray-900 transition">Getting started</a>
        <a href="https://shabeer-syed.github.io/acesinehrs/research/" class="hover:text-gray-900 transition">Research</a>
        <a href="https://shabeer-syed.github.io/acesinehrs/codelistbrowse/" class="hover:text-gray-900 transition">Browse code list</a>
        <a href="https://shabeer-syed.github.io/acesinehrs/ACE-domains/" class="hover:text-gray-900 transition">ACE domains & indicators</a>
      </div>

      <!-- Right Side Icons (Search & Menu) -->
      <div class="flex items-center gap-5 text-gray-500">
        <button class="hover:text-gray-900 transition" aria-label="Search">
          <i class="fas fa-search text-lg"></i>
        </button>
        <button id="menu-toggle" class="hover:text-gray-900 transition focus:outline-none lg:hidden" aria-label="Menu">
          <i class="fas fa-bars text-2xl"></i>
        </button>
      </div>
    </div>

    <!-- Mobile/Dropdown Menu - Font size increased to text-base (16px) -->
    <div id="mobile-menu" class="hidden absolute top-full left-0 w-full bg-white border-b border-gray-200 shadow-md z-40">
      <div class="flex flex-col px-6 py-4 space-y-4 text-base font-medium text-gray-600">
        <a href="https://shabeer-syed.github.io/acesinehrs/about/" class="hover:text-gray-900 transition">About</a>
        <a href="https://shabeer-syed.github.io/acesinehrs/starterguide/" class="hover:text-gray-900 transition">Getting started</a>
        <a href="https://shabeer-syed.github.io/acesinehrs/research/" class="hover:text-gray-900 transition">Research</a>
        <a href="https://shabeer-syed.github.io/acesinehrs/codelistbrowse/" class="hover:text-gray-900 transition">Browse code list</a>
        <a href="https://shabeer-syed.github.io/acesinehrs/ACE-domains/" class="hover:text-gray-900 transition">ACE domains & indicators</a>
        <a href="https://shabeer-syed.github.io/acesinehrs/theory/" class="hover:text-gray-900 transition">Framework & definitions</a>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <header class="relative bg-slate-700 bg-opacity-50 text-white" 
      style="background-image: url('https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEsinEHRs%20home%20page%202024.jpg'); background-size: cover; background-position: center; background-blend-mode: multiply;">
     
    <!-- Banner Content -->
    <div class="relative z-10 max-w-5xl mx-auto px-6 py-24 md:py-32 text-center">
      <h1 class="text-4xl md:text-5xl font-bold tracking-tight mb-6 leading-tight drop-shadow-lg">
        Adverse Childhood Experiences (ACEs) <br> <span class="text-blue-200">in Electronic Health Records</span>
      </h1>
      <p class="text-lg md:text-xl text-slate-100 mb-8 max-w-3xl mx-auto leading-relaxed drop-shadow-md">
        A library of indicators for ACEs in EHRs. Search, discover, and access tools, code lists, and resources to implement clinically relevant and validated indicators of ACEs in your research using de-identified electronic health records.
      </p>
       
      <div class="flex flex-col sm:flex-row justify-center items-center gap-4">
        <a href="/indicators/#download-code-lists" class="inline-flex items-center justify-center px-8 py-4 text-lg font-semibold bg-white text-slate-800 rounded-full shadow-lg hover:bg-slate-100 hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
          Download code lists <i class="fas fa-file-download ml-2 text-blue-600"></i>
        </a>
      </div>

      <div class="mt-8">
        <a href="https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(24)00301-3/fulltext" target="_blank" class="inline-flex items-center px-5 py-2.5 bg-slate-900 bg-opacity-60 border border-blue-400 rounded-full text-sm font-medium hover:bg-opacity-80 transition duration-300 backdrop-blur-sm">
          <span class="flex h-2.5 w-2.5 relative mr-3">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-blue-300 opacity-75"></span>
            <span class="relative inline-flex rounded-full h-2.5 w-2.5 bg-blue-400"></span>
          </span>
          New study out in Lancet Public Health!
        </a>
      </div>
    </div>
  </header>

  <!-- Logos Section WITH LINKS -->
  <section class="bg-white border-b border-gray-200 py-8 shadow-sm relative z-10">
    <div class="max-w-7xl mx-auto px-6 flex flex-wrap justify-center items-center gap-8 opacity-70 grayscale hover:grayscale-0 transition duration-500">
      <a href="https://www.ucl.ac.uk/children-policy-research/" target="_blank" rel="noopener noreferrer">
        <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/NIHR%20CPRU%20logo%20aces%20in%20ehrs%20footer.png" alt="NIHR CPRU" class="h-10 object-contain hover:scale-105 transition-transform">
      </a>
      <a href="https://www.ucl.ac.uk/child-health/great-ormond-street-institute-child-health-0" target="_blank" rel="noopener noreferrer">
        <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/ucl%20ich%20logo%20aces%20in%20ehrs.png" alt="UCL ICH" class="h-10 object-contain hover:scale-105 transition-transform">
      </a>
      <a href="https://www.ox.ac.uk/" target="_blank" rel="noopener noreferrer">
        <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/university%20of%20oxford%20logo%20aces%20in%20ehrs.png" alt="Oxford" class="h-10 object-contain hover:scale-105 transition-transform">
      </a>
      <a href="https://www.gosh.nhs.uk/our-research/our-research-infrastructure/nihr-great-ormond-street-hospital-brc/" target="_blank" rel="noopener noreferrer">
        <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/NIHR%20Great%20ormond%20street%20hospital%20biomedical%20research%20centre%20logo%20aces%20in%20ehrs.png" alt="NIHR GOSH BRC" class="h-10 object-contain hover:scale-105 transition-transform">
      </a>
      <a href="https://www.gosh.nhs.uk/" target="_blank" rel="noopener noreferrer">
        <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/GOSH%20logo%20aces%20in%20ehrs.png" alt="GOSH" class="h-10 object-contain hover:scale-105 transition-transform">
      </a>
      <a href="https://www.bristol.ac.uk/" target="_blank" rel="noopener noreferrer">
        <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/University%20of%20bristol%20logo%20aces%20in%20ehrs.png" alt="Bristol" class="h-10 object-contain hover:scale-105 transition-transform">
      </a>
      <a href="https://www.hdruk.ac.uk/" target="_blank" rel="noopener noreferrer">
        <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/hdruk%20logo%20aces%20in%20ehrs.png" alt="HDRUK" class="h-10 object-contain hover:scale-105 transition-transform">
      </a>
      <a href="https://www.ucl.ac.uk/health-informatics/research/caliber" target="_blank" rel="noopener noreferrer">
        <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/logos/caliber%20ucl%20logo%20aces%20in%20ehrs.png" alt="Caliber UCL" class="h-10 object-contain hover:scale-105 transition-transform">
      </a>
    </div>
  </section>

  <main class="flex-grow">
    <!-- Intro Section -->
    <section class="max-w-4xl mx-auto px-6 py-16 text-center">
      <h2 class="text-3xl font-bold text-slate-800 mb-6">What is ACEs in EHRs?</h2>
      <p class="text-lg text-gray-700 leading-relaxed mb-6">
        <strong class="text-blue-900">The ACEsinEHRs platform provides validated domains, indicators, and code lists to identify adverse childhood experiences (ACEs) in routinely collected de-identified electronic health records of parents and children before and after birth.</strong>
      </p>
      <p class="text-gray-600 mb-6 leading-relaxed">
        Examples of recorded ACEs include child maltreatment (e.g., child protection), exposure to domestic violence and abuse, and growing up with parental mental health problems or substance use problems (e.g., trio of vulnerabilities). This website is continuously updated and provides information on definitions, concepts, measures, and standardised tools to help users apply the developed ACE indicators to create “research-ready” datasets.
      </p>
      <a href="https://shabeer-syed.github.io/acesinehrs/research/" class="text-blue-700 font-semibold hover:text-blue-900 underline underline-offset-4 transition">See publications here</a>
    </section>

    <!-- Grid Cards Section -->
    <section class="max-w-6xl mx-auto px-6 pb-16">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <a href="https://shabeer-syed.github.io/acesinehrs/about/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/Introduction%20aces%20small.png" alt="About" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="text-xl font-bold text-gray-800 group-hover:text-blue-600 transition">About ACEs in EHRs</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/ACE-domains/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/home%20view%20domain%20download%20small.png" alt="Domains" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="text-xl font-bold text-gray-800 group-hover:text-blue-600 transition">ACE Domains</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/codelistbrowse/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png" alt="Code Lists" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="text-xl font-bold text-gray-800 group-hover:text-blue-600 transition">Browse Code Lists</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/starterguide/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/master/images/ACEs%20implementation%20and%20downloads.png" alt="Getting Started" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="text-xl font-bold text-gray-800 group-hover:text-blue-600 transition">Starter Guide</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/theory/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/aces%20in%20ehrs%20definitions%20theories.png" alt="Theory" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="text-xl font-bold text-gray-800 group-hover:text-blue-600 transition">Theory & Definitions</h3>
          </div>
        </a>

        <a href="https://shabeer-syed.github.io/acesinehrs/research/" class="group bg-white rounded-2xl shadow-sm border border-gray-100 flex flex-col overflow-hidden hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
          <div class="h-48 overflow-hidden bg-gray-100">
            <img src="https://raw.githubusercontent.com/shabeer-syed/acesinehrs/refs/heads/master/images/ACEsinEHRs%20research%20outputs%20small.png" alt="Research" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
          </div>
          <div class="p-6 flex-grow">
            <h3 class="text-xl font-bold text-gray-800 group-hover:text-blue-600 transition">Research Outputs</h3>
          </div>
        </a>
      </div>
    </section>

    <!-- NEW MODERN NOTICES SECTION -->
    <section class="max-w-4xl mx-auto px-6 pb-20 space-y-6">
       
      <!-- Notice 1: Update -->
      <div class="relative bg-white rounded-2xl p-6 shadow-[0_2px_10px_-3px_rgba(6,81,237,0.1)] border border-slate-100 flex items-start gap-4 sm:gap-5 hover:shadow-md transition duration-300 overflow-hidden group">
        <div class="absolute left-0 top-0 bottom-0 w-1.5 bg-blue-500 rounded-l-2xl"></div>
        <div class="flex-shrink-0 w-10 h-10 flex items-center justify-center rounded-full bg-blue-50 text-blue-600 mt-0.5 group-hover:bg-blue-100 transition-colors">
          <i class="fas fa-info-circle text-lg"></i>
        </div>
        <div class="flex-1">
          <p class="text-[15px] sm:text-base text-slate-600 leading-relaxed">
            <strong class="text-slate-800 font-semibold">UPDATE July 2023:</strong> To derive ACEs using combined maternal and paternal data, please see the paper published in the Lancet Public Health: <br class="hidden sm:block">
            <a href="https://doi.org/10.1016/S2468-2667(23)00119-6" target="_blank" class="inline-block mt-1 text-blue-600 hover:text-blue-800 font-medium underline decoration-blue-200 underline-offset-4 hover:decoration-blue-400 transition-all">"Family adversity and health characteristics associated with intimate partner violence in children and parents presenting to health care: a population-based birth cohort study in England"</a>.
          </p>
        </div>
      </div>

      <!-- Notice 2: Core Study -->
      <div class="relative bg-white rounded-2xl p-6 shadow-[0_2px_10px_-3px_rgba(6,81,237,0.1)] border border-slate-100 flex items-start gap-4 sm:gap-5 hover:shadow-md transition duration-300 overflow-hidden group">
        <div class="absolute left-0 top-0 bottom-0 w-1.5 bg-blue-500 rounded-l-2xl"></div>
        <div class="flex-shrink-0 w-10 h-10 flex items-center justify-center rounded-full bg-blue-50 text-blue-600 mt-0.5 group-hover:bg-blue-100 transition-colors">
          <i class="fas fa-book-medical text-lg"></i>
        </div>
        <div class="flex-1">
          <p class="text-[15px] sm:text-base text-slate-600 leading-relaxed">
            <strong class="text-slate-800 font-semibold">Core Study:</strong> This library stores ACE indicators and algorithms accompanying the paper published in Lancet Digital Health: <br class="hidden sm:block">
            <a href="https://doi.org/10.1016/S2589-7500(22)00061-9" target="_blank" class="inline-block mt-1 text-blue-600 hover:text-blue-800 font-medium underline decoration-blue-200 underline-offset-4 hover:decoration-blue-400 transition-all">"Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study, (2022)."</a>
          </p>
        </div>
      </div>

      <!-- Notice 3: Red Citation Warning -->
      <div class="relative bg-white rounded-2xl p-6 shadow-[0_2px_10px_-3px_rgba(239,68,68,0.1)] border border-slate-100 flex items-start gap-4 sm:gap-5 hover:shadow-md transition duration-300 overflow-hidden group">
        <div class="absolute left-0 top-0 bottom-0 w-1.5 bg-red-500 rounded-l-2xl"></div>
        <div class="flex-shrink-0 w-10 h-10 flex items-center justify-center rounded-full bg-red-50 text-red-500 mt-0.5 group-hover:bg-red-100 transition-colors">
          <i class="fas fa-exclamation-triangle text-lg"></i>
        </div>
        <div class="flex-1">
          <p class="text-[15px] sm:text-base text-slate-700 leading-relaxed">
            <strong class="text-slate-900 font-semibold">Users must cite</strong> the www.ACEsinEHRs.com library and the accompanying 
            <a href="https://doi.org/10.1016/S2589-7500(22)00061-9" target="_blank" class="text-red-600 hover:text-red-800 font-medium underline decoration-red-200 underline-offset-4 hover:decoration-red-400 transition-all">Lancet Digital Health publication</a> 
            in all research outputs, presentations and reports.
          </p>
        </div>
      </div>

      <!-- Notice 4: Red Disclaimer -->
      <div class="relative bg-white rounded-2xl p-6 shadow-[0_2px_10px_-3px_rgba(239,68,68,0.1)] border border-slate-100 flex items-center gap-4 sm:gap-5 hover:shadow-md transition duration-300 overflow-hidden group">
        <div class="absolute left-0 top-0 bottom-0 w-1.5 bg-red-500 rounded-l-2xl"></div>
        <div class="flex-shrink-0 w-10 h-10 flex items-center justify-center rounded-full bg-red-50 text-red-500 group-hover:bg-red-100 transition-colors">
          <i class="fas fa-shield-alt text-lg"></i>
        </div>
        <div class="flex-1">
          <p class="text-[15px] sm:text-base text-slate-600">
            <strong class="text-slate-800 font-semibold">No EHR or patient data is stored in this library.</strong> The information is not intended for clinical use.
          </p>
        </div>
      </div>
       
    </section>
  </main>

  <!-- Footer -->
  <footer class="bg-slate-900 text-slate-400 py-10 text-center mt-auto">
    <div class="max-w-4xl mx-auto px-6">
      <!-- Hidden text for indexing -->
      <p class="mb-1 text-slate-900 font-medium text-lg select-none">Dr Shabeer Syed</p>
      <p class="text-sm text-slate-900 select-none">Clinical Psychologist & Senior Research Associate</p>
      
      <div class="w-16 h-px bg-slate-900 mx-auto my-6"></div>
      
      <!-- Visible Copyright -->
      <p class="text-xs opacity-60 text-slate-400">&copy; 2024 ACEs in EHRs. All rights reserved.</p>
    </div>
  </footer>

  <!-- Mobile Menu Script -->
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const menuToggle = document.getElementById('menu-toggle');
      const mobileMenu = document.getElementById('mobile-menu');

      menuToggle.addEventListener('click', () => {
        mobileMenu.classList.toggle('hidden');
      });
    });
  </script>

</body>
</html>
