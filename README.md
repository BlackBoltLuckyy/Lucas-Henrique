<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lucas Henrique | Portfólio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #0f172a;
            color: #e2e8f0;
            scroll-behavior: smooth;
        }
        
        .profile-pic {
            width: 200px;
            height: 200px;
            border: 4px solid #38bdf8;
            transition: all 0.3s ease;
        }
        
        .profile-pic:hover {
            transform: scale(1.05);
            box-shadow: 0 0 20px rgba(56, 189, 248, 0.5);
        }
        
        .section-title {
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 3px;
            bottom: -5px;
            left: 0;
            background: linear-gradient(90deg, #38bdf8, #0ea5e9);
            border-radius: 3px;
        }
        
        .skill-badge {
            transition: all 0.3s ease;
        }
        
        .skill-badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 4px 6px rgba(56, 189, 248, 0.3);
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            left: -8px;
            top: 5px;
            background-color: #38bdf8;
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: #38bdf8;
            transition: width 0.3s ease;
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
        
        .active-nav::after {
            width: 100%;
        }
        
        .floating-btn {
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
    </style>
</head>
<body>
    <!-- Header/Navigation -->
    <header class="fixed w-full bg-slate-900/80 backdrop-blur-sm z-50 shadow-lg">
        <div class="container mx-auto px-6 py-4">
            <div class="flex justify-between items-center">
                <a href="#" class="text-2xl font-bold text-sky-400">Lucas<span class="text-white">Henrique</span></a>
                
                <nav class="hidden md:block">
                    <ul class="flex space-x-8">
                        <li><a href="#home" class="nav-link active-nav text-white hover:text-sky-400">Início</a></li>
                        <li><a href="#about" class="nav-link text-white hover:text-sky-400">Sobre</a></li>
                        <li><a href="#experience" class="nav-link text-white hover:text-sky-400">Experiência</a></li>
                        <li><a href="#skills" class="nav-link text-white hover:text-sky-400">Habilidades</a></li>
                        <li><a href="#contact" class="nav-link text-white hover:text-sky-400">Contato</a></li>
                    </ul>
                </nav>
                
                <button id="mobile-menu-button" class="md:hidden text-white focus:outline-none">
                    <i class="fas fa-bars text-2xl"></i>
                </button>
            </div>
        </div>
        
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-slate-800">
            <div class="px-6 py-4">
                <ul class="space-y-4">
                    <li><a href="#home" class="block text-white hover:text-sky-400">Início</a></li>
                    <li><a href="#about" class="block text-white hover:text-sky-400">Sobre</a></li>
                    <li><a href="#experience" class="block text-white hover:text-sky-400">Experiência</a></li>
                    <li><a href="#skills" class="block text-white hover:text-sky-400">Habilidades</a></li>
                    <li><a href="#contact" class="block text-white hover:text-sky-400">Contato</a></li>
                </ul>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="min-h-screen flex items-center pt-20">
        <div class="container mx-auto px-6 py-20">
            <div class="flex flex-col md:flex-row items-center justify-between">
                <div class="md:w-1/2 mb-12 md:mb-0">
                    <h1 class="text-4xl md:text-6xl font-bold mb-4">
                        <span class="text-sky-400">Olá,</span> eu sou<br>
                        <span class="text-white">Lucas Henrique</span>
                    </h1>
                    <h2 class="text-xl md:text-2xl text-slate-300 mb-6">Desenvolvedor Full Stack & Engenheiro de Software</h2>
                    <p class="text-slate-400 mb-8 max-w-lg">
                        CEO da Light Up - Startup de Marketing Full Service | Especialista em desenvolvimento de software com foco em aplicações web e mobile, automação e UX Design.
                    </p>
                    <div class="flex space-x-4">
                        <a href="#contact" class="bg-sky-500 hover:bg-sky-600 text-white px-6 py-3 rounded-lg font-medium transition duration-300 transform hover:scale-105">
                            Contate-me
                        </a>
                        <a href="#about" class="border border-sky-500 text-sky-500 hover:bg-sky-500 hover:text-white px-6 py-3 rounded-lg font-medium transition duration-300 transform hover:scale-105">
                            Saiba mais
                        </a>
                    </div>
                </div>
                
                <div class="md:w-1/2 flex justify-center">
                    <div class="relative">
                        <div class="profile-pic rounded-full overflow-hidden bg-slate-700 flex items-center justify-center">
                            <!-- Placeholder for profile picture - replace with actual image -->
                            <div class="text-6xl text-sky-400">
                                <i class="fas fa-user"></i>
                            </div>
                        </div>
                        <div class="absolute -bottom-5 -right-5 bg-slate-800 px-4 py-2 rounded-full border border-sky-400">
                            <span class="text-sky-400 font-medium">Disponível</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 bg-slate-800/50">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold mb-12 section-title">Sobre Mim</h2>
            
            <div class="flex flex-col md:flex-row gap-12">
                <div class="md:w-1/2">
                    <h3 class="text-xl font-semibold mb-4 text-sky-400">Quem sou eu?</h3>
                    <p class="text-slate-300 mb-6">
                        Sou Lucas Henrique de Souza, brasileiro, 20 anos, empreendedor e apaixonado por tecnologia e desenvolvimento de software. 
                        Fundador da Light Up, startup focada em marketing full service, e atualmente cursando o 3° ano do Ensino Médio integrado ao Curso Técnico de Desenvolvimento de Sistemas no 
                        Colégio Técnico de Limeira (COTIL).
                    </p>
                    <p class="text-slate-300 mb-6">
                        Tenho experiência em desenvolvimento de software full stack, com especialização em aplicações web e mobile. 
                        Além disso, adquiri sólidos conhecimentos em automação durante meu curso de Engenharia de Software, 
                        o que me permite atuar nessas áreas com confiança e eficiência.
                    </p>
                    
                    <div class="grid grid-cols-2 gap-4 mb-8">
                        <div class="bg-slate-700/50 p-4 rounded-lg">
                            <div class="flex items-center mb-2">
                                <div class="w-8 h-8 rounded-full bg-sky-500 flex items-center justify-center mr-3">
                                    <i class="fas fa-birthday-cake text-white text-sm"></i>
                                </div>
                                <span class="font-medium">Idade:</span>
                            </div>
                            <p class="text-slate-300 ml-11">20 anos</p>
                        </div>
                        
                        <div class="bg-slate-700/50 p-4 rounded-lg">
                            <div class="flex items-center mb-2">
                                <div class="w-8 h-8 rounded-full bg-sky-500 flex items-center justify-center mr-3">
                                    <i class="fas fa-map-marker-alt text-white text-sm"></i>
                                </div>
                                <span class="font-medium">Localização:</span>
                            </div>
                            <p class="text-slate-300 ml-11">Brasil</p>
                        </div>
                        
                        <div class="bg-slate-700/50 p-4 rounded-lg">
                            <div class="flex items-center mb-2">
                                <div class="w-8 h-8 rounded-full bg-sky-500 flex items-center justify-center mr-3">
                                    <i class="fas fa-graduation-cap text-white text-sm"></i>
                                </div>
                                <span class="font-medium">Formação:</span>
                            </div>
                            <p class="text-slate-300 ml-11">Cursando Ensino Médio/Técnico</p>
                        </div>
                        
                        <div class="bg-slate-700/50 p-4 rounded-lg">
                            <div class="flex items-center mb-2">
                                <div class="w-8 h-8 rounded-full bg-sky-500 flex items-center justify-center mr-3">
                                    <i class="fas fa-briefcase text-white text-sm"></i>
                                </div>
                                <span class="font-medium">Experiência:</span>
                            </div>
                            <p class="text-slate-300 ml-11">3+ anos</p>
                        </div>
                    </div>
                </div>
                
                <div class="md:w-1/2">
                    <h3 class="text-xl font-semibold mb-6 text-sky-400">Objetivo Profissional</h3>
                    
                    <div class="bg-slate-800 p-6 rounded-xl mb-8 border-l-4 border-sky-500">
                        <div class="flex items-start">
                            <div class="text-sky-400 mr-4 mt-1">
                                <i class="fas fa-bullseye text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-lg mb-2">Freelancer/CLT</h4>
                                <p class="text-slate-300">
                                    Busco oportunidades como desenvolvedor full stack, seja em regime CLT ou como freelancer, 
                                    para aplicar meus conhecimentos em desenvolvimento web e mobile, automação e UX Design,
                                    enquanto continuo desenvolvendo minha startup Light Up.
                                </p>
                            </div>
                        </div>
                    </div>
                    
                    <h3 class="text-xl font-semibold mb-6 text-sky-400">Idiomas</h3>
                    
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="font-medium">Português</span>
                                <span class="text-sky-400">Nativo</span>
                            </div>
                            <div class="w-full bg-slate-700 rounded-full h-2">
                                <div class="bg-sky-500 h-2 rounded-full" style="width: 100%"></div>
                            </div>
                        </div>
                        
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="font-medium">Inglês</span>
                                <span class="text-sky-400">Fluente</span>
                            </div>
                            <div class="w-full bg-slate-700 rounded-full h-2">
                                <div class="bg-sky-500 h-2 rounded-full" style="width: 95%"></div>
                            </div>
                        </div>
                        
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="font-medium">Alemão</span>
                                <span class="text-sky-400">Fluente</span>
                            </div>
                            <div class="w-full bg-slate-700 rounded-full h-2">
                                <div class="bg-sky-500 h-2 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                        
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="font-medium">Francês</span>
                                <span class="text-sky-400">Fluente</span>
                            </div>
                            <div class="w-full bg-slate-700 rounded-full h-2">
                                <div class="bg-sky-500 h-2 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                        
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="font-medium">Italiano</span>
                                <span class="text-sky-400">Fluente</span>
                            </div>
                            <div class="w-full bg-slate-700 rounded-full h-2">
                                <div class="bg-sky-500 h-2 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience & Education Section -->
    <section id="experience" class="py-20">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold mb-12 section-title">Experiência & Educação</h2>
            
            <div class="flex flex-col md:flex-row gap-12">
                <!-- Experience -->
                <div class="md:w-1/2">
                    <h3 class="text-2xl font-semibold mb-8 text-sky-400 flex items-center">
                        <i class="fas fa-briefcase mr-3"></i> Experiência Profissional
                    </h3>
                    
                    <div class="relative">
                        <div class="absolute left-0 top-0 h-full w-0.5 bg-slate-700 ml-1"></div>
                        
                        <div class="relative pl-8 mb-8 timeline-item">
                            <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-sky-500 transition duration-300">
                                <div class="flex justify-between items-start mb-2">
                                    <h4 class="font-medium text-lg">CEO & Fundador</h4>
                                    <span class="bg-sky-900 text-sky-400 text-xs px-2 py-1 rounded">Atual</span>
                                </div>
                                <p class="text-sky-400 mb-2">Light Up - Marketing Full Service</p>
                                <p class="text-slate-400 text-sm mb-3">2023 - Presente</p>
                                <p class="text-slate-300">
                                    Fundador e CEO da Light Up, startup focada em marketing full service que oferece soluções 
                                    integradas de marketing digital, desenvolvimento web e branding para clientes diversos.
                                </p>
                            </div>
                        </div>
                        
                        <div class="relative pl-8 mb-8 timeline-item">
                            <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-sky-500 transition duration-300">
                                <div class="flex justify-between items-start mb-2">
                                    <h4 class="font-medium text-lg">Aprendiz Administrativo</h4>
                                    <span class="bg-sky-900 text-sky-400 text-xs px-2 py-1 rounded">Atual</span>
                                </div>
                                <p class="text-sky-400 mb-2">TTGlog</p>
                                <p class="text-slate-400 text-sm mb-3">2023 - Presente</p>
                                <p class="text-slate-300">
                                    Atuando como aprendiz administrativo, desenvolvendo habilidades em organização, 
                                    gestão de processos e trabalho em equipe.
                                </p>
                            </div>
                        </div>
                        
                        <div class="relative pl-8 mb-8 timeline-item">
                            <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-sky-500 transition duration-300">
                                <h4 class="font-medium text-lg mb-2">Bolsista</h4>
                                <p class="text-sky-400 mb-2">Colégio Técnico de Limeira (COTIL)</p>
                                <p class="text-slate-400 text-sm mb-3">2022 - 2023</p>
                                <ul class="text-slate-300 list-disc pl-5 space-y-1">
                                    <li>Setores Finanças e Suprimentos (9 meses)</li>
                                    <li>Setor Transporte e administrativo (4 meses)</li>
                                </ul>
                            </div>
                        </div>
                        
                        <div class="relative pl-8 timeline-item">
                            <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-sky-500 transition duration-300">
                                <h4 class="font-medium text-lg mb-2">Secretaria Acadêmica</h4>
                                <p class="text-sky-400 mb-2">Colégio Técnico de Limeira (COTIL)</p>
                                <p class="text-slate-400 text-sm mb-3">2021 - 2022</p>
                                <p class="text-slate-300">
                                    Trabalhei na secretaria acadêmica por 1 ano, desenvolvendo habilidades administrativas, 
                                    organização e atendimento ao público.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Education -->
                <div class="md:w-1/2">
                    <h3 class="text-2xl font-semibold mb-8 text-sky-400 flex items-center">
                        <i class="fas fa-graduation-cap mr-3"></i> Educação
                    </h3>
                    
                    <div class="relative">
                        <div class="absolute left-0 top-0 h-full w-0.5 bg-slate-700 ml-1"></div>
                        
                        <div class="relative pl-8 mb-8 timeline-item">
                            <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-sky-500 transition duration-300">
                                <h4 class="font-medium text-lg mb-2">Ensino Médio integrado ao Técnico</h4>
                                <p class="text-sky-400 mb-2">Colégio Técnico de Limeira (COTIL)</p>
                                <p class="text-slate-400 text-sm mb-3">2021 - 2026</p>
                                <p class="text-slate-300">
                                    Cursando o 3° ano do Ensino Médio integrado ao Curso Técnico de Desenvolvimento de Sistemas.
                                </p>
                            </div>
                        </div>
                        
                        <div class="relative pl-8 mb-8 timeline-item">
                            <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-sky-500 transition duration-300">
                                <h4 class="font-medium text-lg mb-2">Engenharia de Software</h4>
                                <p class="text-sky-400 mb-2">Alura</p>
                                <p class="text-slate-400 text-sm mb-3">2024</p>
                                <p class="text-slate-300">
                                    Curso completo de Engenharia de Software, com foco em desenvolvimento de aplicações, 
                                    arquitetura de software e automação.
                                </p>
                            </div>
                        </div>
                        
                        <div class="relative pl-8 timeline-item">
                            <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-sky-500 transition duration-300">
                                <h4 class="font-medium text-lg mb-2">Programador Web</h4>
                                <p class="text-sky-400 mb-2">QualificaMAX</p>
                                <p class="text-slate-400 text-sm mb-3">2023</p>
                                <p class="text-slate-300">
                                    Curso completo de Programação Web, abordando tecnologias front-end e back-end para 
                                    desenvolvimento de aplicações web modernas.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20 bg-slate-800/50">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold mb-12 section-title">Minhas Habilidades</h2>
            
            <div class="mb-12">
                <h3 class="text-xl font-semibold mb-6 text-sky-400">Tecnologias Principais</h3>
                
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fab fa-java text-sky-400"></i>
                        </div>
                        <span class="font-medium">Java</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fab fa-python text-sky-400"></i>
                        </div>
                        <span class="font-medium">Python</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fab fa-js text-sky-400"></i>
                        </div>
                        <span class="font-medium">JavaScript</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fab fa-angular text-sky-400"></i>
                        </div>
                        <span class="font-medium">AngularJS</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fab fa-node-js text-sky-400"></i>
                        </div>
                        <span class="font-medium">Node.js</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fas fa-database text-sky-400"></i>
                        </div>
                        <span class="font-medium">ASP.NET</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fas fa-server text-sky-400"></i>
                        </div>
                        <span class="font-medium">Blazor Server</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fas fa-laptop-code text-sky-400"></i>
                        </div>
                        <span class="font-medium">Sites Responsivos</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fas fa-database text-sky-400"></i>
                        </div>
                        <span class="font-medium">.NET Data Access</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fas fa-code text-sky-400"></i>
                        </div>
                        <span class="font-medium">C#</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fab fa-react text-sky-400"></i>
                        </div>
                        <span class="font-medium">React.js</span>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg flex items-center border border-slate-700 hover:border-sky-500">
                        <div class="w-10 h-10 rounded-full bg-sky-900 flex items-center justify-center mr-3">
                            <i class="fas fa-mobile-alt text-sky-400"></i>
                        </div>
                        <span class="font-medium">Flutter/Dart</span>
                    </div>
                </div>
            </div>
            
            <div>
                <h3 class="text-xl font-semibold mb-6 text-sky-400">Outras Habilidades</h3>
                
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg border border-slate-700 hover:border-sky-500">
                        <div class="flex items-center justify-between mb-2">
                            <span class="font-medium">Desenvolvimento Web</span>
                            <span class="text-sky-400">95%</span>
                        </div>
                        <div class="w-full bg-slate-700 rounded-full h-2">
                            <div class="bg-sky-500 h-2 rounded-full" style="width: 95%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg border border-slate-700 hover:border-sky-500">
                        <div class="flex items-center justify-between mb-2">
                            <span class="font-medium">Back-end Development</span>
                            <span class="text-sky-400">92%</span>
                        </div>
                        <div class="w-full bg-slate-700 rounded-full h-2">
                            <div class="bg-sky-500 h-2 rounded-full" style="width: 92%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg border border-slate-700 hover:border-sky-500">
                        <div class="flex items-center justify-between mb-2">
                            <span class="font-medium">Front-end Development</span>
                            <span class="text-sky-400">90%</span>
                        </div>
                        <div class="w-full bg-slate-700 rounded-full h-2">
                            <div class="bg-sky-500 h-2 rounded-full" style="width: 90%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg border border-slate-700 hover:border-sky-500">
                        <div class="flex items-center justify-between mb-2">
                            <span class="font-medium">.NET Framework</span>
                            <span class="text-sky-400">88%</span>
                        </div>
                        <div class="w-full bg-slate-700 rounded-full h-2">
                            <div class="bg-sky-500 h-2 rounded-full" style="width: 88%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg border border-slate-700 hover:border-sky-500">
                        <div class="flex items-center justify-between mb-2">
                            <span class="font-medium">Automação</span>
                            <span class="text-sky-400">85%</span>
                        </div>
                        <div class="w-full bg-slate-700 rounded-full h-2">
                            <div class="bg-sky-500 h-2 rounded-full" style="width: 85%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg border border-slate-700 hover:border-sky-500">
                        <div class="flex items-center justify-between mb-2">
                            <span class="font-medium">UX/UI Design</span>
                            <span class="text-sky-400">80%</span>
                        </div>
                        <div class="w-full bg-slate-700 rounded-full h-2">
                            <div class="bg-sky-500 h-2 rounded-full" style="width: 80%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg border border-slate-700 hover:border-sky-500">
                        <div class="flex items-center justify-between mb-2">
                            <span class="font-medium">Banco de Dados</span>
                            <span class="text-sky-400">87%</span>
                        </div>
                        <div class="w-full bg-slate-700 rounded-full h-2">
                            <div class="bg-sky-500 h-2 rounded-full" style="width: 87%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-badge bg-slate-800 p-4 rounded-lg border border-slate-700 hover:border-sky-500">
                        <div class="flex items-center justify-between mb-2">
                            <span class="font-medium">Git/Versionamento</span>
                            <span class="text-sky-400">95%</span>
                        </div>
                        <div class="w-full bg-slate-700 rounded-full h-2">
                            <div class="bg-sky-500 h-2 rounded-full" style="width: 95%"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold mb-12 section-title">Entre em Contato</h2>
            
            <div class="flex flex-col md:flex-row gap-12">
                <div class="md:w-1/2">
                    <h3 class="text-xl font-semibold mb-6 text-sky-400">Informações de Contato</h3>
                    
                    <div class="space-y-6">
                        <div class="flex items-start">
                            <div class="bg-sky-900/50 p-3 rounded-full mr-4">
                                <i class="fas fa-envelope text-sky-400 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium mb-1">E-mail</h4>
                                <a href="mailto:lucashenriquedesouza0@gmail.com" class="text-slate-300 hover:text-sky-400 transition duration-300">
                                    lucashenriquedesouza0@gmail.com
                                </a>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-sky-900/50 p-3 rounded-full mr-4">
                                <i class="fas fa-phone-alt text-sky-400 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium mb-1">Telefone</h4>
                                <a href="tel:19995917856" class="text-slate-300 hover:text-sky-400 transition duration-300">
                                    (19) 99591-7856
                                </a>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-sky-900/50 p-3 rounded-full mr-4">
                                <i class="fas fa-map-marker-alt text-sky-400 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium mb-1">Localização</h4>
                                <p class="text-slate-300">Limeira, São Paulo - Brasil</p>
                            </div>
                        </div>
                    </div>
                    
                    <h3 class="text-xl font-semibold mt-10 mb-6 text-sky-400">Redes Sociais</h3>
                    
                    <div class="flex space-x-4">
                        <a href="#" class="bg-slate-800 w-12 h-12 rounded-full flex items-center justify-center hover:bg-sky-500 transition duration-300">
                            <i class="fab fa-linkedin-in text-xl"></i>
                        </a>
                        <a href="#" class="bg-slate-800 w-12 h-12 rounded-full flex items-center justify-center hover:bg-sky-500 transition duration-300">
                            <i class="fab fa-github text-xl"></i>
                        </a>
                        <a href="#" class="bg-slate-800 w-12 h-12 rounded-full flex items-center justify-center hover:bg-sky-500 transition duration-300">
                            <i class="fab fa-instagram text-xl"></i>
                        </a>
                        <a href="#" class="bg-slate-800 w-12 h-12 rounded-full flex items-center justify-center hover:bg-sky-500 transition duration-300">
                            <i class="fab fa-twitter text-xl"></i>
                        </a>
                    </div>
                </div>
                
                <div class="md:w-1/2">
                    <h3 class="text-xl font-semibold mb-6 text-sky-400">Envie uma Mensagem</h3>
                    
                    <form class="space-y-4">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label for="name" class="block mb-2 text-slate-300">Nome</label>
                                <input type="text" id="name" class="w-full bg-slate-800 border border-slate-700 rounded-lg px-4 py-3 focus:outline-none focus:border-sky-500 transition duration-300" placeholder="Seu nome">
                            </div>
                            <div>
                                <label for="email" class="block mb-2 text-slate-300">E-mail</label>
                                <input type="email" id="email" class="w-full bg-slate-800 border border-slate-700 rounded-lg px-4 py-3 focus:outline-none focus:border-sky-500 transition duration-300" placeholder="Seu e-mail">
                            </div>
                        </div>
                        
                        <div>
                            <label for="subject" class="block mb-2 text-slate-300">Assunto</label>
                            <input type="text" id="subject" class="w-full bg-slate-800 border border-slate-700 rounded-lg px-4 py-3 focus:outline-none focus:border-sky-500 transition duration-300" placeholder="Assunto da mensagem">
                        </div>
                        
                        <div>
                            <label for="message" class="block mb-2 text-slate-300">Mensagem</label>
                            <textarea id="message" rows="5" class="w-full bg-slate-800 border border-slate-700 rounded-lg px-4 py-3 focus:outline-none focus:border-sky-500 transition duration-300" placeholder="Sua mensagem"></textarea>
                        </div>
                        
                        <button type="submit" class="bg-sky-500 hover:bg-sky-600 text-white px-6 py-3 rounded-lg font-medium transition duration-300 w-full">
                            Enviar Mensagem
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-slate-900 py-8">
        <div class="container mx-auto px-6">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <a href="#" class="text-2xl font-bold text-sky-400">Lucas<span class="text-white">Henrique</span></a>
                </div>
                
                <div class="text-slate-400 text-sm text-center md:text-right">
                    <p>&copy; 2024 Lucas Henrique de Souza. Todos os direitos reservados.</p>
                    <p class="mt-1">Desenvolvido com <i class="fas fa-heart text-red-500"></i> por Lucas Henrique</p>
                </div>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <a href="#home" class="fixed bottom-6 right-6 bg-sky-500 w-12 h-12 rounded-full flex items-center justify-center text-white shadow-lg floating-btn">
        <i class="fas fa-arrow-up"></i>
    </a>

    <script>
        // Mobile menu toggle
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        
        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (!mobileMenu.classList.contains('hidden')) {
                        mobileMenu.classList.add('hidden');
                    }
                }
            });
        });
        
        // Update active navigation link on scroll
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('.nav-link');
        
        window.addEventListener('scroll', () => {
            let current = '';
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                
                if (pageYOffset >= (sectionTop - 150)) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active-nav');
                if (link.getAttribute('href') === `#${current}`) {
                    link.classList.add('active-nav');
                }
            });
        });
        
        // Form submission
        const contactForm = document.querySelector('form');
        if (contactForm) {
            contactForm.addEventListener('submit', (e) => {
                e.preventDefault();
                
                // Get form values
                const name = document.getElementById('name').value;
                const email = document.getElementById('email').value;
                const subject = document.getElementById('subject').value;
                const message = document.getElementById('message').value;
                
                // Here you would typically send the form data to a server
                // For this example, we'll just show an alert
                alert(`Obrigado, ${name}! Sua mensagem foi enviada com sucesso. Entrarei em contato em breve.`);
                
                // Reset form
                contactForm.reset();
            });
        }
    </script>
</body>
</html>
