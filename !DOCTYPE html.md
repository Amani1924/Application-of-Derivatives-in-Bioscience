<!DOCTYPE html>

<html lang="en">

<head>

&#x20;   <meta charset="UTF-8">

&#x20;   <meta name="viewport" content="width=device-width, initial-scale=1.0">

&#x20;   <title>AquaBio-Calc: Tilapia Growth Rate \& Bioenergetic Optimizer</title>

&#x20;   

&#x20;   <!-- Tailwind CSS for stunning modern dashboard designs -->

&#x20;   <script src="https://cdn.tailwindcss.com"></script>

&#x20;   

&#x20;   <!-- Google Fonts (Inter and Playfair Display) -->

&#x20;   <link rel="preconnect" href="https://fonts.googleapis.com">

&#x20;   <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

&#x20;   <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800\&family=Playfair+Display:ital,wght@0,600;0,700;1,600\&display=swap" rel="stylesheet">

&#x20;   

&#x20;   <!-- Chart.js for real-time mathematical visualizations -->

&#x20;   <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

&#x20;   

&#x20;   <!-- KaTeX for ultra-crisp LaTeX mathematical typography -->

&#x20;   <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/katex.min.css">

&#x20;   <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/katex.min.js"></script>

&#x20;   <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/contrib/auto-render.min.js" onload="renderMathInElement(document.body);"></script>



&#x20;   <!-- Lucide Icons for responsive vector indicators -->

&#x20;   <script src="https://unpkg.com/lucide@latest"></script>



&#x20;   <style>

&#x20;       body {

&#x20;           font-family: 'Inter', sans-serif;

&#x20;       }

&#x20;       .serif-title {

&#x20;           font-family: 'Playfair Display', serif;

&#x20;       }

&#x20;       /\* Elegant smooth scrollbar \*/

&#x20;       ::-webkit-scrollbar {

&#x20;           width: 6px;

&#x20;           height: 6px;

&#x20;       }

&#x20;       ::-webkit-scrollbar-track {

&#x20;           background: #f0f9ff;

&#x20;       }

&#x20;       ::-webkit-scrollbar-thumb {

&#x20;           background: #bae6fd;

&#x20;           border-radius: 4px;

&#x20;       }

&#x20;       ::-webkit-scrollbar-thumb:hover {

&#x20;           background: #38bdf8;

&#x20;       }

&#x20;   </style>

</head>

<body class="bg-sky-50/30 text-slate-800 min-h-screen flex flex-col">



&#x20;   <!-- Top Navigation Header -->

&#x20;   <nav class="bg-gradient-to-r from-cyan-900 via-sky-850 to-indigo-900 text-white shadow-md sticky top-0 z-50">

&#x20;       <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">

&#x20;           <div class="flex flex-col md:flex-row justify-between items-center gap-4">

&#x20;               <div class="flex items-center space-x-3">

&#x20;                   <div class="bg-cyan-500 p-2.5 rounded-xl shadow-lg shadow-cyan-500/20 flex items-center justify-center">

&#x20;                       <i data-lucide="waves" class="w-6 h-6 text-white animate-pulse"></i>

&#x20;                   </div>

&#x20;                   <div>

&#x20;                       <h1 class="text-xl font-extrabold tracking-tight flex items-center gap-2">

&#x20;                           AquaBio-Calc <span class="bg-cyan-950/60 text-cyan-300 text-xs px-2.5 py-1 rounded-full border border-cyan-500/30">v3.1</span>

&#x20;                       </h1>

&#x20;                       <p class="text-xs text-sky-200/90 font-medium">Sustainable Aquaculture Food Security Mathematical Tool</p>

&#x20;                   </div>

&#x20;               </div>

&#x20;               <div class="flex items-center gap-2 bg-cyan-950/50 px-4 py-2 rounded-xl border border-cyan-500/20 text-xs">

&#x20;                   <i data-lucide="anchor" class="w-4 h-4 text-cyan-400"></i>

&#x20;                   <span class="font-semibold text-sky-200">Lake Temenggor (Perak) Red Tilapia Growth Framework</span>

&#x20;               </div>

&#x20;           </div>

&#x20;       </div>

&#x20;   </nav>



&#x20;   <!-- Main Workspace Container -->

&#x20;   <main class="flex-grow max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-8">

&#x20;       

&#x20;       <!-- Introductory Educational Banner -->

&#x20;       <div class="bg-white rounded-2xl border border-sky-100 p-6 md:p-8 shadow-sm mb-8 relative overflow-hidden">

&#x20;           <div class="absolute right-0 top-0 opacity-\[0.03] pointer-events-none transform translate-x-12 -translate-y-12">

&#x20;               <i data-lucide="fish" class="w-96 h-96 text-cyan-950"></i>

&#x20;           </div>

&#x20;           <div class="relative z-10">

&#x20;               <span class="text-xs font-bold uppercase tracking-widest text-sky-600 bg-sky-50 px-3 py-1.5 rounded-full">National Agrofood Policy 2.0 (DAN 2.0) Aquaculture Target</span>

&#x20;               <h2 class="text-2xl md:text-3.5xl font-bold text-slate-900 mt-3 mb-4 serif-title">

&#x20;                   Gompertz Growth Derivatives in Malaysian Tilapia Farming

&#x20;               </h2>

&#x20;               <div class="grid grid-cols-1 lg:grid-cols-3 gap-6 text-sm text-slate-600 leading-relaxed">

&#x20;                   <div class="lg:col-span-2 space-y-3">

&#x20;                       <p>

&#x20;                           To secure cheap, high-quality protein for food security, Malaysia relies heavily on freshwater aquaculture. \*\*Red Tilapia\*\* (\*Oreochromis hybrid\*) makes up over 40% of our local freshwater production. However, feed comprises \*\*60-70% of total operating expenses\*\*. Overfeeding degrades water quality (causing ammonia spikes in lake cages), while underfeeding reduces growth yield.

&#x20;                       </p>

&#x20;                       <p>

&#x20;                           This bio-mathematical simulator applies differential calculus to the \*\*Gompertz Growth Model\*\* to track cumulative body weight $W(t)$ and instantaneous daily weight gain $W'(t)$. By evaluating the mathematical derivative, agronomists identify the exact transition window where feeding strategies must shift from rapid development to maintenance-based biomass retention.

&#x20;                       </p>

&#x20;                   </div>

&#x20;                   <div class="bg-sky-50/50 p-4 rounded-xl border border-sky-100 flex flex-col justify-between">

&#x20;                       <div>

&#x20;                           <h4 class="font-bold text-sky-950 flex items-center gap-1.5 text-xs uppercase tracking-wider mb-2">

&#x20;                               <i data-lucide="help-circle" class="w-4 h-4 text-sky-600"></i> The Role of $W'(t)$

&#x20;                           </h4>

&#x20;                           <p class="text-xs text-slate-600">

&#x20;                               The derivative $W'(t)$ represents the \*\*Instantaneous Daily Weight Gain (g/day)\*\*. Measuring the inflection point (maximum $W'(t)$) allows smart feeding algorithms to adjust feeding schedules (FCR optimization) precisely to temperature fluctuations.

&#x20;                           </p>

&#x20;                       </div>

&#x20;                       <div class="mt-4 pt-3 border-t border-sky-100 flex items-center gap-2">

&#x20;                           <i data-lucide="graduation-cap" class="w-4 h-4 text-sky-800"></i>

&#x20;                           <span class="text-xs font-semibold text-sky-900">Bioscience \& precision modeling</span>

&#x20;                       </div>

&#x20;                   </div>

&#x20;               </div>

&#x20;           </div>

&#x20;       </div>



&#x20;       <div class="grid grid-cols-1 lg:grid-cols-12 gap-8">

&#x20;           

&#x20;           <!-- Left Grid: Math, Controls \& Real-time values -->

&#x20;           <div class="lg:col-span-5 space-y-6">

&#x20;               

&#x20;               <!-- Mathematical Models Card -->

&#x20;               <div class="bg-white rounded-2xl border border-slate-200/80 shadow-sm p-6">

&#x20;                   <h3 class="text-lg font-bold text-slate-900 mb-4 flex items-center gap-2">

&#x20;                       <i data-lucide="variable" class="w-5 h-5 text-sky-600"></i>

&#x20;                       The Bioenergetics Model

&#x20;                   </h3>

&#x20;                   

&#x20;                   <div class="space-y-4">

&#x20;                       <!-- Gompertz Weight Model -->

&#x20;                       <div class="bg-slate-50 p-4 rounded-xl border border-slate-200">

&#x20;                           <div class="flex justify-between items-center mb-1">

&#x20;                               <span class="text-xs font-bold text-slate-500 uppercase">Gompertz Growth Equation</span>

&#x20;                               <span class="text-xs text-cyan-600 bg-cyan-50 px-2 py-0.5 rounded font-mono">W(t)</span>

&#x20;                           </div>

&#x20;                           <div class="py-2 text-center text-lg overflow-x-auto text-slate-800" id="formula-wt">

&#x20;                               $$W(t) = A \\cdot e^{-B \\cdot e^{-k \\cdot t}}$$

&#x20;                           </div>

&#x20;                           <p class="text-\[11px] text-slate-500 mt-1 leading-snug">

&#x20;                               Models standard cumulative body weight (grams). Where asymptotic limit $A = 600\\text{ g}$ (max size), scaling constant $B = 4.8$, and $k$ is the temperature-dependent growth rate coefficient.

&#x20;                           </p>

&#x20;                       </div>



&#x20;                       <!-- Derivative Model -->

&#x20;                       <div class="bg-slate-50 p-4 rounded-xl border border-slate-200">

&#x20;                           <div class="flex justify-between items-center mb-1">

&#x20;                               <span class="text-xs font-bold text-slate-500 uppercase">Instant Daily Growth Rate</span>

&#x20;                               <span class="text-xs text-indigo-600 bg-indigo-50 px-2 py-0.5 rounded font-mono">W'(t)</span>

&#x20;                           </div>

&#x20;                           <div class="py-2 text-center text-lg overflow-x-auto text-slate-800" id="formula-dwt">

&#x20;                               $$W'(t) = W(t) \\cdot B \\cdot k \\cdot e^{-k \\cdot t}$$

&#x20;                           </div>

&#x20;                           <p class="text-\[11px] text-slate-500 mt-1 leading-snug">

&#x20;                               Calculated by applying the chain rule to the natural logarithm index. Represents daily weight gain ($g/\\text{day}$).

&#x20;                           </p>

&#x20;                       </div>

&#x20;                   </div>

&#x20;               </div>



&#x20;               <!-- Interactive Controls \& Output Display -->

&#x20;               <div class="bg-gradient-to-br from-slate-900 to-slate-850 text-white rounded-2xl shadow-xl p-6 relative overflow-hidden">

&#x20;                   <div class="absolute -right-8 -bottom-8 opacity-10">

&#x20;                       <i data-lucide="thermometer" class="w-32 h-32 text-cyan-400"></i>

&#x20;                   </div>

&#x20;                   

&#x20;                   <h3 class="text-lg font-bold mb-1 flex items-center gap-2 text-cyan-400">

&#x20;                       <i data-lucide="sliders" class="w-5 h-5"></i>

&#x20;                       Bioenergetics Controller

&#x20;                   </h3>

&#x20;                   <p class="text-xs text-slate-400 mb-6">Manipulate cultivation parameters to monitor biological responses in real time.</p>



&#x20;                   <div class="space-y-5">

&#x20;                       

&#x20;                       <!-- Water Temperature Slider (Ectothermic Control) -->

&#x20;                       <div class="space-y-2">

&#x20;                           <div class="flex justify-between text-xs font-semibold">

&#x20;                               <span class="flex items-center gap-1">

&#x20;                                   <i data-lucide="droplet" class="w-3.5 h-3.5 text-cyan-400"></i> 

&#x20;                                   Cage Water Temperature

&#x20;                               </span>

&#x20;                               <span class="bg-cyan-500/20 text-cyan-300 border border-cyan-500/30 px-2 py-0.5 rounded" id="temp-badge">28.0°C</span>

&#x20;                           </div>

&#x20;                           <input 

&#x20;                               type="range" 

&#x20;                               id="tempSlider" 

&#x20;                               min="24" 

&#x20;                               max="32" 

&#x20;                               step="0.5"

&#x20;                               value="28" 

&#x20;                               class="w-full h-2 bg-slate-700 rounded-lg appearance-none cursor-pointer accent-cyan-400 focus:outline-none focus:ring-2 focus:ring-cyan-500"

&#x20;                           >

&#x20;                           <div class="flex justify-between text-\[10px] text-slate-400">

&#x20;                               <span>Cold Stress (24°C)</span>

&#x20;                               <span class="text-cyan-300 font-semibold">Optimal (28°C-30°C)</span>

&#x20;                               <span>Anoxic Heat Stress (32°C)</span>

&#x20;                           </div>

&#x20;                       </div>



&#x20;                       <!-- Growth Day Timeline Slider -->

&#x20;                       <div class="space-y-2 pb-2 border-b border-slate-700/50">

&#x20;                           <div class="flex justify-between text-xs font-semibold">

&#x20;                               <span class="flex items-center gap-1">

&#x20;                                   <i data-lucide="calendar" class="w-3.5 h-3.5 text-indigo-400"></i> 

&#x20;                                   Growth Timeline Position

&#x20;                               </span>

&#x20;                               <span class="bg-indigo-500/20 text-indigo-300 border border-indigo-500/30 px-2 py-0.5 rounded" id="day-badge">Day 60</span>

&#x20;                           </div>

&#x20;                           <input 

&#x20;                               type="range" 

&#x20;                               id="daySlider" 

&#x20;                               min="0" 

&#x20;                               max="150" 

&#x20;                               value="60" 

&#x20;                               class="w-full h-2 bg-slate-700 rounded-lg appearance-none cursor-pointer accent-indigo-400 focus:outline-none focus:ring-2 focus:ring-indigo-500"

&#x20;                           >

&#x20;                           <div class="flex justify-between text-\[10px] text-slate-400">

&#x20;                               <span>Stocking (D0)</span>

&#x20;                               <span>Mid-Cycle (D75)</span>

&#x20;                               <span>Harvest (D150)</span>

&#x20;                           </div>

&#x20;                       </div>

&#x20;                   </div>



&#x20;                   <!-- Real-time Mathematical Output Cards -->

&#x20;                   <div class="grid grid-cols-2 gap-3 my-5">

&#x20;                       <div class="bg-slate-800/80 p-3 rounded-xl border border-slate-700">

&#x20;                           <span class="text-\[10px] font-bold tracking-wider text-slate-400 uppercase">Fish Body Weight</span>

&#x20;                           <div class="flex items-baseline gap-1 mt-1 text-cyan-400">

&#x20;                               <span class="text-2xl font-extrabold" id="calc-weight">220.7</span>

&#x20;                               <span class="text-xs font-semibold">g/fish</span>

&#x20;                           </div>

&#x20;                           <p class="text-\[10px] text-slate-400 mt-1 font-mono">W(t) absolute size</p>

&#x20;                       </div>

&#x20;                       

&#x20;                       <div class="bg-slate-800/80 p-3 rounded-xl border border-slate-700">

&#x20;                           <span class="text-\[10px] font-bold tracking-wider text-slate-400 uppercase">Growth Velocity</span>

&#x20;                           <div class="flex items-baseline gap-1 mt-1 text-indigo-400">

&#x20;                               <span class="text-2xl font-extrabold" id="calc-growth-rate">5.74</span>

&#x20;                               <span class="text-xs font-semibold">g/day</span>

&#x20;                           </div>

&#x20;                           <p class="text-\[10px] text-slate-400 mt-1 font-mono">W'(t) first derivative</p>

&#x20;                       </div>

&#x20;                   </div>



&#x20;                   <!-- Scientific Advisory Insight Section -->

&#x20;                   <div class="bg-indigo-950/40 border border-indigo-500/20 rounded-xl p-4">

&#x20;                       <div class="flex items-center gap-2 mb-2">

&#x20;                           <div class="bg-indigo-500/20 p-1.5 rounded-lg">

&#x20;                               <i data-lucide="info" class="w-4 h-4 text-cyan-300" id="advisory-icon"></i>

&#x20;                           </div>

&#x20;                           <h4 class="text-xs font-bold uppercase tracking-wider text-cyan-200" id="advisory-stage">

&#x20;                               Linear Expansion Phase

&#x20;                           </h4>

&#x20;                       </div>

&#x20;                       <p class="text-xs text-slate-300 leading-relaxed mb-3" id="advisory-desc">

&#x20;                           Fish metabolism is performing optimally. This maximum growth slope means feed assimilation efficiency is at its highest point.

&#x20;                       </p>

&#x20;                       

&#x20;                       <div class="bg-slate-900/60 p-2.5 rounded-lg border border-slate-700/50 flex items-start gap-2">

&#x20;                           <i data-lucide="utensils" class="w-4 h-4 text-amber-400 shrink-0 mt-0.5"></i>

&#x20;                           <div class="text-\[11px] text-slate-300">

&#x20;                               <span class="font-bold text-white block">Feeding Ratio Protocol:</span>

&#x20;                               <span id="advisory-feeding">Feed floating pellets (30% Protein) twice daily at 2.5% of total biomass weight.</span>

&#x20;                           </div>

&#x20;                       </div>

&#x20;                   </div>



&#x20;               </div>



&#x20;           </div>



&#x20;           <!-- Right Grid: High fidelity Interactive Graph Plotter -->

&#x20;           <div class="lg:col-span-7 space-y-6">

&#x20;               

&#x20;               <!-- Chart.js Graphics Box -->

&#x20;               <div class="bg-white rounded-2xl border border-slate-200 shadow-sm p-6 flex flex-col h-full">

&#x20;                   <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 mb-4">

&#x20;                       <div>

&#x20;                           <h3 class="text-lg font-bold text-slate-900 flex items-center gap-2">

&#x20;                               <i data-lucide="line-chart" class="w-5 h-5 text-cyan-600"></i>

&#x20;                               Aquaculture Growth \& Rate Interactive Curve

&#x20;                           </h3>

&#x20;                           <p class="text-xs text-slate-500">Analyze the correlation between Cumulative Weight $W(t)$ (Blue) and Instantaneous Derivative $W'(t)$ (Indigo)</p>

&#x20;                       </div>

&#x20;                       <div class="flex gap-2">

&#x20;                           <button id="btnReset" class="text-xs font-semibold text-slate-600 hover:text-cyan-700 bg-slate-100 hover:bg-sky-50 px-3 py-2 rounded-xl transition duration-150 flex items-center gap-1.5">

&#x20;                               <i data-lucide="rotate-ccw" class="w-3.5 h-3.5"></i> Reset to Peak

&#x20;                           </button>

&#x20;                       </div>

&#x20;                   </div>



&#x20;                   <!-- Canvas Box -->

&#x20;                   <div class="relative flex-grow min-h-\[350px] md:min-h-\[420px] bg-slate-50/50 rounded-xl border border-slate-100 p-3">

&#x20;                       <canvas id="aquacultureChart"></canvas>

&#x20;                       

&#x20;                       <!-- Floating instructional cue -->

&#x20;                       <div class="absolute bottom-4 left-4 right-4 bg-slate-900/80 backdrop-blur-sm text-white px-4 py-2 rounded-xl text-center text-xs pointer-events-none flex items-center justify-center gap-2 shadow-lg">

&#x20;                           <i data-lucide="mouse-pointer" class="w-4 h-4 text-cyan-400 animate-bounce"></i>

&#x20;                           <span>Click inside the coordinate matrix to calculate exact rates at specific days!</span>

&#x20;                       </div>

&#x20;                   </div>



&#x20;                   <!-- Color Legend Panel -->

&#x20;                   <div class="grid grid-cols-1 sm:grid-cols-3 gap-3 mt-4 text-xs font-medium text-slate-600">

&#x20;                       <div class="flex items-center gap-2 bg-cyan-50/50 p-2.5 rounded-lg border border-cyan-100/50">

&#x20;                           <div class="w-3.5 h-3.5 bg-cyan-600 rounded"></div>

&#x20;                           <span>Fish Weight: $W(t)$ (g/fish)</span>

&#x20;                       </div>

&#x20;                       <div class="flex items-center gap-2 bg-indigo-50/50 p-2.5 rounded-lg border border-indigo-100/50">

&#x20;                           <div class="w-3.5 h-3.5 bg-indigo-500 rounded"></div>

&#x20;                           <span>Growth Gain: $W'(t)$ (g/day)</span>

&#x20;                       </div>

&#x20;                       <div class="flex items-center gap-2 bg-sky-50/50 p-2.5 rounded-lg border border-sky-100/50">

&#x20;                           <div class="w-3.5 h-1.5 bg-cyan-400 rounded-full"></div>

&#x20;                           <span>Instant Tangent Slope Line</span>

&#x20;                       </div>

&#x20;                   </div>

&#x20;               </div>



&#x20;           </div>



&#x20;       </div>



&#x20;       <!-- Aquaculture Deep-Dive: Growth Stages of Red Tilapia -->

&#x20;       <div class="mt-8 bg-white rounded-2xl border border-slate-200 p-6 md:p-8 shadow-sm">

&#x20;           <h3 class="text-xl font-bold text-slate-900 mb-6 serif-title border-b pb-4 flex items-center gap-2">

&#x20;               <i data-lucide="microscope" class="w-6 h-6 text-cyan-600"></i>

&#x20;               Bioscience Analysis: Biomass Acceleration Stages in Red Tilapia

&#x20;           </h3>

&#x20;           

&#x20;           <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 text-slate-600">

&#x20;               

&#x20;               <div class="space-y-2 border-l-4 border-slate-300 pl-4 py-1">

&#x20;                   <span class="text-\[10px] font-bold text-slate-500 uppercase">Phase 1: Post-Stocking Adaptation</span>

&#x20;                   <h4 class="font-bold text-slate-800 text-sm">Days 0 – 30</h4>

&#x20;                   <p class="text-xs leading-relaxed">

&#x20;                       Fingerlings adjust to Lake cages from hatchery pools. The cumulative Gompertz weight index $W(t)$ remains flat (under 40g). The daily derivative $W'(t)$ is positive but tiny, signifying limited food intake.

&#x20;                   </p>

&#x20;               </div>



&#x20;               <div class="space-y-2 border-l-4 border-cyan-500 pl-4 py-1 bg-cyan-50/20 pr-2 rounded-r-lg">

&#x20;                   <span class="text-\[10px] font-bold text-cyan-700 uppercase">Phase 2: Exponential Mass Gain</span>

&#x20;                   <h4 class="font-bold text-slate-900 text-sm">Days 31 – 70 (The Golden Zone)</h4>

&#x20;                   <p class="text-xs leading-relaxed">

&#x20;                       Skeletal development is complete; muscles start packing weight. Under optimal 28°C, the derivative $W'(t)$ reaches its \*\*maximum peak on Day 60 (\~5.7 g/day)\*\*. Metabolic feed utilization is optimal.

&#x20;                   </p>

&#x20;               </div>



&#x20;               <div class="space-y-2 border-l-4 border-indigo-500 pl-4 py-1">

&#x20;                   <span class="text-\[10px] font-bold text-indigo-700 uppercase">Phase 3: Satiated Growth Tapering</span>

&#x20;                   <h4 class="font-bold text-slate-800 text-sm">Days 71 – 110</h4>

&#x20;                   <p class="text-xs leading-relaxed">

&#x20;                       Fish biomass rises above 400g, but growth velocity $W'(t)$ decelerates. Energy conversion shifts towards tissue maintenance and respiratory consumption rather than generating new cells.

&#x20;                   </p>

&#x20;               </div>



&#x20;               <div class="space-y-2 border-l-4 border-red-500 pl-4 py-1">

&#x20;                   <span class="text-\[10px] font-bold text-red-700 uppercase">Phase 4: Market Maturity Window</span>

&#x20;                   <h4 class="font-bold text-slate-800 text-sm">Days 111 – 150</h4>

&#x20;                   <p class="text-xs leading-relaxed">

&#x20;                       Fish asymptotic threshold is approached near 550-600g. The derivative $W'(t)$ falls below 1.5 g/day. Feeding past this point is extremely wasteful (high FCR values limit profitability).

&#x20;                   </p>

&#x20;               </div>



&#x20;           </div>



&#x20;           <!-- Mathematical Proof Block for Ectothermic Gompertz Modeling -->

&#x20;           <div class="mt-8 p-6 bg-slate-50 rounded-xl border border-slate-200">

&#x20;               <h4 class="text-sm font-bold text-slate-800 uppercase mb-3 tracking-wide flex items-center gap-1.5">

&#x20;                   <i data-lucide="code-xml" class="w-4 h-4 text-cyan-600"></i> Mathematical Derivation of $W'(t)$ \& Temperature Dependence

&#x20;               </h4>

&#x20;               <p class="text-xs text-slate-600 mb-4 leading-relaxed">

&#x20;                   Ectotherms rely on thermal constants to drive biochemical reactions. Here, growth coefficient $k$ is adjusted via $k(T) = k\_{\\text{opt}} \\cdot \[1 - \\beta(T - T\_{\\text{opt}})^2]$ where $T\_{\\text{opt}} = 28^\\circ\\text{C}$ and sensitivity factor $\\beta = 0.015$. The first analytical derivative of $W(t) = A e^{-B e^{-kt}}$ is solved via chain rule:

&#x20;               </p>

&#x20;               <div class="grid grid-cols-1 md:grid-cols-2 gap-4 text-xs font-mono text-slate-700 bg-white p-4 rounded-lg border border-slate-200">

&#x20;                   <div>

&#x20;                       <p class="text-cyan-700 font-bold mb-1">// Step 1: Let substitution u(t) = -B \* e^(-kt)</p>

&#x20;                       <p class="py-1">$$W(t) = A \\cdot e^{u(t)}$$</p>

&#x20;                       <p class="py-1">$$\\frac{d}{dt}\[u(t)] = \\frac{d}{dt}\[-B \\cdot e^{-kt}] = B \\cdot k \\cdot e^{-kt}$$</p>

&#x20;                   </div>

&#x20;                   <div>

&#x20;                       <p class="text-indigo-700 font-bold mb-1">// Step 2: Product chain execution</p>

&#x20;                       <p class="py-1">$$W'(t) = A e^{u(t)} \\cdot u'(t)$$</p>

&#x20;                       <p class="py-1">$$W'(t) = W(t) \\cdot B \\cdot k \\cdot e^{-kt}$$</p>

&#x20;                   </div>

&#x20;               </div>

&#x20;           </div>



&#x20;           <!-- Malaysian Scholarly Citations \& Environmental Policy Notes -->

&#x20;           <div class="mt-6 pt-6 border-t border-slate-200 flex flex-col md:flex-row justify-between items-start gap-6 text-xs text-slate-500">

&#x20;               <div class="space-y-2">

&#x20;                   <span class="font-bold text-slate-700 block uppercase tracking-wider">Malaysian Scientific Data \& Aquaculture References:</span>

&#x20;                   <ul class="list-disc pl-5 space-y-1">

&#x20;                       <li><strong>Lake Temenggor Cage Farms:</strong> Governed by the Perak Fisheries Department, practicing precision feed targets to limit waste sedimentation beneath open-water net cages.</li>

&#x20;                       <li><strong>Gompertz Parameters ($A, B, k$):</strong> Calibrated using research paper data detailing \*Gompertz model simulations of hybrid red tilapia weight indices\* raised in humid tropical reservoirs.</li>

&#x20;                       <li><strong>Temperature-Growth Sensitivity ($k(T)$):</strong> Models physiological limits in thermal boundaries established by the National Aquaculture Extension guidelines of Malaysia (DOF).</li>

&#x20;                   </ul>

&#x20;               </div>

&#x20;               <div class="bg-slate-100 p-4 rounded-xl border border-slate-200 text-slate-600 max-w-sm shrink-0">

&#x20;                   <h5 class="font-bold text-slate-800 text-xs mb-1">Fisheries Research Citation:</h5>

&#x20;                   <p class="text-\[11px] leading-relaxed italic">

&#x20;                       "Evaluating feed optimization metrics and biomathematical kinetics of Oreochromis sp. in Peninsular Malaysia tropical reservoirs", Malaysian Journal of Fisheries Science.

&#x20;                   </p>

&#x20;               </div>

&#x20;           </div>

&#x20;       </div>



&#x20;   </main>



&#x20;   <!-- Footer section -->

&#x20;   <footer class="bg-slate-900 text-slate-400 text-xs py-8 mt-12 border-t border-slate-800">

&#x20;       <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row justify-between items-center gap-4">

&#x20;           <div class="flex items-center space-x-2">

&#x20;               <i data-lucide="shield" class="w-4 h-4 text-cyan-400"></i>

&#x20;               <span class="text-slate-300 font-bold">Malaysia Smart Aquaculture Initiative</span>

&#x20;           </div>

&#x20;           <div class="text-center md:text-right">

&#x20;               <p>Curated for Sustainable Food Security (SFM) Undergraduate Aquaculture Systems.</p>

&#x20;               <p class="text-\[10px] text-slate-500 mt-1">Real-time simulation operates on client-side floating coordinates. No database lag.</p>

&#x20;           </div>

&#x20;       </div>

&#x20;   </footer>



&#x20;   <script>

&#x20;       // Mathematical Constants for Gompertz Red Tilapia Models

&#x20;       const A = 600;       // Asymptotic maximum growth target weight (grams)

&#x20;       const B = 4.8;       // Scaling scaling index reflecting stocking sizes



&#x20;       // Optimal parameters for temperature dependence curve

&#x20;       const kOpt = 0.026;   // Peak growth coefficient at ideal temperature

&#x20;       const TOpt = 28.0;    // Ideal culture temperature for Red Tilapia hybrid

&#x20;       const beta = 0.015;   // Sensivity rate to heat/cold thermal variations



&#x20;       // Calculates dynamic k coefficient dependent on aquaculture water temperature

&#x20;       function getGrowthRateCoefficient(temp) {

&#x20;           // Parabolic thermal enzyme kinetics curve

&#x20;           return kOpt \* (1 - beta \* Math.pow(temp - TOpt, 2));

&#x20;       }



&#x20;       // Gompertz Growth Weight function: W(t)

&#x20;       function W(t, k) {

&#x20;           return A \* Math.exp(-B \* Math.exp(-k \* t));

&#x20;       }



&#x20;       // Instantaneous first derivative weight rate: W'(t)

&#x20;       function dW(t, k) {

&#x20;           const wt = W(t, k);

&#x20;           return wt \* B \* k \* Math.exp(-k \* t);

&#x20;       }



&#x20;       // Linear tangent slope calculator: T(t) = W'(target) \* (t - target) + W(target)

&#x20;       function calculateTangentLine(tValue, targetDay, k) {

&#x20;           const slope = dW(targetDay, k);

&#x20;           const yOffset = W(targetDay, k);

&#x20;           return slope \* (tValue - targetDay) + yOffset;

&#x20;       }



&#x20;       let chartInstance = null;

&#x20;       const totalDays = 150;

&#x20;       const tLabels = Array.from({length: totalDays + 1}, (\_, i) => i);



&#x20;       // Populate datasets for plotting based on active conditions

&#x20;       function generateChartDatasets(selectedDay, currentTemp) {

&#x20;           const currentK = getGrowthRateCoefficient(currentTemp);



&#x20;           // Populate array values with active coefficient

&#x20;           const weightValues = tLabels.map(day => W(day, currentK));

&#x20;           const derivativeValues = tLabels.map(day => dW(day, currentK));



&#x20;           // Populate localized tangent line within a visual neighborhood of +/- 20 days

&#x20;           const tangentValues = tLabels.map(day => {

&#x20;               if (day >= selectedDay - 20 \&\& day <= selectedDay + 20) {

&#x20;                   return calculateTangentLine(day, selectedDay, currentK);

&#x20;               }

&#x20;               return null;

&#x20;           });



&#x20;           // Isolate individual coordinates to render focal point highlights on the grid

&#x20;           const selectedWeightPoint = tLabels.map(day => day === selectedDay ? W(selectedDay, currentK) : null);

&#x20;           const selectedRatePoint = tLabels.map(day => day === selectedDay ? dW(selectedDay, currentK) : null);



&#x20;           return \[

&#x20;               {

&#x20;                   label: 'Cumulative Weight W(t) (g/fish)',

&#x20;                   data: weightValues,

&#x20;                   borderColor: '#0284c7', // Sky Blue 600

&#x20;                   backgroundColor: 'rgba(2, 132, 199, 0.03)',

&#x20;                   borderWidth: 3,

&#x20;                   yAxisID: 'yWeight',

&#x20;                   pointRadius: 0,

&#x20;                   tension: 0.1,

&#x20;                   order: 3

&#x20;               },

&#x20;               {

&#x20;                   label: 'Daily Growth Gain W\\'(t) (g/day)',

&#x20;                   data: derivativeValues,

&#x20;                   borderColor: '#6366f1', // Indigo 500

&#x20;                   borderWidth: 2.5,

&#x20;                   borderDash: \[5, 5],

&#x20;                   yAxisID: 'yRate',

&#x20;                   pointRadius: 0,

&#x20;                   tension: 0.1,

&#x20;                   order: 4

&#x20;               },

&#x20;               {

&#x20;                   label: 'Selected Tangent Vector Slope',

&#x20;                   data: tangentValues,

&#x20;                   borderColor: '#22d3ee', // Cyan 400

&#x20;                   borderWidth: 2,

&#x20;                   yAxisID: 'yWeight',

&#x20;                   pointRadius: 0,

&#x20;                   spanGaps: false,

&#x20;                   order: 2

&#x20;               },

&#x20;               {

&#x20;                   label: 'Active Weight Point',

&#x20;                   data: selectedWeightPoint,

&#x20;                   borderColor: '#0c4a6e', // Cyan Dark

&#x20;                   backgroundColor: '#0ea5e9', // Sky 500

&#x20;                   pointRadius: 8,

&#x20;                   pointHoverRadius: 10,

&#x20;                   yAxisID: 'yWeight',

&#x20;                   order: 1

&#x20;               },

&#x20;               {

&#x20;                   label: 'Active Growth Rate Point',

&#x20;                   data: selectedRatePoint,

&#x20;                   borderColor: '#312e81', // Indigo Dark

&#x20;                   backgroundColor: '#6366f1', // Indigo 500

&#x20;                   pointRadius: 8,

&#x20;                   pointHoverRadius: 10,

&#x20;                   yAxisID: 'yRate',

&#x20;                   order: 1

&#x20;               }

&#x20;           ];

&#x20;       }



&#x20;       // Chronological aquaculture bio-physical stages

&#x20;       const stageGuidelines = \[

&#x20;           {

&#x20;               maxDay: 30,

&#x20;               stage: "Post-Stocking Acclimatization",

&#x20;               desc: "The fish is in acclimation. Growth derivative is low ($W'(t) < 1.0\\\\text{ g/day}$). Tilapia hybrids are sensitive to changes in salinity or oxygen levels at this stage.",

&#x20;               advisory: "Feed strict starter crumbles (38% high-protein pellets) to boost metabolic immune responses.",

&#x20;               icon: "shield-alert"

&#x20;           },

&#x20;           {

&#x20;               maxDay: 50,

&#x20;               stage: "Juvenile Expansion Phase",

&#x20;               desc: "Growth rate accelerates rapidly ($W'(t) \\\\approx 2.5$ to $4.8\\\\text{ g/day}$). Biomass rises as feeding rates and activity increase. Nutrient assimilation is high.",

&#x20;               advisory: "Introduce standard size 2 floating pellets. Monitor DO levels early in the mornings.",

&#x20;               icon: "sparkles"

&#x20;           },

&#x20;           {

&#x20;               maxDay: 70,

&#x20;               stage: "Peak Biomass Acceleration (Inflection Peak)",

&#x20;               desc: "The first derivative $W'(t)$ peaks! At this optimal mathematical point, fish achieve maximum daily cellular weight velocity. This is the inflection point where feeding conversion efficiency is at its maximum.",

&#x20;               advisory: "Maintain maximum feeding protocol twice daily. Do not overfeed past satiation threshold.",

&#x20;               icon: "zap"

&#x20;           },

&#x20;           {

&#x20;               maxDay: 100,

&#x20;               stage: "Steady Linear Maturation",

&#x20;               desc: "Although the absolute fish size $W(t)$ is large, daily weight gain begins to decline ($W'(t) \\\\approx 3.5\\\\text{ g/day}$). Metabolism switches towards skeletal maturity.",

&#x20;               advisory: "Lower protein feed mix to 28% content to minimize nitrate excretion in runoff water.",

&#x20;               icon: "fish"

&#x20;           },

&#x20;           {

&#x20;               maxDay: 125,

&#x20;               stage: "Maintenance Shifting Stage",

&#x20;               desc: "Growth derivative decreases further ($W'(t) < 2.0\\\\text{ g/day}$). Over 80% of dietary intake is consumed for respiration rather than packing on lean muscle.",

&#x20;               advisory: "Decrease feed rations gradually to avoid organic pond waste accumulations and algae blooms.",

&#x20;               icon: "activity"

&#x20;           },

&#x20;           {

&#x20;               maxDay: 150,

&#x20;               stage: "Commercial Harvest Window",

&#x20;               desc: "Growth velocity approaches zero ($W'(t) < 0.8\\\\text{ g/day}$). The asymptotic target mass is reached. Continuing feeding beyond this point lowers farm profitability.",

&#x20;               advisory: "Begin selective harvesting and pond sorting! Transport live fish to local wet markets immediately.",

&#x20;               icon: "award"

&#x20;           }

&#x20;       ];



&#x20;       function getActiveStageInfo(day) {

&#x20;           return stageGuidelines.find(stage => day <= stage.maxDay) || stageGuidelines\[stageGuidelines.length - 1];

&#x20;       }



&#x20;       // Dynamic updates for indicators and labels

&#x20;       function updateDashboardElements(day, temp) {

&#x20;           const activeK = getGrowthRateCoefficient(temp);

&#x20;           const weightVal = W(day, activeK).toFixed(2);

&#x20;           const rateVal = dW(day, activeK).toFixed(3);

&#x20;           

&#x20;           // Text adjustments

&#x20;           document.getElementById('day-badge').innerText = `Day ${day}`;

&#x20;           document.getElementById('temp-badge').innerText = `${temp.toFixed(1)}°C`;

&#x20;           document.getElementById('calc-weight').innerText = weightVal;

&#x20;           document.getElementById('calc-growth-rate').innerText = rateVal;

&#x20;           

&#x20;           // Dynamic Advisory updating

&#x20;           const stageInfo = getActiveStageInfo(day);

&#x20;           document.getElementById('advisory-stage').innerHTML = stageInfo.stage;

&#x20;           document.getElementById('advisory-desc').innerHTML = stageInfo.desc;

&#x20;           document.getElementById('advisory-feeding').innerText = stageInfo.advisory;

&#x20;           

&#x20;           // Re-render Lucide SVG icons

&#x20;           const iconElement = document.getElementById('advisory-icon');

&#x20;           iconElement.setAttribute('data-lucide', stageInfo.icon);

&#x20;           lucide.createIcons();

&#x20;       }



&#x20;       function initAquacultureChart(selectedDay, temp) {

&#x20;           const ctx = document.getElementById('aquacultureChart').getContext('2d');

&#x20;           

&#x20;           chartInstance = new Chart(ctx, {

&#x20;               type: 'line',

&#x20;               data: {

&#x20;                   labels: tLabels,

&#x20;                   datasets: generateChartDatasets(selectedDay, temp)

&#x20;               },

&#x20;               options: {

&#x20;                   responsive: true,

&#x20;                   maintainAspectRatio: false,

&#x20;                   interaction: {

&#x20;                       mode: 'index',

&#x20;                       intersect: false

&#x20;                   },

&#x20;                   plugins: {

&#x20;                       legend: {

&#x20;                           display: false // Use custom legend blocks

&#x20;                       },

&#x20;                       tooltip: {

&#x20;                           callbacks: {

&#x20;                               label: function(context) {

&#x20;                                   let label = context.dataset.label || '';

&#x20;                                   if (label) {

&#x20;                                       label += ': ';

&#x20;                                   }

&#x20;                                   if (context.parsed.y !== null) {

&#x20;                                       label += context.parsed.y.toFixed(3);

&#x20;                                   }

&#x20;                                   return label;

&#x20;                               }

&#x20;                           }

&#x20;                       }

&#x20;                   },

&#x20;                   scales: {

&#x20;                       x: {

&#x20;                           title: {

&#x20;                               display: true,

&#x20;                               text: 'Days of Cultivation Timeline (t)',

&#x20;                               font: {

&#x20;                                   weight: 'bold',

&#x20;                                   family: 'Inter'

&#x20;                               },

&#x20;                               color: '#1e293b'

&#x20;                           },

&#x20;                           grid: {

&#x20;                               color: '#f1f5f9'

&#x20;                           }

&#x20;                       },

&#x20;                       yWeight: {

&#x20;                           type: 'linear',

&#x20;                           position: 'left',

&#x20;                           title: {

&#x20;                               display: true,

&#x20;                               text: 'Fish Weight W(t) \[grams]',

&#x20;                               font: {

&#x20;                                   weight: 'bold',

&#x20;                                   family: 'Inter'

&#x20;                               },

&#x20;                               color: '#0369a1'

&#x20;                           },

&#x20;                           min: 0,

&#x20;                           max: 650,

&#x20;                           grid: {

&#x20;                               color: '#e2e8f0'

&#x20;                           }

&#x20;                       },

&#x20;                       yRate: {

&#x20;                           type: 'linear',

&#x20;                           position: 'right',

&#x20;                           title: {

&#x20;                               display: true,

&#x20;                               text: 'Daily Weight Gain W\\'(t) \[grams/day]',

&#x20;                               font: {

&#x20;                                   weight: 'bold',

&#x20;                                   family: 'Inter'

&#x20;                               },

&#x20;                               color: '#4f46e5'

&#x20;                           },

&#x20;                           min: 0,

&#x20;                           max: 8,

&#x20;                           grid: {

&#x20;                               drawOnChartArea: false // Prevent gridline conflicts

&#x20;                           }

&#x20;                       }

&#x20;                   },

&#x20;                   onClick: (event) => {

&#x20;                       const points = chartInstance.getElementsAtEventForMode(event, 'index', { intersect: false }, true);

&#x20;                       if (points.length > 0) {

&#x20;                           const clickedIndex = points\[0].index;

&#x20;                           document.getElementById('daySlider').value = clickedIndex;

&#x20;                           syncState(clickedIndex, parseFloat(document.getElementById('tempSlider').value));

&#x20;                       }

&#x20;                   }

&#x20;               }

&#x20;           });

&#x20;       }



&#x20;       // Syncs layout components and chart updates

&#x20;       function syncState(day, temp) {

&#x20;           updateDashboardElements(day, temp);

&#x20;           chartInstance.data.datasets = generateChartDatasets(day, temp);

&#x20;           chartInstance.update('none'); // Update smoothly without visual jumps

&#x20;       }



&#x20;       window.onload = function() {

&#x20;           lucide.createIcons();

&#x20;           

&#x20;           const daySlider = document.getElementById('daySlider');

&#x20;           const tempSlider = document.getElementById('tempSlider');

&#x20;           const btnReset = document.getElementById('btnReset');



&#x20;           // Initialize plot at ideal parameters on Day 60 at 28.0°C

&#x20;           initAquacultureChart(60, 28);

&#x20;           updateDashboardElements(60, 28);



&#x20;           // Slider listeners

&#x20;           daySlider.addEventListener('input', function(e) {

&#x20;               const day = parseInt(e.target.value, 10);

&#x20;               const temp = parseFloat(tempSlider.value);

&#x20;               syncState(day, temp);

&#x20;           });



&#x20;           tempSlider.addEventListener('input', function(e) {

&#x20;               const temp = parseFloat(e.target.value);

&#x20;               const day = parseInt(daySlider.value, 10);

&#x20;               syncState(day, temp);

&#x20;           });



&#x20;           // Reset mechanism

&#x20;           btnReset.addEventListener('click', function() {

&#x20;               daySlider.value = 60;

&#x20;               tempSlider.value = 28;

&#x20;               syncState(60, 28);

&#x20;           });

&#x20;       };

&#x20;   </script>

</body>

</html>

