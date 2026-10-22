<!DOCTYPE html>
<html lang="en">
<head>
  <!-- 1. UTF-8 Character Encoding -->
  <meta charset="UTF-8">
  <!-- 2. Responsive Mobile Viewport -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- 3. Meaningful Title -->
  <title>Assignment 4.5 - Multi-Page College Club Website Hub</title>
  <!-- 4. Meta Description -->
  <meta name="description" content="Assignment 4.5 multi-page college club website for Innovators & Developers Club featuring Home, About Us, Registration, and Contact pages with interactive navigation testing workbench.">
  <!-- 5. Favicon Link (SVG Data URI) -->
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='25' fill='%232563eb'/><path d='M30 35h40M30 50h40M30 65h25' stroke='%23ffffff' stroke-width='8' stroke-linecap='round'/><circle cx='70' cy='65' r='8' fill='%2338bdf8'/></svg>">
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts: Inter & JetBrains Mono -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
  
  <style>
    body {
      font-family: 'Inter', sans-serif;
    }
    code, pre {
      font-family: 'JetBrains Mono', monospace;
    }
    /* Custom scrollbars */
    ::-webkit-scrollbar {
      width: 8px;
      height: 8px;
    }
    ::-webkit-scrollbar-track {
      background: #0f172a;
    }
    ::-webkit-scrollbar-thumb {
      background: #334155;
      border-radius: 4px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #475569;
    }
  </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col selection:bg-blue-500 selection:text-white">

  <!-- Toast Notification Container -->
  <div id="toast" class="fixed top-5 right-5 z-50 transform translate-y-[-100px] opacity-0 transition-all duration-300 ease-in-out pointer-events-none">
    <div class="bg-emerald-500 text-slate-950 font-semibold px-4 py-3 rounded-xl shadow-2xl flex items-center space-x-2 border border-emerald-400">
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 13l4 4L19 7"></path>
      </svg>
      <span id="toastMessage">Copied to clipboard!</span>
    </div>
  </div>

  <!-- Main Header Bar -->
  <header class="border-b border-slate-800 bg-slate-900/90 backdrop-blur-md sticky top-0 z-40">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4">
        <div class="flex items-center space-x-3">
          <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-blue-600 via-indigo-500 to-sky-400 flex items-center justify-center shadow-lg shadow-blue-500/20 ring-1 ring-white/20">
            <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"></path>
            </svg>
          </div>
          <div>
            <div class="flex items-center space-x-2">
              <span class="bg-blue-500/10 text-blue-400 text-xs font-bold px-2.5 py-0.5 rounded-full border border-blue-500/20">Assignment 4.5</span>
              <span class="text-xs text-slate-400 hidden sm:inline">• Multi-Page College Club Site</span>
            </div>
            <h1 class="text-xl sm:text-2xl font-extrabold text-white tracking-tight">Tech Innovators & Developers Club</h1>
          </div>
        </div>

        <!-- Quick Status Badges -->
        <div class="flex items-center space-x-2 text-xs">
          <div class="bg-slate-800/80 border border-slate-700/60 px-3 py-1.5 rounded-lg flex items-center space-x-2">
            <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span>
            <span class="text-slate-300 font-medium">4 HTML Pages Linked</span>
          </div>
          <div class="bg-slate-800/80 border border-slate-700/60 px-3 py-1.5 rounded-lg text-slate-300 font-medium hidden md:flex items-center space-x-1">
            <span>Metadata & Favicons Validated</span>
          </div>
        </div>
      </div>
    </div>
  </header>

  <!-- Main Content Layout -->
  <main class="flex-1 max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-8 space-y-8">

    <!-- Page Switcher Tabs -->
    <div class="bg-slate-900 border border-slate-800 rounded-2xl p-2 shadow-xl">
      <div class="flex flex-col md:flex-row items-stretch md:items-center justify-between gap-3">
        <div class="grid grid-cols-2 sm:grid-cols-4 gap-2 flex-1" role="tablist">
          
          <button 
            id="tab-page1" 
            onclick="switchPage('page1')"
            class="tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all bg-blue-600 text-white shadow-lg shadow-blue-600/25"
          >
            <div class="flex items-center space-x-2.5 truncate">
              <span class="p-1 rounded-lg bg-white/10 text-white">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
              </span>
              <span class="truncate">Home</span>
            </div>
            <span class="text-[10px] uppercase tracking-wider font-mono px-1.5 py-0.5 rounded bg-white/20 text-white hidden lg:inline">index.html</span>
          </button>

          <button 
            id="tab-page2" 
            onclick="switchPage('page2')"
            class="tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/60"
          >
            <div class="flex items-center space-x-2.5 truncate">
              <span class="p-1 rounded-lg bg-slate-800 text-slate-400 border border-slate-700">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
              </span>
              <span class="truncate">About Club</span>
            </div>
            <span class="text-[10px] uppercase tracking-wider font-mono px-1.5 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700 hidden lg:inline">about.html</span>
          </button>

          <button 
            id="tab-page3" 
            onclick="switchPage('page3')"
            class="tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/60"
          >
            <div class="flex items-center space-x-2.5 truncate">
              <span class="p-1 rounded-lg bg-slate-800 text-slate-400 border border-slate-700">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18 9v3m0 0v3m0-3h3m-3 0h-3m-2-5a4 4 0 11-8 0 4 4 0 018 0zM3 20a6 6 0 0112 0v1H3v-1z"></path></svg>
              </span>
              <span class="truncate">Registration</span>
            </div>
            <span class="text-[10px] uppercase tracking-wider font-mono px-1.5 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700 hidden lg:inline">registration.html</span>
          </button>

          <button 
            id="tab-page4" 
            onclick="switchPage('page4')"
            class="tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/60"
          >
            <div class="flex items-center space-x-2.5 truncate">
              <span class="p-1 rounded-lg bg-slate-800 text-slate-400 border border-slate-700">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
              </span>
              <span class="truncate">Contact Us</span>
            </div>
            <span class="text-[10px] uppercase tracking-wider font-mono px-1.5 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700 hidden lg:inline">contact.html</span>
          </button>

        </div>

        <!-- Mode Toggle Switcher -->
        <div class="flex items-center bg-slate-950 p-1.5 rounded-xl border border-slate-800 self-center md:self-auto">
          <button 
            id="view-preview-btn" 
            onclick="switchViewMode('preview')"
            class="px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 bg-blue-600 text-white transition-all shadow-sm"
          >
            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path></svg>
            <span>Live Interactive Preview</span>
          </button>
          <button 
            id="view-code-btn" 
            onclick="switchViewMode('code')"
            class="px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 text-slate-400 hover:text-slate-200 transition-all"
          >
            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path></svg>
            <span>HTML Source</span>
          </button>
        </div>
      </div>
    </div>

    <!-- Active Metadata Spotlight Bar -->
    <div class="bg-gradient-to-r from-blue-900/30 via-slate-900 to-indigo-900/30 border border-blue-500/20 rounded-2xl p-5 relative overflow-hidden">
      <div class="absolute -right-10 -bottom-10 w-40 h-40 bg-blue-500/10 rounded-full blur-3xl pointer-events-none"></div>
      
      <div class="flex flex-col lg:flex-row lg:items-center justify-between gap-4">
        <div class="space-y-1">
          <div class="flex items-center space-x-2">
            <span class="text-xs font-bold uppercase tracking-wider text-blue-400">Page Metadata & Route Focus</span>
            <span class="text-slate-600">•</span>
            <span id="spotlight-filename" class="text-xs font-mono text-emerald-400 font-semibold">index.html</span>
          </div>
          <h2 id="spotlight-title" class="text-lg font-bold text-white">Innovators & Developers Club — Home Page</h2>
        </div>

        <!-- Quick Copy Head Tag Button -->
        <button 
          onclick="copyActiveMetadataHead()" 
          class="inline-flex items-center justify-center space-x-2 bg-slate-800 hover:bg-slate-700 active:bg-slate-900 text-slate-200 text-xs font-semibold px-4 py-2.5 rounded-xl border border-slate-700/80 transition shadow-sm self-start lg:self-auto cursor-pointer"
        >
          <svg class="w-4 h-4 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
          </svg>
          <span>Copy &lt;head&gt; Metadata Block</span>
        </button>
      </div>

      <!-- Metadata Attributes Grid -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-3 mt-4 pt-4 border-t border-slate-800/80">
        <div class="bg-slate-950/60 p-3 rounded-xl border border-slate-800/60">
          <div class="text-[10px] uppercase tracking-wider text-slate-500 font-bold mb-1">Encoding</div>
          <div class="text-xs font-mono text-slate-200 truncate" id="meta-encoding">&lt;meta charset="UTF-8"&gt;</div>
        </div>

        <div class="bg-slate-950/60 p-3 rounded-xl border border-slate-800/60">
          <div class="text-[10px] uppercase tracking-wider text-slate-500 font-bold mb-1">Viewport Setup</div>
          <div class="text-xs font-mono text-slate-200 truncate" id="meta-viewport">width=device-width, initial-scale=1.0</div>
        </div>

        <div class="bg-slate-950/60 p-3 rounded-xl border border-slate-800/60">
          <div class="text-[10px] uppercase tracking-wider text-slate-500 font-bold mb-1">Page Title</div>
          <div class="text-xs font-mono text-emerald-300 truncate" id="meta-title">Innovators Club — Home Page</div>
        </div>

        <div class="bg-slate-950/60 p-3 rounded-xl border border-slate-800/60">
          <div class="text-[10px] uppercase tracking-wider text-slate-500 font-bold mb-1">Favicon Asset</div>
          <div class="text-xs font-mono text-blue-300 flex items-center space-x-1.5 truncate">
            <span id="meta-favicon-icon" class="w-3.5 h-3.5 flex-shrink-0"></span>
            <span class="truncate">SVG Embedded Data URI</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Main Workspace Container (Preview vs Code Toggle) -->
    <div class="bg-slate-900 border border-slate-800 rounded-2xl shadow-2xl overflow-hidden">
      
      <!-- Interactive Simulated Browser Frame (Preview Mode) -->
      <div id="preview-container" class="block">
        
        <!-- Browser Top Header Bar with Simulated Tab & URL Bar -->
        <div class="bg-slate-900 border-b border-slate-800 p-3 flex flex-col sm:flex-row items-stretch sm:items-center justify-between gap-3">
          
          <!-- Browser Tab Bar Simulation -->
          <div class="flex items-center space-x-2">
            <!-- Mac window controls -->
            <div class="flex items-center space-x-1.5 mr-3">
              <span class="w-3 h-3 rounded-full bg-rose-500/80 inline-block"></span>
              <span class="w-3 h-3 rounded-full bg-amber-500/80 inline-block"></span>
              <span class="w-3 h-3 rounded-full bg-emerald-500/80 inline-block"></span>
            </div>

            <!-- Active Simulated Tab -->
            <div class="bg-slate-950 text-slate-200 text-xs font-semibold px-3 py-2 rounded-t-xl border-t border-x border-slate-800 flex items-center space-x-2 max-w-[240px] sm:max-w-xs truncate shadow-inner">
              <div id="browser-tab-icon" class="w-4 h-4 flex-shrink-0">
                <!-- SVG Icon inserted dynamically -->
              </div>
              <span id="browser-tab-title" class="truncate text-slate-200">Home Page</span>
            </div>
          </div>

          <!-- Browser URL Bar Simulation -->
          <div class="flex-1 max-w-xl bg-slate-950 border border-slate-800 rounded-lg px-3 py-1.5 flex items-center space-x-2 text-xs font-mono text-slate-400 shadow-inner">
            <svg class="w-3.5 h-3.5 text-emerald-400 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path>
            </svg>
            <span class="text-slate-500">https://college-club.edu/</span>
            <span id="browser-url-path" class="text-blue-400">index.html</span>
          </div>

          <!-- Viewport Label -->
          <div class="flex items-center space-x-2 text-slate-500 text-xs">
            <span class="bg-slate-950 border border-slate-800 px-2.5 py-1 rounded-md text-[11px] font-mono text-emerald-400 font-medium">Internal Links Working</span>
          </div>
        </div>

        <!-- Rendered Iframe Content -->
        <div class="relative w-full bg-slate-950 min-h-[650px] h-[700px]">
          <iframe 
            id="page-iframe" 
            class="w-full h-full border-none"
            title="Page Live Preview"
          ></iframe>
        </div>
      </div>

      <!-- Syntax Highlighted Code Viewer Container (Code Mode) -->
      <div id="code-container" class="hidden">
        
        <!-- Code Toolbar -->
        <div class="bg-slate-950 border-b border-slate-800 px-4 py-3 flex items-center justify-between">
          <div class="flex items-center space-x-3">
            <span class="w-3 h-3 rounded-full bg-blue-500 inline-block"></span>
            <span id="code-filename-label" class="text-xs font-mono text-slate-300 font-semibold">index.html</span>
            <span class="text-xs text-slate-600">•</span>
            <span class="text-xs text-slate-500 font-mono">Complete HTML Source with Nav & Metadata</span>
          </div>

          <div class="flex items-center space-x-3">
            <button 
              onclick="copyFullSourceCode()" 
              class="bg-blue-600 hover:bg-blue-500 active:scale-95 text-white text-xs font-semibold px-3 py-1.5 rounded-lg transition shadow flex items-center space-x-1.5"
            >
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 002 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
              </svg>
              <span>Copy Page HTML Source</span>
            </button>
          </div>
        </div>

        <!-- Code Content Block -->
        <div class="p-4 bg-slate-950 overflow-x-auto max-h-[700px]">
          <pre><code id="source-code-block" class="text-xs text-slate-300 font-mono leading-relaxed">Loading page source...</code></pre>
        </div>
      </div>

    </div>

    <!-- Assignment Requirements Checklist & Documentation -->
    <div class="bg-slate-900 border border-slate-800 rounded-2xl p-6 sm:p-8 space-y-6 shadow-xl">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 border-b border-slate-800 pb-5">
        <div>
          <div class="inline-flex items-center space-x-2 text-emerald-400 text-xs font-bold uppercase tracking-wider mb-1">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span>Assignment 4.5 Completion Checklist</span>
          </div>
          <h2 class="text-xl sm:text-2xl font-bold text-white">Multi-Page Architecture & Requirements Summary</h2>
        </div>
        <div class="text-xs text-slate-400 bg-slate-950 px-3 py-2 rounded-xl border border-slate-800 font-mono">
          4 Independent HTML Pages Integrated
        </div>
      </div>

      <!-- Grid of Assignment Requirements -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
        
        <!-- Req 1: Index Page -->
        <div class="bg-slate-950 p-4 rounded-xl border border-slate-800 space-y-2">
          <div class="flex items-center justify-between">
            <span class="text-xs font-mono font-bold text-blue-400">1. `index.html`</span>
            <span class="text-[10px] text-emerald-400 bg-emerald-500/10 px-2 py-0.5 rounded border border-emerald-500/20 font-semibold">Home</span>
          </div>
          <p class="text-xs text-slate-400 leading-relaxed">
            Club introduction hero section, core club activities, feature highlights, and interactive annual events schedule table.
          </p>
        </div>

        <!-- Req 2: About Page -->
        <div class="bg-slate-950 p-4 rounded-xl border border-slate-800 space-y-2">
          <div class="flex items-center justify-between">
            <span class="text-xs font-mono font-bold text-blue-400">2. `about.html`</span>
            <span class="text-[10px] text-emerald-400 bg-emerald-500/10 px-2 py-0.5 rounded border border-emerald-500/20 font-semibold">About</span>
          </div>
          <p class="text-xs text-slate-400 leading-relaxed">
            Mission statement, vision, detailed club history, and a modern member directory featuring leadership profiles and roles.
          </p>
        </div>

        <!-- Req 3: Registration Page -->
        <div class="bg-slate-950 p-4 rounded-xl border border-slate-800 space-y-2">
          <div class="flex items-center justify-between">
            <span class="text-xs font-mono font-bold text-blue-400">3. `registration.html`</span>
            <span class="text-[10px] text-emerald-400 bg-emerald-500/10 px-2 py-0.5 rounded border border-emerald-500/20 font-semibold">Form</span>
          </div>
          <p class="text-xs text-slate-400 leading-relaxed">
            Complete student membership registration form with field validation, department selection, and interest checkboxes.
          </p>
        </div>

        <!-- Req 4: Contact Page -->
        <div class="bg-slate-950 p-4 rounded-xl border border-slate-800 space-y-2">
          <div class="flex items-center justify-between">
            <span class="text-xs font-mono font-bold text-blue-400">4. `contact.html`</span>
            <span class="text-[10px] text-emerald-400 bg-emerald-500/10 px-2 py-0.5 rounded border border-emerald-500/20 font-semibold">Contact</span>
          </div>
          <p class="text-xs text-slate-400 leading-relaxed">
            Contact emails, physical campus location details, interactive inquiry submission form, and office hours summary.
          </p>
        </div>

      </div>
    </div>

  </main>

  <!-- Footer -->
  <footer class="border-t border-slate-800 bg-slate-900/60 py-6 text-center text-xs text-slate-500">
    <div class="max-w-7xl mx-auto px-4 flex flex-col sm:flex-row items-center justify-between gap-3">
      <div>
        <span>Assignment 4.5 — Multi-Page College Club Website</span>
      </div>
      <div class="flex items-center space-x-4 text-slate-400">
        <span>Consistent Header Navigation & Global Metadata Implemented</span>
      </div>
    </div>
  </footer>

  <!-- Page Database & Dynamic Navigation Logic -->
  <script>
    // Embedded SVG Favicon Data Strings
    const SVG_FAVICON_CLUB = `<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='25' fill='%232563eb'/><path d='M30 35h40M30 50h40M30 65h25' stroke='%23ffffff' stroke-width='8' stroke-linecap='round'/><circle cx='70' cy='65' r='8' fill='%2338bdf8'/></svg>`;

    // Helper Generator for Consistent Header Navigation Bar in all files
    function generateSharedHeader(activePage) {
      return `<header class="bg-slate-900 border-b border-slate-800 sticky top-0 z-30 shadow-md">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 py-3.5 flex items-center justify-between">
      <!-- Club Logo & Title Link -->
      <a href="index.html" onclick="parent.switchPage('page1'); return false;" class="flex items-center space-x-3 group">
        <div class="w-9 h-9 rounded-lg bg-blue-600 flex items-center justify-center text-white font-bold text-lg shadow-md group-hover:bg-blue-500 transition">
          ⚡
        </div>
        <div>
          <span class="font-extrabold text-white text-base tracking-tight block">Innovators Club</span>
          <span class="text-[10px] text-blue-400 font-mono tracking-widest uppercase">Tech & Engineering</span>
        </div>
      </a>

      <!-- Consistent Navigation Bar -->
      <nav class="flex items-center space-x-1 sm:space-x-2">
        <a href="index.html" onclick="parent.switchPage('page1'); return false;" class="px-3 py-2 rounded-lg text-xs sm:text-sm font-semibold transition ${activePage === 'index.html' ? 'bg-blue-600 text-white shadow' : 'text-slate-300 hover:text-white hover:bg-slate-800'}">Home</a>
        <a href="about.html" onclick="parent.switchPage('page2'); return false;" class="px-3 py-2 rounded-lg text-xs sm:text-sm font-semibold transition ${activePage === 'about.html' ? 'bg-blue-600 text-white shadow' : 'text-slate-300 hover:text-white hover:bg-slate-800'}">About</a>
        <a href="registration.html" onclick="parent.switchPage('page3'); return false;" class="px-3 py-2 rounded-lg text-xs sm:text-sm font-semibold transition ${activePage === 'registration.html' ? 'bg-blue-600 text-white shadow' : 'text-slate-300 hover:text-white hover:bg-slate-800'}">Registration</a>
        <a href="contact.html" onclick="parent.switchPage('page4'); return false;" class="px-3 py-2 rounded-lg text-xs sm:text-sm font-semibold transition ${activePage === 'contact.html' ? 'bg-blue-600 text-white shadow' : 'text-slate-300 hover:text-white hover:bg-slate-800'}">Contact</a>
      </nav>
    </div>
  </header>`;
    }

    // Helper Generator for Shared Footer
    function generateSharedFooter() {
      return `<footer class="bg-slate-900 border-t border-slate-800 py-8 text-xs text-slate-400">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 flex flex-col sm:flex-row items-center justify-between gap-4">
      <div class="flex items-center space-x-2">
        <span class="font-bold text-white">Innovators & Developers Club</span>
        <span>© 2026 Campus Student Organization</span>
      </div>
      <div class="flex items-center space-x-4 font-mono text-[11px]">
        <a href="index.html" onclick="parent.switchPage('page1'); return false;" class="hover:text-blue-400 transition">index.html</a>
        <a href="about.html" onclick="parent.switchPage('page2'); return false;" class="hover:text-blue-400 transition">about.html</a>
        <a href="registration.html" onclick="parent.switchPage('page3'); return false;" class="hover:text-blue-400 transition">registration.html</a>
        <a href="contact.html" onclick="parent.switchPage('page4'); return false;" class="hover:text-blue-400 transition">contact.html</a>
      </div>
    </div>
  </footer>`;
    }

    // Full 4 Page HTML Source Database
    const pagesData = {
      page1: {
        filename: "index.html",
        title: "Innovators Club — Home Page",
        description: "Official homepage of the Innovators & Developers Club featuring club activities and annual events schedule.",
        encoding: 'UTF-8',
        viewport: 'width=device-width, initial-scale=1.0',
        faviconSvg: SVG_FAVICON_CLUB,
        get code() {
          return `<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Metadata & Setup -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Innovators Club — Home Page</title>
  <meta name="description" content="Official homepage of the Innovators & Developers Club featuring club activities and annual events schedule.">
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='25' fill='%232563eb'/><path d='M30 35h40M30 50h40M30 65h25' stroke='%23ffffff' stroke-width='8' stroke-linecap='round'/><circle cx='70' cy='65' r='8' fill='%2338bdf8'/></svg>">
  
  <script src="https://cdn.tailwindcss.com"><\/script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style> body { font-family: 'Inter', sans-serif; } </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col justify-between">

  <!-- Header Navigation -->
  ${generateSharedHeader('index.html')}

  <!-- Main Content -->
  <main class="max-w-6xl mx-auto px-4 sm:px-6 py-10 space-y-12 flex-1 w-full">
    
    <!-- Hero Banner -->
    <section class="relative bg-gradient-to-r from-blue-900/40 via-slate-900 to-indigo-900/40 border border-blue-500/30 rounded-3xl p-8 sm:p-12 overflow-hidden shadow-2xl">
      <div class="max-w-2xl space-y-4">
        <span class="inline-block bg-blue-500/10 text-blue-400 text-xs font-bold px-3 py-1 rounded-full border border-blue-500/20 uppercase tracking-wider">Welcome to College Club Portal</span>
        <h1 class="text-3xl sm:text-5xl font-extrabold text-white tracking-tight leading-tight">Shape the Future of Technology & Engineering</h1>
        <p class="text-slate-300 text-sm sm:text-base leading-relaxed">
          The Tech Innovators & Developers Club provides students with hands-on coding experience, hackathons, open-source contribution mentorship, and industry workshops.
        </p>
        <div class="flex flex-wrap gap-3 pt-2">
          <a href="registration.html" onclick="parent.switchPage('page3'); return false;" class="bg-blue-600 hover:bg-blue-500 text-white font-semibold text-sm px-6 py-3 rounded-xl shadow-lg shadow-blue-600/30 transition">
            Join the Club Today
          </a>
          <a href="about.html" onclick="parent.switchPage('page2'); return false;" class="bg-slate-800 hover:bg-slate-700 text-slate-200 font-semibold text-sm px-6 py-3 rounded-xl border border-slate-700 transition">
            Explore Member Directory
          </a>
        </div>
      </div>
    </section>

    <!-- Core Club Activities Grid -->
    <section class="space-y-6">
      <div>
        <h2 class="text-2xl font-bold text-white tracking-tight">Our Core Activities</h2>
        <p class="text-xs sm:text-sm text-slate-400">Discover what we do every week across campus</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="bg-slate-900 border border-slate-800 p-6 rounded-2xl space-y-3 hover:border-blue-500/40 transition">
          <div class="w-10 h-10 rounded-xl bg-blue-500/10 text-blue-400 flex items-center justify-center font-bold text-xl">
            💻
          </div>
          <h3 class="font-bold text-white text-base">Weekly Code Sprints</h3>
          <p class="text-xs text-slate-400 leading-relaxed">
            Collaborative coding sessions focusing on web development, mobile apps, and algorithm practice every Tuesday afternoon.
          </p>
        </div>

        <div class="bg-slate-900 border border-slate-800 p-6 rounded-2xl space-y-3 hover:border-blue-500/40 transition">
          <div class="w-10 h-10 rounded-xl bg-purple-500/10 text-purple-400 flex items-center justify-center font-bold text-xl">
            🚀
          </div>
          <h3 class="font-bold text-white text-base">Annual Hackathon</h3>
          <p class="text-xs text-slate-400 leading-relaxed">
            24-hour inter-college innovation challenge with cash prizes, mentor guidance, and sponsor recruitment booths.
          </p>
        </div>

        <div class="bg-slate-900 border border-slate-800 p-6 rounded-2xl space-y-3 hover:border-blue-500/40 transition">
          <div class="w-10 h-10 rounded-xl bg-emerald-500/10 text-emerald-400 flex items-center justify-center font-bold text-xl">
            🎓
          </div>
          <h3 class="font-bold text-white text-base">Tech Workshops</h3>
          <p class="text-xs text-slate-400 leading-relaxed">
            Guest lectures from tech industry professionals covering AI tools, cloud computing, and career readiness.
          </p>
        </div>
      </div>
    </section>

    <!-- Requirement 6: Events Schedule Information Table -->
    <section class="bg-slate-900 border border-slate-800 rounded-2xl overflow-hidden shadow-xl space-y-4 p-6 sm:p-8">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-2 border-b border-slate-800 pb-4">
        <div>
          <span class="text-xs text-blue-400 font-bold uppercase tracking-wider">Requirement #6 — Data Table</span>
          <h2 class="text-xl font-bold text-white">Upcoming Club Events Schedule</h2>
        </div>
        <span class="text-xs bg-slate-800 text-slate-300 font-mono px-3 py-1 rounded-lg self-start sm:self-auto">Semester I - 2026</span>
      </div>

      <div class="overflow-x-auto">
        <table class="w-full text-left border-collapse">
          <thead class="bg-slate-950 text-slate-300 uppercase text-xs font-semibold tracking-wider border-b border-slate-800">
            <tr>
              <th scope="col" class="py-3.5 px-4">Date</th>
              <th scope="col" class="py-3.5 px-4">Event Name</th>
              <th scope="col" class="py-3.5 px-4">Category</th>
              <th scope="col" class="py-3.5 px-4">Location</th>
              <th scope="col" class="py-3.5 px-4 text-center">Status</th>
            </tr>
          </thead>
          <tbody class="divide-y divide-slate-800 text-xs sm:text-sm text-slate-300">
            <tr class="hover:bg-slate-800/50 transition">
              <td class="py-3.5 px-4 font-mono text-blue-400 font-semibold">Nov 12, 2026</td>
              <td class="py-3.5 px-4 font-bold text-white">Git & Open Source Bootcamp</td>
              <td class="py-3.5 px-4">Workshop</td>
              <td class="py-3.5 px-4 text-slate-400">Lab 3, CS Block</td>
              <td class="py-3.5 px-4 text-center"><span class="bg-emerald-500/10 text-emerald-400 text-[11px] font-bold px-2.5 py-0.5 rounded-full border border-emerald-500/20">Open</span></td>
            </tr>
            <tr class="hover:bg-slate-800/50 transition">
              <td class="py-3.5 px-4 font-mono text-blue-400 font-semibold">Nov 28, 2026</td>
              <td class="py-3.5 px-4 font-bold text-white">Winter Hackathon 2026</td>
              <td class="py-3.5 px-4">Competition</td>
              <td class="py-3.5 px-4 text-slate-400">Main Auditorium</td>
              <td class="py-3.5 px-4 text-center"><span class="bg-amber-500/10 text-amber-400 text-[11px] font-bold px-2.5 py-0.5 rounded-full border border-amber-500/20">Registrations Open</span></td>
            </tr>
            <tr class="hover:bg-slate-800/50 transition">
              <td class="py-3.5 px-4 font-mono text-blue-400 font-semibold">Dec 05, 2026</td>
              <td class="py-3.5 px-4 font-bold text-white">AI & Machine Learning Seminar</td>
              <td class="py-3.5 px-4">Guest Lecture</td>
              <td class="py-3.5 px-4 text-slate-400">Hall B & Online</td>
              <td class="py-3.5 px-4 text-center"><span class="bg-blue-500/10 text-blue-400 text-[11px] font-bold px-2.5 py-0.5 rounded-full border border-blue-500/20">Upcoming</span></td>
            </tr>
          </tbody>
        </table>
      </div>
    </section>

  </main>

  <!-- Footer -->
  ${generateSharedFooter()}

</body>
</html>`;
        }
      },
      page2: {
        filename: "about.html",
        title: "Innovators Club — About Us & Members",
        description: "Learn about the mission, history, and active member directory of the Tech Innovators Club.",
        encoding: 'UTF-8',
        viewport: 'width=device-width, initial-scale=1.0',
        faviconSvg: SVG_FAVICON_CLUB,
        get code() {
          return `<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Metadata & Setup -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Innovators Club — About Us & Members</title>
  <meta name="description" content="Learn about the mission, history, and active member directory of the Tech Innovators Club.">
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='25' fill='%232563eb'/><path d='M30 35h40M30 50h40M30 65h25' stroke='%23ffffff' stroke-width='8' stroke-linecap='round'/><circle cx='70' cy='65' r='8' fill='%2338bdf8'/></svg>">
  
  <script src="https://cdn.tailwindcss.com"><\/script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style> body { font-family: 'Inter', sans-serif; } </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col justify-between">

  <!-- Header Navigation -->
  ${generateSharedHeader('about.html')}

  <!-- Main Content -->
  <main class="max-w-6xl mx-auto px-4 sm:px-6 py-10 space-y-12 flex-1 w-full">
    
    <!-- Page Title Header -->
    <div class="border-b border-slate-800 pb-6 space-y-2">
      <span class="bg-blue-500/10 text-blue-400 text-xs font-bold px-3 py-1 rounded-full border border-blue-500/20 uppercase tracking-wider">About Our Organization</span>
      <h1 class="text-3xl sm:text-4xl font-extrabold text-white">Club Mission & Executive Board</h1>
      <p class="text-xs sm:text-sm text-slate-400">Empowering student developers and creators through community and innovation</p>
    </div>

    <!-- About Mission & Story -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
      <div class="space-y-4 text-sm text-slate-300 leading-relaxed">
        <h2 class="text-xl font-bold text-white">Our Mission Statement</h2>
        <p>
          Founded in 2022, the Tech Innovators Club was established to bridge the gap between academic theory and real-world software development. We believe in learning by building.
        </p>
        <p>
          Our members work on peer-led open-source projects, organize hackathons, and collaborate on software applications that benefit campus student life.
        </p>
      </div>

      <div class="bg-slate-900 border border-slate-800 p-6 rounded-2xl space-y-4">
        <h3 class="font-bold text-white text-base border-b border-slate-800 pb-2">Quick Club Statistics</h3>
        <div class="grid grid-cols-2 gap-4 text-center">
          <div class="bg-slate-950 p-4 rounded-xl border border-slate-800">
            <span class="text-2xl font-extrabold text-blue-400 block">150+</span>
            <span class="text-xs text-slate-400">Active Members</span>
          </div>
          <div class="bg-slate-950 p-4 rounded-xl border border-slate-800">
            <span class="text-2xl font-extrabold text-emerald-400 block">24+</span>
            <span class="text-xs text-slate-400">Projects Built</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Executive Leadership & Member Directory -->
    <section class="space-y-6">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-2 border-b border-slate-800 pb-4">
        <div>
          <h2 class="text-2xl font-bold text-white tracking-tight">Executive Committee & Leads</h2>
          <p class="text-xs sm:text-sm text-slate-400">Meet the team driving the club's initiatives</p>
        </div>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
        
        <!-- Member 1 -->
        <div class="bg-slate-900 border border-slate-800 p-5 rounded-2xl space-y-3 text-center hover:border-blue-500/40 transition">
          <div class="w-16 h-16 rounded-full bg-blue-600/20 text-blue-400 font-bold text-xl flex items-center justify-center mx-auto ring-2 ring-blue-500/30">
            AJ
          </div>
          <div>
            <h3 class="font-bold text-white text-base">Alex Johnson</h3>
            <span class="text-xs text-blue-400 font-medium block">Club President</span>
            <span class="text-[11px] text-slate-500 font-mono">Senior • Computer Science</span>
          </div>
        </div>

        <!-- Member 2 -->
        <div class="bg-slate-900 border border-slate-800 p-5 rounded-2xl space-y-3 text-center hover:border-blue-500/40 transition">
          <div class="w-16 h-16 rounded-full bg-purple-600/20 text-purple-400 font-bold text-xl flex items-center justify-center mx-auto ring-2 ring-purple-500/30">
            SM
          </div>
          <div>
            <h3 class="font-bold text-white text-base">Sophia Martinez</h3>
            <span class="text-xs text-purple-400 font-medium block">Vice President</span>
            <span class="text-[11px] text-slate-500 font-mono">Junior • Software Eng.</span>
          </div>
        </div>

        <!-- Member 3 -->
        <div class="bg-slate-900 border border-slate-800 p-5 rounded-2xl space-y-3 text-center hover:border-blue-500/40 transition">
          <div class="w-16 h-16 rounded-full bg-emerald-600/20 text-emerald-400 font-bold text-xl flex items-center justify-center mx-auto ring-2 ring-emerald-500/30">
            LW
          </div>
          <div>
            <h3 class="font-bold text-white text-base">Liam Williams</h3>
            <span class="text-xs text-emerald-400 font-medium block">Technical Lead</span>
            <span class="text-[11px] text-slate-500 font-mono">Senior • Data Science</span>
          </div>
        </div>

        <!-- Member 4 -->
        <div class="bg-slate-900 border border-slate-800 p-5 rounded-2xl space-y-3 text-center hover:border-blue-500/40 transition">
          <div class="w-16 h-16 rounded-full bg-amber-600/20 text-amber-400 font-bold text-xl flex items-center justify-center mx-auto ring-2 ring-amber-500/30">
            EB
          </div>
          <div>
            <h3 class="font-bold text-white text-base">Emma Brown</h3>
            <span class="text-xs text-amber-400 font-medium block">Events Coordinator</span>
            <span class="text-[11px] text-slate-500 font-mono">Junior • Electrical Eng.</span>
          </div>
        </div>

      </div>
    </section>

  </main>

  <!-- Footer -->
  ${generateSharedFooter()}

</body>
</html>`;
        }
      },
      page3: {
        filename: "registration.html",
        title: "Innovators Club — Student Registration",
        description: "Official online student membership registration form for joining the Innovators Club.",
        encoding: 'UTF-8',
        viewport: 'width=device-width, initial-scale=1.0',
        faviconSvg: SVG_FAVICON_CLUB,
        get code() {
          return `<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Metadata & Setup -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Innovators Club — Student Registration</title>
  <meta name="description" content="Official online student membership registration form for joining the Innovators Club.">
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='25' fill='%232563eb'/><path d='M30 35h40M30 50h40M30 65h25' stroke='%23ffffff' stroke-width='8' stroke-linecap='round'/><circle cx='70' cy='65' r='8' fill='%2338bdf8'/></svg>">
  
  <script src="https://cdn.tailwindcss.com"><\/script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style> body { font-family: 'Inter', sans-serif; } </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col justify-between">

  <!-- Header Navigation -->
  ${generateSharedHeader('registration.html')}

  <!-- Main Content -->
  <main class="max-w-3xl mx-auto px-4 sm:px-6 py-10 flex-1 w-full space-y-8">
    
    <div class="text-center space-y-2">
      <span class="bg-blue-500/10 text-blue-400 text-xs font-bold px-3 py-1 rounded-full border border-blue-500/20 uppercase tracking-wider">Membership Enrollment</span>
      <h1 class="text-3xl font-extrabold text-white">Join Tech Innovators Club</h1>
      <p class="text-xs sm:text-sm text-slate-400">Fill out the form below to register for membership and event access</p>
    </div>

    <!-- Registration Form -->
    <div class="bg-slate-900 border border-slate-800 rounded-2xl p-6 sm:p-8 shadow-2xl">
      <form onsubmit="event.preventDefault(); alert('Registration submitted successfully! Check your email for confirmation.');" class="space-y-6">
        
        <!-- Full Name -->
        <div>
          <label for="fullName" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Student Full Name *</label>
          <input type="text" id="fullName" required placeholder="e.g. Michael Chen" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
        </div>

        <!-- Student ID & Email -->
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
          <div>
            <label for="studentId" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Student Roll ID *</label>
            <input type="text" id="studentId" required placeholder="CS-2026-88" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
          </div>
          <div>
            <label for="email" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">College Email Address *</label>
            <input type="email" id="email" required placeholder="student@college.edu" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
          </div>
        </div>

        <!-- Academic Department & Academic Year -->
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
          <div>
            <label for="department" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Department *</label>
            <select id="department" required class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
              <option value="">Select Department...</option>
              <option value="cs">Computer Science & Engineering</option>
              <option value="ee">Electrical & Electronics</option>
              <option value="me">Mechanical Engineering</option>
              <option value="is">Information Technology</option>
            </select>
          </div>
          <div>
            <label for="year" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Year of Study *</label>
            <select id="year" required class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
              <option value="1">First Year (Freshman)</option>
              <option value="2">Second Year (Sophomore)</option>
              <option value="3" selected>Third Year (Junior)</option>
              <option value="4">Fourth Year (Senior)</option>
            </select>
          </div>
        </div>

        <!-- Primary Areas of Interest -->
        <div class="space-y-2">
          <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300">Areas of Tech Interest</label>
          <div class="grid grid-cols-2 gap-2 text-xs text-slate-300">
            <label class="flex items-center space-x-2 bg-slate-950 p-2.5 rounded-xl border border-slate-800 cursor-pointer hover:border-slate-700">
              <input type="checkbox" class="rounded text-blue-600 focus:ring-0">
              <span>Web Development</span>
            </label>
            <label class="flex items-center space-x-2 bg-slate-950 p-2.5 rounded-xl border border-slate-800 cursor-pointer hover:border-slate-700">
              <input type="checkbox" class="rounded text-blue-600 focus:ring-0">
              <span>AI & Machine Learning</span>
            </label>
            <label class="flex items-center space-x-2 bg-slate-950 p-2.5 rounded-xl border border-slate-800 cursor-pointer hover:border-slate-700">
              <input type="checkbox" class="rounded text-blue-600 focus:ring-0">
              <span>Mobile Apps</span>
            </label>
            <label class="flex items-center space-x-2 bg-slate-950 p-2.5 rounded-xl border border-slate-800 cursor-pointer hover:border-slate-700">
              <input type="checkbox" class="rounded text-blue-600 focus:ring-0">
              <span>Cybersecurity</span>
            </label>
          </div>
        </div>

        <!-- Submit Button -->
        <button type="submit" class="w-full bg-blue-600 hover:bg-blue-500 active:scale-98 text-white font-semibold py-3.5 rounded-xl shadow-lg shadow-blue-600/30 transition text-sm">
          Submit Club Registration
        </button>

      </form>
    </div>

  </main>

  <!-- Footer -->
  ${generateSharedFooter()}

</body>
</html>`;
        }
      },
      page4: {
        filename: "contact.html",
        title: "Innovators Club — Contact & Location",
        description: "Get in touch with the Tech Innovators Club leadership team, office location, and inquiry form.",
        encoding: 'UTF-8',
        viewport: 'width=device-width, initial-scale=1.0',
        faviconSvg: SVG_FAVICON_CLUB,
        get code() {
          return `<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Metadata & Setup -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Innovators Club — Contact & Location</title>
  <meta name="description" content="Get in touch with the Tech Innovators Club leadership team, office location, and inquiry form.">
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='25' fill='%232563eb'/><path d='M30 35h40M30 50h40M30 65h25' stroke='%23ffffff' stroke-width='8' stroke-linecap='round'/><circle cx='70' cy='65' r='8' fill='%2338bdf8'/></svg>">
  
  <script src="https://cdn.tailwindcss.com"><\/script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style> body { font-family: 'Inter', sans-serif; } </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col justify-between">

  <!-- Header Navigation -->
  ${generateSharedHeader('contact.html')}

  <!-- Main Content -->
  <main class="max-w-6xl mx-auto px-4 sm:px-6 py-10 space-y-12 flex-1 w-full">
    
    <!-- Page Header -->
    <div class="border-b border-slate-800 pb-6 space-y-2">
      <span class="bg-blue-500/10 text-blue-400 text-xs font-bold px-3 py-1 rounded-full border border-blue-500/20 uppercase tracking-wider">Contact & Inquiries</span>
      <h1 class="text-3xl font-extrabold text-white">Get in Touch with Us</h1>
      <p class="text-xs sm:text-sm text-slate-400">Have questions about upcoming events or sponsorship opportunities?</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      
      <!-- Contact Info Cards -->
      <div class="space-y-6">
        
        <div class="bg-slate-900 border border-slate-800 p-6 rounded-2xl space-y-4">
          <h2 class="text-lg font-bold text-white border-b border-slate-800 pb-2">Club Office & Meeting Room</h2>
          
          <div class="space-y-3 text-xs sm:text-sm text-slate-300">
            <div class="flex items-start space-x-3">
              <span class="text-blue-400 font-bold text-base">📍</span>
              <div>
                <strong class="text-white block">Campus Location:</strong>
                <span>Student Activity Center, Room 204<br>Engineering Campus, University Block A</span>
              </div>
            </div>

            <div class="flex items-center space-x-3">
              <span class="text-blue-400 font-bold text-base">✉️</span>
              <div>
                <strong class="text-white block">Email Address:</strong>
                <a href="mailto:innovators@university.edu" class="text-blue-400 hover:underline">innovators@university.edu</a>
              </div>
            </div>

            <div class="flex items-center space-x-3">
              <span class="text-blue-400 font-bold text-base">🕒</span>
              <div>
                <strong class="text-white block">Office Hours:</strong>
                <span>Monday – Friday: 3:00 PM – 6:00 PM</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Social / Links Card -->
        <div class="bg-slate-900 border border-slate-800 p-6 rounded-2xl space-y-3">
          <h3 class="font-bold text-white text-sm">Follow Our Projects</h3>
          <div class="flex space-x-3 text-xs">
            <span class="bg-slate-950 px-3 py-2 rounded-xl border border-slate-800 text-slate-300 font-mono">github.com/club-devs</span>
            <span class="bg-slate-950 px-3 py-2 rounded-xl border border-slate-800 text-slate-300 font-mono">discord.gg/innovators</span>
          </div>
        </div>

      </div>

      <!-- Quick Contact / Inquiry Form -->
      <div class="bg-slate-900 border border-slate-800 p-6 sm:p-8 rounded-2xl space-y-4 shadow-xl">
        <h2 class="text-lg font-bold text-white">Send Us a Direct Message</h2>
        <form onsubmit="event.preventDefault(); alert('Inquiry message sent successfully!');" class="space-y-4">
          <div>
            <label for="cName" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1.5">Your Name *</label>
            <input type="text" id="cName" required placeholder="Alex Turner" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
          </div>

          <div>
            <label for="cEmail" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1.5">Email Address *</label>
            <input type="email" id="cEmail" required placeholder="alex@gmail.com" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
          </div>

          <div>
            <label for="cMsg" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1.5">Message / Inquiry *</label>
            <textarea id="cMsg" rows="4" required placeholder="How can I sign up as a workshop mentor?" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
          </div>

          <button type="submit" class="w-full bg-blue-600 hover:bg-blue-500 active:scale-98 text-white font-semibold py-3 rounded-xl shadow-lg shadow-blue-600/30 transition text-sm">
            Send Message
          </button>
        </form>
      </div>

    </div>

  </main>

  <!-- Footer -->
  ${generateSharedFooter()}

</body>
</html>`;
        }
      }
    };

    let currentPageKey = 'page1';
    let currentViewMode = 'preview'; // 'preview' | 'code'

    // Initialize Hub
    document.addEventListener('DOMContentLoaded', () => {
      renderActivePage();
    });

    // Switch Active Page Tab
    function switchPage(pageKey) {
      currentPageKey = pageKey;
      
      // Update Tab Styles
      ['page1', 'page2', 'page3', 'page4'].forEach(key => {
        const btn = document.getElementById(`tab-${key}`);
        if (key === pageKey) {
          btn.className = "tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all bg-blue-600 text-white shadow-lg shadow-blue-600/25";
        } else {
          btn.className = "tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/60";
        }
      });

      renderActivePage();
    }

    // Switch View Mode (Preview vs Full Code)
    function switchViewMode(mode) {
      currentViewMode = mode;
      const previewContainer = document.getElementById('preview-container');
      const codeContainer = document.getElementById('code-container');
      const previewBtn = document.getElementById('view-preview-btn');
      const codeBtn = document.getElementById('view-code-btn');

      if (mode === 'preview') {
        previewContainer.classList.remove('hidden');
        previewContainer.classList.add('block');
        codeContainer.classList.add('hidden');
        codeContainer.classList.remove('block');

        previewBtn.className = "px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 bg-blue-600 text-white transition-all shadow-sm";
        codeBtn.className = "px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 text-slate-400 hover:text-slate-200 transition-all";
      } else {
        previewContainer.classList.add('hidden');
        previewContainer.classList.remove('block');
        codeContainer.classList.remove('hidden');
        codeContainer.classList.add('block');

        codeBtn.className = "px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 bg-blue-600 text-white transition-all shadow-sm";
        previewBtn.className = "px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 text-slate-400 hover:text-slate-200 transition-all";
      }
    }

    // Render active page data into spotlight, iframe, and code blocks
    function renderActivePage() {
      const data = pagesData[currentPageKey];

      // 1. Update Spotlight Info
      document.getElementById('spotlight-filename').innerText = data.filename;
      document.getElementById('spotlight-title').innerText = `${data.title} — Page Metadata & Route Overview`;
      document.getElementById('meta-encoding').innerText = `<meta charset="${data.encoding}">`;
      document.getElementById('meta-viewport').innerText = data.viewport;
      document.getElementById('meta-title').innerText = data.title;
      document.getElementById('meta-favicon-icon').innerHTML = data.faviconSvg;

      // 2. Update Browser Simulation Header
      document.getElementById('browser-tab-icon').innerHTML = data.faviconSvg;
      document.getElementById('browser-tab-title').innerText = data.title;
      document.getElementById('browser-url-path').innerText = data.filename;

      // 3. Update Iframe Content
      const iframe = document.getElementById('page-iframe');
      iframe.srcdoc = data.code;

      // 4. Update Source Code Block
      document.getElementById('code-filename-label').innerText = data.filename;
      document.getElementById('source-code-block').textContent = data.code;
    }

    // Copy Head Block Metadata
    function copyActiveMetadataHead() {
      const data = pagesData[currentPageKey];
      const headSnippet = `<head>
  <meta charset="${data.encoding}">
  <meta name="viewport" content="${data.viewport}">
  <title>${data.title}</title>
  <meta name="description" content="${data.description}">
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,${encodeURIComponent(data.faviconSvg)}">
</head>`;
      
      copyToClipboard(headSnippet, "Copied <head> metadata block to clipboard!");
    }

    // Copy Full Source Code
    function copyFullSourceCode() {
      const data = pagesData[currentPageKey];
      copyToClipboard(data.code, `Copied complete ${data.filename} source code!`);
    }

    // Copy Helper Utility
    function copyToClipboard(text, successMsg) {
      const textarea = document.createElement('textarea');
      textarea.value = text;
      document.body.appendChild(textarea);
      textarea.select();
      document.execCommand('copy');
      document.body.removeChild(textarea);

      // Trigger Toast Notification
      const toast = document.getElementById('toast');
      const toastMessage = document.getElementById('toastMessage');
      toastMessage.innerText = successMsg;

      toast.classList.remove('translate-y-[-100px]', 'opacity-0');
      toast.classList.add('translate-y-0', 'opacity-100');

      setTimeout(() => {
        toast.classList.remove('translate-y-0', 'opacity-100');
        toast.classList.add('translate-y-[-100px]', 'opacity-0');
      }, 2500);
    }
  </script>
</body>
</html>