



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animated About Me | GitHub</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: #f8fafc;
            overflow-x: hidden;
        }
        
        .floating {
            animation: floating 6s ease-in-out infinite;
        }
        
        .floating-delay-1 {
            animation-delay: 1s;
        }
        
        .floating-delay-2 {
            animation-delay: 2s;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        .gradient-text {
            background: linear-gradient(90deg, #6366f1, #8b5cf6, #ec4899);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: gradient 8s ease infinite;
            background-size: 200% 200%;
        }
        
        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .neumorphic {
            border-radius: 20px;
            background: linear-gradient(145deg, #1e293b, #1e293b);
            box-shadow:  10px 10px 20px #0f172a, 
                        -10px -10px 20px #334155;
            transition: all 0.3s ease;
        }
        
        .neumorphic:hover {
            transform: translateY(-5px);
            box-shadow:  15px 15px 30px #0f172a, 
                        -15px -15px 30px #334155;
        }
        
        .glow {
            animation: glow 2s ease-in-out infinite alternate;
        }
        
        @keyframes glow {
            from {
                box-shadow: 0 0 5px -5px #6366f1;
            }
            to {
                box-shadow: 0 0 10px 5px #6366f1;
            }
        }
        
        .card-enter {
            animation: cardEnter 1s ease-out forwards;
        }
        
        @keyframes cardEnter {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .tech-icon {
            transition: all 0.3s ease;
        }
        
        .tech-icon:hover {
            transform: scale(1.2) rotate(5deg);
            filter: drop-shadow(0 0 8px rgba(99, 102, 241, 0.7));
        }
        
        .pulse {
            animation: pulse 2s ease infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .border-animation {
            position: relative;
        }
        
        .border-animation::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, #6366f1, #8b5cf6);
            transition: width 0.5s ease;
        }
        
        .border-animation:hover::after {
            width: 100%;
        }
        
        .animate-cards > div:nth-child(1) { animation-delay: 0.1s; }
        .animate-cards > div:nth-child(2) { animation-delay: 0.2s; }
        .animate-cards > div:nth-child(3) { animation-delay: 0.3s; }
        .animate-cards > div:nth-child(4) { animation-delay: 0.4s; }
        
        .scroll-indicator {
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
            40% {transform: translateY(-20px);}
            60% {transform: translateY(-10px);}
        }
    </style>
</head>
<body class="min-h-screen flex flex-col items-center justify-center p-4 md:p-8">
    <div class="w-full max-w-4xl mx-auto">
        <!-- Header Section -->
        <header class="text-center mb-12 overflow-hidden">
            <div class="flex justify-center mb-6 floating">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/22a108cd-c5c8-4f5f-b1f8-4401352cfb51.png" alt="Profile picture of developer" class="rounded-full w-32 h-32 md:w-40 md:h-40 object-cover border-4 border-indigo-500/50 glow" />
            </div>
            <h1 class="text-3xl md:text-5xl font-bold mb-4 gradient-text">
                Hello, I'm <span class="border-animation">[Your Name]</span> 👋
            </h1>
            <p class="text-lg text-slate-300 max-w-2xl mx-auto">
                Passionate <span class="font-semibold text-indigo-300">Frontend Developer</span> crafting beautiful, interactive user experiences.
            </p>
        </header>
        
        <!-- About Card -->
        <div class="neumorphic p-8 mb-10 card-enter animate-cards">
            <h2 class="text-2xl font-bold mb-4 flex items-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2 text-indigo-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                </svg>
                About Me
            </h2>
            <p class="text-slate-300 leading-relaxed mb-4">
                I'm a creative frontend developer with expertise in modern JavaScript frameworks like React, Vue and Next.js. 
                I specialize in building responsive, accessible and high-performance user interfaces.
            </p>
            <p class="text-slate-300 leading-relaxed">
                When I'm not coding, you can find me exploring new technologies, contributing to open-source projects, 
                or mentoring junior developers.
            </p>
        </div>
        
        <!-- Skills and Tech -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-10">
            <!-- Skills Card -->
            <div class="neumorphic p-6 card-enter animate-cards">
                <h2 class="text-xl font-bold mb-4 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-indigo-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
                    </svg>
                    Skills
                </h2>
                <div class="grid grid-cols-2 gap-2">
                    <div class="flex items-center py-1">
                        <div class="w-2 h-2 bg-indigo-500 rounded-full mr-2"></div>
                        <span class="text-slate-300">Frontend</span>
                    </div>
                    <div class="flex items-center py-1">
                        <div class="w-2 h-2 rounded-full mr-2" style="background: #EC4899"></div>
                        <span class="text-slate-300">Backend</span>
                    </div>
                    <div class="flex items-center py-1">
                        <div class="w-2 h-2 rounded-full mr-2" style="background: #8B5CF6"></div>
                        <span class="text-slate-300">UI/UX Design</span>
                    </div>
                    <div class="flex items-center py-1">
                        <div class="w-2 h-2 rounded-full mr-2" style="background: #6366F1"></div>
                        <span class="text-slate-300">DevOps</span>
                    </div>
                </div>
            </div>
            
            <!-- Technologies Card -->
            <div class="neumorphic p-6 card-enter animate-cards">
                <h2 class="text-xl font-bold mb-4 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-indigo-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
                    </svg>
                    Technologies
                </h2>
                <div class="flex flex-wrap gap-3">
                    <span class="tech-icon bg-indigo-900/30 text-indigo-300 px-3 py-1 rounded-full text-sm">React</span>
                    <span class="tech-icon bg-indigo-900/30 text-indigo-300 px-3 py-1 rounded-full text-sm">Next.js</span>
                    <span class="tech-icon bg-indigo-900/30 text-indigo-300 px-3 py-1 rounded-full text-sm">TypeScript</span>
                    <span class="tech-icon bg-indigo-900/30 text-indigo-300 px-3 py-1 rounded-full text-sm">Vue</span>
                    <span class="tech-icon bg-indigo-900/30 text-indigo-300 px-3 py-1 rounded-full text-sm">Tailwind CSS</span>
                    <span class="tech-icon bg-indigo-900/30 text-indigo-300 px-3 py-1 rounded-full text-sm">GSAP</span>
                    <span class="tech-icon bg-indigo-900/30 text-indigo-300 px-3 py-1 rounded-full text-sm">Framer Motion</span>
                    <span class="tech-icon bg-indigo-900/30 text-indigo-300 px-3 py-1 rounded-full text-sm">CSS3/Sass</span>
                </div>
            </div>
        </div>
        
        <!-- Projects and Contact -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-10">
            <!-- Projects Card -->
            <div class="neumorphic p-6 card-enter animate-cards">
                <h2 class="text-xl font-bold mb-4 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-indigo-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4" />
                    </svg>
                    Projects
                </h2>
                <div class="space-y-4">
                    <div class="group">
                        <h3 class="font-semibold text-indigo-300 group-hover:text-indigo-200 transition-colors">Interactive Landing Page</h3>
                        <p class="text-sm text-slate-400">GSAP animations and micro-interactions portfolio piece</p>
                    </div>
                    <div class="group">
                        <h3 class="font-semibold text-indigo-300 group-hover:text-indigo-200 transition-colors">React Component Library</h3>
                        <p class="text-sm text-slate-400">Reusable, accessible UI components</p>
                    </div>
                    <div class="group">
                        <h3 class="font-semibold text-indigo-300 group-hover:text-indigo-200 transition-colors">E-commerce Frontend</h3>
                        <p class="text-sm text-slate-400">Next.js storefront with dynamic cart</p>
                    </div>
                </div>
                <button class="mt-4 w-full py-2 bg-indigo-600/50 hover:bg-indigo-600 transition-colors rounded-full text-sm font-medium text-indigo-100">
                    View All Projects
                </button>
            </div>
            
            <!-- Contact Card -->
            <div class="neumorphic p-6 card-enter animate-cards">
                <h2 class="text-xl font-bold mb-4 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-indigo-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                    </svg>
                    Contact Me
                </h2>
                <div class="space-y-3">
                    <div class="flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-indigo-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                        </svg>
                        <span class="text-slate-300">+1 (555) 123-4567</span>
                    </div>
                    <div class="flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-indigo-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                        </svg>
                        <span class="text-slate-300">hello@example.com</span>
                    </div>
                    <div class="flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-indigo-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                        </svg>
                        <span class="text-slate-300">github.com/yourusername</span>
                    </div>
                </div>
                <div class="flex justify-center space-x-4 mt-6">
                    <a href="#" class="p-2 bg-slate-800 rounded-full hover:bg-indigo-600 transition-colors">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                        </svg>
                    </a>
                    <a href="#" class="p-2 bg-slate-800 rounded-full hover:bg-blue-600 transition-colors">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
                        </svg>
                    </a>
                    <a href="#" class="p-2 bg-slate-800 rounded-full hover:bg-blue-400 transition-colors">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
                        </svg>
                    </a>
                    <a href="#" class="p-2 bg-slate-800 rounded-full hover:bg-purple-600 transition-colors">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M12 0c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm-2 16h-2v-6h2v6zm-1-6.891c-.607 0-1.1-.496-1.1-1.109 0-.612.492-1.109 1.1-1.109s1.1.497 1.1 1.109c0 .613-.493 1.109-1.1 1.109zm8 6.891h-1.998v-2.861c0-1.881-2.002-1.722-2.002 0v2.861h-2v-6h2v1.093c.872-1.616 4-1.736 4 1.548v3.359z"/>
                        </svg>
                    </a>
                </div>
            </div>
        </div>
        
        <!-- Footer -->
        <footer class="text-center text-slate-500 mt-12 mb-6">
            <p class="text-sm">
                © <span id="current-year"></span> [Your Name]. All Rights Reserved.
            </p>
            <p class="text-xs mt-1">
                Made with ❤️ using HTML, CSS & JavaScript
            </p>
        </footer>
    </div>

    <!-- Animated Elements Floating Around -->
    <div class="absolute top-1/4 left-1/6 w-4 h-4 rounded-full bg-indigo-500/30 opacity-70 floating-delay-1"></div>
    <div class="absolute top-2/3 right-1/5 w-6 h-6 rounded-full bg-purple-500/20 opacity-60 floating-delay-2"></div>
    <div class="absolute bottom-1/4 right-1/4 w-3 h-3 rounded-full bg-pink-500/30 opacity-80 floating"></div>
    <div class="absolute top-1/3 left-1/4 w-5 h-5 rounded-full bg-indigo-500/20 opacity-50 floating-delay-2"></div>
    <div class="absolute bottom-1/5 left-1/3 w-8 h-8 rounded-full bg-purple-500/10 opacity-40 floating-delay-1"></div>

    <script>
        // Set current year
        document.getElementById('current-year').textContent = new Date().getFullYear();
        
        // Add animations to cards on scroll
        document.addEventListener('DOMContentLoaded', () => {
            const cards = document.querySelectorAll('.card-enter');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('card-enter');
                    }
                });
            }, { threshold: 0.1 });
            
            cards.forEach(card => observer.observe(card));
            
            // Typewriter effect for optional text animations
            const typewriterEls = document.querySelectorAll('.typewriter');
            typewriterEls.forEach(el => {
                const text = el.textContent;
                el.textContent = '';
                
                let i = 0;
                const speed = 50; // typing speed in ms
                
                function typeWriter() {
                    if (i < text.length) {
                        el.textContent += text.charAt(i);
                        i++;
                        setTimeout(typeWriter, speed);
                    }
                }
                
                typeWriter();
            });
        });
        
        // Interactive tech icons animation
        document.querySelectorAll('.tech-icon').forEach(icon => {
            icon.addEventListener('mouseover', () => {
                icon.style.transition = 'all 0.3s ease';
            });
        });
    </script>
</body>
</html>
