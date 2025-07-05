<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Priyanshu Raj | UX/UI & Digital Product Designer</title>
  <!-- SEO & Open Graph -->
  <meta name="description" content="Portfolio of Priyanshu Raj, UX/UI & Digital Product Designer. Explore projects, skills, and experience.">
  <meta property="og:title" content="Priyanshu Raj | UX/UI & Digital Product Designer">
  <meta property="og:description" content="Portfolio of Priyanshu Raj, UX/UI & Digital Product Designer. Explore projects, skills, and experience.">
  <meta property="og:image" content="file:///D:/bla%20bla/profile%20image.jpg">
  <meta property="og:url" content="https://www.linkedin.com/in/uxwithpriyanshuraj/">
  <meta name="twitter:card" content="summary_large_image">
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- AOS.js for scroll animations -->
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&family=Montserrat:wght@700&display=swap" rel="stylesheet">
  <link rel="manifest" href="/manifest.json">
  <meta name="theme-color" content="#18181b">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  <meta name="mobile-web-app-capable" content="yes">
  <style>
    html { scroll-behavior: smooth; }
    body {
      background: #0a0a0f;
      color: #eaf6ff;
      font-family: 'Inter', 'Montserrat', Arial, sans-serif;
      position: relative;
      min-height: 100vh;
      overflow-x: hidden;
      transition: background 0.5s, color 0.5s;
    }
    /* Wavy animated SVG background */
    .wavy-bg {
      position: fixed;
      top: 0; left: 0; width: 100vw; height: 100vh;
      z-index: 0;
      pointer-events: none;
      overflow: hidden;
    }
    /* Futuristic glowing cursor */
    .glow-cursor {
      pointer-events: none;
      position: fixed;
      left: 0; top: 0;
      width: 80px; height: 80px;
      border-radius: 50%;
      background: radial-gradient(circle, #7c3aed 0%, #6366f1 60%, transparent 100%);
      box-shadow: 0 0 32px 8px #7c3aed99, 0 0 64px 16px #6366f199;
      z-index: 9999;
      transform: translate(-50%, -50%);
      transition: box-shadow 0.2s, background 0.2s, opacity 0.2s;
      mix-blend-mode: lighten;
      opacity: 0.8;
      pointer-events: none;
    }
    .glow-cursor.active {
      box-shadow: 0 0 64px 24px #7c3aedcc, 0 0 128px 32px #6366f1cc;
      opacity: 1;
    }
    /* Neon blue accent */
    :root {
      --neon-blue: #6366f1;
      --neon-shadow: 0 0 16px #6366f1, 0 0 32px #7c3aed44;
    }
    .floating-img {
      box-shadow: 0 8px 32px var(--neon-blue);
      animation: float 3s ease-in-out infinite alternate;
      border: 4px solid var(--neon-blue);
    }
    @keyframes float { to { transform: translateY(-18px); } }
    .typewriter {
      display: inline-block;
      border-right: 2px solid var(--neon-blue);
      white-space: nowrap;
      overflow: hidden;
      animation: typing 2.5s steps(30, end), blink-caret .75s step-end infinite;
      color: var(--neon-blue);
      text-shadow: 0 0 8px var(--neon-blue);
    }
    @keyframes typing { from { width: 0 } to { width: 100% } }
    @keyframes blink-caret { from, to { border-color: transparent } 50% { border-color: var(--neon-blue); } }
    .scrollspy-active { color: var(--neon-blue) !important; font-weight: bold; text-shadow: 0 0 8px var(--neon-blue); }
    .dark .scrollspy-active { color: #fff !important; }
    /* Neon button */
    .neon-btn {
      background: transparent;
      color: var(--neon-blue);
      border: 2px solid var(--neon-blue);
      box-shadow: var(--neon-shadow);
      transition: background 0.2s, color 0.2s, box-shadow 0.2s;
    }
    .neon-btn:hover {
      background: var(--neon-blue);
      color: #0a0a0f;
      box-shadow: 0 0 32px var(--neon-blue), 0 0 64px var(--neon-blue);
    }
    /* Neon blue cursor glow */
    .neon-cursor {
      pointer-events: none;
      position: fixed;
      left: 0; top: 0;
      width: 80px; height: 80px;
      border-radius: 50%;
      background: radial-gradient(circle, #6366f1 0%, #7c3aed 80%, transparent 100%);
      z-index: 9999;
      transform: translate(-50%, -50%);
      transition: box-shadow 0.2s, background 0.2s;
      mix-blend-mode: lighten;
    }
    /* Neon intensifies at edges */
    .neon-cursor.edge {
      background: radial-gradient(circle, #7c3aed 0%, #6366f1 80%, transparent 100%);
      box-shadow: 0 0 64px 16px #7c3aed99;
    }
    /* Grid overlay */
    .grid-bg {
      pointer-events: none;
      position: fixed;
      top: 0; left: 0; width: 100vw; height: 100vh;
      z-index: 0;
      background-image: linear-gradient(rgba(255,255,255,0.5) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.5) 1px, transparent 1px);
      background-size: 40px 40px;
      opacity: 0.5;
    }
    /* Professional/maze style tweaks */
    .bg-card {
      background: #10182a;
      border: 1.5px solid #1a2a3a;
      box-shadow: 0 2px 24px #00eaff22;
    }
    .text-neon { color: var(--neon-blue); text-shadow: 0 0 8px var(--neon-blue); }
    .border-neon { border-color: var(--neon-blue); }
    .shadow-neon { box-shadow: var(--neon-shadow); }
    /* Hero Section Styles */
    .hero-title {
      font-family: 'Montserrat', Arial, sans-serif;
      color: #fff;
      font-size: 2.8rem;
      font-weight: 700;
      letter-spacing: 1px;
      margin-bottom: 0.5rem;
      text-shadow: 0 2px 16px #000a;
    }
    .hero-role {
      color: #fff;
      font-size: 1.4rem;
      font-weight: 500;
      margin-bottom: 1.2rem;
      letter-spacing: 0.5px;
      font-family: 'Inter', Arial, sans-serif;
    }
    .hero-tagline {
      color: #b3e6ff;
      font-size: 1.1rem;
      font-weight: 400;
      margin-bottom: 2.2rem;
      font-family: 'Inter', Arial, sans-serif;
      max-width: 420px;
      text-align: left;
      line-height: 1.6;
    }
    .hero-flex {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 3rem;
      flex-wrap: wrap;
      min-height: 60vh;
    }
    .hero-img-wrap {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .floating-img {
      width: 160px;
      height: 160px;
      border-radius: 50%;
      object-fit: cover;
      border: 5px solid #fff;
      box-shadow: 0 8px 32px #00eaff44;
      background: #222;
      margin-bottom: 0;
      margin-right: 0;
      z-index: 2;
    }
    .hero-img-glow {
      position: absolute;
      width: 200px;
      height: 200px;
      border-radius: 50%;
      background: radial-gradient(circle, #00eaff33 0%, transparent 80%);
      z-index: 1;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      pointer-events: none;
    }
    @media (max-width: 700px) {
      .hero-flex { flex-direction: column; gap: 2rem; }
      .hero-title { font-size: 2rem; }
      .hero-role { font-size: 1.1rem; }
      .hero-tagline { font-size: 1rem; }
      .floating-img { width: 110px; height: 110px; }
      .hero-img-glow { width: 140px; height: 140px; }
    }
    .nav-link::after {
      content: '';
      display: block;
      height: 2px;
      background: linear-gradient(90deg, #7c3aed, #6366f1);
      width: 0;
      transition: width 0.3s;
      margin-top: 2px;
    }
    .nav-link:hover::after {
      width: 100%;
    }
    .animate-float {
      animation: float 3s ease-in-out infinite alternate;
    }
    @keyframes float {
      to { transform: translateY(-16px); }
    }
    /* Creative fade-in-up animation */
    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(40px) scale(0.96); }
      100% { opacity: 1; transform: translateY(0) scale(1); }
    }
    .animate-fadeInUp {
      animation: fadeInUp 1s cubic-bezier(.77,0,.18,1) both;
    }
    .animate-fadeInUp.delay-100 { animation-delay: 0.1s; }
    .animate-fadeInUp.delay-200 { animation-delay: 0.2s; }
    /* Animated gradient text */
    @keyframes gradient-x {
      0%, 100% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
    }
    .animate-gradient-x {
      background-size: 200% 200%;
      animation: gradient-x 4s ease-in-out infinite;
    }
  </style>
</head>
<body class="bg-black text-white transition-colors duration-500">
  <!-- Sticky Header Navbar -->
  <header class="navbar sticky top-0 z-50 flex items-center justify-between px-8 py-4 bg-black/80 backdrop-blur-md shadow-lg">
    <div class="logo text-2xl font-bold tracking-wide text-white">Priyanshu Raj</div>
    <nav>
      <ul class="flex gap-8 text-lg relative">
        <li class="relative"><a href="#home" class="nav-link">Home</a></li>
        <li class="relative"><a href="#about" class="nav-link">About</a></li>
        <li class="relative"><a href="#portfolio" class="nav-link">Portfolio</a></li>
        <li class="relative"><a href="#contact" class="nav-link">Contact</a></li>
      </ul>
    </nav>
    <div class="search-bar relative">
      <input id="siteSearchInput" type="text" placeholder="Search..." class="pl-10 pr-4 py-2 rounded-lg bg-[#18181b] text-white border border-gray-700 focus:outline-none focus:ring-2 focus:ring-pink-500" />
      <button id="siteSearchBtn" class="absolute left-3 top-1/2 -translate-y-1/2 text-gray-400 focus:outline-none"><i class="fas fa-search"></i></button>
    </div>
  </header>

  <!-- Split Hero Section -->
  <section id="home" class="w-full min-h-screen flex flex-col md:flex-row items-stretch justify-center bg-black relative overflow-hidden">
    <!-- Background pattern and low-opacity text -->
    <div class="absolute inset-0 z-0 pointer-events-none">
      <div class="w-full h-full bg-[url('https://www.transparenttextures.com/patterns/binary.png')] opacity-10"></div>
      <div class="absolute left-10 top-1/3 text-[8rem] font-extrabold text-white opacity-5 select-none">Portfolio</div>
      <div class="absolute right-10 bottom-10 text-[5rem] font-extrabold text-white opacity-5 select-none">Designer</div>
    </div>
    <!-- Left: Hero -->
    <div class="flex-1 flex flex-col justify-center items-start px-10 py-16 z-10">
      <div class="flex items-center gap-6 mb-8">
        <!-- Profile image removed from hero section -->
        <div></div>
        <div>
          <h1 class="text-4xl md:text-5xl font-extrabold text-white mb-2">Priyanshu Raj</h1>
          <h2 class="text-xl md:text-2xl font-semibold text-pink-400 mb-4 tracking-wide">UX/UI DESIGNER | DIGITAL PRODUCT DESIGNER</h2>
          <p class="text-lg text-gray-200 mb-6 max-w-md">Crafting human-centered digital experiences that blend logic, emotion, and usability. Let’s make design impactful.</p>
          <a href="#about" class="inline-block px-8 py-3 rounded-full bg-gradient-to-r from-purple-500 to-pink-500 text-white font-bold text-lg shadow-lg transform transition hover:scale-105 hover:shadow-pink-500/40 focus:outline-none focus:ring-2 focus:ring-pink-400">Learn More</a>
        </div>
      </div>
      <a class="cv-btn fixed bottom-8 left-8 px-6 py-2 rounded-full bg-white/10 border border-pink-400 text-pink-400 font-semibold shadow-lg backdrop-blur-md hover:bg-pink-500 hover:text-white transition" href="file:///C:/Users/hp/Desktop/updated%20cv.pdf" target="_blank">CV</a>
    </div>
    <!-- Right: Skills Glassmorphism Panel -->
    <div class="flex-1 flex flex-col justify-center items-center px-6 py-16 z-10">
      <div class="w-full max-w-lg bg-[#000000aa] rounded-3xl border border-pink-400 shadow-2xl backdrop-blur-lg p-8 flex flex-col items-center" style="box-shadow: 0 0 32px 4px #ff4fd8aa;">
        <h3 class="text-2xl font-bold text-white mb-8 text-center">My Skills</h3>
        <div class="grid grid-cols-3 md:grid-cols-5 gap-6">
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://1000logos.net/wp-content/uploads/2024/09/Figma-Emblem-500x281.png" alt="Figma" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">Figma</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://logos-world.net/wp-content/uploads/2020/11/Adobe-Photoshop-Logo-700x394.png" alt="Photoshop" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">Photoshop</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Adobe_Illustrator_CC_icon.svg/1200px-Adobe_Illustrator_CC_icon.svg.png" alt="Illustrator" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">Illustrator</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://upload.wikimedia.org/wikipedia/commons/c/cb/Adobe_After_Effects_CC_icon.svg" alt="After Effects" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">After Effects</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://tse4.mm.bing.net/th/id/OIP.KNUWp-5eUtk92ziIj9mJSwAAAA?rs=1&pid=ImgDetMain&o=7&rm=3" alt="JavaScript" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">JavaScript</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg" alt="HTML" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">HTML</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://upload.wikimedia.org/wikipedia/commons/a/ab/Official_CSS_Logo.svg" alt="CSS" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">CSS</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://tse1.mm.bing.net/th/id/OIP.W9Khd3FQl6OUH4B09-miTQHaHa?rs=1&pid=ImgDetMain&o=7&rm=3" alt="Framer" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">Framer</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://logos-world.net/wp-content/uploads/2023/02/ChatGPT-Logo.jpg" alt="ChatGPT" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">ChatGPT</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://tse4.mm.bing.net/th/id/OIP.Y3O9nYOMRQ10LKqVQ5c8vQHaHu?rs=1&pid=ImgDetMain&o=7&rm=3" alt="Notion" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">Notion</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://static.vecteezy.com/system/resources/previews/026/227/030/original/a-b-testing-icon-vector.jpg" alt="A/B Testing" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">A/B Testing</span>
          </div>
          <div class="flex flex-col items-center">
            <div class="rounded-xl bg-[#18181b] p-4 shadow-md border border-pink-400 hover:scale-110 hover:shadow-pink-400/60 transition">
              <img src="https://cdn.dribbble.com/users/1168716/screenshots/6660681/ux-research-strategy-logo.jpg" alt="UX Research" class="w-8 h-8 object-contain" />
            </div>
            <span class="mt-2 text-white text-sm">UX Research</span>
          </div>
          <!-- Add more skills as needed -->
        </div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="max-w-3xl mx-auto py-16 px-4 bg-[#18181b] rounded-3xl shadow-2xl border border-pink-400/40 mb-12" data-aos="fade-up">
    <h2 class="text-3xl font-bold mb-4 text-pink-400">About Me</h2>
    <div class="flex items-center gap-8 mb-6">
      <img src="file:///D:/bla%20bla/profile%20image.jpg" alt="Priyanshu Raj" class="w-40 h-40 object-cover rounded-[16px] shadow-2xl border-4 border-white/20 animate-float bg-[#18181b]" />
      <p class="text-lg text-gray-200">I’m Priyanshu Raj, a UX/UI & Digital Product Designer passionate about crafting delightful, human-centered digital experiences. I blend design thinking, research, and frontend skills to deliver impactful solutions.</p>
    </div>
    <div class="flex flex-wrap gap-3 mb-2">
      <span class="bg-gradient-to-r from-purple-500 to-pink-500 text-white px-4 py-1 rounded-full font-semibold shadow-md">UX/UI</span>
      <span class="bg-gradient-to-r from-purple-500 to-pink-500 text-white px-4 py-1 rounded-full font-semibold shadow-md">Human-Centered Design</span>
      <span class="bg-gradient-to-r from-purple-500 to-pink-500 text-white px-4 py-1 rounded-full font-semibold shadow-md">A/B Testing</span>
      <span class="bg-gradient-to-r from-purple-500 to-pink-500 text-white px-4 py-1 rounded-full font-semibold shadow-md">Information Architecture</span>
      <span class="bg-gradient-to-r from-purple-500 to-pink-500 text-white px-4 py-1 rounded-full font-semibold shadow-md">Design Systems</span>
      <span class="bg-gradient-to-r from-purple-500 to-pink-500 text-white px-4 py-1 rounded-full font-semibold shadow-md">Web Design</span>
      <span class="bg-gradient-to-r from-purple-500 to-pink-500 text-white px-4 py-1 rounded-full font-semibold shadow-md">HTML</span>
      <span class="bg-gradient-to-r from-purple-500 to-pink-500 text-white px-4 py-1 rounded-full font-semibold shadow-md">CSS</span>
    </div>
  </section>
  <!-- Projects Section -->
  <section id="projects" class="max-w-6xl mx-auto py-24 px-4 relative min-h-[60vh]" data-aos="fade-up">
    <h2 class="text-4xl font-extrabold mb-16 text-center text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-pink-500 tracking-tight animate-gradient-x">Projects</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12">
      <div class="group relative bg-gradient-to-br from-[#232336] to-[#18181b] rounded-3xl shadow-2xl p-8 border border-pink-400/30 overflow-hidden hover:scale-105 hover:shadow-pink-400/40 transition-all duration-500 animate-fadeInUp">
        <div class="absolute -top-10 -right-10 w-32 h-32 bg-gradient-to-br from-pink-400/30 to-purple-500/10 rounded-full blur-2xl opacity-60 group-hover:scale-125 transition-transform"></div>
        <h3 class="text-2xl font-bold text-pink-400 mb-3">Portfolio Website</h3>
        <p class="text-gray-200 mb-4">A modern, animated portfolio to showcase my work and skills.</p>
        <a href="#" class="inline-block px-5 py-2 rounded-full bg-gradient-to-r from-purple-500 to-pink-500 text-white font-semibold shadow-lg hover:scale-105 hover:shadow-pink-500/40 transition">View Project</a>
      </div>
      <div class="group relative bg-gradient-to-br from-[#232336] to-[#18181b] rounded-3xl shadow-2xl p-8 border border-pink-400/30 overflow-hidden hover:scale-105 hover:shadow-pink-400/40 transition-all duration-500 animate-fadeInUp delay-100">
        <div class="absolute -top-10 -right-10 w-32 h-32 bg-gradient-to-br from-pink-400/30 to-purple-500/10 rounded-full blur-2xl opacity-60 group-hover:scale-125 transition-transform"></div>
        <h3 class="text-2xl font-bold text-pink-400 mb-3">UX Case Study</h3>
        <p class="text-gray-200 mb-4">Redesigning a SaaS dashboard for better usability and engagement.</p>
        <a href="#" class="inline-block px-5 py-2 rounded-full bg-gradient-to-r from-purple-500 to-pink-500 text-white font-semibold shadow-lg hover:scale-105 hover:shadow-pink-500/40 transition">View Project</a>
      </div>
      <div class="group relative bg-gradient-to-br from-[#232336] to-[#18181b] rounded-3xl shadow-2xl p-8 border border-pink-400/30 overflow-hidden hover:scale-105 hover:shadow-pink-400/40 transition-all duration-500 animate-fadeInUp delay-200">
        <div class="absolute -top-10 -right-10 w-32 h-32 bg-gradient-to-br from-pink-400/30 to-purple-500/10 rounded-full blur-2xl opacity-60 group-hover:scale-125 transition-transform"></div>
        <h3 class="text-2xl font-bold text-pink-400 mb-3">Behance Projects</h3>
        <p class="text-gray-200 mb-4">See more projects on Behance.</p>
        <a href="https://www.behance.net/priyanshukeshri1" target="_blank" class="inline-block px-5 py-2 rounded-full bg-gradient-to-r from-purple-500 to-pink-500 text-white font-semibold shadow-lg hover:scale-105 hover:shadow-pink-500/40 transition">View on Behance</a>
      </div>
    </div>
  </section>

  <!-- Experience & Education Section -->
  <section id="experience" class="max-w-6xl mx-auto py-24 px-4 relative">
    <h2 class="text-4xl font-extrabold mb-16 text-center text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-pink-500 tracking-tight animate-gradient-x">Experience & Education</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
      <div class="bg-[#232336] rounded-3xl shadow-2xl p-10 border border-pink-400/30 animate-fadeInUp">
        <div class="text-lg font-bold text-pink-400 mb-2">UX/UI Designer</div>
        <div class="text-gray-200 mb-1">Freelance & Agency Projects</div>
        <div class="text-sm text-gray-400 mb-4">since 2023</div>
        <ul class="list-disc list-inside text-gray-300 text-base space-y-2">
          <li>Led multiple SaaS dashboard redesigns</li>
          <li>Collaborated with cross-functional teams</li>
          <li>Delivered user-centered solutions</li>
        </ul>
      </div>
      <div class="bg-[#232336] rounded-3xl shadow-2xl p-10 border border-pink-400/30 animate-fadeInUp delay-100">
        <div class="text-lg font-bold text-pink-400 mb-2">B.Des, World University of Design</div>
        <div class="text-gray-200 mb-1">Specialization: UX/UI & Digital Product Design</div>
        <div class="text-sm text-gray-400 mb-4">2024 - 2028</div>
        <ul class="list-disc list-inside text-gray-300 text-base space-y-2">
          <li>Specialized in digital product design</li>
          <li>Completed major UX research projects</li>
          <li>Graduated with distinction</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="max-w-4xl mx-auto py-24 px-4 relative">
    <h2 class="text-4xl font-extrabold mb-16 text-center text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-pink-500 tracking-tight animate-gradient-x">Contact</h2>
    <div class="bg-[#232336] rounded-3xl shadow-2xl p-10 border border-pink-400/30 animate-fadeInUp">
      <form id="contactForm" action="https://formspree.io/f/your-form-id" method="POST" class="flex flex-col gap-6">
        <input type="text" name="name" placeholder="Your Name" required class="px-4 py-3 rounded-lg border-2 border-pink-400 bg-[#18181b] text-white focus:outline-none focus:ring-2 focus:ring-pink-400 transition" />
        <input type="email" name="email" placeholder="Your Email" required class="px-4 py-3 rounded-lg border-2 border-pink-400 bg-[#18181b] text-white focus:outline-none focus:ring-2 focus:ring-pink-400 transition" />
        <textarea name="message" rows="4" placeholder="Your Message" required class="px-4 py-3 rounded-lg border-2 border-pink-400 bg-[#18181b] text-white focus:outline-none focus:ring-2 focus:ring-pink-400 transition"></textarea>
        <button type="submit" class="bg-gradient-to-r from-purple-500 to-pink-500 text-white font-bold px-8 py-3 rounded-full hover:scale-105 hover:shadow-pink-500/40 transition">Send Message</button>
      </form>
      <div class="flex gap-6 text-2xl mt-8 justify-center">
        <a href="https://www.linkedin.com/in/uxwithpriyanshuraj/" target="_blank" title="LinkedIn" class="text-pink-400 hover:text-white transition"><i class="fab fa-linkedin"></i></a>
        <a href="https://www.behance.net/priyanshukeshri1" target="_blank" title="Behance" class="text-pink-400 hover:text-white transition"><i class="fab fa-behance"></i></a>
        <a href="https://github.com/uxwithpriyanshuraj" target="_blank" title="GitHub" class="text-pink-400 hover:text-white transition"><i class="fab fa-github"></i></a>
      </div>
    </div>
  </section>
  <!-- Top Floating Card Banner (Optional Above Footer) -->
  <div class="w-full flex justify-center items-end pb-8">
    <div class="w-full max-w-5xl mx-auto rounded-2xl bg-gradient-to-br from-[#18181b]/80 to-[#232336]/90 shadow-2xl backdrop-blur-lg flex flex-col md:flex-row items-center justify-between px-8 py-6 gap-6 relative z-10 aos-init aos-animate" data-aos="fade-up">
      <div class="flex-1 text-left">
        <div class="text-2xl md:text-3xl font-bold font-inter text-white mb-2">The range of functionalities offered on the platforms includes the ability to connect</div>
      </div>
      <div class="flex-1 flex flex-col md:items-end gap-3">
        <div class="text-gray-300 text-base mb-2 max-w-md">With existing algorithmic strategies that reduce risk and automatically execute buy and sell orders.</div>
        <div class="flex gap-3">
          <button class="px-6 py-2 rounded-full bg-white text-[#18181b] font-semibold shadow-lg hover:shadow-pink-400/40 transition flex items-center gap-2">Get started <span><i class="fas fa-arrow-down"></i></span></button>
          <button class="px-6 py-2 rounded-full border border-white text-white font-semibold bg-transparent hover:bg-white/10 hover:shadow-pink-400/40 transition flex items-center gap-2">Watch how it works <span><i class="fas fa-play"></i></span></button>
        </div>
      </div>
    </div>
  </div>
  <!-- Main Footer -->
  <footer class="w-full bg-[#18181b] border-t border-pink-400/20 px-6 md:px-20 py-12 mt-0">
    <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-12 items-start">
      <!-- Left Column -->
      <div class="flex flex-col items-start gap-4">
        <div class="flex items-center gap-2">
          <span class="text-2xl font-extrabold font-inter text-white tracking-wide">nock</span>
        </div>
        <div class="text-gray-300 text-sm font-inter mb-2">Designing seamless, human-centered digital journeys.</div>
        <div class="flex items-center gap-2 bg-[#232336] px-3 py-1 rounded-full text-xs text-green-400 font-semibold shadow-inner">
          <span class="inline-block w-2 h-2 bg-green-400 rounded-full"></span>
          All systems operational
        </div>
      </div>
      <!-- Center Column -->
      <div class="grid grid-cols-2 gap-6 justify-items-center">
        <div class="flex flex-col gap-2">
          <a href="#about" class="text-gray-300 hover:text-white font-inter transition">About</a>
          <a href="#features" class="text-gray-300 hover:text-white font-inter transition">Features</a>
          <a href="#pricing" class="text-gray-300 hover:text-white font-inter transition">Pricing</a>
          <a href="#contact" class="text-gray-300 hover:text-white font-inter transition">Contact</a>
          <a href="#blog" class="text-gray-300 hover:text-white font-inter transition">Blog</a>
        </div>
        <div class="flex flex-col gap-2">
          <a href="#docs" class="text-gray-300 hover:text-white font-inter transition">Documentation</a>
          <a href="#faq" class="text-gray-300 hover:text-white font-inter transition">FAQ</a>
          <a href="#support" class="text-gray-300 hover:text-white font-inter transition">Support</a>
        </div>
      </div>
      <!-- Right Column -->
      <div class="flex flex-col items-start md:items-end gap-4">
        <div class="flex gap-4">
          <a href="https://x.com" target="_blank" class="text-gray-300 hover:text-white text-xl transition"><i class="fab fa-x-twitter"></i></a>
          <a href="https://linkedin.com/in/uxwithpriyanshuraj" target="_blank" class="text-gray-300 hover:text-white text-xl transition"><i class="fab fa-linkedin"></i></a>
          <a href="https://youtube.com" target="_blank" class="text-gray-300 hover:text-white text-xl transition"><i class="fab fa-youtube"></i></a>
        </div>
        <div class="text-xs text-gray-500 mt-4 md:mt-0">&copy; 2025 Priyanshu Raj. All rights reserved.</div>
      </div>
    </div>
  </footer>

  <!-- Scripts -->
  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <script>
    // AOS init
    AOS.init({ duration: 1000 });
    // Modal logic for projects
    document.querySelectorAll('.project-card').forEach(card => {
      card.onclick = () => {
        document.getElementById('projectModal').classList.remove('hidden');
        document.getElementById('modalTitle').textContent = card.dataset.title;
        document.getElementById('modalDesc').textContent = card.dataset.desc;
        document.getElementById('modalLink').href = card.dataset.link;
      };
    });
    document.getElementById('closeModal').onclick = () => {
      document.getElementById('projectModal').classList.add('hidden');
    };
    window.onclick = (e) => {
      if (e.target === document.getElementById('projectModal')) {
        document.getElementById('projectModal').classList.add('hidden');
      }
    };
    // Contact form validation
    document.getElementById('contactForm').onsubmit = function(e) {
      e.preventDefault();
      alert('Thank you for reaching out!');
      this.reset();
    };
    // Scrollspy
    const sections = document.querySelectorAll('section');
    const navLinks = document.querySelectorAll('.nav-link');
    window.addEventListener('scroll', () => {
      let current = '';
      sections.forEach(section => {
        const sectionTop = section.offsetTop - 80;
        if (pageYOffset >= sectionTop) {
          current = section.getAttribute('id');
        }
      });
      navLinks.forEach(link => {
        link.classList.remove('scrollspy-active');
        if (link.getAttribute('href') === '#' + current) {
          link.classList.add('scrollspy-active');
        }
      });
    });
    // Neon blue cursor effect
    const neonCursor = document.getElementById('neonCursor');
    document.addEventListener('mousemove', (e) => {
      neonCursor.style.left = e.clientX + 'px';
      neonCursor.style.top = e.clientY + 'px';
      // Intensify glow near edges
      const edgeThreshold = 80;
      if (
        e.clientX < edgeThreshold ||
        e.clientY < edgeThreshold ||
        window.innerWidth - e.clientX < edgeThreshold ||
        window.innerHeight - e.clientY < edgeThreshold
      ) {
        neonCursor.classList.add('edge');
      } else {
        neonCursor.classList.remove('edge');
      }
    });
    // Animate SVG wave horizontally
    const wave = document.getElementById('hero-wave');
    const path = document.getElementById('wave-path');
    let t = 0;
    function animateWave() {
      t += 0.015;
      const amplitude = 40;
      const freq = 1.5;
      const y1 = 300 + Math.sin(t) * amplitude;
      const y2 = 300 + Math.cos(t * freq) * amplitude * 0.7;
      const y3 = 300 + Math.sin(t * 0.7) * amplitude * 0.5;
      path.setAttribute('d', `M0 300 Q150 ${y1} 300 ${y2} T600 ${y3} V600 H0 Z`);
      requestAnimationFrame(animateWave);
    }
    if (wave && path) animateWave();
    // Wavy background animation
    function animateWaves() {
      const t = Date.now() * 0.001;
      const wave1 = document.getElementById('wave1');
      const wave2 = document.getElementById('wave2');
      const wave3 = document.getElementById('wave3');
      if (wave1 && wave2 && wave3) {
        wave1.setAttribute('d', `M0,800 Q960,${1000 + Math.sin(t)*40} 1920,800 L1920,1080 L0,1080 Z`);
        wave2.setAttribute('d', `M0,900 Q960,${1100 + Math.cos(t*1.2)*60} 1920,900 L1920,1080 L0,1080 Z`);
        wave3.setAttribute('d', `M0,1000 Q960,${1200 + Math.sin(t*0.7)*80} 1920,1000 L1920,1080 L0,1080 Z`);
      }
      requestAnimationFrame(animateWaves);
    }
    animateWaves();
    // Futuristic glowing cursor
    const glowCursor = document.getElementById('glowCursor');
    document.addEventListener('mousemove', (e) => {
      glowCursor.style.left = e.clientX + 'px';
      glowCursor.style.top = e.clientY + 'px';
      glowCursor.classList.add('active');
      clearTimeout(glowCursor._timeout);
      glowCursor._timeout = setTimeout(() => glowCursor.classList.remove('active'), 120);
    });
    // Smart search navigation
    document.getElementById('siteSearchBtn').onclick = function(e) {
      e.preventDefault();
      const query = document.getElementById('siteSearchInput').value.trim().toLowerCase();
      if (!query) return;
      // Map keywords to section ids
      const sectionMap = [
        { keywords: ['about', 'bio', 'profile'], id: 'about' },
        { keywords: ['project', 'work', 'portfolio', 'case study'], id: 'projects' },
        { keywords: ['experience', 'education', 'degree', 'school', 'college'], id: 'experience' },
        { keywords: ['contact', 'email', 'message', 'reach'], id: 'contact' },
        { keywords: ['home', 'landing', 'main'], id: 'home' }
      ];
      let found = false;
      for (const section of sectionMap) {
        if (section.keywords.some(k => query.includes(k))) {
          document.getElementById(section.id)?.scrollIntoView({ behavior: 'smooth' });
          found = true;
          break;
        }
      }
      if (!found) {
        // Optionally show a not found message or shake the input
        document.getElementById('siteSearchInput').classList.add('ring-2', 'ring-red-500');
        setTimeout(() => document.getElementById('siteSearchInput').classList.remove('ring-2', 'ring-red-500'), 800);
      }
    };
    // Catch and alert JS errors in production
    window.addEventListener('error', function(e) {
      if (location.hostname !== 'localhost') {
        alert('A site error occurred: ' + e.message);
      }
    });
  </script>
  <div class="wavy-bg>
    <svg id="wavySVG" width="100%" height="100%" viewBox="0 0 1920 1080" preserveAspectRatio="none" style="position:absolute;top:0;left:0;">
      <defs>
        <linearGradient id="waveGradient" x1="0" y1="0" x2="1" y2="1">
          <stop offset="0%" stop-color="#6366f1"/>
          <stop offset="100%" stop-color="#7c3aed"/>
        </linearGradient>
      </defs>
      <path id="wave1" fill="url(#waveGradient)" fill-opacity="0.18" d="M0,800 Q960,1000 1920,800 L1920,1080 L0,1080 Z"/>
      <path id="wave2" fill="url(#waveGradient)" fill-opacity="0.12" d="M0,900 Q960,1100 1920,900 L1920,1080 L0,1080 Z"/>
      <path id="wave3" fill="url(#waveGradient)" fill-opacity="0.10" d="M0,1000 Q960,1200 1920,1000 L1920,1080 L0,1080 Z"/>
    </svg>
  </div>
  <div class="glow-cursor" id="glowCursor"></div>

  <!-- Portfolio Gradient Header with Low Opacity Text -->
  <header class="relative w-full flex flex-col items-center justify-center pt-12 pb-4">
    <div class="absolute inset-0 flex flex-col items-center justify-center pointer-events-none select-none"></div>
      <span class="text-[7vw] font-extrabold uppercase opacity-10 bg-gradient-to-r from-blue-400 via-purple-400 to-pink-400 bg-clip-text text-transparent" style="letter-spacing: 0.1em;">Portfolio</span>
    </div>
    <h1 class="relative z-10 text-5xl md:text-7xl font-extrabold text-center bg-gradient-to-r from-blue-400 via-purple-400 to-pink-400 bg-clip-text text-transparent" style="line-height:1.1; margin-bottom:-1.5rem;">Portfolio</h1>
    <div class="w-full h-12 bg-gradient-to-b from-transparent to-[#0a0a0f] -mt-8"></div>
  </header>

  <!-- End of Page Content -->
</body>
</html>